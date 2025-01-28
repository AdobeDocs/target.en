---
keywords: catalog search;catalog;search;exclusion;collection;filter;recommendations
description: Learn how to use the [!DNL Recommendations] [!UICONTROL Catalog Search] to locate products or content, remove items from your catalog, and more.
title: How Do I Use the [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
hide: yes
hidefromtoc: yes
exl-id: 6b0175b1-0eee-498d-8a08-513cf6695114
---
# [!UICONTROL Catalog Search]

The [!UICONTROL Catalog Search] page in [!DNL Adobe Recommendations] helps you locate the products or content in your catalog. The most basic task you can perform on this page is to search for an item. In addition, you can change the environment, filter facets, modify columns in the table, add new search facets, and more.

Catalogs refer to your entire product set (entities). Your catalog can contain many collections, a way to organize your products in logical buckets.

## Access [!UICONTROL Catalog Search]

1. To access the [!UICONTROL Catalog Search] page, click **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

1. (Optional) To apply filters to your search, click the **[!UICONTROL Show Filters]** icon ( ![Show Filters icon](/help/main/assets/icons/Filter.svg) ). You can filter by [!UICONTROL Environment], [!UICONTROL Collections], [!UICONTROL Category], [!UICONTROL Brand], [!UICONTROL Inventory], and [!UICONTROL Value].

## Perform a simple search

1. Type a search term in the **[!UICONTROL Search In]** field.

1. (Optional) You can refine your search by selecting a search option from the options menu that displays when you click the down arrow in the [!UICONTROL Search In] field.

   Search options include the following:

   * ID
   * Name
   * Message

1. Scroll through the items in the search results to view thumbnails and other product information.

   >[!NOTE]
   >
   > When you perform a catalog search on a custom attribute with a numeric value, the results treat the custom attribute to be a string type instead of a numeric value.
   >
   >There is no functionality currently available that lets you change the type of an attribute. To make a change, [open a customer issue](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) referencing the attributes that need the type changed from string to numeric.

<!-- ### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.-->

## View an item's details

You can view an individual item's details, including ID, name, message, category, and more by viewing its details.

1. Click an item in the search results to view its details.

## Remove an item from the catalog

1. Click an item in the search results to view its details.

1. Click **[!UICONTROL Remove from Catalog]**.

1. Confirm that you want to remove the item.

All information about that item is removed from the catalog index. The item will be included in your catalog only if it is added again in a data feed. A deleted item must be separately deleted from feeds.

## Refresh the catalog

The index of your catalog is automatically created when you upload your first feed, and refreshed according to the [specified schedule](/help/main/c-recommendations/c-products/feeds.md#steps).

The catalog is automatically refreshed when updates are received via feed files, API, or mbox updates. Updates are usually completed within an hour. If updates are in progress, the time that the most recent update started displays. If no updates are in progress, the time that the most recent update started and finished displays.

<!-- ## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.-->

## Change the environment

[Environments](/help/main/administrating-target/environments.md) let you organize your sites and pre-production environments for easy management and separated reporting.

1. Click the Show Filters icon ( ![Show Filters icon](/help/main/assets/icons/Filter.svg) ).

1. Select the desired environment from the **[!UICONTROL Environment]** drop-down list.

<!-- ## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.-->

## Modify columns

You can modify the active columns on the [!UICONTROL Catalog Search] page.

1. Click the **[!UICONTROL Customize Table]** icon (  ![Customize Table icon](/help/main/assets/icons/ColumnSetting.svg) ).

1. Select or deselect the desired columns that you want to display or hide.

Any changes you make are persistent across sessions.
