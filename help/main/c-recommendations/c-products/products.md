---
keywords: product;collections
description: Learn about entities in Adobe [!DNL Target] Recommendations. Entities refer to the items you want to recommend using [!DNL Target], such as articles, movies, or products.
title: How Do I use Entities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: ffe23eea-b914-4c86-ad54-c63c1cc1c0d7
TQID: 'https://experienceleague.adobe.com/zfISb59XJ5qrD1-FA0syglPPswIL8cA0N0pBpY4tgIE'
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
# Get started with entities {#get-started-entities}

>[!BEGINSHADEBOX]

**On this page:** Learn what entities are in [!DNL Adobe Target Recommendations] and where to manage them.

>[!ENDSHADEBOX]

Entities are the items that [!DNL Recommendations] can recommend. An entity can be a product, a piece of content (such as an article, slide show, image, movie, or TV show), a job listing, a restaurant, and so forth.

[!DNL Recommendations] displays items from your collections according to the criteria that you set up.

## How entities reach Recommendations

Information about your entities can be passed to [!DNL Recommendations] in several ways, including:

* With [entity attributes](/help/main/c-recommendations/c-products/entity-attributes.md) sent from your pages, using an mbox or `targetPageParams`.
* With [feeds](/help/main/c-recommendations/c-products/feeds.md), which can use CSV files, the [!DNL Google Product Search] feed format, or [!DNL Adobe Analytics] product classifications.
* With the Delivery API.

If [!DNL Target] collects data for an item from both a feed and an mbox, the most recent data is used.

Uploaded entities and entity attribute values expire after 61 days. Send each item again at least once every 60 days. Otherwise, [!DNL Target] considers the item no longer relevant and removes it from the catalog.

## Manage your entities

Use the following pages to work with your entities:

* [Entity attributes](/help/main/c-recommendations/c-products/entity-attributes.md) and [Custom entity attributes](/help/main/c-recommendations/c-products/custom-entity-attributes.md): Define the product or content information that you pass to [!DNL Recommendations].
* [Feeds](/help/main/c-recommendations/c-products/feeds.md): Get entity or content information into your recommendations.
* [Catalog search](/help/main/c-recommendations/c-products/catalog-search.md): Locate items in your catalog.
* [Collections](/help/main/c-recommendations/c-products/collections.md): Set up your collections. A collection is selected for each experience when you create a [!DNL Recommendations] activity.
* [Exclusions](/help/main/c-recommendations/c-products/exclusions.md): Prevent certain items from displaying in your recommendations. Exclusions apply to all activities in the account.
