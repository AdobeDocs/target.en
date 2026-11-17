---
keywords: auto-target;targeting;traffic allocation;frequently asked questions;faq;troubleshooting;trouble shooting
description: Learn how an [!UICONTROL Auto-Target] activity serves the most tailored experience to each visitor based on customer profiles and the behavior of similar visitors.
title: What Is an [!UICONTROL Auto-Target] Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
TQID: 'https://experienceleague.adobe.com/uKmfIlOcT-tZgOjuvERXuif-Y5-2Jw3prtPbuBjv1is'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
---
# Get started with [!UICONTROL Auto-Target] {#auto-target-overview}

>[!BEGINSHADEBOX]

**On this page:** Learn how an **[!UICONTROL Auto-Target]** activity serves the most tailored experience to each visitor, how it works, how to choose the traffic allocation, and how it compares with **[!UICONTROL Automated Personalization]**.

>[!ENDSHADEBOX]

**[!UICONTROL Auto-Target]** activities in [!DNL Adobe Target] use advanced machine learning to select from multiple high-performing, marketer-defined experiences to personalize content and drive conversions. **[!UICONTROL Auto-Target]** serves the most tailored experience to each visitor based on the individual customer profile and the behavior of previous visitors with similar profiles.

>[!NOTE]
>
>* **[!UICONTROL Auto-Target]** is available as part of the [!DNL Target Premium] solution. This feature is not available in [!DNL Target Standard] without a [!DNL Target Premium] license. For more information about the advanced features this license provides, see [Target Premium](/help/main/c-intro/intro.md).
>
>* **[!UICONTROL Analytics for Target]** (A4T) supports **[!UICONTROL Auto-Target]** activities. For more information, see [A4T support for Auto-Allocate and Auto-Target activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

When you [create an A/B activity](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) with the three-step guided workflow, choose the **[!UICONTROL Auto-Target for personalized experiences]** option on the **[!UICONTROL Targeting]** page (step 2). For the steps, see [Create an Auto-Target activity](/help/main/c-activities/auto-target/create-auto-target.md).

![Traffic Allocation Method settings](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

This option within the A/B activity flow lets you use machine learning to personalize content, based on a set of marketer-defined experiences, in one click. **[!UICONTROL Auto-Target]** is designed to deliver maximum optimization, compared to traditional A/B testing or **[!UICONTROL Auto-Allocate]**, by determining which experience to display for each visitor. Unlike an A/B activity, in which the objective is to find a single winner, **[!UICONTROL Auto-Target]** automatically determines the best experience for a given visitor. The best experience is based on the visitor profile and other contextual information.

Similarly to **[!UICONTROL Automated Personalization]**, **[!UICONTROL Auto-Target]** uses a [Random Forest algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), a leading data science ensemble method, to determine the best experience to show to a visitor. **[!UICONTROL Auto-Target]** can adapt to changes in visitor behavior, so it can run perpetually to provide lift. This method is sometimes referred to as "always-on" mode.

Unlike an A/B activity, in which the experience allocation for a given visitor is sticky, **[!UICONTROL Auto-Target]** optimizes the specified business goal over each visit. As in **[!UICONTROL Automated Personalization]**, **[!UICONTROL Auto-Target]** reserves part of the activity traffic as a control group by default, to measure lift. Visitors in the control group are served a random experience in the activity.

## Considerations {#considerations}

Keep the following points in mind when you use **[!UICONTROL Auto-Target]**:

* Pay attention to the activity shape. Performance depends more on the number of locations × offers than on the raw experience count. Large cartesian combinations can slow loading and editing in the **[!UICONTROL Visual Experience Composer]**, even below the documented experience limits.

  As a best practice, keep **[!UICONTROL Auto-Target]** and **[!UICONTROL Automated Personalization]** activities to 4–6 locations with 4–6 offers per location. Larger configurations are not recommended. These activities are built directly in the **[!UICONTROL Experiences]** step, so the [!DNL Target] UI may show inline warnings or block saving when the configuration exceeds supported thresholds.

* You cannot switch a specific activity from **[!UICONTROL Auto-Target]** to **[!UICONTROL Automated Personalization]**, or the opposite way.
* You cannot switch from **[!UICONTROL Manual]** traffic allocation (traditional **[!UICONTROL A/B Test]**) to **[!UICONTROL Auto-Target]**, or the opposite way, after an activity is saved as a draft.
* One model is built to identify the performance of the personalized strategy versus randomly served traffic versus sending all traffic to the overall winning experience. This model considers hits and conversions in the default environment only.

  A second set of models is built for each modeling group (AP) or experience (AT). For each of these models, hits and conversions across all environments are considered.

  Requests are served with the same model, regardless of environment. However, the plurality of traffic should come from the default environment to ensure that the identified overall winning experience is consistent with real-world behavior.

* Use a minimum of two experiences.

## Terminology {#section_A309B7E0B258467789A5CACDC1D923F3}

The following terms are useful when discussing **[!UICONTROL Auto-Target]**:

|  Term  | Definition  |
|---|---|
|[Multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank}| A multi-armed bandit approach to optimization balances exploratory learning and exploitation of that learning.|
|[Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)|Random Forest is a leading machine learning approach. In data-science terms, it is an ensemble classification, or regression method, that works by constructing many decision trees based on visitor and visit attributes. Within [!DNL Target], Random Forest is used to determine which experience is expected to have the highest likelihood of conversion (or highest revenue per visit) for each specific visitor.|
|[Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank}|The goal of Thompson Sampling is to determine which experience is the best overall (non-personalized), while minimizing the "cost" of finding that experience. Thompson Sampling always picks a winner, even if there is no statistical difference between two experiences.|

## How [!UICONTROL Auto-Target] works {#section_77240E2DEB7D4CD89F52BE0A85E20136}

The following pages describe the data and algorithms underlying **[!UICONTROL Auto-Target]** and **[!UICONTROL Automated Personalization]**:

| Topic | Details |
|--- |--- |
|[Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)|The main personalization algorithm of [!DNL Target], used in both **[!UICONTROL Auto-Target]** and **[!UICONTROL Automated Personalization]**, is Random Forest. Ensemble methods, such as Random Forest, use multiple learning algorithms to obtain better predictive performance than could be obtained from any of the constituent learning algorithms. The Random Forest algorithm in **[!UICONTROL Automated Personalization]** and **[!UICONTROL Auto-Target]** activities is a classification, or regression method, that operates by constructing a multitude of decision trees at training time.|
|[Uploading Data For [!DNL Target] Personalization Algorithms](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md)|There are several ways to input data for **[!UICONTROL Auto-Target]** and **[!UICONTROL Automated Personalization]** models.|
|[Data Collection for [!DNL Target] Personalization Algorithms](/help/main/c-activities/t-automated-personalization/ap-data.md)|The personalization algorithms of [!DNL Target] automatically collect various data.|

## Determine the traffic allocation {#section_AB3656F71D2D4C67A55A24B38092958F}

Depending on the goal of your activity, you can choose a different traffic allocation between control and personalized experiences. Best practice is to determine this goal before you make your activity live.

The **[!UICONTROL Custom Allocation]** drop-down list lets you choose from the following options:

* **[!UICONTROL Evaluate Personalization Algorithm (50/50)]**
* **[!UICONTROL Maximize Personalization Traffic (90/10)]**
* **[!UICONTROL Custom Allocation]**

![Allocation Goal drop-down list](/help/main/c-activities/assets/split-new-ui.png)

The following table explains the three options:

| Activity Goal | Suggested Traffic Allocation | Tradeoffs |
|--- |--- |--- |
|**[!UICONTROL Evaluate Personalization Algorithm (50/50)]**: If your goal is to test the algorithm, use a 50/50 percent split of visitors between the control and the targeted algorithm. This split gives the most accurate estimate of the lift. Suggested for use with "random experiences" as your control.|50% Control / 50% Personalized Experience split|<ul><li>Maximizes accuracy of lift between control and personalized</li><li>Relatively fewer visitors have a personalized experience</li></ul>|
|**[!UICONTROL Maximize Personalization Traffic (90/10)]**: If your goal is to create an "always on" activity, put 10% of the visitors into the control to ensure that there is enough data for the algorithms to continue learning over time. The tradeoff here is that in exchange for personalizing a larger proportion of your traffic, you have less precision in what the exact lift is. No matter your goal, this is the recommended traffic split when using a specific experience as the control.|Best practice is to use a 10% - 30% Control / 70% - 90% Personalized Experience split|<ul><li>Maximizes the number of visitors who have a personalized experience</li><li>Maximizes lift</li><li>Less accuracy as to what the lift is for the activity</li></ul>|
|**[!UICONTROL Custom Allocation]**|Manually split the percentage as desired.|<ul><li>You might not achieve the desired results. If you are unsure, follow the suggestions for either of the preceding options</li></ul>|

To adjust the **[!UICONTROL Control]** percentage, click **[!UICONTROL Experiences]** in the **[!UICONTROL Traffic Allocation]** pane, then adjust the percentages as desired. You cannot decrease the control group to less than 10%.

You can [select a specific experience to use as control](/help/main/c-activities/t-automated-personalization/experience-as-control.md), or you can use the **[!UICONTROL Random experience]** option.

## Compare [!UICONTROL Auto-Target] and [!UICONTROL Automated Personalization] {#compare-at-ap}

**[!UICONTROL Auto-Target]** and **[!UICONTROL Automated Personalization]** share the same algorithm and data, but they differ in how the experiences are built and how much traffic the models need.

### What the two activity types have in common {#section_2A601F482F9A44E38D4B694668711319}

* **Optimization for each visit.** The algorithm predicts the propensity of a visitor to convert (or the estimated revenue from the conversion) to serve the best experience. A visitor is eligible for a new experience at the end of an existing session. The exception is a visitor in the control group, who keeps the experience assigned on the first visit. Within a session, the prediction does not change, to maintain visual consistency.
* **Adaptation to changes in visitor behavior.** The multi-armed bandit always "spends" a small fraction of traffic to continue to learn throughout the life of the activity and to prevent over-exploitation of previously learned trends. The underlying models are rebuilt every 24 hours using the latest visitor behavior data. If the algorithm cannot determine winning experiences for individuals, it automatically switches to showing the overall best-performing experience, found using [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling), while it continues to look for personalized winners.
* **A single goal metric.** The algorithm continually optimizes for one metric, which can be conversion-based or revenue-based (more specifically, **[!UICONTROL Revenue per Visit]**).
* **Automatic data collection.** [!DNL Target] automatically collects information about visitors to build the personalization models. For more information about the parameters used, see [Automated Personalization Data Collection](/help/main/c-activities/t-automated-personalization/ap-data.md).
* **Shared audiences.** [!DNL Target] automatically uses all [!DNL Adobe Experience Cloud] shared audiences to build the personalization models. You do not have to do anything specific to add audiences to the model. For information about using [!DNL Experience Cloud Audiences] with [!DNL Target], see [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).
* **Custom data.** Marketers can upload offline data, propensity scores, or other custom data to build personalization models. Learn more about [uploading data for Auto-Target and Automated Personalization](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

### How the two activity types differ {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

Consider **[!UICONTROL Auto-Target]** instead of **[!UICONTROL Automated Personalization]** when you want to define the entire experience, use the full set of **[!UICONTROL Visual Experience Composer]** (VEC) features, or make structural changes to your page.

| | [!UICONTROL Auto-Target] | [!UICONTROL Automated Personalization] |
|---|---|---|
| **Experience definition** | You define the entire experience, which can contain multiple changes. | Individual offers are automatically combined to form an experience. |
| **[!UICONTROL Visual Experience Composer] features** | **[!UICONTROL Auto-Target]** is embedded in the A/B activity workflow, so it benefits from the more mature and full-fledged VEC. You can also use [QA links](/help/main/c-activities/c-activity-qa/activity-qa.md). | The custom code editor, multiple experience audiences, and other features are not supported. |
| **Structural changes to the page** | More appropriate. For example, you can rearrange elements on your home page. | Less appropriate. |
| **Number of experiences** | Usually fewer, because one experience can contain multiple changes. | Usually more, because the experiences are all the combinations of offers and locations. |
| **Traffic needed to build the models** | Frequently less in total. | Frequently more in total. |

The amount of traffic *per experience* required to build the models is the same for both activity types. **[!UICONTROL Auto-Target]** frequently requires less total traffic because it usually has fewer experiences.

For example, in an **[!UICONTROL Automated Personalization]** activity with two offers per location and two locations, there are four (2 × 2 = 4) total experiences in the activity (with no exclusions). In **[!UICONTROL Auto-Target]**, you could set experience 1 to include offer 1 in location 1 and offer 2 in location 2, and experience 2 to include offer 2 in location 1 and offer 1 in location 2. **[!UICONTROL Auto-Target]** allows multiple changes within one experience, so you can reduce the total number of experiences in your activity.

### Traffic requirements for [!UICONTROL Auto-Target] {#traffic-requirements}

The following rules of thumb help to understand the traffic requirements:

* **When [!UICONTROL Conversion] is your success metric:** 1,000 visits and at least 50 conversions per day per experience. In addition, the activity must have at least 7,000 visits and 350 conversions.
* **When [!UICONTROL Revenue per Visit] is your success metric:** 1,000 visits and at least 50 conversions per day per experience. In addition, the activity must have at least 1,000 conversions per experience. **[!UICONTROL Revenue per Visit]** usually requires more data to build models, because the variance in visit revenue is typically higher than in conversion rate.

**[!UICONTROL Auto-Target]** also provides an extensive online testing framework. The multi-armed bandit is part of a larger online-testing framework that allows [!DNL Adobe] data scientists and researchers to understand the benefits of their continual improvements in real-world conditions. In the future, this test bed will allow [!DNL Adobe] to open its machine learning platform to data-savvy clients, so that they can bring in their own models to augment the [!DNL Target] models.

For more information about reporting, see [Reporting and Auto-Target](/help/main/c-activities/auto-target/reporting-and-auto-target.md).
