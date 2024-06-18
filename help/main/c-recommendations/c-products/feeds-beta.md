---
keywords: recommendations feed;feed;SAINT;ftp;csv;classifications;analytics classifications
description: Learn how feeds import entities into [!DNL Adobe Target] [!DNL Recommendations] using CSV files, the [!DNL Google Product Search] feed format, and [!DNL Analytics] product classifications.
title: How Do I Use [!UICONTROL Feeds] in [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
hide: yes
hidefromtoc: yes
exl-id: 53adc701-c389-4adf-a9c8-ca778aa0a8f3
---
# Feeds

Use feeds to get entities imported into [!DNL Adobe Target] [!DNL Recommendations]. Entities can be sent using CSV files, the [!DNL Google Product Search] feed format, and [!DNL Adobe Analytics] product classifications. 

## Feeds overview {#concept_D1E9C7347C5D4583AA69B02E79607890}

Feeds let you pass [Entities](/help/main/c-recommendations/c-products/products.md) or augment your mbox data with information that is either unavailable on the page or is unsafe to send directly from the page. For example, margin, Cost of Goods Sold (COGS), and so on.

Feeds also let you pass detailed item information into [!DNL Recommendations], such as product ID, category, name, message, and other attributes.

You can select which columns from your [!DNL Target] product classifications file or [!DNL Google Product Search] file you want to send to the [!DNL Recommendations] server. 

These pieces of data about each item can then be used to:

* Display values in designs
* Define criteria inclusion rules
* Sort items into different collections
* Apply exclusions to recommendations

Item descriptions can be passed into [!DNL Target] using feeds or mboxes. If [!DNL Target] collects data using both an entity feed and an mbox, the most recent data wins. Usually, the most recent data comes from an mbox, because it is viewed more often. In the rare event that entity feed data and mbox data hit at the same time, the mbox data is used.

The [!UICONTROL Feeds] list ( **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]**) provides information about any feeds that you have created. 

![Feeds page](/help/main/c-recommendations/c-products/assets/feeds-page-new.png)

The [!UICONTROL Feeds] page contains the following columns:

