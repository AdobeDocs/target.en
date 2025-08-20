---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: August 20, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice. Information in this article is updated frequently, especially before releases.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.8.3 (August 21, 2025)

This release contains the following updates and fixes:

**Offer decisions**

+++See details
* **Fixed an issue preventing customers from editing decision offers and selecting specific page elements in the updated UI**: In the updated activity-create process, customers were unable to edit existing decision offers or select specific page elements in the Visual Experience Composer (VEC). Decision offers were incorrectly displayed as HTML offers, and changes made during editing were not saved. Additionally, certain regional URLs, such as the Japan site, failed to load properly in VEC, blocking activity creation and updates. (TGT-53425)
* **Fixed an issue where [!UICONTROL Offer Decision] selectors could not be modified and changed unexpectedly after saving**: In the updated activity-create process, customers were unable to modify the [!UICONTROL Offer Decision] selector as intended. Attempts to change the selector were unsuccessful, and the selector reverted to an incorrect value after saving. This caused the decision offer to disappear from the Visual Experience Composer (VEC), blocking further edits. (TGT-53433)
* **Fixed an issue where [!UICONTROL Offer Decisions] disappeared from the activity after saving**: [!UICONTROL Offer Decisions] added during the activity-create process were not retained after saving and reopening the activity. This issue occurred when editing dynamic content and inserting [!UICONTROL Offer Decisions ]with specific selectors and properties. (TGT-53434)

+++

**Recommendations**

+++See details
* **Fixed issue in Recs UI where custom criteria CSV download returned 404 error**: Fixed an issue where customers were unable to download the custom criteria CSV in the activity-create process. (TGT-51966)
* **Fixed inconsistent image loading in [!UICONTROL Catalog Search]**: Fixed an issue where thumbnails and images in[!UICONTROL  Catalog Search] were not loading consistently in the activity-create process. Images failed to appear unless the "Thumbnail URL" column was visible and some product images loaded partially or not at all after navigation or search actions. (TGT-52778)
* **Fixed an issue where editing a recommendation in a duplicated experience impacted the original experience**: Customers reported that modifying a recommendation in a duplicated experience unintentionally altered the original experience. Specifically, after duplicating Experience B in the activity-create process and editing its design or criteria, the same changes were reflected in the original Experience B, despite being separate entities. (TGT-53369)
* **Fixed an issue where changes to a duplicated experience unintentionally affected the original experience in an activity:** Customers reported that when duplicating an experience within an activity and assigning a new audience, any changes made to the duplicated experience's design or criteria were also reflected in the original experience. This occurred even though no edits were made directly to the original version, impacting the ability to create independent variations within the same activity. (TGT-53361)
* **Fixed an issue where the [!UICONTROL Recommendation Catalog] intermittently failed to display complete product attribute data**: In the updated [!DNL Recommendations] UI, customers experienced an issue where certain product attributes, such as message, were not consistently displayed in the catalog search results, even though the data existed in the feed. This issue required customers to manually reconfigure the column visibility to retrieve the missing values. (TGT-52769)
* **Fixed an issue where a [!UICONTROL Front Promotion] could not be disabled in a live activity**: Attempts to disable a [!UICONTROL Front Promotion] in a live activity were not saved. After selecting [!UICONTROL Change Promotion] and disabling it, the promotion remained active upon re-editing the activity, preventing updates to recommendation configurations. Promotion settings now save correctly, allowing customers to disable or modify promotions in live activities as expected. (TGT-53231)
* **Fixed an issue where enabling a [!DNL Recommendations] [!UICONTROL Promotion] without data triggered an unclear error message**: Enabling a [!UICONTROL Front] or [!UICONTROL Back Promotion] in a [!DNL Recommendations] activity without specifying required values resulted in a generic "Invalid input error" message. The underlying issue was a missing configuration field, but the error message did not clearly indicate the cause, making troubleshooting difficult. The activity-create process now provides a clear and actionable error message when required fields, such as `collectionId` or rules, are missing, helping customers quickly identify and resolve configuration issues. (TGT-52616)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* **Fixed issue in activity-create process that blocked progression to [!UICONTROL Targeting] step in AP activities**: Fixed an issue in the activity-create process where customers were unable to proceed to the [!UICONTROL Targeting] step in [!UICONTROL Automated Personalization] (AP) activities unless two locations were added. This behavior differed from the previous experience, where a single location with multiple offers was sufficient. The requirement has been corrected, allowing customers to continue using single-location setups as part of their AP workflows. (TGT-53426)
* **Fixed an issue where the new activity-create process did not set the fmt=png-alpha parameter for transparent images**: In the updated UI, images inserted during the activity-create process no longer included the `fmt=png-alpha` parameter by default, resulting in loss of transparency. This behavior differed from the previous UI, which automatically appended the parameter to image URLs, preserving transparent backgrounds. (TGT-52615)

+++

**[!UICONTROL Workspaces]**

+++See details
* **Fixed an issue where a customer restricted to a single workspace could view activities from other workspaces**: Customers with access limited to one workspace were unexpectedly able to view activities across all workspaces when selecting [!UICONTROL All Workspaces] in the activity-create process. This visibility posed a risk of unintended changes to live activities in other workspaces, potentially impacting website performance. (TGT-53101)
* **Fixed an issue where a customer could view activities from the [!UICONTROL Default Workspace] without having access:** A customer with access limited to the staging workspace was able to view activities from the [!UICONTROL Default Workspace] via the activity-create process. This occurred despite correct backend configuration and access rights. (TGT-53297)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
