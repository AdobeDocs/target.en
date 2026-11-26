---
keywords: promotions;front promotions;back promotions;promotions type;list of items;promote by attribute;promote a collection
description: Learn how to add promoted items and control their placement in your Adobe [!DNL Target] Recommendations designs. You can add static and dynamic promotions.
title: How Do I Add Promotions in Recommendations Designs?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
TQID: 'https://experienceleague.adobe.com/tAfKOzwjnUJgypDh-4LdVukNlTVwMS4UkvcNmCaCV0E'
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
# Add promotions {#add-promotions}

>[!BEGINSHADEBOX]

**On this page:** Learn how to add promoted items to a [!DNL Recommendations] design and how their sort order is determined.

>[!ENDSHADEBOX]

Promotions place specific items in a [!DNL Recommendations] design, in addition to the items recommended by the criteria. They use available slots in the design and take precedence over criteria results and backup recommendations. For example, if a design has six slots and two of them are used for promotions, four slots remain for items recommended based on criteria.

Promotions are de-duplicated against the items recommended by the criteria for the activity, so a given item does not appear twice in a single recommendations tray.

![Change promotion dialog with the Front Promotion and Back Promotion toggles turned off](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Using promotions changes the CSV structure and output. These changes can affect any external process that involves CSV, such as email.

## Add a promotion {#add-promotion}

A promotion defines which items are promoted, how many design slots they use, and the period during which they display.

1. On the **[!UICONTROL Options]** page, click the **[!UICONTROL Front Promotion]** or **[!UICONTROL Back Promotion]** toggle.

   The following illustration shows the **[!UICONTROL Front Promotion]** toggle in the "On" position. Promotions can be inserted both before and after the criteria results.

   ![Change promotion dialog with the Front Promotion toggle turned on, showing the Number of Design Slots, Scheduling, and Promotion Type options](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

1. Set the **[!UICONTROL Number of design slots]** to use for promoted items.

   Up to 20 slots can be used, depending on the [!DNL Recommendations] design. Each slot that is used becomes unavailable for the recommendations returned based on the criteria.

1. Set a **Start** date and an **End** date for the promoted items.

   If no start date is set, the promotion begins immediately. If no end date is set, the promotion runs indefinitely.

1. Select a **[!UICONTROL Promotion Type]**:

   * **[!UICONTROL List of items]**: Enter the `entity.id` values of the items to promote, separated by commas.
   * **[!UICONTROL Promote by attribute]**: Add rules to define the attributes of the items to promote. This option allows dynamic matches through static and dynamic inclusion rules. For detailed information, examples, and use-case scenarios, see [Use dynamic and static inclusion rules](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#inclusion-rules).
   * **[!UICONTROL Promote a collection]**: Choose the collection of items to promote. New collections can be created for promotions. See [Create a collection](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08).

   The promotion type also determines the sort order of the promoted items. See [Promotion types and sort order](#promotion-sort-order).

   ![Change promotion dialog with the Promotion Type options highlighted: List of items, Promote by attribute, and Promote a collection](/help/main/c-recommendations/t-create-recs-activity/assets/promotion_type.png)

1. Click **[!UICONTROL Save]**.

Promotions are applied to all experiences in the activity.

## Promotion types and sort order {#promotion-sort-order}

The sort order of the promoted items depends on the promotion type, as the following table shows.

|Promotion type|Default sort|Backup sort|Dynamic filtering option|
| --- | --- | --- | --- |
|**[!UICONTROL List of Items]**|Order entered in the [!DNL Target] UI or API|Random (when selected through the UI or API)|No|
|**[!UICONTROL Promote by Attribute]**|`entity.value` (descending order)|No randomization|Yes|
|**[!UICONTROL Promote a Collection]**|`entity.value` (descending order)|No randomization|No|

* **[!UICONTROL List of Items]**: The default sort order is the order entered in the [!DNL Target] UI or API. The **[!UICONTROL Randomize Item Order]** check box is available for this type. When the list includes more items than the number of slots set for promotions, this option randomizes which promoted items display in the design. On each hit, [!DNL Target] randomly selects the items enabled for promotions in the template from the entire promotion set.
* **[!UICONTROL Promote by Attribute]** and **[!UICONTROL Promote a Collection]**: The default order is based on the `entity.value` attribute, in descending numeric order. Randomizing the order is not applicable.

If the entities do not have an `entity.value` attribute (for example, the business does not sell products), a numeric value such as the publishing date can be passed into the `entity.value` attribute. The promoted items are then ordered by the most recent publishing date, in descending order. The `entity.value` attribute is of type double and does not accept strings.