* **Name**: The name of the feed specified during creation. To edit the name of a feed, you must edit the feed itself. When you save the feed with the new name, the feed is refreshed.
* **Status**: The feed's current [status](/help/main/c-recommendations/c-products/feeds.md#concept_E475986720D1400999868B3DFD14A7A0).
* **Type**: Types include [CSV](/help/main/c-recommendations/c-products/feeds.md#section_65CC1148C7DD448FB213FDF499D35FCA), [[!DNL Google Product Feed]](/help/main/c-recommendations/c-products/feeds.md#section_8EFA98B5BC064140B3F74534AA93AFFF), and [Analytics Classifications](/help/main/c-recommendations/c-products/feeds.md#section_79E430D2C75443BEBC9AA0916A337E0A).
* **Items**: Displays the number of items in the feed.
* **Schedule**: Displays the update schedule for the feed: [!UICONTROL Daily], [!UICONTROL Weekly], [!DNL Every 2 Weeks], or [!UICONTROL Never].
* **Last Updated**: Displays the date and time when the feed was last updated and the name of the person who updated the feed.

Click the [!UICONTROL Customize Table] icon ( ![Customize Table icon](/help/main/c-recommendations/c-products/assets/customize-table-icon.png) ) to select or deselect columns that you want to display.

Click the [!UICONTROL Information] icon to display a card that displays the last upload date and the feed's URL.

Click the ellipsis icon to access the following actions: [!UICONTROL Deactivate], [!DNL Edit], [!UICONTROL Copy], and [!UICONTROL Delete].

>[!IMPORTANT]
>
>Uploaded entities and entity attributes expire after 61 days. This means:
>
>* Your feed should run at least monthly to ensure that your catalog contents do not expire.
>* Removing an item from your feed file does not remove that item from your catalog. To remove the item from the catalog, manually delete the item via the [!DNL Target] UI or API. Or, modify the item attributes (such as inventory) to ensure that the item is excluded from consideration.

## Source types

Entities can be sent using CSV files, the [!DNL Google Product Search] feed format, and [!DNL Adobe Analytics] product classifications.

### CSV {#section_65CC1148C7DD448FB213FDF499D35FCA}

You can create a .csv file using the [!DNL Adobe] proprietary CSV upload format. The file contains display information about the reserved and custom attributes for your products. To upload attributes specific to your implementation, replace `CustomN` in the header row with the name of the attribute you want to use. In the example below, `entity.Custom1` has been replaced by: `entity.availability`. You can then bulk upload the file to the [!DNL Recommendations] server.

Using the .csv format has the following advantages over the [!DNL Google] feed format:

* The .csv format doesn't require field mappings.
* The .csv format supports multi-value attributes (see example below).
* The .csv format supports up to 100 custom attributes. If you need more than 100 custom attributes, you can create a second feed file with a different set of custom attributes specified.

Use the bulk upload method to send display information if you don't have mboxes on your page, or if you want to supplement your display information with items that are not available on your site. For example, you might want to send inventory information that might not be published on your site.

Any data uploaded using the .csv file, Google Product Feed, or [!DNL Analytics] Product classification feed overwrites the existing entity attribute value in the database. If you send price information via mbox requests and then send different price values in the file, the values in the file overwrite the values set with the mbox request. An exception to this is the `categoryId` entity attribute where the category values are appended instead of being overwritten up to the 250-character limit.

>[!IMPORTANT]
>
>Do not enclose values in double quotes ( " ) in your .csv file unless they are intentional. If you enclose values in double quotes, you must escape them by enclosing them in another set of double quotes. Double quotes that are not escaped prevent the recommendations feed from loading properly.

For example, the following syntax is incorrect:

```
"Apples "Bananas" Grapes"",
```

The following syntax is correct:

```
"Apples ""Bananas"" Grapes""",
```

>[!NOTE]
>
>You can't overwrite an existing value with a blank value. Pass another value in its place to overwrite the existing value. In the case of a sale price, a common solution is to either pass in an actual "NULL" or some other message. You can then write a template rule to exclude items with that value.

The product is available in the admin interface approximately two hours after successfully uploading its entity.

The following is sample code for a .csv file:

```
## RECSRecommendations Upload File 
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines. 
## RECS 
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left. 
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'. 
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations. 
## RECSentity.id,entity.name,entity.categoryId,entity.message,entity.thumbnailUrl,entity.value,entity.pageUrl,entity.inventory,entity.margin,entity.last_updated_by,entity.multi_english,entity.availability,entity.tax_country,entity.tax_region,entity.tax_rate,entity.product_type,entity.item_group_id,entity.color,entity.size,entity.brand,entity.gtin 
na3456,RipCurl Watch with Titanium Dial,Watches & Sport,Cutting edge titanium with round case,https://example.com/s7/na3456_Viewer,425,https://example.com/shop/en-us/na3456_RipCurl,24,0.25,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Titanium,44mm,RipCurl,"075380 01050 5" 
na3457,RipCurl Watch with Black Dial,Watches & Sport,Cutting edge matte black with round case,https://example.com/s7/na3457_Viewer,275,https://example.com/shop/en-us/na3457_RipCurl,24,0.27,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Black,44mm,RipCurl,"075340 01060 7"
```

### [!DNL Google] {#section_8EFA98B5BC064140B3F74534AA93AFFF}

The [!DNL Google Product Search] feed type uses the [!DNL Google] format. This is different from the [!DNL Adobe] proprietary CSV upload format.

If you have an existing [!DNL Google Product Feed], you can use that as your import file.

>[!NOTE]
>
>It is not required to use [!DNL Google] data. [!DNL Recommendations] uses the same format as [!DNL Google]. You can use this method to upload any data you have, and use the available scheduling features. However, you must retain the [!DNL Google] predefined attribute names when you set up the file.

Most retailers upload products to [!DNL Google], so when a visitor uses the [!DNL Google] product search, their products display. [!DNL Recommendations] follows the [!DNL Google] specification exactly for entity feeds. Entity feeds can be sent to [!DNL Recommendations] via .xml, .txt, or .tsv, and can use the [attributes defined by Google](https://support.google.com/merchants/answer/188494?hl=en&topic=2473824&ctx=topic#US). The results are searchable on the [[!DNL Google] shopping pages](https://www.google.com/prdhp).

>[!NOTE]
>
>The POST method must be allowed on the server that is hosting the [!DNL Google] feed content.

Because [!DNL Recommendations] users already configure .xml or .txt feeds to send to [!DNL Google] either via URL or FTP, entity feeds accept that product data and use it to build the recommendations catalog. Specify where that feed exists and the recommendations server retrieves the data.

If you use [!DNL Google Product Search] for the entity feed upload, you still must have a product page mbox on the page if you want to show recommendations there or track product views for algorithm delivery based on views.

[!DNL Google] feeds do not support multiple values for a custom attribute.

The feed runs at the time that you save and activate it. It runs at the time that you save the feed, then every day an hour later.

The following is sample code for a [!DNL Google Product Search] feed .xml file:

```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
<feed xmlns="https://www.w3.org/2005/Atom" xmlns:ns2="https://base.google.com/ns/1.0" xmlns:ns3="https://base.google.com/cns/1.0"> 
    <title>Product Feed</title> 
    <link href="https://example.com"/> 
    <updated>2017-12-13T08:45:04.918-08:00</updated> 
    <author> 
        <name>Product Feed Author</name> 
    </author> 
    <id>https://example.com</id> 
    <entry> 
        <title>RipCurl Watch with Titanium Dial</title> 
        <description>Cutting edge Titanium with Round case</description> 
        <ns2:id>na3452</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3452_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 01050 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3452_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3452_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>425</ns2:price> 
        <ns2:product_review_average>5.0</ns2:product_review_average> 
        <ns2:product_review_count>30</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>375</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
    <entry> 
        <title>RipCurl Watch with Black Dial</title> 
        <description>Cutting edge matte black with Round case</description> 
        <ns2:id>na3453</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3453_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 013450 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3453_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3453_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>275</ns2:price> 
        <ns2:product_review_average>4.8</ns2:product_review_average> 
        <ns2:product_review_count>23</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>249</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
</feed> 
```

The following is sample code for a [!DNL Google Product Search] feed .tsv file:

```
id    title    description    link    price    condition    availability    image_link    tax    shipping_weight    shipping    google_product_category    product_type    item_group_id    color    size    gender    age_group    pattern    brand    gtin    mpn 
na3454    RipCurl Watch with Titanium Dial    Cutting edge titanium with round case    https://example.com/shop/en-us/na3454_RipCurl    425    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075380 01050 5    DZ1437 
na3455    RipCurl Watch with Black Dial    Cutting edge matte black with round case    https://example.com/shop/en-us/na3455_RipCurl    275    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075340 01060 7    DZ1446
```

### [!DNL Analytics] Product Classifications {#section_79E430D2C75443BEBC9AA0916A337E0A}

The [!DNL Adobe Analytics] Product classification is the only classification available for recommendations. For more information about this classification file, see [About classifications](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) in the *Analytics Components* guide. It's possible that not all the information you need for recommendations is available in your current implementation, so follow this user guide if you want to add to your classifications file.

>[!IMPORTANT]
>
>Before importing entity data into [!DNL Recommendations] using [!DNL Analytics] product classifications, be aware that this is not the preferred method.
>
> Be aware of the following caveats:
>
>* Updates to entity attributes incur an additional delay of up to 24 hours.  
>* [!DNL Target] supports [!UICONTROL Product Classifications] only. The [!DNL Analytics] product SKU must map to the same level as the [!DNL Recommendations] `entity.id`. Custom [!DNL Analytics] Classifications can be engineered using [!UICONTROL Adobe Consulting Services]. Contact your Account Manager with questions.

## Create Feed {#steps}

Create a feed to insert information about your products or services into [!DNL Recommendations].

1. From within the [!DNL Target] interface, click **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]**.

   ![Create Feed dialog box](assets/CreateFeed.png)

1. Specify a descriptive name for your feed.
1. Select a **[!UICONTROL Source Type]**.

   * [!UICONTROL CSV] 
   * [!UICONTROL Google Product Feed]
   * [!UICONTROL Analytics Classifications]

   For information about the [!UICONTROL CSV] and [!UICONTROL Google Product Feed] feed types, see [Feeds Overview](/help/main/c-recommendations/c-products/feeds.md#concept_D1E9C7347C5D4583AA69B02E79607890). You can also [download a model CSV guide](/help/main/c-recommendations/c-products/assets/EntityFileUploadTemplate.csv) to help you format the feed correctly.

1. (Conditional) If you selected **[!UICONTROL CSV]** or **[!UICONTROL Google Product Feed]**, specify the location where the feed can be accessed.

   * **FTP**: If you selected FTP, provide the FTP server information, the login credentials, the filename, and the FTP directory. You can use FTP with SSL (FTPS) for more secure uploads.

     Supported FTP server settings:

     * FTP and FTPS must be set to use Passive FTP.
     * For FTPS, configure the server to accept Explicit FTPS connections.
     * SFTP is not supported.
     * You can manually specify a port on which to initiate the connection (for example, `ftp://ftp.yoursite.com:2121`). If you do not specify a port, the default FTP or FTPS port is used.

   * **URL**: If you select [!UICONTROL URL], specify the URL.

1. (Conditional) If you selected **[!UICONTROL Analytics Classifications]**, choose the report suite from the drop-down list.

1. Click the **[!UICONTROL Next]** arrow to display the [!UICONTROL Schedule] options.

   ![Step Result](assets/CreateFeedSchedule.png)

1. Select an update option:

    * [!UICONTROL Daily] 
    * [!UICONTROL Weekly] 
    * [!UICONTROL Every 2 Weeks] 
    * [!UICONTROL Never]: Do not schedule an update. Choose this if you do not want this feed to run.

1. Specify the time that you want your feed to run.

   This option is based on the time zone used in your browser. If you want to use a time in a different time zone, you must calculate that time according to your time zone.

1. Click the **[!UICONTROL Next]** arrow to display the [!UICONTROL Mapping] options, then specify how you want to map your data to [!DNL Target] definitions.

   ![Step Result](assets/CreatFeedMapping.png)

1. (Optional) If you want the feed to belong to an environment (host group), select the host group.

   By default the feed belongs to all host groups. This ensures that items in this feed are available in any environment. For more information, see [Hosts](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

1. Click **[!UICONTROL Save]**.

After you create or edit a feed, the feed runs immediately. The feed then updates according to the parameters that you set. It takes some time for the information to be available. First, the feed must sync, then it must be processed and indexed before it can be published and made available. The current status appears under [Feed Status](/help/main/c-recommendations/c-products/feeds.md#status) in the [!UICONTROL Feeds] list. You can close [!DNL Target] before the process is complete and the process continues.

While indexing is in progress, products and feed headers appear before individual values have been indexed. This lets you search and see products so you can create collections, exclusions, designs, and activities before indexing has been completed.

When the Status says "Success," it means that the file was found and it parsed correctly. The information is not available to use within [!DNL Recommendations] until the file is indexed, which can take some time, depending on the size of your file. If the process fails, it means that the file was not found. For example, you used an incorrect URL or your FTP information was incorrect, or that there was a parsing error.

## Feed Statuses and Indicators {#concept_E475986720D1400999868B3DFD14A7A0}

Information about the possible feed statuses and their indicators. 

### Feed Statuses {#status}

The following are possible statuses for a feed:

| Status | Description |
|--- |--- |
|[!UICONTROL Syncing]|Feed setup details are being saved to [!DNL Target].|
|[!UICONTROL Sync Failed]|Feed setup details could not be saved to [!DNL Target]. Try again.|
|[!UICONTROL No Feed Run]|You have created a feed but it has not been scheduled (the frequency is set to Never).|
|Scheduled at *date and time*|The feed has not been run, but is scheduled to run at the specified date and time.|
|[!UICONTROL Waiting for Download]|[!DNL Target] is preparing to download the feed file.|
|[!UICONTROL Downloading Feed File]|[!DNL Target] is downloading the feed file.|
|[!UICONTROL Importing Items]|[!DNL Target] is importing items from the feed file.|
|Feed Imported Successfully at *time*|[!DNL Target] has imported the feed file into its content delivery system. Changes to item attributes have been made in the content delivery system and will soon be reflected in delivered recommendations. If you do not see the expected changes, try again and refresh the page containing recommendations.<br>Notes:<ul><li>If changes to an item's attributes result in an item being excluded from recommendations, the exclusion is immediately reflected. If an item is newly added, or changes to attributes result in an item being *no longer* excluded from recommendations, it is not reflected until the next algorithm update, which occurs within 24 hours.</li><li>When this status is displayed, updates might not yet be reflected in the [!UICONTROL Catalog Search] UI. A separate status is listed in [!UICONTROL Catalog Search] indicating the last time that the searchable catalog was updated.</li></ul>|
|[!UICONTROL Failed to Index]|The index operation failed. Try again.|
|[!UICONTROL Server Not Found]|FTP or URL locations are invalid or otherwise unreachable.|

To update a feed (for example, to make changes to your feed configuration or feed file), open the feed, make any desired changes, and click **[!UICONTROL Save]**. 

>[!IMPORTANT]
>
>Uploaded entities expire after 61 days. This means that your feed file should be uploaded at least every 60 days to avoid a disruption to your recommendations activities. If an item is not included in a feed file (or other entity update method) at least once every 60 days, [!DNL Target] infers the item is no longer relevant and removes it from the catalog.

### Feed Status Indicators {#section_3C8A236C5CB84C769A9E9E36B8BFABA4}

The following feed status indicators display in the [!UICONTROL Status] column: 

| Status Indicator | Description |
|--- |--- |
|Green status indicator|When a feed successfully finishes indexing, a green status dot indicates that the feed is in a successful state.|
|Yellow status indicator|When a feed or feed index is delayed by 25% of the feed frequency, a yellow status dot displays. For example, a yellow dot displays for a feed set to run daily if the index hasn't completed six hours after the scheduled time. Note: Once the feed status is "Waiting for Index Queue," the newly updated values are available in delivery and criteria processing.|
|White status indicator|When a feed is not scheduled, a white status dot indicates that the feed has not run yet.|
|Red status indicator|If the feed fails to upload data to the server, a red status indicator is shown.|

Consider the following examples: 

**Example 1:** 

* Day one: daily feed processes at 9:00 a.m. PST.
* Day two: it is 3:30 p.m. and the feed hasn't run since yesterday at 9:00 a.m. 

The status should be yellow because the index should have run roughly 6.5 hours ago. 6.5 hours +24 is 127% of the feed window. 

**Example 2:** 

* January 1: monthly feed processes at 9:00 a.m. PST.
* February 3: it is 10:00 a.m. and the feed hasn't run for one month, one day, and one hour ago. 

The status should be yellow because the index should have run roughly one day and one hour ago. Although this is only (31+(1/25))/30 = 1.03% of frequency setting, it surpassed the maximum of one-day delay. 

## Training videos

The following videos contain more information about the concepts discussed in this article.

### Understanding feeds in Recommendations (3:01) ![Overview badge](/help/main/assets/overview.png)

This video contains the following information:

* Understand the purpose of feeds
* Understand the value of feeds

>[!VIDEO](https://video.tv.adobe.com/v/27695)

### Create a feed (6:44) ![Tutorial badge](/help/main/assets/tutorial.png)

This video contains the following information:

* Set up a feed
* Know which type of feed to use

>[!VIDEO](https://video.tv.adobe.com/v/27696)
