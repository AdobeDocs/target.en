---
keywords: automated personalization;ap;audiences;ensemble;random forest;multi-armed bandit;thompson sampling;ml;machine learning
description: Learn how to use [!UICONTROL Automated Personalization] (AP) activities in [!DNL Adobe Target] that use advanced machine learning to match different offer variations to each visitor.
title: What is an [!UICONTROL Automated Personalization] (AP) Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
---
# [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP) activities in [!DNL Adobe Target] combine offers or messages, and uses advanced machine learning to match different offer variations to each visitor based on their individual customer profile to personalize content and drive lift.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is available as part of the [!DNL Target Premium] solution. This feature is not available in [!DNL Target Standard] without a [!DNL Target Premium] license. For more information about the advanced features this license provides, see [Target Premium](/help/main/c-intro/intro.md#premium).

Similarly to [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] uses a [Random Forest algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), a leading data science ensemble method, as its main personalization algorithm to determine the best experience to show a visitor. [!UICONTROL Automated Personalization] can be valuable in the discovery phase of testing. It is also useful to allow machine learning to determine the most effective content when targeting diverse visitors. Over time, the algorithm learns to predict the most effective content and displays the content most likely to achieve your goals.

To find more information about how [!UICONTROL Automated Personalization] differs from [!UICONTROL Auto-Target], see [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Marketers implement one file on their site, which lets them point and click any content and then visually create and select additional content options for that area using the [!UICONTROL Visual Experience Composer] (VEC). Then, the algorithm automatically determines which piece of content to deliver to each individual visitor based on all the behavioral data that the system has about that visitor, providing a personalized experience. Because [!UICONTROL Automated Personalization] can adapt to changes in visitor behavior, it can be run without a set end date to provide ongoing lift and personalization. This mode is sometimes referred to as "always-on." The marketer does not need to run a test, analyze the results, then deliver a winner before realizing the lift found from optimization, which is a standard order of operations to implement the outcome of a standard A/B activity.

The following terms are useful when discussing [!UICONTROL Automated Personalization]:

|Term|Definition|
|---|---|
|Multi-armed bandit| A multi-armed bandit approach to optimization balances exploratory learning and exploitation of that learning.|
|Random Forest|A leading machine-learning approach. In data-science terms, it is an ensemble classification or regression method that works by constructing many decision trees based on visitor and visit attributes.|
|Thompson Sampling|The goal of Thompson Sampling is to determine which experience is the best overall (non-personalized), while minimizing the "cost" of finding that experience. Thompson sampling always picks a winner, even if there is no statistical difference between two experiences. For more information, see [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling).|

Consider the following details when using [!UICONTROL Automated Personalization]:

## [!UICONTROL Automated Personalization] uses a Random Forest algorithm to personalize

Random Forest is a leading machine-learning approach. In data-science terms, it is an ensemble classification or regression method that works by constructing many decision trees based on visitor and visit attributes. Within [!DNL Target], Random Forest is used to determine which experience is expected to have the highest likelihood of conversion (or highest revenue per visit) for each specific visitor. For example, visitors who use Chrome, are gold loyalty members, and access your site on Tuesdays might be more likely to convert with Experience A. Visitors from New York might be more likely to convert with Experience B. For more information about Random Forest in [!DNL Target], see [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## The personalization model optimizes for each visit

* The algorithm predicts a visitor's likelihood of conversion (or estimated revenue from conversion) to serve the best experience. 
* A visitor is eligible for a new experience upon the end of an existing session, unless that visitor is in the control group. If the visitor is in the control group, the experience that the visitor sees on the first visit is the same experience seen in subsequent visits. 
* The experience presented does not change within a session to maintain visual consistency.

## The personalization model adapts to changes in visitor behavior

* The multi-arm bandit ensures that the model is always "spending" a small fraction of traffic to continue learning throughout the life of the activity and to prevent over-exploitation of previously learned trends. 
* The underlying models are rebuilt every 24 hours using the latest visitor behavior data to ensure that [!DNL Target] is always using changing visitor preferences. 
* If the algorithm can't determine winning experiences for individual visitors, it automatically switches to showing the overall best-performing experience, while still continuing to look for personalized winners. The best-performing experience is found using [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling).

## The model continually optimizes a single goal metric

* This metric could be conversion-based or revenue-based (more specifically, [!UICONTROL Revenue per Visitor]).

## [!DNL Target] automatically collects information about visitors to build the personalization models

* For more information about the attributes used in [!UICONTROL Auto-Target] and [!UICONTROL Automated Personalization], see [Automated Personalization Data Collection](/help/main/c-activities/t-automated-personalization/ap-data.md).

## [!DNL Target] automatically uses all [!DNL Adobe Experience Cloud] shared audiences to build the personalization models

* You don't need to do anything specific to add audiences to the model. For information about using [!DNL Experience Cloud Audiences] with [!DNL Target], see [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).

## Marketers can upload offline data, propensity scores, or other custom data to build personalization models

Offline data, such as CRM information or customer-churn propensity scores, can be incredibly valuable when building personalization models. There are several ways to input data in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] personalization algorithms.

* [mbox parameters](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank} 
* [Profile parameters](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank} 
* [Server-side APIs for profile update](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}

For information about the data automatically collected and used by [!UICONTROL Automated Personalization] and [!UICONTROL Auto-Target] personalization algorithms, see [Automated Personalization Data Collection](/help/main/c-activities/t-automated-personalization/ap-data.md). 

## Training video: Activity Types

This video explains the activity types available in [!DNL Target]. [!UICONTROL Automated Personalization] is discussed beginning at 5:55.

* Describe the types of activities included in [!DNL Adobe Target] 
* Select the appropriate activity type to achieve your goals 
* Describe the three-step guided workflow that applies to all activity types

>[!VIDEO](https://video.tv.adobe.com/v/17386)
