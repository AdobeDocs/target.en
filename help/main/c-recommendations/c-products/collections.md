---
keywords: collection;Targeting
description: Learn how to use collections of products or items in [!DNL Target Recommendations].
title: How Do I Use Collections in Recommendations Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
TQID: 'https://experienceleague.adobe.com/kdjl2cpjaRWYZRqHFqARHvbTaTuu0iAH7ZWbD2Lrs7o'
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
# Collections {#collections}

>[!BEGINSHADEBOX]

**On this page:** Learn how to create, manage, and use collections of items in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

A collection is a set of products or items that are eligible for a recommendation. A collection is defined by the conditions that items must meet to be part of it. Items can be grouped in any way that makes sense for the business, such as similar or related items, products in a certain price range or color, or items that are likely to be interesting in a particular geographical area.

Collections organize products into logical buckets. For example, if some items are available in one region but not another, a collection can exclude the items that are unavailable in the visitor's region. Collections can also organize seasonal items or any other organizational parameters that apply to the business. Items can be grouped into catalogs, and separate recommendations can then be created for each collection.

The following points describe how collections interact with the rest of [!DNL Recommendations]:

* [Backup recommendations](/help/main/c-recommendations/c-algorithms/backup-recs.md) generated for each criteria within the recommendation also use the collection, so only items in the collection are included in the backup recommendation. As a result, only products that make sense to show in a location are displayed.
* Collections are rebuilt or updated every time each criteria runs.
* Collection rules apply to recommendation items generated after the criteria run. They affect only Entity Recommendations (ERs) in the output, not the key.
* Collections are not applied when using the **[!UICONTROL Recently Viewed Items]** recommendation key.
* Inclusion criteria allow similar results, but they must be set up every time an activity is created. A collection is created one time, then used whenever it is appropriate without being set up again.
* When you create or edit a [!DNL Recommendations] activity, the collection name appears next to the **[!UICONTROL Criteria]** label on the activity diagram.

## Create a collection {#task_1256DFF6842141FCAADD9E1428EF7F08}

Collections are available across the entire account, so a collection that is created once can be selected in any [!DNL Recommendations] activity. The rules are defined in the collection, so they do not have to be set up again for each activity.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** to display the list of existing collections.

   The **[!UICONTROL Collections]** page displays a list of your existing collections. To create a collection, click **[!UICONTROL Create Collection]**. To edit, copy, or delete an existing collection, click the More Actions icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallList.svg) ) next to the collection and then click the desired option.

   >[!NOTE]
   >
   >The "Number of Items" reported for each collection on the **[!UICONTROL Collections]** list view is the number of products matching the rules for that collection within the configured default Recommendations [host group](/help/main/administrating-target/hosts.md) (environment). See [Settings](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} to change the default host group.

1. Click **[!UICONTROL Create Collection]**.

    ![More Actions icon](../assets/collection_1.png)

1. Type a **[!UICONTROL Name]** for the collection. An optional **[!UICONTROL Description]** can also be entered.

1. (Conditional) Choose an [environment](/help/main/administrating-target/environments.md) from the **[!UICONTROL Environment]** filter to preview the contents of the collection in that environment. By default, results from the default host group are displayed.

1. Set the rules used to build the collection.

   A collection can be built around a product ID or category, margin, or any other parameter in the list. Add rules to use multiple parameters to define a collection. Multiple rules are joined with an AND operator, so all specified rules must be matched for the collection to apply.

1. Click **[!UICONTROL Create]**.

1. After creating your collection, click the More Actions icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallList.svg) ) and select the appropriate option: **[!UICONTROL Edit]**, **[!UICONTROL Copy]**, or **[!UICONTROL Delete]**.

    ![More Actions icon](../assets/collection_2.png)

<!--
## Create a collection using [!UICONTROL Advanced Search]

You can also create collections using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned.
-->

## Use a collection in an activity

A collection is selected for each experience of a [!DNL Recommendations] activity. The collection determines which items are eligible to appear in the recommendations of that experience.

1. [Create a collection](#task_1256DFF6842141FCAADD9E1428EF7F08).

    ![More Actions icon](../assets/collection_3.png)

1. Click **[!UICONTROL Activities]** and [create a new Recommendations activity](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) or edit an existing activity.

    ![More Actions icon](../assets/collection_4.png)

1. After you select a criteria and design, select the desired collection on the **[!UICONTROL Options]** page.

1. (Conditional) To change the collection of an existing activity, click a location where you placed recommendations on the **[!UICONTROL Experiences]** pages, click **[!UICONTROL Change Collection]**, then select the desired collection.
