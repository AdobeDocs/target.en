---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: Learn how to use [!DNL Adobe Analytics] as the behavioral data source in [!DNL Target Recommendations].
title: Use Adobe Analytics with Recommendations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
TQID: 'https://experienceleague.adobe.com/2ryixOT-YoKjDlMbqs8g2DJElNVmlCUFhbdZzpfSnNs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
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
# Use [!DNL Adobe Analytics] with [!DNL Recommendations] {#use-analytics-with-recommendations}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use [!DNL Adobe Analytics] as the behavioral data source in [!DNL Adobe Target Recommendations] activities.

>[!ENDSHADEBOX]

Using [!DNL Adobe Analytics] as the behavioral data source allows [!DNL Adobe Target Recommendations] activities to use the view-based and purchase-based behavioral data from [!DNL Analytics]. This is useful when the [!DNL Target Recommendations] setup is new and [!DNL Analytics] has a lot of historical data to use. The data might also include information from a third-party source or feed that is shared only with [!DNL Analytics].

The data source is selected with the **[!UICONTROL Behavioral Data Source]** option while [creating criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in [!DNL Recommendations]: **[!UICONTROL Adobe Target]** or **[!UICONTROL Analytics]**.

>[!NOTE]
>
>If these two options do not display in the account, contact [Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Use cases for [!DNL Analytics] data in [!DNL Target] {#use-cases}

Using [!DNL Analytics] as the behavioral data source also allows specific use cases to be deployed without tagging entity pages with all the [!DNL Target] entity parameters. This requires certain prerequisites, and the availability of "Product Variables" is the most important one. Regular eVars and Props are not sufficient for [!DNL Analytics] and [!DNL Target] to exchange this data automatically.

[!DNL Analytics] can be used as the behavioral data source to:

* Display recommendations on a retail site to users on a product detail page, based on what other users purchased from the same category in the last month, using [!DNL Analytics] data.
* Display content on the home screen of a media site for the most popular content in a particular category that is currently trending, based on [!DNL Analytics] data.

## Implementation in [!DNL Analytics]

### Prerequisites: set up product variables in [!DNL Analytics] {#prerequisites}

Implement product variables in [!DNL Analytics] with the attributes that are required for [!DNL Target Recommendations]. A [!DNL Target Recommendations] sample feed format guides which attributes must be defined in the product variables. These values must later be "mapped" in the [!DNL Target] UI to the respective [!DNL Target] entity values.

>[!NOTE]
>
>If it is a content site, the respective content pieces must be treated as "products", and the associated attributes of that content must be passed as attributes. Such attributes can include author name, publish date, content title, month of release, and so forth. The business should decide the granularity of the category level, or the category types, based on the requirements of the use case.

For more details on how to set up product variables, see [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) in the *Implement Adobe Analytics* guide. Some of the notes in that documentation, for example about Category, require the judgment of the team that deploys it. Consulting [!DNL Adobe] before this activity is recommended.

### Considerations {#considerations}

[!DNL Analytics] data is sent through a daily feed. Behavioral results can take up to 24 hours to be reflected in the recommendations results on the site. As with all [!DNL Recommendations] criteria settings, this data source should be tested.

To choose a data source:

* A [!DNL Target] mbox is a good fit when a lot of organic data is generated every day by users and little dependency on historical data is required.
* [!DNL Analytics] is a good fit when less organic data has been generated recently and the [!DNL Analytics] data is to be used.

The `entity.id` and `entity.categoryId` values must still be passed in the [!DNL Target] mbox call. The other attributes can be passed through an [!DNL Analytics] feed, as described on this page.

Dynamic inclusion rules, such as matching an entity parameter to a profile attribute, can be used with the [!DNL Analytics] feed approach. The method is similar to using [!DNL Target] stand-alone, but the timing must be considered: the entity variables that are supposed to match the profile variables depend on the data layer, which might appear much later on the page.

## Implement in [!DNL Target] {#implement-target}

The product variables are mapped in [!DNL Target] to provide a continuous supply of behavioral data.

1. In [!DNL Target], click **[!UICONTROL Recommendations]**, then click the **[!UICONTROL Feeds]** tab.

1. Click **[!UICONTROL Create Feed]**.

1. Select **[!UICONTROL Analytics Classifications]**, then specify the report suite.

1. Click **[!UICONTROL Next]** to advance to the **[!UICONTROL Schedule]** settings, then select a frequency for the feed: **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Every 2 weeks]**, or **[!UICONTROL Never]**. The time of day for the feed to process can also be selected.

1. Click **[!UICONTROL Next]** to advance to the **[!UICONTROL Mapping]** settings, then map the field column headers to the appropriate **[!UICONTROL Recommendations]** field names.

1. Click **[!UICONTROL Save]**.

For more information about creating a feed, see [Create a feed](/help/main/c-recommendations/c-products/feeds.md#steps).
