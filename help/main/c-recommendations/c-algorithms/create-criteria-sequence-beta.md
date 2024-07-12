---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;limit number of items returned;slot level control;slot
description: Learn how to set sequences of up to five criteria to exercise greater control of the items that appear in your Recommendations activities.
title: How Do I Create Criteria Sequences in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
hide: yes
hidefromtoc: yes
---
# Create criteria sequences

Use sequences of up to five criteria to exercise greater control of the items that appear in your [!DNL Adobe Target] [!UICONTROL Recommendations] activities. You can also limit the number of items returned (sometimes referred to as "slot level control").

>[!NOTE]
>
>Criteria sequences cannot be used with [!UICONTROL Recommendations] activities created before the October 2016 Release of [!DNL Target Premium].

To create a criteria sequence, you must first create the criteria you want to include in the sequence. See [Create criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) for more information.

By using a criteria sequence, you can provide additional targeted recommendations, instead of using more generic backup recommendations, when a criteria doesn't return enough results to fill your design. Typically, a criteria sequence proceeds from more specific targeting, which might return fewer results, to more general targeting, which usually returns more results.

Your criteria sequences might vary in order depending on the page type, as shown in the following examples:

|Page type|Possible sequence order|
| --- | --- |
|Product page|<ol><li>Based on current item, from the same brand</li><li>Based on current item, from all brands</li><li>Based on content similarity</li><li>Based on top sellers</li><li>Based on most-viewed items across the site</li></ol>|
|Home page|<ol><li>Based on visitor's last purchase </li><li>Based on visitor's favorite item</li><li>Based on visitor's favorite category</li><li>Based on top sellers</li><li>Based on most-viewed across site</li></ol>|

## Create a criteria sequence

You create criteria sequences from the [!UICONTROL Create Criteria Sequence] screen.

There are multiple ways to reach the [!UICONTROL Create Criteria Sequence] screen. Some screen options vary depending on how you reach the screen.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Criteria you create here are automatically made available for all [!UICONTROL Recommendations] activities.
* When you are creating a [!UICONTROL Recommendations] activity, from the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. You have the option to save your new criteria sequence for use with other [!UICONTROL Recommendations] activities. 
* When you are editing a [!UICONTROL Recommendations] activity, click in a [!UICONTROL Recommendations Location] box on your page, then select **[!UICONTROL Change Criteria]**. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. You have the option to save your new criteria for use with other [!UICONTROL Recommendations] activities. 

The following steps assume you access the [!UICONTROL Create Criteria Sequence] screen by using the first method: the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

1. Fill in the information in the [Basic Information](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) section.

1. In the **[!UICONTROL Criteria Sequence]** section, click the Plus ( + ) sign to add one or more criteria sequences.

   The sequence order defines the order in which a design is filled. If Criteria 1 does not have enough recommendations to fill your design, the remaining slots are filled with Criteria 2, and so on.

1. On the [!UICONTROL Select Criteria] screen, select a criteria, then click **[!UICONTROL Save]**.

   You can use the [!UICONTROL Search] box and the filter option to find the desired criteria.

1. (Optional) Slide the **[!UICONTROL Limit the number of items returned]** toggle to the "on" position, then specify the number of items (between 1 and 50).

   To help you understand the value of the [!UICONTROL Limit the number of items returned] option (sometimes called "slot level control,") consider the following use cases:

   * **Use Case 1**: You want to have a mix of different kinds of items in a single recommendations tray. For example, you want to show a mix of outerwear (jackets) and tops (shirts, T-shirts). To achieve this, use a Collection for the activity that includes all of the potential product types you want in any slots in your design. Then, set up your first criteria with a static filter limiting the criteria to include only outerwear, and set up your second criteria with a static filter limiting the criteria to include only tops. Finally, add both criteria to a criteria sequence and limit the first criteria to 2 slots.

     The recommendations tray might look like this on your site:

     ![Featured Products recommendations tray](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Use Case 2**: You want a mix of both alternative items and complementary items. Set up one criteria to use a viewed/viewed algorithm and use a dynamic filter that limits the recommended items to the current item's category. Set up the second criteria to use a viewed/bought algorithm and use a dynamic filter that includes only recommended items that do not match the current item's category. Finally, add both criteria to a sequence and limit the first criteria to 2 slots.

1. Continue adding additional criteria to your sequence. You can add up to five criteria to a sequence. 

1. Enable [Backup Content options](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Click **[!UICONTROL Create]**.

   The criteria sequence displays in the [!UICONTROL Criteria] list.

   For more information about recommendation logic options, see [Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md).