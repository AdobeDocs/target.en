---
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;automated personalization;control;default experience;best practices
description: Explore a list of frequently asked questions (FAQs) and answers about [!UICONTROL Automated Personalization] (AP) activities in [!UICONTROL Adobe Target].
title: How Can I Find FAQs about [!UICONTROL Automated Personalization] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
---
# Automated Personalization FAQs

Consult the following FAQs and answers as you work with [!UICONTROL Automated Personalization] activities in [!DNL Adobe Target].

## Can I specify a specific experience to be used as a control in an [!UICONTROL Automated Personalization] activity?

+++See details

You can select an experience to be used as a control while creating an [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activity.

This feature lets you route the entire control traffic to a specific experience, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against control traffic to that one experience.

For more information, see [Use a specific experience as control](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

## How can I compare [!UICONTROL Automated Personalization] to a default experience? {#section_46C1A620A2384C2C8392D6716DD18495}

+++See details

There is no turn-key option of comparing [!UICONTROL Automated Personalization] to a default experience. However, as a workaround, if a default offer or experience exists as part of the overall activity, to understand its baseline performance, click the "[!UICONTROL Control]" segment in reports and locate that particular offer in the resulting offer-level report. The conversion rate recorded for this offer can be used to compare with the conversation rate of the entire "Random Forest" segment. This helps to compare how the machine is doing compared to the default offer.

+++

## What are the best practices to set up an [!UICONTROL Automated Personalization] activity? {#section_E155B26282BE49B58EA2683413D11DE6}

+++See details

* If you are looking to personalize a lower-traffic page, or you want to make structural changes to the experience you are personalizing, consider using an [!UICONTROL Auto-Target] activity in place of [!UICONTROL Automated Personalization]. See [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md). 
* Consider completing an [!UICONTROL A/B Test] activity between the offers and locations that you are planning to use in your [!UICONTROL Automated Personalization] activity to ensure that the location and offers have an impact on the optimization goal. If an [!UICONTROL A/B Test] activity fails to demonstrate a significant difference, [!UICONTROL Automated Personalization] likely also fails to generate lift.

    * If an A/B…N test shows no statistically significant differences between experiences, one or more of the following situations is probably responsible:
    
      * The offers are likely not sufficiently different from each other.
      * The locations you selected do not impact the success metric.
      * The optimization goal is too far in the conversion funnel to be affected by your chosen offers.

* Make sure to use the [Traffic Estimator](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) so you can have a sense of how long it takes for personalization models to build in your [!UICONTROL Automated Personalization] activity. 
* Decide on the allocation between the control and targeted before beginning the activity, based on your goals.

  There are three scenarios to consider based on the goal of your activity and the type of control you've selected:

  * **Random Experiences as your control and your activity goal is to test the effectiveness of the personalization algorithm**: If your goal is to evaluate the personalization algorithm, you want to have a more accurate picture of lift. You also most likely want to compare what the conversion rate for your experiences or offers is if you simply did an [!UICONTROL A/B Test] (a randomly served control). In that situation, using a 50% allocation to a control of randomly served experiences is recommended.
  * **"Random Experiences" as your control and your activity goal is to maximize personalized traffic**: If you are comfortable with the algorithm and want to have the maximum amount of traffic personalized, a 10% to 30% allocation to control is recommended. The tradeoff here is the accuracy that you see in your lift information. The confidence intervals of your control traffic are larger because there is less traffic flowing to them.
  * **Specific Experience as your control, with either goal type**: If you want to compare a specific marketer-driven experience to the personalization models, a 10% to 30% allocation to control is recommended. When you select only one experience as a control, that traffic isn't spread across every offer or experience in the activity.

* Targeting rules should be used as sparingly as possible because they can interfere with the model's ability to optimize. 
* Reporting groups can limit the success of your [!UICONTROL Automated Personalization] activity. Use reporting groups only under specific conditions:

    * Use reporting groups only if the following conditions are met: 
    
      * You plan on replacing or adding new offers while the activity is running.
      * The offers in the reporting group appeal to the same visitors.
      * The offers in that reporting group have about the same overall response rate.

    * There is no personalization between offers in a reporting group. The offers are all treated as the same by the personalization model. 
    * Never put all offers in an activity into a single reporting group. Doing so causes all offers to be uniformly randomly served to all visitors in the activity.

+++

## What are some limits in [!UICONTROL Automated Personalization]? {#section_08BA09ED51B547299963C94FE6417CFA}

+++See details

[!DNL Target] has a hard limit of 30,000 experiences, but it functions at its best when fewer than 10,000 experiences are created.

This same limit is applied even when the activity has enabled the [!UICONTROL Disalow Duplicates] option.

For more information about character limits and other limits (offer size, audiences, profiles, values, parameters, and so forth) that affect activities and other elements in [!DNL Target], see [Limits](/help/main/r-troubleshooting-target/target-limits.md).

+++

## How is offer-level targeting implemented? {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++See details

When each visitor arrives, the set of possible offers the visitor can see is determined by the offer-level targeting rules. Then, the algorithm chooses the offer that the model predicts has the best expected revenue or chance of conversion from among those offers. Offer targeting impacts the efficacy of [!DNL Target] machine learning algorithms and, as a result, should be used as sparingly as possible.

+++

## Why is my [!UICONTROL Automated Personalization] activity not showing lift? {#section_BFA07C8C258F45318F73A461B8F32737}

+++See details

There are four factors required for an [!UICONTROL Automated Personalization] activity to generate lift:

* The offers in each location must be different enough to influence visitors. 
* The locations must be somewhere that make a difference to the optimization goal. 
* There must be enough traffic and statistical power in the activity to detect the lift. 
* The personalization algorithm must work well.

The best course of action is to first make sure the content and locations that make up the activity experiences truly make a difference to the overall response rates using a simple, non-personalized [!UICONTROL A/B Test] activity. Be sure to compute the sample sizes ahead of time to ensure there is enough power to see a reasonable lift and run the A/B test for a fixed duration without stopping it or making any changes. If the A/B test results show statistically significant lift on one or more experiences, it is likely that a personalized activity is successful. Personalization can work even if there are no differences in the overall response rates of the experiences. Typically, the issue stems from the offers or locations not having a large enough impact on the optimization goal to be detected with statistical significance.

For more information, [Troubleshooting Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

+++

## How is [!UICONTROL Automated Personalization] allocating my activity's traffic? {#section_4369364F77804E0D9B78BEE551DA5659}

+++See details

[!UICONTROL Automated Personalization] routes visitors to the experience that has the highest forecasted success metric based on the most recent [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) models built for each model. This forecast is based on the visitor's specific information and visit context.

For example, assume that an [!UICONTROL Automated Personalization] activity had two locations with two offers each. In the first location, Offer A has a forecasted conversion rate of 3% for a specific visitor, and Offer B has a forecasted conversion rate of 1%. In the second location, Offer C has a forecasted conversion rate of 2% for the same visitor, and Offer D has a forecasted conversion rate of 5%. Therefore, [!UICONTROL Automated Personalization] serves this visitor an experience with Offer A and Offer D.

+++

## When should I stop my [!UICONTROL Automated Personalization] activity? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++See details

[!UICONTROL Automated Personalization] can be used as "always on" personalization that constantly optimizes. Especially for evergreen content, there is no need to stop your [!UICONTROL Automated Personalization] activity. If you want to make substantial changes to the content that aren't similar to offers currently in your [!UICONTROL Automated Personalization] activity, the best practice is to start a new activity. Starting a new activity helps other users reviewing reports to not confuse or relate past results with different content.

+++

## How long should I wait for models to build? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++See details

The time it takes for models to build in your activity typically depends on the traffic to your selected activity locations and your activity success metric. Use the [Traffic Estimator](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) to determine the expected length of time it takes for models to build in your activity.

+++

## One model is built within my [!UICONTROL Automated Personalization] activity. Are the visits to that experience personalized? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++See details

No, there must be at least two models built within your activity for personalization to begin.

+++

## When can I look at the results of my [!UICONTROL Automated Personalization] activity? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++See details

You can begin to look at the results of your [!UICONTROL Automated Personalization] activity after you have at least two experiences with models built (green checkmark) for the experience that has models built.

+++

## How can I decrease the time needed for models to build in my [!UICONTROL Automated Personalization] activity? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++See details

Review your activity setup and see if there are any changes you are willing to make to improve the speed at which models build.

* Is your success metric far down the sales funnel from your activity experiences? A lower activity conversion rate increases the traffic requirements needed for models to build, as a minimum number of conversions is required. 
* If your success metric is set to RPV, can you change to conversion? Conversion activities tend to require less traffic to build models. 
* Are there some experiences that you can drop from your activity? Decreasing the number of experiences in an activity speeds the time to build models. 
* Is there a higher-traffic page where this activity would be more successful? The more traffic and conversions in your activity locations, the quicker models build.

+++

## Why are visitors seeing experiences for an [!UICONTROL Automated Personalization] activity that they shouldn't see? {#section_41CECEAE0881446A8D9F3B016857914B}

+++See details

[!UICONTROL Automated Personalization] activities are evaluated once per session. If there are active sessions that have qualified for a particular experience and now new offers have been added to it, visitors will see the new content along with the previously shown offers. Because these visitors previously qualified for those experiences, they still see those experiences during the session. To evaluate this at every page visit, you should change to the [!UICONTROL Experience Targeting] (XT) activity type.

+++

## Can I change the goal metric midway through an [!UICONTROL Automated Personalization] activity? {#change-metric}

+++See details

[!DNL Adobe] does not recommend that you change the goal metric midway through an activity. Although it is possible to change the goal metric during an activity using the [!DNL Target] UI, you should always start a new activity. [!DNL Adobe] do not warranty what happens if you change the goal metric in an activity after it is running. 

This recommendation applies to [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Automated Personalization] activities that use either [!DNL Target] or [!DNL Analytics] (A4T) as the reporting source.

+++

## Can I use the [!UICONTROL Reset Report Data] option while running an [!UICONTROL Automated Personalization] activity?

+++See details

[!DNL Adobe] does not recommend using the [!UICONTROL Reset Report Data] option for [!UICONTROL Automated Personalization] activities. Although it removes the visible reporting data, this option does not remove all training records from the [!UICONTROL Automated Personalization] model. Instead of using the [!UICONTROL Reset Report Data] option for [!UICONTROL Automated Personalization] activities, create a new activity and deactivate the original activity. This guidance also applies to [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities.

+++

## How does [!UICONTROL Automated Personalization] build models with regard to environments?

+++See details

One model is built to identify the performance of the personalized strategy versus randomly served traffic versus sending all traffic to the overall winning experience. This model considers hits and conversions in the default environment only. 

Traffic from a second set of models is built for each modeling group ([!UICONTROL Automated Personalization]) or experience ([!UICONTROL Auto-Target]). For each of these models, hits and conversions across all environments are considered. 
  
Requests are, therefore, served with the same model, regardless of environment. However, the plurality of traffic should come from the default environment to ensure that the identified overall winning experience is consistent with real-world behavior.

+++
