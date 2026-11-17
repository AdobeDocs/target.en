---
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;automated personalization;control;default experience;best practices
description: Explore a list of frequently asked questions (FAQs) and answers about [!UICONTROL Automated Personalization] (AP) activities in [!UICONTROL Adobe Target].
title: How Can I Find FAQs about [!UICONTROL Automated Personalization] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
TQID: 'https://experienceleague.adobe.com/cYdFwvkJDlfGYdcxql9iWGwNiTed4Lb2kC7JdN7xgdo'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
---
# Automated Personalization FAQs {#ap-faq}

>[!BEGINSHADEBOX]

**On this page:** Find answers to frequently asked questions about **[!UICONTROL Automated Personalization]** activities.

>[!ENDSHADEBOX]

The following questions and answers cover how to set up **[!UICONTROL Automated Personalization]** activities in [!DNL Adobe Target], how the personalization models are built, how traffic is allocated, and how to read the results.

## Set up an activity {#set-up-an-activity}

+++ What are the best practices to set up an [!UICONTROL Automated Personalization] activity?

* Pay close attention to the *activity shape* (number of locations × number of offers), not only to the total experience count. The cartesian combinations of locations and offers affect authoring-time performance more than the raw number of experiences. For optimal performance and manageability, limit **[!UICONTROL Automated Personalization]** and **[!UICONTROL Auto-Target]** activities to 4–6 locations with 4–6 offers per location, as described in the question "What are some limits in Automated Personalization?" in this section. Larger configurations are not recommended and can lead to slow loading or editing in the **[!UICONTROL Visual Experience Composer]**.
* To personalize a lower-traffic page, or to make structural changes to the experience that you are personalizing, consider using an [**[!UICONTROL Auto-Target]** activity](/help/main/c-activities/auto-target/auto-target-to-optimize.md) instead of **[!UICONTROL Automated Personalization]**.
* Consider running an **[!UICONTROL A/B Test]** activity between the offers and locations that you plan to use in your **[!UICONTROL Automated Personalization]** activity, to confirm that the locations and offers have an impact on the optimization goal. If the **[!UICONTROL A/B Test]** activity fails to demonstrate a significant difference, **[!UICONTROL Automated Personalization]** likely also fails to generate lift.

  If an A/B…N test shows no statistically significant differences between experiences, one or more of the following situations is probably responsible:

  * The offers are likely not sufficiently different from each other.
  * The locations that you selected do not impact the success metric.
  * The optimization goal is too far in the conversion funnel to be affected by your chosen offers.

* Use the [Traffic Estimator](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator) to get a sense of how long it takes for personalization models to build in your **[!UICONTROL Automated Personalization]** activity.
* Decide on the allocation between the control and the targeted traffic before beginning the activity, based on your goals. The following table lists the three scenarios to consider, based on the goal of your activity and the type of control that you selected.

  | Control and activity goal | Recommended allocation to the control | Details |
  | --- | --- | --- |
  | **[!UICONTROL Random Experiences]** as the control, and the goal is to test the effectiveness of the personalization algorithm | 50% | This goal requires a more accurate picture of lift. You also most likely want to compare the conversion rate of your experiences or offers with the rate that a simple **[!UICONTROL A/B Test]** (a randomly served control) would give. |
  | **[!UICONTROL Random Experiences]** as the control, and the goal is to maximize personalized traffic | 10% to 30% | Use this option if you are comfortable with the algorithm and want the maximum amount of traffic personalized. The tradeoff is the accuracy of your lift information: the confidence intervals of the control traffic are larger, as less traffic flows to them. |
  | **[!UICONTROL Specific Experience]** as the control, with either goal | 10% to 30% | Use this option to compare a specific marketer-driven experience to the personalization models. When you select only one experience as the control, that traffic is not spread across every offer or experience in the activity. |

