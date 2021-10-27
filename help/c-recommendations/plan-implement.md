---
keywords: Recommendations;settings;preferences;industry vertical;filter incompatible criteria;default host group;thumb base url;recommendations api token
description: Learn how to implement Recommendations activities in Adobe Target. 
title: How Do I Implement Recommendations Activities?
feature: Recommendations
exl-id: b6edb504-a8b6-4379-99c1-6907e71601f9
---
# ![PREMIUM](/help/assets/premium.png) Plan and implement [!DNL Recommendations] 

Before setting up your first [!DNL Recommendations] activity in [!DNL Adobe Target], complete the following steps:

1. [Implement [!DNL Target]](#implement-target) on the web and mobile app surfaces that you want to use for capturing user behavior and delivering recommendations.
1. [Set up your [!DNL Recommendations] catalog](#rec-catalog) of products or content that you want to recommend to your users.
1. [Pass behavioral information and context](#pass-behavioral) to [!DNL Target Recommendations] to allow it to deliver personalized recommendations.
1. [Configure global exclusions](#exclusions).
1. [Configure [!DNL Recommendations] settings](#concept_C1E1E2351413468692D6C21145EF0B84).

## Implement [!DNL Target] {#implement-target}

[!DNL Target Recommendations] requires you to implement the [!DNL Adobe Experience Platform Web SDK] or at.js 0.9.2 (or later). See [Implement [!DNL Target]](/help/c-implementing-target/implementing-target.md) for more information.

## Set up your Recommendations catalog {#rec-catalog}

To deliver high-quality recommendations, [!DNL Target] must know about the products or content that you want to recommend. Your catalog should usually include three types of information about the items you want to recommend. Suppose that you are recommending movies. Include the following:

1. Data that you want to display to the user receiving the recommendation. For example, you can display the name of the movie and a URL for a thumbnail image of the movie poster.
1. Data that is useful for applying marketing and merchandising controls. For example, you can display the rating of the movie so that you do not recommend NC-17 movies.
1. Data that is useful for determining the similarity of items to other pieces of items. For example, you can display the genre of the movie and director of the movie.

[!DNL Target] offers multiple integration options to populate your catalog. These options can be used in combination to update different items in the catalog or to update different item attributes on different frequencies.

|Method|What it is|When to use it|Additional information|
| --- | --- | --- | --- |
|Catalog feed|Schedule a feed (CSV, Google Product XML, or [!DNL Analytics Product Classifications]) to be uploaded and ingested on a daily basis.|For sending information about multiple items at a time. For sending information that changes infrequently.|See [Feeds](/help/c-recommendations/c-products/feeds.md).|
|Entities API|Call an API to send to-the-minute updates for a single item.|For sending updates as they happen about one item at a time. For sending information that changes frequently (for example price, inventory/stock level).|See the [Entities API developer documentation](https://developers.adobetarget.com/api/recommendations/#tag/Entities).|
|Pass updates on the page|Send to-the-minute updates for a single item using JavaScript on the page or using the Delivery API.|For sending updates as they happen about one item at a time. For sending information that changes frequently (for example price, inventory/stock level).|See [Item views/product pages](#items-product-pages) below.|

Most customers should implement at least one feed. You can then choose to complement your feed with updates for frequently changed attributes or items using either the Entities API or on-the-page method.

## Pass behavioral information and context {#pass-behavioral}

The behavioral information and context that you should pass to [!DNL Target] depends on the action your visitor is taking, which is often associated with the type of page that your visitor is interacting with.

### Item views/product pages {#items-product-pages}

On pages where a visitor is viewing a single item, such as a product detail page, you should pass the identity of the item the visitor is viewing. You should also pass the most granular category of the item that the visitor is viewing, to allow filtering recommendations to the current category.

You can also pass certain quickly changing attributes on the product page itself. For example, you can pass the price (`value`) and inventory/stock level.

```
<script type="text/javascript">
function targetPageParams() { 
   return { 
      "entity": { 
         "id": "32323", 
         "categoryId": "running-shoes", 
         "value": 119.99, 
         "inventory": 329 
      } 
   } 
}
</script>
```

### Category views/category pages

On a category page, you likely want to restrict your recommendations to products or content within that category. To do so, ensure you pass the identity of the currently viewed category.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "running-shoes" 
      } 
   } 
}
```

### Cart adds/cart views/checkout pages {#cart}

On a cart page, you can recommend items based on the contents of the visitor's current cart. To do so, pass the IDs of all items in the visitor's current cart using the special parameter `cartIds`.

```
function targetPageParams() {
   return {
      "cartIds": ["352", "223", "23432", "432", "553"]
      }
}
```

Cart-based recommendation logic is similar to the "[!UICONTROL Recommended For You]"  user-based algorithm and to the "[!UICONTROL People Who Viewed These, Bought Those]" and "[!UICONTROL People Who Bought These, Bought Those]" item-based algorithms. 

[!DNL Target] uses collaborative filtering techniques to determine similarities for each item in the visitor's cart, then combines these behavioral similarities across each item to get a merged list. 

[!DNL Target] also gives marketers the choice of looking at visitor behavior within a single session or across multiple sessions:

* **Within a single session**: Based on what other visitors did within a single session.

  Looking at behavior within a single session might make sense when there's a sense that products strongly "go with" each other based on a usage, occasion, or event. For example, a visitor is buying a printer and might also need ink and paper. Or, a visitor is buying peanut butter and might also need bread and jelly.

* **Across multiple sessions**: Based on what other visitors did across multiple sessions.

  Looking at behavior across multiple sessions might make sense when there's a sense that products strongly "go with" each other based on visitor preference or taste. For example, a visitor likes Star Wars and might also like Indiana Jones, even if the visitor doesn't necessarily want to watch both movies in the same sitting. Or, a visitor likes the board game "Codenames" and might also like the board game "Avalon," even if the visitor cannot play both games simultaneously. 

Regardless of whether you look at visitor behavior within a single session or over multiple sessions, [!DNL Target] makes recommendations for this visitor based on the items in their current cart.

### Exclude items already in the visitor's cart

On pages throughout your site, you can exclude some items from recommendations. For example, you might not want to recommend items that are already in the visitor’s current cart. To do so, pass the IDs of all items you want to exclude using the special parameter `excludedIds`.

```
function targetPageParams() {
   return {
      "excludedIds": ["352", "223", "23432", "432", "553"]
      }
}
```

### Purchases/order confirmation pages

When a purchase event occurs, pass the identity of the purchased item or items. See [Track Conversions](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053) in *Implement [!DNL Target] without a tag manager*.

## Configure global exclusions {#exclusions}

Exclude any items on a global level that you never want recommended to a visitor. See [Exclusions](/help/c-recommendations/c-products/exclusions.md). 
 
## Configure [!DNL Recommendations] settings {#concept_C1E1E2351413468692D6C21145EF0B84}

Use settings to manage your [!DNL Recommendations] implementation.

To access the [!UICONTROL Recommendations Settings] options, open [!DNL Target] in the [!DNL Adobe Experience Cloud], then click **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

![](assets/recs_settings.png)

The following options are available:

| Setting | Description |
|--- |--- |
|Custom Global Mbox|(Optional) Specify the custom global mbox used to serve [!DNL Target] activities. By default, the global mbox used by [!DNL Target] is used for [!DNL Recommendations].<br>Note: This option is set on the [!DNL Target] [!UICONTROL Administration] page. Open [!DNL Target], then click [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer].|
|Industry Vertical|The industry vertical is used to help categorize your recommendations criteria. This information helps members of your team find criteria that make sense for a particular page, such as criteria that are best for the shopping cart page or for a media page.|
|Filter Incompatible Criteria|Enable this option to show only those criteria where the selected page passes the required data. Not every criteria runs correctly on every page. The page or mbox must pass in `entity.id` or `entity.categoryId` for the current item/current category recommendations to be compatible. In general, it is best to show only compatible criteria. However, if you want incompatible criteria to be available for the activity, uncheck this option.<br>It is recommended that you disable this option if using a tag management solution.<br>For more information about this option, see [Recommendations FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md).|
|Default Host Group|Select your default host group.<br>The host group can be used to separate the available items in your catalog for different uses. For example, you can use host groups for Development and Production environments, different brands, or different geographies. By default, preview results in Catalog Search, Collections, and Exclusions are based on the default host group. (You can also select a different host group to preview results, by using the Environment filter.) By default, newly added items are available in all host groups unless an environment ID is specified when creating or updating the item. Delivered recommendations depend on the host group specified in the request.<br>If you don't see your products, make sure that you are using the correct host group. For example, if you set up your recommendation to use a staging environment and you set your host group to Staging, you might need to re-create your collections in the staging environment for the products to show. To see which products are available in each environment, use Catalog Search with each environment. You can also preview the contents of Recommendations collections and exclusions for a selected environment (host group).<br>**Note:** After changing the selected environment, you must click Search to update the returned results.<br>The [!UICONTROL Environment] filter is available from the following places in the [!DNL Target] UI:<ul><li>Catalog Search ([!UICONTROL Recommendations] > Catalog Search)</li><li>Create Collection dialog box ([!UICONTROL Recommendations > Collections > Create New])</li><li>Update Collection dialog box ([!UICONTROL Recommendations > Collections > Edit])</li><li>Create Exclusion dialog box ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>Update Exclusion dialog box ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul>For more information, see [Hosts](/help/administrating-target/hosts.md).|
|Thumbnail Base URL|Setting a base URL for your product catalog makes it possible to use relative URLs when specifying thumbnails of your products when passing in your thumbnail URL.<br>For example:<br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br>sets a URL relative to the thumbnail base URL.|
|Recommendations API Token|Use this token in Recommendations API calls, such as the Download API.|
