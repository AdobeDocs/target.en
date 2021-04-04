---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Learn how to filter dynamically in Adobe Target Recommendations by comparing a pool of potential items to a specific item that the user has interacted with.
title: How Do I Filter by Entity Attribute Matching In Recommendations Activities?
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
---
# ![PREMIUM](/help/assets/premium.png) Entity Attribute Matching

Filter dynamically in [!DNL Adobe Target] [!DNL Recommendations] by comparing a pool of potential recommendations items to a specific item that the user has interacted with.

>[!NOTE]
>
>The [process for creating and using inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) for criteria and promotions is similar, as are the use cases and examples.

For example, recommend only items that match the current item’s brand as in the following example:

If the mbox on a Brand Landing Page returns `entity.brand=brandA`, then only Brand A products are returned and displayed on that page. Similarly, on the Brand Landing Page for Brand B, only Brand B products are returned. With this type of dynamic inclusion rule, the user has to only specify one recommendation rule that returns relevant brand results across all brand pages rather than specifying a collection or a static filter to match each brand name.

Note that you must deliver the `entity.brand` in the mbox on those landing pages for this to work.

## Entity Attribute Matching examples 

[!UICONTROL Entity Attribute Matching] allows you to recommend only the items that match, for example:

* An attribute from the item the user is currently viewing
* The item the user most recently viewed
* The item the user most recently purchased
* The item the user most frequently viewed
* An item stored in a custom attribute in the visitor's profile

### Recommending items based on brand

After your entity attribute rules are built, they will filter out all recommendations with attributes that do not match the entity value passed on the page.

The following example shows recommendations matching product brand shown on the page:

When you visit a page that features a Brand A product, the page sets the value of the `entity.brand` parameter to “BrandA”.

![Example Target call](/help/c-recommendations/c-algorithms/assets/example-target-call.png)

In the recommendations on the page, you will see Brand A products only.

![Brand A recommendations](/help/c-recommendations/c-algorithms/assets/brandA.png)

If you then view a Brand B product page, the `entity.brand` value will be reset to “BrandB” and you will see Brand B products recommended on Brand B product pages.

![Brand B recommendations](/help/c-recommendations/c-algorithms/assets/brandB.png)

### Upselling to a more expensive product

Suppose that you're an apparel retailer and want to encourage users to consider higher-priced and, therefore, more profitable items. You can use the "equals" and "is between" operators to promote more expensive items that are from the same category and the same brand. For example, a shoe retailer can promote more expensive running shoes in an effort to up-sell a visitor looking at running shoes, as in the following sample:

![Upselling](/help/c-recommendations/c-algorithms/assets/upsell.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And 
Entity Attribute Matching
brand - equals - current item's - brand 
And 
Entity Attribute Matching
value - is between - 100% and 1000% of - current item's - value
```

### Promoting private-label products

You can mix dynamic and static filters to promote private-label products. For example, an office supply company can promote toner cartridges of the company's house brand to drive a more profitable sale for a visitor looking at toner -- and promote pens of the company's house brand to drive a more profitable sale for a visitor looking at pens, as in the following sample:

![House Brand](/help/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
