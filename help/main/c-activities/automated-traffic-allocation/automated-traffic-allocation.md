---
keywords: automated traffic allocation;targeting;Increment Count and Keep User in Activity;traffic allocation;auto-allocate;auto allocate
description: Learn how to use an Auto-Allocate activity in Adobe [!DNL Target] that identifies a winner among two or more experiences and automatically reallocates more traffic to the winner.
title: What is an Auto-Allocate Activity?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
---
# [!UICONTROL Auto-Allocate] overview

An [!UICONTROL Auto-Allocate] activity in [!DNL Adobe Target] identifies a winner among two or more experiences and automatically reallocates more traffic to the winner to increase conversions while the test continues to run and learn.

While creating an A/B activity using the three-step guided workflow, you can choose the [!UICONTROL Auto-Allocate to best experience] option.

## The challenge {#section_85D5A03637204BACA75E19646162ACFF}

Standard A/B tests have an inherent cost. You must spend traffic to measure performance of each experience and through analysis figure out the winning experience. Traffic distribution remains fixed even after you recognize that some experiences are outperforming others. Also, it's complicated to figure out the sample size, and the activity must run its entire course before you can act on a winner. And, there is still a chance the identified winner is not a true winner.

## The solution: [!UICONTROL Auto-Allocate] {#section_98388996F0584E15BF3A99C57EEB7629}

[!UICONTROL Auto-Allocate] reduces this cost and overhead of determining a winning experience. [!UICONTROL Auto-Allocate] monitors the goal metric performance of all experiences and sends more new entrants to the high-performing experiences proportionately. Enough traffic is reserved to explore the other experiences. You can see the benefits of the test on your results, even while the activity is still running: optimization occurs in parallel with learning.

[!UICONTROL Auto-Allocate] moves visitors toward winning experiences gradually, rather than requiring that you wait until an activity ends to determine a winner. You benefit from lift more quickly because activity entrants who would have been sent to less-successful experiences are shown potential winning experiences.

A normal A/B test in [!DNL Target] shows only pairwise comparisons of challengers with control. For example, if an activity has experiences: A, B, C, and D where A is the control, a normal [!DNL Target] A/B test would compare A versus B, A versus C, and A versus D.

