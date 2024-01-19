---
keywords: entity;entity attributes;pass information to Recommendations;behavioral data;data counter;define relative URL;display inventory level;define price;define profit margin;custom attributes
description: Learn how to use entity attributes to pass product or content information to [!DNL Target] Recommendations.
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
title: How Do I Use Entity Attributes?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
---
# Entity attributes

Use entity attributes to pass product or content information to [!DNL Adobe Target Recommendations].

Entities refer to the items you want to recommend. Entities can include products, content (articles, slide shows, images, movies, and television shows), job listings, restaurants, and so forth.

[!DNL Recommendations] sends the `productId` or `productPurchasedId` (referred to as `entity.id` in the code) that is used in the algorithms.

Consider the following:

* `entity.id` must match the `productPurchasedId` sent to the order confirmation page and the `productId` used in [!DNL Adobe Analytics] product reports.
* Entity attribute values that you pass to [!DNL Recommendations] expire after 61 days. Adobe recommends that you pass the latest value of each entity attribute to [!DNL Recommendations] at least once per month for each item in your catalog.

Most predefined parameters accept a single value only, with new values overwriting old values. The `categoryId` parameter can accept a comma-delimited list of values for each category containing that product. New `categoryId` values do not overwrite existing values but instead are appended during entity update (250-character limit).

In general, the display information mbox looks like the following example if you are using at.js 1.*x* with `mboxCreate`. All entity parameter attributes are case-sensitive.

>[!NOTE]
>
>If you are using at.js 2.*x*, `mboxCreate` (as used in the  following example) is no longer supported. To pass product or content information to [!DNL Recommendations] using at.js 2.*x*, use [targetPageParams](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparams.html){target=_blank}. For an example, see [Plan and implement Recommendations](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

```javascript
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id=67833', 
 
'entity.name=GIANTS VS ROCKIES 5/12', 
 
'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
 
'entity.pageUrl=/help/baseball/giants-tix/giantsvrockies5.12.2000-67833', 
 
'entity.venue=AT&T PARK', 
 
'entity.secondary=ROCKIES', 
 
'entity.thumbnailUrl=/help/baseball/giants-tix/giants-136px.gif', 
 
'entity.message=FAMILY SPECIAL', 
 
'entity.value=15.99', 
 
'entity.inventory=1' 
 
); 
 
</script>
```

>[!NOTE]
>
>Relative URLs are preferred for `pageUrl` and `thumbnailUrl` rather than absolute URLs because recommendations receive data being sent from all environments on your site. Using relative URLs avoids hardcoded links to a staging or development server.

If the mbox is on a product page, you can include both the product ID and category ID. The selected algorithm determines which displays. The product ID is used for affinity algorithms and the category ID is used for category algorithms.

## Available variables

The following list describes the available variables.

### entity.id

Singe value only.

This required parameter identifies the product. This alphanumeric ID must be the same across all [!DNL Adobe Experience Cloud] products that are used, including [!DNL Analytics], for the various products to recognize the item and share data about it.

The `entity.id` values must *not* contain spaces, slashes, ampersands, question marks, percentage symbols, commas, or other punctuation characters that require URL encoding when passed in a REST API call. Hyphens and underscores are allowed. Including invalid punctuation in an `entity.id` value causes some [!DNL Recommendations] functionality to fail.

Example: `'entity.id=67833'`

### entity.name

Single-value only.

The product name that is displayed on the Web site when the product is recommended.

Example: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Supports multi-value (comma-delimited list).

Category of the current page. The entity.categoryID can include multiple categories, such as a cardigans sub-subsection (for example, womens, womens:sweaters, womens:sweaters:cardigans). Multiple categories must be separated by commas.

The `categoryId` value is limited to 250 characters.

>[!NOTE]
>
>To show a recommendation based on a category in a [!UICONTROL Category] page, only one `categoryId` can be passed into the mbox used to display that particular recommendation. The value of the `categoryId` must match exactly the value of `entity.categoryId` passed on the [!UICONTROL Product Detail] page.

Examples:

* Example Product Detail Page: womens, womens:sweaters, womens:sweaters:cardigans
* Example Category Page Sweaters: womens:sweaters
* Example Category Page Cardigans: womens:sweaters:cardigans

For category-based recommendations, a comma separates category value. Any values separated by commas become categories. You can also define subcategories by using a different separator, such as a colon (:), to separate subcategories within the category value.

For example, in the following code the Women's category is divided into several subcategories:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban', 'entity.thumbnailUrl=...', 'entity.message=...', );
```

For the mbox delivery, the longest attribute name is used for the key. If there is a tie, the last attribute is used. In the example above, the category key is Womens:Outerwear:Jackets:Caban.

### entity.brand

Single-value only.

Displays an item's brand name.

Example: `'entity.brand=brandxyz'`

### entity.pageUrl

Single-value only.

Defines the relative URL of the page where the item can be purchased.

Example: `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'`

### entity.thumbnailUrl

Single-value only.

Defines the relative URL to the thumbnail image that displays with the item.

Example: `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'`

### entity.message

Single-value only.

A message about the product that is displayed in the recommendation, such as "on sale" or "clearance." The message is typically more verbose than the product name. Use entity.message to define additional information to display with the product in the template.

Example: `'entity.message=Family&nbsp;special'`

### entity.inventory

Single-value only. Requires an integer or long value.

Displays the inventory level of the item.

Example: `'entity.inventory=1'`

**Empty Inventory Attribute Handling:** For delivery, if you have an inclusion rule, collection rule, or criteria setting with `entity.inventory` > 0 or `entity.inventory` = 0 and the product has inventory not set, [!DNL Target] evaluates this value to TRUE and includes products where the inventory is not set. As a result, products with inventory that is not set display in recommendation results.

Similarly, if you have a global exclusion rule with `entity.inventory` = 0 and `entity.inventory` is not set, [!DNL Target] evaluates this rule to be TRUE and excludes the product.

**Known issue:** Product Search is inconsistent with delivery for inventory value attributes that are not set. For example, for a rule with `entity.inventory` = 0 , Product Search does not display products where the inventory value is not set.

### entity.value

Single-value only.

Defines the price or value of the item.

Example: `'entity.value=15.99'`

entity.value supports decimal format only (for example, 15.99). The comma format (15,99) is not supported.

### entity.margin

Single-value only.

The profit margin or other value of the item.

Example: `'entity.margin=1.00'`

### entity.*custom*

Supports multi-value (JSON array).

Define up to 100 custom variables that provide additional information about the item. You can specify any unused attribute name for each custom attribute. For example, you can create a custom attribute called `entity.genre` to define a book or movie. A ticket vendor can create attributes for an event venue for a secondary performer, such as a visiting team in a sporting event or an opening act in a concert.

Restrictions:

* You cannot use predefined entity attribute names for custom entity attributes.
* The attribute entity.environment is reserved by the system and cannot be used for custom entity attributes. Attempts to pass entity.environment using targetPageParams, feed, or API are ignored.

Examples:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Custom entity attributes support multiple values. See [Custom entity attributes](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) for character and value limits. 

Example: `'entity.secondary=["band1",&nbsp;"band2"]'`

Multi-value custom entity attributes require valid JSON arrays. For correct syntax information, see [Custom Entity Attributes](/help/main/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly

Single-value only.

Used to prevent an mbox call from incrementing behavioral data counters for an algorithm.

Example: `'entity.event.detailsOnly=true'`

In the examples below, the first mbox call updates the catalog and behavioral data. The second mbox call updates only the catalog.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
``` 

>[!MORELIKETHIS]
>
>* [Custom Entity Attributes](/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