* Use targeting rules as sparingly as possible, as they can interfere with the ability of the model to optimize. For more information, see [Target Automated Personalization offers](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).
* Reporting groups can limit the success of your **[!UICONTROL Automated Personalization]** activity, so use them only under specific conditions. For more information, see [Offer reporting groups in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

  * Use reporting groups only if all of the following conditions are met:

    * You plan to replace or add offers while the activity is running.
    * The offers in the reporting group appeal to the same visitors.
    * The offers in the reporting group have about the same overall response rate.

  * There is no personalization between offers in a reporting group. The personalization model treats all the offers as the same.
  * Never put all offers in an activity into a single reporting group. Doing so causes all offers to be uniformly randomly served to all visitors in the activity.

+++

+++ What are some limits in [!UICONTROL Automated Personalization]?

[!DNL Target] has a hard limit of 30,000 experiences, but it functions at its best when fewer than 10,000 experiences are created. The same limit applies when the activity has the **[!UICONTROL Disallow Duplicates]** option enabled.

Although **[!UICONTROL Automated Personalization]** and **[!UICONTROL Auto-Target]** activities can support a large number of experiences, authoring performance depends heavily on the *activity shape* (number of locations × number of offers). Certain configurations create large cartesian combinations that can significantly impact load and edit performance, even below the documented experience limits.

For optimal performance and manageability, limit **[!UICONTROL Automated Personalization]** and **[!UICONTROL Auto-Target]** activities to 4–6 locations with 4–6 offers per location. Larger configurations are not recommended and may be restricted in the [!DNL Target] UI.

In the current [!DNL Target] UI, **[!UICONTROL Automated Personalization]** and **[!UICONTROL Auto-Target]** activities are configured directly in the **[!UICONTROL Experiences]** step. [!DNL Target] may display inline warnings or prevent you from saving an activity when the configuration exceeds the supported thresholds, and it re-validates the activity shape on **[!UICONTROL Next]**, **[!UICONTROL Save]**, and **[!UICONTROL Publish]**.

For more information about character limits and other limits (offer size, audiences, profiles, values, parameters, and so forth) that affect activities and other elements in [!DNL Target], see [Limits](/help/main/r-troubleshooting-target/target-limits.md).

+++

+++ Can I specify a specific experience to be used as a control in an [!UICONTROL Automated Personalization] activity?

You can select a specific experience to be used as the control while creating an [**[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/automated-personalization.md#automated-personalization-overview) (AP) or [**[!UICONTROL Auto-Target]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activity.

This feature lets you route the entire control traffic to that experience, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against the control traffic to that one experience.

For more information, see [Select the control experience](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

+++ How is offer-level targeting implemented?

When each visitor arrives, the offer-level targeting rules determine the set of offers that the visitor can see. The algorithm then chooses, from among those offers, the offer that the model predicts has the best expected revenue or chance of conversion. Offer targeting impacts the efficacy of the [!DNL Target] machine-learning algorithms, so use it as sparingly as possible. For more information, see [Target Automated Personalization offers](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

+++

## Model building and traffic allocation {#models-and-traffic}

+++ How is [!UICONTROL Automated Personalization] allocating my activity's traffic?

**[!UICONTROL Automated Personalization]** routes visitors to the experience that has the highest forecasted success metric, based on the most recent [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) models. This forecast is based on the specific information and visit context of the visitor.

For example, assume that an **[!UICONTROL Automated Personalization]** activity has two locations with two offers each. In the first location, Offer A has a forecasted conversion rate of 3% for a specific visitor, and Offer B has a forecasted conversion rate of 1%. In the second location, Offer C has a forecasted conversion rate of 2% for the same visitor, and Offer D has a forecasted conversion rate of 5%. Therefore, **[!UICONTROL Automated Personalization]** serves this visitor an experience with Offer A and Offer D.

+++

+++ How does [!UICONTROL Automated Personalization] build models with regard to environments?

One model is built to identify the performance of the personalized strategy versus randomly served traffic versus sending all traffic to the overall winning experience. This model considers hits and conversions in the default environment only.

A second set of models is built for each reporting group (**[!UICONTROL Automated Personalization]**) or experience (**[!UICONTROL Auto-Target]**). For each of these models, hits and conversions across all environments are considered.

Requests are, therefore, served with the same model, regardless of environment. However, the plurality of traffic should come from the default environment to ensure that the identified overall winning experience is consistent with real-world behavior.

+++

+++ How long should I wait for models to build?

The time it takes for models to build in your activity typically depends on the traffic to your selected activity locations and on your activity success metric. Use the [Traffic Estimator](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator) to determine the expected length of time it takes for models to build in your activity.

+++

+++ How can I decrease the time needed for models to build in my [!UICONTROL Automated Personalization] activity?

Review your activity setup for changes that improve the speed at which models build. For example, change an RPV success metric to conversion, choose a success metric that is closer to your activity experiences in the sales funnel, drop some experiences from the activity, or use a higher-traffic page. For more information, see [Troubleshoot Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-trouble.md).

+++

+++ One model is built within my [!UICONTROL Automated Personalization] activity. Are the visits to that experience personalized?

No. At least two models must be built within your activity for personalization to begin.

+++

## Results and lift {#results-and-lift}

+++ When can I look at the results of my [!UICONTROL Automated Personalization] activity?

You can begin to look at the results of your **[!UICONTROL Automated Personalization]** activity after at least two experiences have models built (indicated by a green checkmark).

+++

+++ Why is my [!UICONTROL Automated Personalization] activity not showing lift?

Four factors are required for an **[!UICONTROL Automated Personalization]** activity to generate lift:

* The offers in each location must be different enough to influence visitors.
* The locations must be somewhere that makes a difference to the optimization goal.
* There must be enough traffic and statistical power in the activity to detect the lift.
* The personalization algorithm must work well.

The best course of action is to first make sure, by using a simple, non-personalized **[!UICONTROL A/B Test]** activity, that the content and locations that make up the activity experiences truly make a difference to the overall response rates. For the complete procedure, see [Troubleshoot Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-trouble.md).

+++

+++ How can I compare [!UICONTROL Automated Personalization] to a default experience?

There is no turnkey option to compare **[!UICONTROL Automated Personalization]** to a default experience. As a workaround, if a default offer or experience exists as part of the activity, click the **[!UICONTROL Control]** segment in reports and locate that offer in the resulting offer-level report. The conversion rate recorded for this offer can be compared with the conversion rate of the entire "Random Forest" segment. This comparison shows how the model performs compared to the default offer.

+++

## Manage a live activity {#manage-live-activity}

+++ When should I stop my [!UICONTROL Automated Personalization] activity?

**[!UICONTROL Automated Personalization]** can be used as "always on" personalization that constantly optimizes. Especially for evergreen content, there is no need to stop your **[!UICONTROL Automated Personalization]** activity. If you want to make substantial changes to the content that are not similar to the offers currently in your activity, the best practice is to start a new activity. Starting a new activity helps other users who review reports to avoid confusing or relating past results with different content.

+++

+++ Can I change the goal metric midway through an [!UICONTROL Automated Personalization] activity?

[!DNL Adobe] does not recommend that you change the goal metric midway through an activity. Although it is possible to change the goal metric during an activity by using the [!DNL Target] UI, always start a new activity instead. [!DNL Adobe] does not guarantee what happens if you change the goal metric in an activity after it is running.

This recommendation applies to **[!UICONTROL Auto-Allocate]**, **[!UICONTROL Auto-Target]**, and **[!UICONTROL Automated Personalization]** activities that use either [!DNL Target] or [!DNL Analytics] (A4T) as the reporting source.

+++

+++ Can I use the [!UICONTROL Reset Report Data] option while running an [!UICONTROL Automated Personalization] activity?

[!DNL Adobe] does not recommend using the **[!UICONTROL Reset Report Data]** option for **[!UICONTROL Automated Personalization]** activities. Although it removes the visible reporting data, this option does not remove all training records from the **[!UICONTROL Automated Personalization]** model. Instead of using the **[!UICONTROL Reset Report Data]** option, create a new activity and deactivate the original activity. This guidance also applies to **[!UICONTROL Auto-Allocate]** and **[!UICONTROL Auto-Target]** activities.

+++

+++ Why are visitors seeing experiences for an [!UICONTROL Automated Personalization] activity that they should not see?

**[!UICONTROL Automated Personalization]** activities are evaluated once per session. If there are active sessions that have qualified for a particular experience and new offers have since been added to it, visitors see the new content along with the previously shown offers. These visitors previously qualified for those experiences, so they still see those experiences during the session. To evaluate the activity at every page visit, change to the **[!UICONTROL Experience Targeting]** (XT) activity type.

+++
