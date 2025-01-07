---
keywords: content;assets;manage content;offers;manage assets;enter selection mode;selection mode
description: Discover how to efficiently manage code and image offers using the [!UICONTROL Offers] library.
title: How Do I Manage Code and Image Offers?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
---
# Offers

Discover how to efficiently manage code and image offers using the [!UICONTROL Offers] library in [!DNL Adobe Target]. 

To display the [!UICONTROL Offers] library, click the **[!UICONTROL Offers]** tab at the top of the [!DNL Target] UI.

![Offers page](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

>[!NOTE]
>
>This article documents the updated [!UICONTROL Offers] UI released January 9, 2025. If you prefer to use the legacy [!UICONTROL Offers] UI, toggle [!UICONTROL Switch to the Old Experience] to the on position. 

The [!UICONTROL Offers] library contains offers that have been set up via [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS), and APIs. Offers created in [!DNL Target Classic] or other solutions are editable in [!DNL Target Standard/Premium].

The [!UICONTROL Offers] library provides an overview of all code and image offers and lets you perform various actions:

| Element | Description |
|--- |--- |
|Left-navigation rail|Switch between displaying [!UICONTROL Code Offers] or [!UICONTROL Image Offers].|
|[!UICONTROL Show Folders] / [!UICONTROL Hide Folders]<P>![Show Filters/Hide Filters icon](/help/main/assets/icons/RailLeft.svg)|Click the **[!UICONTROL Show Folders]** or **[!UICONTROL Hide Folders]** icon to toggle between displaying your offers folder structure or not displaying your folder structure.<P>For more information, see [Create offer folders](/help/main/c-experiences/c-manage-content/create-content-folder.md).|
|[!UICONTROL Show filters] icon<P>![Show Filters icon](/help/main/assets/icons/Filter.svg)|Click the **[!UICONTROL Show filters]** icon to filter offers by [!UICONTROL Type], [!UICONTROL Source], and [!UICONTROL AEM Type].<P>For more information, see [Apply filters to the Offers list](#filters) below.|
|Search fields|Use the **[!UICONTROL Search in]** fields to quickly find an offer or to reduce the number of offers displayed in the [!UICONTROL Offers] library. You can search by [!UICONTROL Offer Name], [!UICONTROL AEM Paths], or [!UICONTROL AEM Tags]. Search options are session-persistent.|
|[!UICONTROL Create Folder]|Click **[!UICONTROL Create Folder]** to create folders in the [!UICONTROL Offer] library to hold code offers, image offers, as well as other folders to create a sub-folder structure.<P>For more information, see [Create offer folders](/help/main/c-experiences/c-manage-content/create-content-folder.md).|
|[!UICONTROL [!UICONTROL Create Offer]]|Click **[!UICONTROL Create Offer]** to create an offer.<P>For more information about creating the various offer types, see: <ul><li>HTML Offer</li><li>[JSON Offer](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Redirect Offer](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Remote Offer](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul>|
|Bulk operations checkboxes<P>![Bulk Operations icon](/help/main/assets/icons/Rectangle.svg)|Click the [!UICONTROL Bulk Operations] checkboxes to perform bulk operations on all offers or on selected offers.<P>For a list of actions that are available (depending on your permissions and the offer status), see [Perform quick actions](#quick-actions) below.|
|[!UICONTROL Name]|The name of each offer.<P>Click the **[!UICONTROL Quick Info]** icon ( ![Quick Info icon](/help/main/assets/icons/InfoOutline.svg) ) next to each offer name to view more information about that offer in a pop-up card, including the offer ID, type, date the offer was last modified and by whom, and more.<p>Click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallList.svg) ) next to each offer name to open a menu that lets you perform quick actions on an activity. The following actions are available (depending on your permissions and the offer status): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], and [!UICONTROL Move]. For more information about each action, see [Perform quick actions](#quick-actions) below.<P>Click the table header to sort the list alphabetically in ascending or descending order by name.|
|[!UICONTROL Type]|The offer type: [!UICONTROL HTML Offers], [[!UICONTROL Redirect Offers]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offers]](/help/main/c-experiences/c-manage-content/about-remote-offers.md), and [[!UICONTROL JSON Offers]](/help/main/c-experiences/c-manage-content/create-json-offer.md).|
|[!UICONTROL Source]|Shows where the offer was created: [!DNL Adobe Target], [!DNL Adobe Target Classic], and [!DNL Adobe Experience Manager].|
|[!UICONTROL Last updated]|Displays the date and time that the offer was last modified and by whom.<P>Click the table header to sort the list in ascending or descending order by date.|

## Apply filters to the Offers library {#filters}

Click the **[!UICONTROL Show filters]** icon ( ![Show Filters icon on the Offers page](/help/main/assets/icons/Filter.svg)) to filter offers by [!UICONTROL Type], [!UICONTROL Source], and [!UICONTROL AEM Type].

The **[!UICONTROL Show filters]** icon lets you filter offers by the following categories:

* **[!UICONTROL Type]**: [!UICONTROL HTML Offer], [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md), and [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md). 

* **[!UICONTROL Source]**: [!DNL Adobe Target], [!DNL Adobe Target Classic], and [!DNL Adobe Experience Manager].

* **AEM Type**: [Content Fragments](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) and [Experience Fragments](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). For more information about the different fragment types, see [AEM Experience Fragments and Content Fragments overview](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

Filters are session-persistent.

## Perform quick actions {#quick-actions}

You can perform the following quick actions by clicking the appropriate icon:

### Quick Info

Click the **[!UICONTROL Quick Info]** icon ( ![Quick Info icon](/help/main/assets/icons/InfoOutline.svg) ) next to each offer name to view more information about that offer in a pop-up card, including the offer ID, type, date the offer was last modified and by whom, and more. The available options depend on the offer type: [!UICONTROL HTML Offer], [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

### More Actions

The actions available for [!UICONTROL Code Offers] and for [!UICONTROL Image Offers] differ slightly. The following sections contain more information:

#### [!UICONTROL Code Offer] options

Click the **[!UICONTROL More actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallList.svg) ) next to each offer name to open a menu that lets you perform quick actions on an activity. 

The following actions are available (depending on your permissions and the offer status):

* [!UICONTROL Edit]
* [!UICONTROL Copy]
* [!UICONTROL Delete]
* [!UICONTROL Move] (For example, to move one or more items into a folder, click **[!UICONTROL Move]** next to the desired item, click the desired folder, then click **[!UICONTROL Move]**.)

Depending on your permissions, you might not see icons for all options. For example, a user with [!UICONTROL Observer] permissions does not have the rights to use the [!UICONTROL Copy] option.

For detailed information about the tasks you can perform on offers and folders, see [Work with content in the Asset library](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] options

Perform additional tasks by hovering over the desired image offer or folder on the [!UICONTROL Image Offers] tab, then by clicking the desired icon.

Options include:

* [!UICONTROL Select]
* [!UICONTROL Download]
* [!UICONTROL View Properties]
* [!UICONTROL More Actions]
* [!UICONTROL Edit]
* [!UICONTROL Annotate]
* [!UICONTROL Copy]

For detailed information about the tasks you can perform on offers and folders, see [Work with content in the Asset library](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Image offers are not part of the [Enterprise User Permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) model.

## Viewing offer definitions {#section_6B059DD121434E6292CAB393507D010E}

To view offer definition details on a pop-up card in the [!UICONTROL Offers] library without opening the offer, click the ( ![Quick Info icon](/help/main/assets/icons/InfoOutline.svg) ).

The following information is available:

* [!UICONTROL Name] 
* [!UICONTROL Offer ID ] 
* [!UICONTROL Type]
* [!UICONTROL Last Modified]

Click the [!UICONTROL View Full Details] link to view the offer's attributes and activities that reference a code offer in each offer's definition pop-up card. This functionality does not apply to image offers. This way you can avoid impact to other activities while editing offers. Information includes details for [!UICONTROL Live Activities] and [!UICONTROL Inactive Activities].
