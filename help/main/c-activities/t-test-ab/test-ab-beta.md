---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content;auto-target;auto-allocate
description: Explore the A/B Test activities in [!DNL Target] - [!UICONTROL Manual], [!UICONTROL Auto-Allocate], and [!UICONTROL Auto-Target].
title: Discover the A/B Test Activities Available in [!DNL Target].
feature: A/B Tests
hide: yes
hidefromtoc: yes
exl-id: 7d5546b9-ee2d-4737-ad28-218863bee55a
---
# A/B Test overview

A manual [!UICONTROL A/B Test] activity (sometimes referred to as an A/B...N test) compares two or more versions of your Web site content to see which version best lifts your conversions, sales, or other metrics you identify. Use an A/B test to compare changes to your page against your default page design to determine which experience produces the best results.

>[!TIP]
>
>In addition to the [!UICONTROL Manual] (Default) [!UICONTROL A/B Test] activity (discussed in this article), [!DNL Target] provides two additional types of [!UICONTROL A/B Test] activities: [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]. See [Types of A/B Testing activities](#types) below for more information.

Manual A/B tests are useful when you have a clear hypothesis of ways to improve your page performance based on success metrics or alternative content delivery.

Manual A/B tests are well suited for large changes that might involve new layouts or drastically different treatments of the elements. If your test design does not easily break down into individual page elements, you should run an A/B test before running a [multivariate test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

When you set up your A/B test, you can determine the percentage of visitors that see each experience. For example, you might split traffic evenly between the control and a second experience, or you might test a new, more risky experience by showing it to only 5% of your audience.

>[!NOTE]
>
>For detailed information about determining the optimum sample size for an A/B test, see [Plan Your A/B Test](/help/main/c-activities/t-test-ab/sample-size-determination.md).

When the number of different experiences exceeds five and spans two or more locations, it's a good idea to consider an [MVT test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) before running your A/B tests. The multivariate test shows which areas on the page are most likely to improve conversion. These areas are the locations that a marketer should focus on. For example, the MVT test might show that the call to action is the most important location for meeting your goals. After you determine which locations and content are most useful for helping you meet your goals, you can then run an A/B test to further refine the results. For example, to test two specific images against each other, or to compare the wording or colors of a call to action. By following an MVT test with one or more A/B tests, you can determine the best possible content for the results you desire.

## Types of A/B Testing activities {#types}

In addition to the manual [!UICONTROL A/B Test] activity, [!DNL Target] provides two additional types of [!UICONTROL A/B Testing] activities: [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target].

|Activity Type|Description|
| --- | --- |
|[!UICONTROL Manual A/B Test]|Compares two or more experiences to see which experience best improves conversions throughout a pre-specified test period.<P>This section describes how to set up a manual [!UICONTROL A/B Test] activity, but the steps for the other types of [!UICONTROL A/B Test] activities are similar.|
|[!UICONTROL Auto-Allocate]|Identifies a winner among two or more experiences, and then redirects traffic to the winner, increasing conversion as the test runs and learns.<P>To learn about the benefits of using an [!UICONTROL Auto-Allocate] activity, see [Auto-Allocate](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *How long should you run an A/B Test* and [Auto-Allocate overview](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).|
|![Premium badge](/help/main/assets/premium.png) [!UICONTROL Auto-Target]|Uses advanced machine learning to personalize content and drive conversions by identifying multiple high-performing, marketer-defined experiences. The most tailored experience is then served to visitors based on their individual customer profiles and past behaviors of similar visitors.<P>For more information, see [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md).|

For more information about which of these [!UICONTROL A/B Test] activities is right for you, see the interactive [Adobe Target Activities Guide PDF](/help/main/c-activities/target-activities-guide.md).

The steps for creating the three types of [!UICONTROL A/B Test] activities are similar. To create an [!UICONTROL Auto-Allocate] or [!UICONTROL Auto-Target] activity:

1. Start by [creating an A/B Test activity](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).
1. When you get to the [!UICONTROL Targeting] page, click the [!UICONTROL Traffic Allocation] control, then choose the desired traffic allocation method in the right pane, as shown below:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experience]

   ![Traffic Allocation Method settings](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

## Include recommendations inside A/B activities

You can include recommendations inside [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], and [!UICONTROL Auto-Target] activities (and [!UICONTROL Experience Targeting] (XT) activities). For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md). 

This functionality requires that you have a [Target Premium license](/help/main/c-intro/intro.md#premium).
