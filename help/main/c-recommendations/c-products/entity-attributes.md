---
keywords: entity;entity attributes;pass information to Recommendations;behavioral data;data counter;define relative URL;display inventory level;define price;define profit margin;custom attributes
description: Learn how to use entity attributes to pass product or content information to [!DNL Target] Recommendations.
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
title: How Do I Use Entity Attributes?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
TQID: 'https://experienceleague.adobe.com/GXQOxQxTV0vTYsWy9Ky9wPNEqoRSAhIA5zlBd4Cr4Ec'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
---
# Entity attributes {#entity-attributes}

>[!BEGINSHADEBOX]

**On this page:** Learn which entity attributes pass product or content information to [!DNL Adobe Target Recommendations] and how to define each one.

>[!ENDSHADEBOX]

Use entity attributes to pass product or content information to [!DNL Adobe Target Recommendations], where it can be displayed in designs and used in inclusion rules, collections, and exclusions. Entities are the items you want to recommend, such as products, content (articles, slide shows, images, movies, and television shows), job listings, restaurants, and so forth. [!DNL Recommendations] sends the `productId` or `productPurchasedId` (referred to as `entity.id` in the code) that is used in the algorithms.

Consider the following:

* `entity.id` must match the `productPurchasedId` sent to the order confirmation page and the `productId` used in [!DNL Adobe Analytics] product reports.
* Entity attribute values that you pass to [!DNL Recommendations] expire after 61 days. Adobe recommends that you pass the latest value of each entity attribute to [!DNL Recommendations] at least once per month for each item in your catalog.

