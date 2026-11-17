---
keywords: automated personalization;ap;audiences;ensemble;random forest;multi-armed bandit;thompson sampling;ml;machine learning
description: Learn how to use [!UICONTROL Automated Personalization] (AP) activities in [!DNL Adobe Target] that use advanced machine learning to match different offer variations to each visitor.
title: What is an [!UICONTROL Automated Personalization] (AP) Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
TQID: 'https://experienceleague.adobe.com/BBtKgNRTlqNFFoAjr1LQkhHyZeAlXG2h8D7bsndh4kQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
---
# [!UICONTROL Automated Personalization] (AP) {#automated-personalization-overview}

>[!BEGINSHADEBOX]

**On this page:** Learn how an **[!UICONTROL Automated Personalization]** activity matches offer variations to each visitor, and what to consider when you use it.

>[!ENDSHADEBOX]

>[!NOTE]
>
>**[!UICONTROL Automated Personalization]** is available as part of the [!DNL Target Premium] solution. This feature is not available in [!DNL Target Standard] without a [!DNL Target Premium] license. For more information about the advanced features this license provides, see [Target Premium](/help/main/c-intro/intro.md#premium).

**[!UICONTROL Automated Personalization]** (AP) activities in [!DNL Adobe Target] combine offers or messages, and use advanced machine learning to match different offer variations to each visitor based on their individual customer profile, to personalize content and drive lift.

Marketers implement one file on their site, which lets them point and click any content and then visually create additional content options for that area using the **[!UICONTROL Visual Experience Composer]** (VEC). The algorithm then automatically determines which piece of content to deliver to each visitor, based on all the behavioral data that the system has about that visitor.

**[!UICONTROL Automated Personalization]** adapts to changes in visitor behavior, so it can run without a set end date to provide ongoing lift and personalization. This mode is sometimes referred to as "always-on." The marketer does not need to run a test, analyze the results, and then deliver a winner before realizing the lift. **[!UICONTROL Automated Personalization]** is also valuable in the discovery phase of testing and when you target diverse visitors. For more information about how it differs from **[!UICONTROL Auto-Target]**, see [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

The following terms are useful when discussing **[!UICONTROL Automated Personalization]**:

|Term|Definition|
|---|---|
|Multi-armed bandit| A multi-armed bandit approach to optimization balances exploratory learning and exploitation of that learning.|
|Random Forest|A leading machine-learning approach. In data-science terms, it is an ensemble classification or regression method that works by constructing many decision trees based on visitor and visit attributes.|
|Thompson Sampling|The goal of Thompson Sampling is to determine which experience is the best overall (non-personalized), while minimizing the "cost" of finding that experience. Thompson Sampling always picks a winner, even if there is no statistical difference between two experiences. For more information, see [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling).|

## How the personalization model works {#how-ap-works}

**[!UICONTROL Automated Personalization]** uses a Random Forest algorithm to personalize. Random Forest is a leading machine-learning approach. In data-science terms, it is an ensemble classification or regression method that works by constructing many decision trees based on visitor and visit attributes. Within [!DNL Target], Random Forest is used to determine which experience is expected to have the highest likelihood of conversion (or highest revenue per visit) for each specific visitor. 

For example, visitors who use Chrome, are gold loyalty members, and access your site on Tuesdays might be more likely to convert with Experience A. Visitors from New York might be more likely to convert with Experience B. 

For more information about Random Forest in [!DNL Target], see [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

| Aspect | How it works |
|---|---|
| **Optimization for each visit** | The algorithm predicts the likelihood of a visitor to convert (or the estimated revenue from the conversion) to serve the best experience. A visitor is eligible for a new experience at the end of an existing session, unless that visitor is in the control group. A visitor in the control group sees the same experience as on the first visit. The experience does not change within a session, to maintain visual consistency. |
| **Adaptation to changes in visitor behavior** | The multi-armed bandit always spends a small fraction of traffic to continue learning throughout the life of the activity and to prevent over-exploitation of previously learned trends. The underlying models are rebuilt every 24 hours using the latest visitor behavior data. If the algorithm cannot determine winning experiences for individual visitors, it shows the overall best-performing experience, found using [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling), while it continues to look for personalized winners. |
| **Goal metric** | The model continually optimizes a single goal metric, which can be conversion-based or revenue-based (more specifically, **[!UICONTROL Revenue per Visit]**). |
| **Data and audiences** | [!DNL Target] automatically collects information about visitors to build the personalization models. For more information about the attributes used in **[!UICONTROL Auto-Target]** and **[!UICONTROL Automated Personalization]**, see [Automated Personalization Data Collection](/help/main/c-activities/t-automated-personalization/ap-data.md). [!DNL Target] also automatically uses all [!DNL Adobe Experience Cloud] shared audiences, so you do not need to do anything specific to add audiences to the model. For more information, see [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md). |
| **Custom data** | Marketers can upload offline data, such as CRM information or customer-churn propensity scores, or other custom data to build personalization models. The data can be input with [mbox parameters](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, [profile parameters](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, or [server-side APIs for profile update](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}. |

## Training video: Activity Types {#training-video}

This video explains the activity types available in [!DNL Target]. **[!UICONTROL Automated Personalization]** is discussed beginning at 5:55.

* Describe the types of activities included in [!DNL Adobe Target]
* Select the appropriate activity type to achieve your goals
* Describe the three-step guided workflow that applies to all activity types

>[!VIDEO](https://video.tv.adobe.com/v/17386)