In such tests, most products, including [!DNL Target], use a [Welch's t-test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} to produce p-value-based confidence. This confidence value is then used to determine if the challenger is sufficiently different from the control. However, [!DNL Target] doesn't automatically perform the implicit comparisons (B versus C, B versus D, and C versus D) that are required in order to find the "best" experience. As a result, the marketer must manually analyze the results to determine the "best" experience.

[!UICONTROL Auto-Allocate] performs all implicit comparisons across experiences and produces a "true" winner. There is no notion of a "control" experience in the test.

[!UICONTROL Auto-Allocate] intelligently allocates new visitors to experiences until the confidence interval of the best experience does not overlap with the confidence interval of any other experience. Normally this process could produce false positives, but [!UICONTROL Auto-Allocate] uses confidence intervals based on the [Bernstein Inequality](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) that compensates for repeated evaluations. At this point, there is a true winner. When [!UICONTROL Auto-Allocate] stops, provided there is no substantial time-dependence to the visitors who arrive at the page, there is at least a 95% chance that [!UICONTROL Auto-Allocate] returns an experience whose true response is no worse than 1% (relative) less than the true response of the winning experience.

## When to use [!UICONTROL Auto-Allocate] versus A/B or [!UICONTROL Automated Personalization] {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Use **[!UICONTROL Auto-Allocate]** when you want to optimize your activity from the beginning and identify the winning experiences as quickly as possible. By serving high-performing experiences more often the overall activity performance is increased. 
* Use a standard **[A/B test](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** when you want to characterize the performance of all experiences before optimizing your site. An A/B test helps you rank all of your experiences, whereas [!UICONTROL Auto-Allocate] finds top performers but does not guarantee differentiation among the lower performers. 
* Use [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) when you want optimization algorithms of the highest complexity, such as machine-learning models that build predictions based on individual profile attributes. [!UICONTROL Auto-Allocate] looks at the aggregate behavior of experiences (just like standard A/B tests), and doesn't differentiate between visitors.

## Key benefits {#section_0913BF06F73C4794862561388BBDDFF0}

* Preserves the strictness of an A/B test 
* Finds a statistically significant winner faster than a manual A/B test 
* Provides higher average campaign lift than a manual A/B test

## Terminology {#section_670F8785BA894745B43B6D4BFF953188}

The following terms are useful when discussing [!UICONTROL Auto-Allocate]:

**Multi-armed bandit:** A [multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit) approach to optimization balances exploratory learning and exploitation of that learning.

## How the algorithm works {#section_ADB69A1C7352462D98849F2918D4FF7B}

The overall logic behind [!UICONTROL Auto-Allocate] incorporates both measured performance (such as conversion rate) and confidence intervals of the cumulative data. Unlike a standard A/B test where traffic is split evenly between experiences, [!UICONTROL Auto-Allocate] changes traffic allocation across experiences.

* 80% of visitors are allocated using the intelligent logic described below. 
* 20% of visitors are randomly assigned across all experiences in order to adapt to changing visitor behavior.

The multi-armed bandit approach keeps some experiences free for exploration while exploiting the experiences that are performing well. More new visitors are placed into better performing experiences while preserving the ability to react to changing conditions. These models update at least once an hour to ensure that the model reacts to the latest data.

As more visitors enter the activity, some experiences start to become more successful, and more traffic is sent to the successful experiences. 20% of traffic continues to be served randomly to explore all experiences. If one of the lower-performing experiences starts to perform better, more traffic is allocated to that experience. Or if the success of a higher-performing activity decreases, less traffic is allocated to that experience. For example, if an event causes visitors to look for different information on your media site, or weekend sales on your retail site provide different results.

The following illustration represents how the algorithm might perform during a test with four experiences:

![auto-allocate image](assets/auto-allocate.png)

The illustration shows how the traffic allocated to each experience progresses over several rounds of the activity lifetime until a clear winner is determined.

| Round | Description |
|--- |--- |
|![Warm-up round](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png)|**Warm-Up Round (0)**: During the warm-up round, each experience gets equal traffic allocation until each experience in the activity has a minimum of 1,000 visitors and 50 conversions.<ul><li>Experience A=25%</li><li>Experience B=25%</li><li>Experience C=25%</li><li>Experience D=25%</li></ul>After each experience gets 1,000 visitors and 50 conversions, Target starts automated traffic allocation. All allocations happen in rounds and two experiences are picked for each round.<br>Only two experiences move forward into the next round: D and C.<br>Moving forward means that the two experiences are allocated 80% of the traffic equally. The other two experiences continue to participate but are only served as part of the 20% random traffic allocation as new visitors enter the activity.<br>All allocations are updated every hour (shown by rounds along the x-axis above). After each round, the cumulative data is compared.|
|![Round 1](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png)|**Round 1**: During this round, 80% of traffic is allocated to experiences C and D (40% each). 20% of traffic is allocated randomly to experiences A, B, C, and D (5% each). During this round, experience A performs well.<ul><li>The algorithm picks experience D to move forward into the next round because it has the highest conversion rate (as indicated by  on each activity's vertical scale).</li><li>The algorithm picks experience A to move forward as well because it has the highest upper bound of the Bernstein 95% confidence interval of the remaining experiences.</li></ul>Experiences D and A move forward.|
|![Round 2](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png)|**Round 2**: During this round, 80% of traffic is allocated to experiences A and D (40% each). 20% of traffic is allocated randomly, so that means A, B, C, and D each get 5% of traffic. During this round, experience B performs well.<ul><li>The algorithm picks experience D to move forward into the next round because it has the highest conversion rate (as indicated by  on each activity's vertical scale).</li><li>The algorithm picks experience B to move forward as well because it has the highest upper bound of the Bernstein 95% confidence interval of the remaining experiences.</li></ul>Experiences D and B move forward.|
|![Round 3](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png)|**Round 3**: During this round, 80% of traffic is allocated to experiences B and D (40% each). 20% of traffic is allocated randomly, so that means A, B, C, and D each get 5% of traffic. During this round, experience D continues to perform well and experience C performs well.<ul><li>The algorithm picks experience D to move forward into the next round because it has the highest conversion rate (as indicated by  on each activity's vertical scale).</li><li>The algorithm picks experience C to move forward as well because it has the highest upper bound of the Bernstein 95% confidence interval of the remaining experiences.</li></ul>Experiences D and C move forward.|
|![Round 4](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png)|**Round 4**: During this round, 80% of traffic is allocated to experiences C and D (40% each). 20% of traffic is allocated randomly, so that means A, B, C, and D each get 5% of traffic. During this round, experience C performs well.<ul><li>The algorithm picks experience C to move forward into the next round because it has the highest conversion rate (as indicated by on each activity's vertical scale).</li><li>The algorithm picks experience D to move forward as well because it has the highest upper bound of the Bernstein 95% confidence interval of the remaining experiences.</li></ul>Experiences C and D move forward.|
|![Round n](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png)|**Round n**: As the activity progresses, a high-performing experience starts to emerge and the process continues until there is a winning experience. When the confidence interval of the experience with the highest conversion rate doesn't overlap with any other experience's confidence interval, it is labeled the winner. A [badge displays on the winning activity's page](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) and in the [!UICONTROL Activity] list.<ul><li>The algorithm picks experience C as the clear winner</li></ul>At this point the algorithm serves 80% of traffic to experience C, while 20% of traffic continues to be served randomly to all experiences (A, B, C, and D). In total, C gets 85% of traffic. In the unlikely event that the confidence interval of the winner begins to overlap again, the algorithm reverts to the behavior of round 4 above.<br>**Important**: If you manually chose a winner earlier in the process, it would have been easy to choose the wrong experience. For this reason, it is best practice to wait until the algorithm determines the winning experience.|

>[!NOTE]
>
>If an activity has only two experiences, both experiences get equal traffic until [!DNL Target] finds a winning experience with 75% confidence. At that point, two-thirds of the traffic is allocated to the winner, and one-third to the loser. After that, when an experience reaches 95% confidence, 90% of traffic is allocated to the winner, and 10% is allocated to the loser. [!DNL Target] always maintains some traffic being sent to the "losing" experience in order to avoid false positives in the end (i.e. maintain some exploration).

After an [!UICONTROL Auto-Allocate] activity is activated, the following operations from the UI are not allowed:

* Switching the "Traffic Allocation" mode to "Manual" 
* Changing the goal metric type 
* Changing options in the "Advanced Settings" panel

## See how Auto-Allocate works

For more information, see [Auto-Allocate can give you faster test results and higher revenue than a manual test](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md)

## Caveats {#section_5C83F89F85C14FD181930AA420435E1D}

**The [!UICONTROL Auto-Allocate] feature works with only one advanced metric setting: [!UICONTROL Increment Count and Keep User in Activity]**

The following advanced metric settings are not supported: [!UICONTROL Increment Count], [!UICONTROL Release User], [!UICONTROL Allow Reentry and Increment Count], and [!UICONTROL Release User and Bar from Reentry]. 

**Frequent return visitors can inflate experience conversion rates.** 

If a visitor who sees experience A returns frequently and converts several times, the Conversion Rate (CR) of experience A is artificially increased. Compare this result to experience B, where visitors convert but do not return often. As a result, the CR of experience A looks better than the CR of experience B, so new visitors are more likely to be allocated to A than to B. If you choose to count once per entrant, the CR of A and CR of B might be identical.

If return visitors are randomly distributed, their effect on conversion rates is more likely to be evened out. To mitigate this effect, consider changing the counting method of the goal metric to count only once per entrant. 

**Differentiates between high-performers, not between low-performers.** 

[!UICONTROL Auto-Allocate] is good at differentiating between high-performing experiences (and finding a winner). There could be times when you don't have enough differentiation among the under-performing experiences.

If you want to produce statistically significant differentiation between all experiences, you might want to consider using the manual traffic allocation mode. 

**Time-correlated (or contextually varying) conversion rates can skew allocation amounts.** 

Some factors that can be ignored during a standard A/B test because they affect all experiences equally cannot be ignored in an [!UICONTROL Auto-Allocate] test. The algorithm is sensitive to the observed conversion rates. Following are examples of factors that can affect experience performance unequally:

* Experiences with varying contextual (time, location, gender, and so on) relevance.

  For example:

  * "Thank God it's Friday" results in higher conversions on Friday
  * "Jump-start your Monday" has higher conversion on Monday 
  * "Gear up for an East-coast winter" provides higher conversion in East-coast or winter-afflicted locations

Using experiences with varying contextual relevance can skew the results in an [!UICONTROL Auto-Allocate] test more than in an A/B test because the A/B test analyzes the results over a longer period. 

* Experiences with varying delays in conversion, possibly due to the urgency of the message.

  For example, "30% sale ends today" signals the visitor to convert today, but "50% off first purchase" doesn't create the same sense of urgency.

## Frequently Asked Questions {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Consult the following FAQs and answers as you work with [!UICONTROL Auto-Allocate] activities:

### Does [!UICONTROL Analytics for Target] (A4T) support [!UICONTROL Auto-Allocate] activities?

Yes. For more information, see [A4T support for Auto-Allocate and Auto-Target activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

### Are returning visitors automatically reallocated to high-performing experiences?

No. Only new visitors are automatically allocated. Returning visitors continue to see their original experience to protect the validity of the A/B test.

### How does the algorithm treat false positives?

The algorithm guarantees a 95% confidence or 5% false-positive rate if you wait until the winner-badge appears.

### When does [!UICONTROL Auto-Allocate] start allocating traffic?

The algorithm starts working after all experiences in the activity have a minimum of 1,000 visitors and 50 conversions.

### How aggressively does the algorithm exploit?

80% of traffic is served using [!UICONTROL Auto-Allocate] and 20% of traffic is served randomly. When a winner as been identified, all of the 80% of traffic goes to it, while all experiences continue to get some traffic as part of the 20%, including the winning experience.

### Are losing experiences shown at all?

Yes. The multi-armed bandit ensures that at least 20% of traffic is reserved to explore changing patterns or conversion rates across all experiences.

### What happens to activities with long conversion delays?

As long as all experiences being optimized face similar delays, the behavior is the same as an activity with a faster conversion cycle. However, it takes longer to reach the 50 conversion threshold before the traffic allocation process begins.

### How is [!UICONTROL Auto-Allocate] different from [!UICONTROL Automated Personalization]?

[!UICONTROL Automated Personalization] uses each visitor's profile attributes to determine the best experience. In doing so, it not only optimizes, but also personalizes the activity for that user.

[!UICONTROL Auto-Allocate], on the other hand, is an A/B test that produces an aggregate winner (the most popular experience, but not necessarily the most effective experience for each visitor).

### Do returning visitors inflate conversion rate on my success metric?

Currently, the logic favors visitors that convert quickly or visit more often because such visitors temporarily inflate the overall conversion rate of the experience they belong to. The algorithm adjusts itself frequently, so the increase in conversion rate is amplified at each snapshot. If the site gets numerous return visitors, their conversions can potentially inflate the overall conversion rate for the experience they belong to. There is a good chance that return visitors are randomly distributed, in which case the aggregate effect (increased lift) is evened out. To mitigate this effect, consider changing the counting method of the success metric to count only once per entrant.

### Can I use the sample size calculator when using [!UICONTROL Auto-Allocate] to estimate how long the activity takes to identify the winner?

You can use the existing [!DNL Adobe Target] [Sample Size Calculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) to get an estimate of how long the test runs. (As with traditional A/B testing, apply Bonferroni correction if you are testing more than two offers or more than one conversion metric/hypothesis.) This calculator is designed for traditional fixed-horizon A/B testing and provides an estimate only. Using the calculator for an [!UICONTROL Auto-Allocate] activity is optional because [!UICONTROL Auto-Allocate] declares a winner for you. You don't need to pick a fixed point in time to look at the test results. The provided values are always statistically valid. 

In our experiments, we've found the following:

* When testing exactly two experiences, [!UICONTROL Auto-Allocate] finds a winner more quickly than fixed-horizon testing (i.e. the timeframe suggested by the sample size calculator) when the performance difference between experiences is large. However, [!UICONTROL Auto-Allocate] might require extra time to identify a winner when the performance difference between experiences is small. In these cases, fixed-horizon tests would typically have ended without a statistically significant result.
* When testing more than two experiences, [!UICONTROL Auto-Allocate] finds a winner more quickly than fixed-horizon testing (i.e. the time frame suggested by the sample size calculator) when a single experience strongly out-performs all other experiences. When two or more experiences are both "winning" against other experiences but closely matched to each other, [!UICONTROL Auto-Allocate] might require extra time to determine which is superior. In these cases, fixed-horizon tests would typically have ended by concluding that the "winning" experiences were better than the lower-performing experiences, but not have identified which one was superior.

### Should I remove an under-performing experience from an [!UICONTROL Auto-Allocate] activity to speed the process of determining a winner?

There is really no reason to remove an under-performing experience. [!UICONTROL Auto-Allocate] automatically serves high-performing experiences more often and serves under-performing experiences less often. Leaving an under-performing experience in the activity does not significantly impact the speed to determine a winner.

20% of visitors are randomly assigned across all experiences. The amount of traffic served to an under-performing experience is minimal (20% divided by the number of experiences).

### Can I change the goal metric midway through an [!UICONTROL Auto-Allocate] activity? {#change-metric}

[!DNL Adobe] does not recommend that you change the goal metric midway through an activity. Although it is possible to change the goal metric during an activity using the [!DNL Target] UI, you should always start a new activity. [!DNL Adobe] does not guarantee what happens if you change the goal metric in an activity after it is running. 

This recommendation applies to [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Automated Personalization] activities that use either [!DNL Target] or [!DNL Analytics] (A4T) as the reporting source.

### Can I change the reporting source midway through an [!UICONTROL Auto-Allocate] activity? {#change-reporting}

[!DNL Adobe] does not recommend that you change the reporting source midway through an activity. Although it is possible to change the reporting source (from [!DNL Target] to A4T or vice versa) during an activity using the [!DNL Target] UI, you should always start a new activity. [!DNL Adobe] does not guarantee what happens if you change the reporting source in an activity after it is running.

This recommendation applies to [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Automated Personalization] activities that use either [!DNL Target] or [!DNL Analytics] (A4T) as the reporting source.

### Can I use the [!UICONTROL Reset Report Data] option while running an [!UICONTROL Auto-Allocate] activity?

Using the [!UICONTROL Reset Report Data] option for [!UICONTROL Auto-Allocate] activities is not suggested. Although it removes the visible reporting data, this option does not remove all training records from the [!UICONTROL Auto-Allocate] model. Instead of using the [!UICONTROL Reset Report Data] option for [!UICONTROL Auto-Allocate] activities, create a new activity and de-activate the original activity. (This guidance also applies to [!UICONTROL Auto-Target] and [!UICONTROL Automated Personalization] activities.)

### How does [!UICONTROL Auto-Allocate] build models with regard to environments?

[!UICONTROL Auto-Allocate] builds models based on the traffic and conversion behavior recorded in the default environment only. By default, [!UICONTROL Production] is the default environment, but the default environment can be changed in [!DNL Target] [Administration > Environments](/help/main/administrating-target/environments.md).

If a hit occurs in another (non-default) environment, traffic is distributed according to the observed conversion behavior in the default environment. The result of that hit (conversion or non-conversion) is recorded for reporting purposes but not considered in the [!UICONTROL Auto-Allocate] model.

When selecting another environment, the report shows traffic and conversions for that environment. The default selected environment for a report is the account-wide default that is selected. The default environment cannot be set on a per-activity basis.

### Can an [!UICONTROL Auto-Allocate] activity adjust the lookback window over the course of a test to take into consideration changing trends over time?

For example, can the activity consider the month of December for deciding how to allocate traffic, rather than looking at September visitor data (when the test began)?

No, [!UICONTROL Auto-Allocate] considers performance of the entire activity. 

### Does [!UICONTROL Auto-Allocate] show a winning experience to a returning visitor if the winning experience is different from what the visitor saw when qualifying for the activity?

[!UICONTROL Auto-Allocate] uses sticky decisioning for the same reasons that [!UICONTROL A/B Test] activities are sticky. The traffic allocation works for new visitors only.

## Training videos {#section_893E5B36DC4A415C9B1D287F51FCCB83}

The following videos contain more information about the concepts discussed in this article.

### Activity Workflow - Targeting (2:14) ![Tutorial badge](/help/main/assets/tutorial.png)

This video includes information about setting up traffic allocation.

* Assign an audience to your activity 
* Throttle traffic up or down 
* Select your traffic allocation method 
* Allocate traffic between different experiences

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Creating A/B Tests (8:36) ![Tutorial badge](/help/main/assets/tutorial.png)

This video demonstrates how to create an A/B test using the Target three-step guided workflow. [!UICONTROL Auto-Allocate] is discussed beginning at 4:45.

* Create an A/B activity in [!DNL Adobe Target] 
* Allocate traffic using a manual split or automatic traffic allocation

>[!VIDEO](https://video.tv.adobe.com/v/17391)