Most predefined parameters accept a single value only, with new values overwriting old values. The `categoryId` parameter is the exception (see [entity.categoryId](#entity-category-id)).

In general, the display information mbox looks like the following example if you are using at.js 1.*x* with `mboxCreate`. All entity parameter attributes are case-sensitive.

If you are using at.js 2.*x*, `mboxCreate` (as used in the following example) is no longer supported. To pass product or content information to [!DNL Recommendations] using at.js 2.*x*, use [targetPageParams](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparams.html){target=_blank}. For an example, see [Plan and implement Recommendations](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

+++ Example of an mbox that passes entity attributes

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

+++

>[!NOTE]
>
>Relative URLs are preferred for `pageUrl` and `thumbnailUrl` rather than absolute URLs because recommendations receive data being sent from all environments on your site. Using relative URLs avoids hardcoded links to a staging or development server.

If the mbox is on a product page, you can include both the product ID and category ID. The selected algorithm determines which displays. The product ID is used for affinity algorithms and the category ID is used for category algorithms.

## Available variables

The following table lists the available variables. Subsections after the table give more information about the variables that need it.

| Variable | Values | Description | Example |
|---|---|---|---|
| `entity.id` | Single value only. Required. | Identifies the product. See [entity.id](#entity-id). | `'entity.id=67833'` |
| `entity.name` | Single value only. | The product name that is displayed on the website when the product is recommended. | `'entity.name=Giants& vs& Rockies& 5/12'` |
| `entity.categoryId` | Multi-value (comma-delimited list). | The category of the current page. See [entity.categoryId](#entity-category-id). | `'entity.categoryId=womens:sweaters'` |
| `entity.brand` | Single value only. | Displays an item's brand name. | `'entity.brand=brandxyz'` |
| `entity.pageUrl` | Single value only. | Defines the relative URL of the page where the item can be purchased. | `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'` |
| `entity.thumbnailUrl` | Single value only. | Defines the relative URL to the thumbnail image that displays with the item. | `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'` |
| `entity.message` | Single value only. | A message about the product that is displayed in the recommendation, such as "on sale" or "clearance." The message is typically more verbose than the product name. Use `entity.message` to define additional information to display with the product in the template. | `'entity.message=Family&nbsp;special'` |
| `entity.inventory` | Single value only. Requires an integer or long value. | Displays the inventory level of the item. See [entity.inventory](#entity-inventory). | `'entity.inventory=1'` |
| `entity.value` | Single value only. | Defines the price or value of the item. Only the decimal format is supported (for example, 15.99). The comma format (15,99) is not supported. | `'entity.value=15.99'` |
| `entity.margin` | Single value only. | The profit margin or other value of the item. | `'entity.margin=1.00'` |
| `entity.`*custom* | Multi-value (JSON array). | Custom variables that provide additional information about the item. See [entity.*custom*](#entity-custom). | `'entity.secondary=Rockies'` |
| `entity.event.detailsOnly` | Single value only. | Prevents an mbox call from incrementing behavioral data counters for an algorithm. See [entity.event.detailsOnly](#entity-event-details-only). | `'entity.event.detailsOnly=true'` |

### entity.id {#entity-id}

The alphanumeric ID must be the same across all [!DNL Adobe Experience Cloud] products that are used, including [!DNL Analytics], for the various products to recognize the item and share data about it.

The `entity.id` values must *not* contain spaces, slashes, ampersands, question marks, percentage symbols, commas, or other punctuation characters that require URL encoding when passed in a REST API call. Hyphens and underscores are allowed. Including invalid punctuation in an `entity.id` value causes some [!DNL Recommendations] functionality to fail.

### entity.categoryId {#entity-category-id}

The `entity.categoryId` value can include multiple categories, such as a cardigans sub-subsection (for example, `womens`, `womens:sweaters`, `womens:sweaters:cardigans`). Multiple categories must be separated by commas. New `categoryId` values do not overwrite existing values but instead are appended during entity update. The `categoryId` value is limited to 250 characters.

>[!NOTE]
>
>To show a recommendation based on a category in a **[!UICONTROL Category]** page, only one `categoryId` can be passed into the mbox used to display that particular recommendation. The value of the `categoryId` must match exactly the value of `entity.categoryId` passed on the **[!UICONTROL Product Detail]** page.

Examples:

* Example Product Detail Page: `womens`, `womens:sweaters`, `womens:sweaters:cardigans`
* Example Category Page Sweaters: `womens:sweaters`
* Example Category Page Cardigans: `womens:sweaters:cardigans`

For category-based recommendations, a comma separates category value. Any values separated by commas become categories. You can also define subcategories by using a different separator, such as a colon (:), to separate subcategories within the category value.

For example, in the following code the Women's category is divided into several subcategories:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban', 'entity.thumbnailUrl=...', 'entity.message=...');
```

For the mbox delivery, the longest attribute name is used for the key. If there is a tie, the last attribute is used. In the example above, the category key is `Womens:Outerwear:Jackets:Caban`.

### entity.inventory {#entity-inventory}

**Empty inventory attribute handling:** For delivery, if you have an inclusion rule, collection rule, or criteria setting with `entity.inventory` > 0 or `entity.inventory` = 0 and the product has inventory not set, [!DNL Target] evaluates this value to TRUE and includes products where the inventory is not set. As a result, products with inventory that is not set display in recommendation results.

Similarly, if you have a global exclusion rule with `entity.inventory` = 0 and `entity.inventory` is not set, [!DNL Target] evaluates this rule to be TRUE and excludes the product.

>[!NOTE]
>
>**Known issue:** Product Search is inconsistent with delivery for inventory value attributes that are not set. For example, for a rule with `entity.inventory` = 0, Product Search does not display products where the inventory value is not set.

### entity.*custom* {#entity-custom}

You can define up to 100 custom variables. You can specify any unused attribute name for each custom attribute. For example, you can create a custom attribute called `entity.genre` to define a book or movie. A ticket vendor can create attributes for an event venue for a secondary performer, such as a visiting team in a sporting event or an opening act in a concert.

Restrictions:

* You cannot use predefined entity attribute names for custom entity attributes.
* The attribute `entity.environment` is reserved by the system and cannot be used for custom entity attributes. Attempts to pass `entity.environment` using `targetPageParams`, feed, or API are ignored.

Examples:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Custom entity attributes support multiple values. See [Custom entity attributes](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) for character and value limits.

Example: `'entity.secondary=["band1",&nbsp;"band2"]'`

Multi-value custom entity attributes require valid JSON arrays. For correct syntax information, see [Custom entity attributes](/help/main/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly {#entity-event-details-only}

Use this parameter to prevent an mbox call from incrementing behavioral data counters for an algorithm.

In the following examples, the first mbox call updates the catalog and behavioral data. The second mbox call updates only the catalog.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york', 'entity.id = 123', 'entity.inventory = 4' )
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york', 'entity.id = 123', 'entity.inventory = 4', 'entity.event.detailsOnly=true' )
``` 
