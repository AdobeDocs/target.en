---
keywords: content;assets;manage content;offers;manage assets;enter selection mode;selection mode
description: Learn how to manage code and image offers by using the Offers library.
title: How Do I Manage Code and Image Offers?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
hide: yes
hidefromtoc: yes
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
---
# Offers

Use the [!UICONTROL Offers] library in [!DNL Adobe Target] to manage your code and image offer content.

>[!NOTE]
>
>This article contains information about updates to the [!DNL Target] user interface that is currently part of a Beta program. The [!DNL Adobe Target] team often enables new features for select customers for testing and feedback purposes. After the testing period completes, these features are enabled for all customers in future [!DNL Target Standard/Premium] releases and announced in release notes.

Click the **[!UICONTROL Offers]** tab at the top of the [!DNL Target] UI to display the [!UICONTROL Offers] library.

![Offers library in Adobe Target](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

The [!UICONTROL Offers] library contains offers that have been set up via [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS), and APIs. Offers created in [!DNL Target Classic] or other solutions are editable in [!DNL Target Standard/Premium].

The Offers library provides an overview of all code and image offers and lets you perform various actions:

| Element | Description |
|--- |--- |
|Left-navigation rail|Switch between listing [!UICONTROL Code Offers] or [!UICONTROL Image Offers].|
|[!UICONTROL Show filters] icon<P>![Show Filters icon](/help/main/c-activities/assets/show-filters-icon.png)|Click the **[!UICONTROL Show filters]** icon to filter offers by [!UICONTROL Type], [!UICONTROL Source], and [!UICONTROL AEM Type]<P>For more information, see [Apply filters to the Offers list](#filters) below.|
|Search fields|Use the **[!UICONTROL Search in]** fields to quickly find an offer or to reduce the number of offers displayed in the [!UICONTROL Offers] library. You can search by [!UICONTROL Offer Name], [!UICONTROL AEM Paths], or [!UICONTROL AEM Tags].|
|[!UICONTROL Create Folder]|Click Create Folder to create folders in the [!UICONTROL Offer] library to hold code offers, image offers, as well as other folders to create a sub-folder structure. For more information, see [Create offer folders](/help/main/c-experiences/c-manage-content/create-content-folder.md).|
|[!UICONTROL [!UICONTROL Create Offer]]|Create an offer. For more information about creating the various offer types, see: <ul><li>HTML Offer</li><li>[JSON Offer](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Redirect Offer](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Remote Offer](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul>|
|Bulk operations checkboxes|Perform bulk operations on all activities or on selected activities.<P>For a list of actions that are available (depending on your permissions and the offer status), see [Perform quick actions](#quick-actions) below.|
|[!UICONTROL Name]|The name of each offer.<P>Click the **[!UICONTROL Quick Info]** icon next to each offer name to view more information about that offer in a pop-up card, including the offer ID, type, date the offer was last modified and by whom, and more.<p>Click the **[!UICONTROL More actions]** icon (the horizontal ellipsis) next to each offer name to open a menu that lets you perform quick actions on an activity. The following actions are available (depending on your permissions and the offer status): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], and [!UICONTROL Move]. For more information about each action, see [Perform quick actions](#quick-actions) below.<P>Click the table header to sort the list alphabetically in ascending or descending order by name.|
|[!UICONTROL Type]|The offer type: HTML Offers, [Redirect Offers](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote Offers](/help/main/c-experiences/c-manage-content/about-remote-offers.md), and [JSON Offers](/help/main/c-experiences/c-manage-content/create-json-offer.md).|
|[!UICONTROL Source]|Shows where the offer was created: [!DNL Adobe Target], [!DNL Adobe Target Classic], and [!DNL Adobe Experience Manager].|

## Apply filters to the Offers library {#filters}

Click the **[!UICONTROL Show filters]** icon ( ![Show Filters icon on the Offers page](/help/main/c-experiences/c-manage-content/assets/show-filters-icon.png) ) to filter offers by [!UICONTROL Type], [!UICONTROL Source], and [!UICONTROL AEM Type].

![offers_filter image](assets/offers-filter-new.png)

The **[!UICONTROL Show filters]** icon lets you filter offers by the following categories:

* **Type**: HTML Offer, [JSON Offer](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Redirect Offer](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote Offer](/help/main/c-experiences/c-manage-content/about-remote-offers.md). 

* **Source**: [!DNL Adobe Target], [!DNL Adobe Target Classic], and [!DNL Adobe Experience Manager].

* **AEM Type**: [Content Fragments](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) and [Experience Fragments](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). For more information about the different fragment types, see [AEM Experience Fragments and Content Fragments overview](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Perform quick actions {#quick-actions}

You can perform the following quick actions by clicking the appropriate icon:

### Quick Info

Click the **[!UICONTROL Quick Info]** icon next to each offer name to view more information about that offer in a pop-up card, including the offer ID, type, date the offer was last modified and by whom, and more. The available options depend on the offer type: HTML Offer, [JSON Offer](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Redirect Offer](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Remote Offer](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

![](/help/main/c-experiences/c-manage-content/assets/quick-actions.png)

### More Actions

Click the **[!UICONTROL More actions]** icon (the horizontal ellipsis) next to each offer name to open a menu that lets you perform quick actions on an activity. The following actions are available (depending on your permissions and the offer status): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], and [!UICONTROL Move].

![More Actions option in the Target Offers library](/help/main/c-experiences/c-manage-content/assets/more-actions.png)

* Edit
* Copy
* Delete
* Move (For example, to move one or more items into a folder, click the **[!UICONTROL Move]** icon for the desired item, click the desired folder, then click **[!UICONTROL Drop]**.)

Depending on your permissions, you might not see icons for all options. For example, a user with [!UICONTROL Observer] permissions does not have the rights to use the [!UICONTROL Copy] option.

For detailed information about the tasks you can perform on offers and folders, see [Work with content in the Asset library](/help/main/c-experiences/c-manage-content/assets-working.md).

Perform additional tasks by hovering over the desired image offer or folder on the [!UICONTROL Image Offers] tab, then by clicking the desired icon.

![Image Offers options](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

Options include:

* Select
* Download
* View Properties
* Edit
* Annotate
* Copy

For detailed information about the tasks you can perform on offers and folders, see [Work with content in the Asset library](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Image offers are not part of the [Enterprise User Permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) model.

<!--

## Viewing offer definitions {#section_6B059DD121434E6292CAB393507D010E}

You can view offer definition details on a pop-up card in the [!UICONTROL Offers] library without opening the offer.

For example, the following offer definition card for an HTML offer is accessed by hovering over an offer on the [!UICONTROL Content] list, then clicking the information icon:

![offer-card-html image](assets/offer-card-html.png)

The following information is available:

* Name 
* Source 
* Type 
* Offer ID 
* Offer path 
* Last Modified

Click the [!UICONTROL Offer Usage] tab to view the activities that reference a code offer in each offer's definition pop-up card. This functionality does not apply to image offers. This way you can avoid impact to other activities while editing offers. Information includes [!UICONTROL Live Activities] and [!UICONTROL Inactive Activities].

![offer-card-usage image](assets/offer-card-usage.png)

The following offer definition card for a Redirect offer:

![offer-card-redirect image](assets/offer-card-redirect.png)

The following information is available:

* Name 
* Source 
* Type 
* Offer ID 
* Offer Path 
* Last Modified 
* Redirect URL 
* Include all URL parameters (On or Off) 
* Pass mbox session ID (On or Off)

The following offer definition card for a Remote offer:

![offer-card-remote image](assets/offer-card-remote.png)

The following information is available:

* Name 
* Source 
* Type 
* Offer ID 
* Offer Path 
* Last Modified 
* Redirect URL Type 
* Absolute or Relative URL

## Training video: The Content Repository ![Overview badge](/help/main/assets/overview.png)

This video includes information about managing offers.

* Connection between the [Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) and the Target Content Library 
* Custom HTML Offers 
* Custom HTML Offer in the Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)

-->
