---
keywords: activities guide;activities;activity;activity types;activity actions
description: Download an interactive PDF that describes the different activity types in [!DNL Adobe Target].
title: Which Activity Types Are Available in [!DNL Target]?
feature: Activities
exl-id: fa62592d-230a-4388-94bb-d9bc3bdfe973
---
# [!DNL Target] activity types

Download an interactive PDF that describes the different activity types in [!DNL Adobe Target].

>[!NOTE]
>
>For the best experience and to share with others, download the interactive [Adobe Target Activities Guide PDF](/help/main/assets/activities_guide_82817.pdf).
>
>This article does not contain information about [[!UICONTROL Recommendations] activities](/help/main/c-recommendations/recommendations.md). However, you can include recommendations inside [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Experience Targeting] (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md). This functionality requires that you have a [Target Premium license](/help/main/c-intro/intro.md#premium).

## What does it do? {#section_4ECAACC68723402EB3649033190E1BBC}

| Activity Type | Details |
|--- |--- |
|Manual [!UICONTROL A/B Test]<P>![icon](/help/main/c-activities/assets/icon_ab.png)|Compares two or more experiences to see which experience best improves conversions throughout a pre-specified test period.<P>For more information, see [A/B Test](/help/main/c-activities/t-test-ab/test-ab.md).|
|[!UICONTROL Auto-Allocate]<P>![Icon Auto-allocate](/help/main/c-activities/assets/icon_auto_allocate.png)|Identifies a winner among two or more experiences, and then redirects traffic to the winning experience, increasing conversion as the test runs and learns.<P>For more information, see [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).|
|[!UICONTROL Auto-Target]<P>![Icon AT](/help/main/c-activities/assets/icon_auto_target.png)|Uses advanced machine learning to personalize content and drive conversions by identifying multiple high-performing, marketer-defined experiences, and then serving the most tailored experience to visitors based on their individual customer profiles and past behaviors of similar visitors.<P>For more information, see  [Auto-Target For Personalized Experiences](/help/main/c-activities/auto-target/auto-target-to-optimize.md).|
|[!UICONTROL Automated Personalization] (AP)<P>![Icon AP](/help/main/c-activities/assets/icon_ap.png)|Uses advanced machine learning to personalize content and drive conversions by combining specific offers or messages, and then matching different offer variations to visitors, based on their individual customer profiles.<P>For more information, see [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md).|
|[!UICONTROL Multivariate Test] (MVT)<P>![Icon MVT](/help/main/c-activities/assets/icon_mvt.png)|Compares combinations of offers among elements on a page to see which combination of offers performs the best for a specific audience. Also, identifies which element of the page best improves conversions throughout a pre-specified test period.<P>For more information, see [Multivariate Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).|
|Experience Targeting (XT)<P>![Icon XT](/help/main/c-activities/assets/icon_xt.png)|Delivers content to a specific audience based on a set of marketer-defined rules and criteria.<P>For more information, see [Experience Targeting](/help/main/c-activities/t-experience-target/experience-target.md).|

## Why are you using this type of activity? {#section_46A70DD7CE3448749E635DDF5EAFC131}

| Activity Type | Reason |
|--- |--- |
|Manual [!UICONTROL A/B Test]|A highly controlled experiment with traffic measurements, split by percentages rather than by a rule, allowing you to analyze the test data, glean insights about your audience, and determine which experience performs the best.|
|[!UICONTROL Auto-Allocate]|A way to identify a winning experience and adjust traffic allocation to deliver the winning experience to visitors as fast as possible, supporting a faster and higher likelihood of conversion.|
|[!UICONTROL Auto-Target]|A way to identify the winners among multiple experiences, and then deliver the most appropriate experience to specific visitors. The targeting adapts over time as visitors' interests change, because the algorithm predicts a visitor's propensity for conversion on a certain experience at a certain time.|
|[!UICONTROL Automated Personalization] (AP)|A way to personalize a set of offers (created or pre-defined, in elements on a single page or across multiple pages) and deliver offer combinations that work the best to attract specific visitors.|
|[!UICONTROL Multivariate Testing] (MVT)|A way to display multiple offers in multiple elements, and then test the resulting unique experiences concurrently against a specific goal, which helps determine which element variation is the most successful. An MVT activity can also reveal which elements have the greatest positive or negative impact on a visitor's interaction.|
|[!UICONTROL Experience Targeting] (XT)|A way to target specific content to a specific audience based on a set of defined allocation rules.|

## What kind of marketer should use type of activity? {#section_A843D663D3E543FFB1A594266B560395}

| Activity Type | The Marketer |
|--- |--- |
|Manual [!UICONTROL A/B Test]|Is knowledgeable in stats.<P>Has the time to wait until end of test period to analyze results.|
|[!UICONTROL Auto-Allocate]|Has a short time frame.<P>Must identify the best experience and deliver quickly.<P>Wants to be able to "peek" at results as test runs.|
|[!UICONTROL Auto-Target]|Has several eligible experiences.<P>Wants to match experiences to specific visitors at optimal times based on their dynamic and changing profiles.|
|[!UICONTROL Automated Personalization] (AP)|Has one or more offers.<P>Wants to create offers combinations that yield optimal personalized experiences for specific visitors across various unique profiles and behaviors.|
|[!UICONTROL Multivariate Testing] (MVT)|Is knowledgeable in stats.<P>Has one or more offers.<P>Wants to analyze conversion trends relating to page element interactions.|
|[!UICONTROL Experience Targeting] (XT)|Must deliver a specific experience or piece of content to a specific audience.|

## Statistical details {#section_22CF2D07DB054505AB5EC702B99A5BB0}

| Activity Type | Details |
|--- |--- |
|Manual [!UICONTROL A/B Test]|The test compares each challenger experience to a control experience and then ranks the performance of all experiences, identifying both a winning experience and a losing experience when compared to the control.|
|[!UICONTROL Auto-Allocate]|The test produces a statistical guarantee on a true winner right away, and then directs more traffic towards audiences who have a higher likelihood of conversion with that winning experience.|
|[!UICONTROL Auto-Target]|The optimization mechanism identifies the relevant audience for each experience by showing increases and decreases in lift over time, and before it determines which experience to deliver to which visitor. The optimization mechanism is informed by conversions, segments, parameters, and profile scripts. From there, the mechanism automatically chooses which algorithm to use to generate a higher lift and conversion rate.|
|[!UICONTROL Automated Personalization] (AP)|The optimization mechanism constantly adjusts which experiences are delivered to which visitors based on new visitor behavior and past behaviors of similar visitors, with an offer's performance being measured against concurrent control groups.|
|[!UICONTROL Multivariate Testing] (MVT)|The test helps uncover the relative influence that specific elements have on conversion.|
|[!UICONTROL Experience Targeting] (XT)|The method defines rules that target either a specific experience or a specific piece of content to a specific audience. Customers can make updates at the experience level.|

## Benefits and considerations {#section_56C46ABEF7B945DDA0C1E6D714377123}

| Activity Type | Benefits | Considerations |
|--- |--- |--- |
|Manual [!UICONTROL A/B Test]|A/B resting helps you gain a full understanding of how each experience performs, beyond just which experience performs the best.|In an [!UICONTROL A/B Test], if you look at the test results before the sample size is reached, you risk relying on inaccurate results (you cannot "peek"earlier!).<P>Unlike [!UICONTROL Auto-Allocate], in an A/B test, the traffic distribution remains fixed even after you recognize that some experiences are outperforming others.<P>For information about best practices for [!UICONTROL A/B Test] activities, see [How long should you run an A/B Test](/help/main/c-activities/t-test-ab/sample-size-determination.md) and [Ten common A/B testing pitfalls and how to avoid them](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).|
|[!UICONTROL Auto-Allocate]|[!UICONTROL Auto-Allocate] reduces the cost of a typical A/B test because it has a higher overall conversion rate than a manual A/B test. The conversion rate is higher because [!UICONTROL Auto-Allocate] pushes more traffic to the highest performing experience, meaning you can realize the benefit of that winning experience earlier than the end of the test period (you can peek!).|[!UICONTROL Auto-Allocate] identifies the winner but does not differentiate among the losers. If you must know how each experience performed, A/B testing is preferable.<P>The [!UICONTROL Auto-Allocate] feature works with only one advanced metric setting, which is "Increment Count and Keep User in Activity." If you do not want to count repeat conversions, you should use A/B testing instead.|
|[!UICONTROL Auto-Target]|With [!UICONTROL Auto-Target], machine learning is applied to any kind of experience, including multi-page experiences. An [!UICONTROL Auto-Target] activity also lets you gain the value of [!UICONTROL Automated Personalization] while using the familiar A/B testing workflow.|With [!UICONTROL Auto-Target], if you want to change the content of your offers often or frequently, the algorithm needs enough time after each change to exploit what it learns and to deliver that content to the right visitors.|
|[!UICONTROL Automated Personalization] (AP)|With [!UICONTROL Automated Personalization], you can collect all of your offers in one place, and the algorithm determines the best combination of offers. You do not need to specify or build individual experiences. [!UICONTROL Automated Personalization] uses the same machine learning algorithms as [!UICONTROL Auto-Target].|When you combine multiple offers, a combinatorial explosion occurs resulting in the need for a significant amount of traffic. The [!UICONTROL Automated Personalization] algorithm accounts for many factors; therefore, requiring the most amount of traffic.<P>[!UICONTROL Automated Personalization] cannot consume reports in [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).|
|[!UICONTROL Multivariate Testing] (MVT)|With [!UICONTROL Multivariate Testing], you can test multiple elements simultaneously.|A [!UICONTROL Multivariate Test] is time consuming, and due to the multiple variables at play, it does not necessarily produce a winning experience with confidence.<P>It is often challenging to reach the amount of traffic needed to complete the test. Because all [!UICONTROL Multivariate Test] experiments are fully factorial, too many changing elements at once can quickly add up to many possible combinations that must be tested.<P>Even a site with fairly high traffic might have trouble completing a test with more than 25 combinations in a feasible amount of time.|
|[!UICONTROL Experience Targeting] (XT)|With [!UICONTROL Experience Targeting], you can quickly act on insights deduced from any activity results.<P>For example, if you ran an A/B test where the challenger did not outperform the control, but the results indicate that a specific segment of visitors converted four times more with the challenger than they did with the control, then you can use [!UICONTROL Experience Targeting] to direct the challenger experience to that particular segment.|[!UICONTROL Experience Targeting] does not allow you to control the percentage split of an experience across multiple audiences.|
