---
keywords: content library;assets;annotate;copy;delete asset;download asset;edit content;share card;view content properties
description: Discover the process of organizing and optimizing your code and image offers within the [!DNL Target] [!UICONTROL Offers] library.
title: Master Content Management in the [!UICONTROL Offers] Library
feature: Experiences and Offers
hide: yes
hidefromtoc: yes
exl-id: 5d836037-3f51-4c63-8717-65de72e5c793
---
# Work with content in the Asset library

Information about the tasks you can perform on an asset in the [!UICONTROL Content Library] in [!DNL Adobe Target]. Tasks include annotating, copying, deleting, downloading, editing, sharing, and viewing properties.

1. Click **[!UICONTROL Offers]** > **[!UICONTROL Code Offers]** or **[!UICONTROL Image Offers]**.

   For more information about searching the [!UICONTROL Offer library] and creating [!UICONTROL Smart Collections], see [Filter and Search Content](/help/main/c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276). 

1. (Conditional) For image offers, toggle between the [!UICONTROL Card View] and [!UICONTROL List View], click the [!UICONTROL Card View] icon or the [!UICONTROL List View] icon in the upper right corner of the content library. You can also use [!UICONTROL View Settings] to configure the columns when viewing the [!UICONTROL List View]. 

   The following illustration shows the available options when viewing the [!UICONTROL List View]:

   ![List View options](/help/main/c-experiences/c-manage-content/assets/view-settings-options.png)

1. Perform the desired action, as explained in the following sections:

## [!UICONTROL Code Offers] options

When viewing the [!UICONTROL Code Offers] page, you can perform the following actions on an item by hovering over an offer or folder, then selecting the appropriate icon.

![Hover icons on Code Offers tab](/help/main/c-experiences/c-manage-content/assets/code-offers-hover-icons-new.png)

* **Information**: Click the [!UICONTROL Information] icon to view the offer's information, including [!UICONTROL Offer ID], [!UICONTROL Type], [!UICONTROL Last Modified] (date, time, and modifier's name). Click [!UICONTROL Full Details] to view additional information, including the offer attributes and activity usage (activity name, status, workspace, and modified date and time).
* **Edit**: Edit the folder or offer.
* **Copy**: Copy the offer. Copying and then editing the offer lets you easily create a similar new offer.
* **Delete**: Delete the offer or folder. See [Considerations when deleting items](#delete).
* **Move**: Click the [!UICONTROL Move] icon, navigate to the location to which you want to move the offer or folder, then click **[!UICONTROL Move]**. For example, you can move one or more folders into another folder to create sub-folders.

## [!UICONTROL Image Offers] options

When viewing the [!UICONTROL Image Offers] page, you can perform the following actions on an item by hovering over an offer or folder, then selecting the appropriate icon.

The following illustration shows the hover icons when viewing the [!UICONTROL Card View].

![Hover icons on the Image Offers tab when in Card View](/help/main/c-experiences/c-manage-content/assets/image-offers-hover-icons.png)

The following illustration shows the hover icons when viewing the [!UICONTROL List View]. To display the icons, click an item in the list.

![Hover icons on the Image Offers tab when in List View](/help/main/c-experiences/c-manage-content/assets/list-view-hover.png)

* **Select**: Select one or more folders on which to perform the following actions:

  * Download
  * Copy
  * Move
  * Delete (See [Considerations when deleting items](#delete).)

  Select one or more image offers on which to perform the following actions:

  * Share
  * Download
  * View Properties
  * Edit
  * Annotate
  * Move

* **Download**: Download the image offer or the folder and its contents.
* **View Properties**: View the item's properties. Be sure to click the [!UICONTROL Basic] tab and the [!UICONTROL Advanced] tab to view all available information. You can edit the properties and add more information. You can add metadata information, publication status, and license data.
* **More Actions**: Display additional options when in [!UICONTROL Card View].
* **Edit**: Edit the folder or offer.
* **Annotate**: Add a note to the asset. Click the asset, then select the area you want to annotate and type your note.
* **Copy**: Copy the offer. Copying and then editing the offer lets you easily create a similar new offer.
* **Move**: Click the [!UICONTROL Move] icon, navigate to the location to which you want to move the offer or folder, then click **[!UICONTROL Move]**. For example, you can move one or more folders into another folder to create sub-folders.

## Considerations when deleting items {#delete}

* You can delete an entire folder containing any number of assets and sub-folders inside. This feature is available in the [!DNL Target] UI as well in the [!DNL Adobe Experience Cloud Assets] UI.
* If you delete a folder with a large number of images, the process running behind the scenes can take time (several minutes) before the UI refreshes to show the final state. The amount of time necessary is a function of the number of images, not the size of the images. A good estimate is ten minutes for 2,000 images. You can proceed with other work and check the final state after several minutes to verify the deletion.
* Non-empty folders in the [!UICONTROL Image Offer library] can be deleted. If all images within the folder are not referenced in any activity, the entire folder and its contents are deleted. If some images within the folder are referenced in any activity, all unreferenced images are deleted, but referenced images and folders containing those images are retained.
