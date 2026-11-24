---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;limit number of items returned;slot level control;slot
description: Learn how to set sequences of up to five criteria to exercise greater control of the items that appear in your Recommendations activities.
title: How Do I Create Criteria Sequences in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
TQID: 'https://experienceleague.adobe.com/dxO5cKxesTxgzZyfcvydQUlSq4TAgFN0ztT5VIe1WKU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Create criteria sequences {#create-criteria-sequence}

>[!BEGINSHADEBOX]

**On this page:** Learn how to create criteria sequences to control the items that appear in [!DNL Adobe Target Recommendations] activities.

>[!ENDSHADEBOX]

Sequences of up to five criteria give greater control of the items that appear in [!DNL Adobe Target] **[!UICONTROL Recommendations]** activities. The number of items returned can also be limited (sometimes referred to as "slot level control").

When a criteria does not return enough results to fill the design, a criteria sequence provides additional targeted recommendations instead of more generic backup recommendations. Typically, a criteria sequence proceeds from more specific targeting, which might return fewer results, to more general targeting, which usually returns more results.

>[!NOTE]
>
>Criteria sequences cannot be used with **[!UICONTROL Recommendations]** activities created before the October 2016 Release of [!DNL Target Premium].

To create a criteria sequence, first create the criteria to include in the sequence. See [Create criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) for more information.

The order of a criteria sequence can vary depending on the page type, as shown in the following examples:

|Page type|Possible sequence order|
| --- | --- |
|Product page|<ol><li>Based on current item, from the same brand</li><li>Based on current item, from all brands</li><li>Based on content similarity</li><li>Based on top sellers</li><li>Based on most-viewed items across the site</li></ol>|
|Home page|<ol><li>Based on visitor's last purchase </li><li>Based on visitor's favorite item</li><li>Based on visitor's favorite category</li><li>Based on top sellers</li><li>Based on most-viewed across site</li></ol>|

## Create a criteria sequence

Criteria sequences are created from the **[!UICONTROL Create Criteria Sequence]** screen. There are multiple ways to reach this screen. Some screen options vary depending on how the screen is reached.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Criteria created here are automatically made available for all **[!UICONTROL Recommendations]** activities.
* When creating a **[!UICONTROL Recommendations]** activity, from the **[!UICONTROL Select Criteria]** screen, click **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. The new criteria sequence can be saved for use with other **[!UICONTROL Recommendations]** activities.
* When editing a **[!UICONTROL Recommendations]** activity, click in a **[!UICONTROL Recommendations Location]** box on the page, then select **[!UICONTROL Change Criteria]**. On the **[!UICONTROL Select Criteria]** screen, click **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. The new criteria can be saved for use with other **[!UICONTROL Recommendations]** activities.

The following steps assume that the **[!UICONTROL Create Criteria Sequence]** screen is accessed via the **[!UICONTROL Criteria]** menu.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

    ![Featured Products recommendations tray](../assets/criteria_create_6.png)

1. Fill in the information in the [Basic Information](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) section.

1. In the **[!UICONTROL Criteria Sequence]** section, click the Plus ( + ) sign to add one or more criteria sequences.

   The sequence order defines the order in which a design is filled. If Criteria 1 does not have enough recommendations to fill the design, the remaining slots are filled with Criteria 2, and so on.
  
    ![Featured Products recommendations tray](../assets/criteria_create_7.png)

1. On the **[!UICONTROL Select Criteria]** screen, select a criteria, then click **[!UICONTROL Save]**.

   The **[!UICONTROL Search]** box and the filter option can be used to find the desired criteria.

1. (Optional) Enable **[!UICONTROL Limit the number of items returned]**, then specify the number of items (between 1 and 50).

    ![Featured Products recommendations tray](../assets/criteria_create_8.png)

   The following use cases illustrate the value of the **[!UICONTROL Limit the number of items returned]** option (sometimes called "slot level control").

   +++ Use cases for limiting the number of items returned

   * **Use Case 1**: You want to have a mix of different kinds of items in a single recommendations tray. For example, you want to show a mix of outerwear (jackets) and tops (shirts, T-shirts). To achieve this, use a Collection for the activity that includes all of the potential product types you want in any slots in your design. Then, set up your first criteria with a static filter limiting the criteria to include only outerwear, and set up your second criteria with a static filter limiting the criteria to include only tops. Finally, add both criteria to a criteria sequence and limit the first criteria to 2 slots.

     The recommendations tray might look like this on your site:

     ![Featured Products recommendations tray](assets/featured-products.png)

   * **Use Case 2**: You want a mix of both alternative items and complementary items. Set up one criteria to use a viewed/viewed algorithm and use a dynamic filter that limits the recommended items to the current item's category. Set up the second criteria to use a viewed/bought algorithm and use a dynamic filter that includes only recommended items that do not match the current item's category. Finally, add both criteria to a sequence and limit the first criteria to 2 slots.

   +++

1. Continue adding additional criteria to the sequence. Up to five criteria can be added to a sequence.

1. Enable [Backup Content options](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Click **[!UICONTROL Create]**.

The criteria sequence displays in the **[!UICONTROL Criteria]** list.

For more information about recommendation logic options, see [Get started with Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md).
