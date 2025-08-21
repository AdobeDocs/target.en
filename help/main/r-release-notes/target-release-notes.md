---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: August 21, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice. Information in this article is updated frequently, especially before releases.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.8.3 (August 21, 2025)

This release contains the following updates and fixes:

**[!UICONTROL Activities]**

+++See details
* **Fixed an issue where saving activities triggered an invalid user input error due to malformed property data**: Customers encountered a critical error when attempting to save existing activities. The error message indicated invalid user input, specifically referencing an unrecognized property name content in the JSON payload. Notably, new activities using the same property were saved successfully, suggesting the issue was isolated to legacy activity data. The activity-create process now correctly handles legacy property configurations, preventing invalid input errors and ensuring consistent save behavior across new and existing activities. (TGT-53507)
* **Fixed an issue that prevented customers from saving an activity due to an InvalidProperty.Json error**: Customers encountered an error when attempting to save an activity in the updated UI, even without making any modifications. The error message indicated an invalid JSON structure: "Invalid Json. Unrecognized property name 'content'. Location: line - 1, column - 432." This issue was caused by an unrecognized property in the request payload and has now been resolved. Customers can save activities successfully without encountering this error. (TGT-53513)
* **Fixed an issue where scheduled activities incorrectly displayed a [!UICONTROL Live] status until page refresh**: Customers observed that when scheduling an activity to go live at a future date and time, the status immediately appeared as [!UICONTROL Live] instead of [!UICONTROL Scheduled]. This caused confusion, even though the confirmation message correctly indicated that the activity was scheduled. Refreshing the page corrected the status display. This issue has now been resolved, and scheduled activities correctly show the Scheduled status without requiring a refresh. (TGT-52937)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details
* **Fixed an issue where customers could not type report suite names during the activity-create process**: Customers using [!DNL Adobe Analytics] as the reporting source during the activity-create process were unable to type into the [!UICONTROL Report Suite] drop-down list to search for specific report suites. This impacted workflows for organizations with large numbers of report suites, where manual scrolling significantly delayed setup. The drop-down list was not alphabetically ordered and did not consistently respond to typed input, making it difficult to locate report suites like "Office + Store - Web - Prod." This issue has been resolved, and customers can now efficiently search by typing report suite names. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++See details
* **Fixed an issue where expired "Time Frame" audiences blocked activity saving even after removal**: Customers were unable to save activities in the updated UI due to an error related to expired "Time Frame" audiences. Even after removing the affected audience, the error message persisted: "Activity contains audience with invalid time frame." This issue occurred because the system continued to validate the activity-only audience, even when it was no longer in use. The behavior was further complicated by time-zone discrepancies. The validation logic has been corrected, and customers can now save activities without encountering this error. (TGT-53517)

+++

**[!UICONTROL Experience Fragment]s**

+++See details
* **Fixed an issue that prevented customers from inserting Experience Fragments using [!UICONTROL Insert Before] or [!UICONTROL Insert After] in the UI** Customers encountered an error when attempting to insert [!UICONTROL Experience Fragments] into an activity using the "Insert Before" or "Insert After" options in the updated UI. The error message displayed was: "Offer content must contain exactly one HTML element." This issue was specific to the updated UI and did not occur in the previous version. This issue has now been resolved, and customers can successfully insert [!UICONTROL Experience Fragments] without encountering this error. (TGT-53442)
* **

+++

**[!UICONTROL Offer decisions]**

+++See details
* **Fixed an issue preventing customers from editing decision offers and selecting specific page elements in the updated UI**: In the updated activity-create process, customers were unable to edit existing decision offers or select specific page elements in the Visual Experience Composer (VEC). Decision offers were incorrectly displayed as HTML offers, and changes made during editing were not saved. Additionally, certain regional URLs, such as the Japan site, failed to load properly in VEC, blocking activity creation and updates. Decision offers now display correctly, page elements are selectable as expected, and regional URLs load properly in the VEC, restoring full editing functionality. (TGT-53425)
* **Fixed an issue where [!UICONTROL Offer Decision] selectors could not be modified and changed unexpectedly after saving**: In the updated activity-create process, customers were unable to modify the [!UICONTROL Offer Decision] selector as intended. Attempts to change the selector were unsuccessful, and the selector reverted to an incorrect value after saving. This behavior caused the decision offer to disappear from the Visual Experience Composer (VEC), blocking further edits. Selector changes are now preserved correctly, and decision offers remain visible and editable in the VEC after saving.(TGT-53433)
* **Fixed an issue where [!UICONTROL Offer Decisions] disappeared from the activity after saving**: [!UICONTROL Offer Decisions] added during the activity-create process were not retained after saving and reopening the activity. This issue occurred when editing dynamic content and inserting [!UICONTROL Offer Decisions ]with specific selectors and properties. [!UICONTROL Offer Decisions] now persist correctly after saving, and selectors remain intact, ensuring consistent targeting and editing behavior. (TGT-53434)

+++

**[!DNL Recommendations]**

+++See details
* **Fixed issue in [!DNL Recommendations] UI where custom criteria CSV download returned 404 error**: Fixed an issue where customers were unable to download the custom criteria CSV in the activity-create process. The download link now functions correctly, allowing customers to export custom criteria as expected. (TGT-51966)
* **Fixed inconsistent image loading in [!UICONTROL Catalog Search]**: Fixed an issue where thumbnails and images in[!UICONTROL  Catalog Search] were not loading consistently in the activity-create process. Images failed to appear unless the "Thumbnail URL" column was visible and some product images loaded partially or not at all after navigation or search actions. Image loading behavior has been stabilized, and thumbnails now display reliably regardless of column visibility or navigation actions. (TGT-52778)
* **Fixed an issue where editing a recommendation in a duplicated experience impacted the original experience**: Customers reported that modifying a recommendation in a duplicated experience unintentionally altered the original experience. Specifically, after duplicating Experience B in the activity-create process and editing its design or criteria, the same changes were reflected in the original Experience B, despite being separate entities. Duplicated experiences now maintain separate configurations, ensuring that edits to one experience do not affect the original. (TGT-53369)
* **Fixed an issue where changes to a duplicated experience unintentionally affected the original experience in an activity**: Customers reported that when duplicating an experience within an activity and assigning a new audience, any changes made to the duplicated experience's design or criteria were also reflected in the original experience. This issue occurred even though no edits were made directly to the original version, impacting the ability to create independent variations within the same activity. The activity-create process now correctly isolates duplicated experiences, ensuring that edits made to one experience do not affect the original. (TGT-53361)
* **Fixed an issue where the [!UICONTROL Recommendation Catalog] intermittently failed to display complete product attribute data**: In the updated [!DNL Recommendations] UI, customers experienced an issue where certain product attributes, such as message, were not consistently displayed in the [!UICONTROL Catalog Search] results, even though the data existed in the feed. This issue required customers to manually reconfigure the column visibility to retrieve the missing values. [!UICONTROL Catalog Search] now reliably displays all configured attributes, eliminating the need for manual column resets. (TGT-52769)
* **Fixed an issue where a [!UICONTROL Front Promotion] could not be disabled in a live activity**: Attempts to disable a [!UICONTROL Front Promotion] in a live activity were not saved. After selecting [!UICONTROL Change Promotion] and disabling it, the promotion remained active upon re-editing the activity, preventing updates to recommendation configurations. Promotion settings now save correctly, allowing customers to disable or modify promotions in live activities as expected. (TGT-53231)
* **Fixed an issue where enabling a [!DNL Recommendations] [!UICONTROL Promotion] without data triggered an unclear error message**: Enabling a [!UICONTROL Front] or [!UICONTROL Back Promotion] in a [!DNL Recommendations] activity without specifying required values resulted in a generic "Invalid input error" message. The underlying issue was a missing configuration field, but the error message did not clearly indicate the cause, making troubleshooting difficult. The activity-create process now provides a clear and actionable error message when required fields, such as `collectionId` or rules, are missing, helping customers quickly identify and resolve configuration issues. (TGT-52616)
* **Fixed an issue that prevented the [!UICONTROL Product] list from displaying in the [!UICONTROL Edit] modal within the [!UICONTROL Recommendations] tab**: Customers were unable to view the filtered product list when editing a [!UICONTROL collection] or [!UICONTROL exclusion] in the [!UICONTROL Recommendations] tab. The list was expected to update in real time based on applied rules, but it did not appear as intended. This issue has been resolved, and the product list now displays correctly and updates dynamically as rules are modified. (TGT-53481)
* **Fixed an issue with the layout of the View Details dialog in the updated UI**: The layout of the View Details modal in the updated UI has been modified to improve clarity and usability. The dialog now includes two tabs:
  * [!UICONTROL Details] tab: Displays all relevant information for the selected item.
  * [!UICONTROL Inventory] tab: Shows all products filtered by the current collection and exclusion rules.

  This enhancement helps customers more easily navigate and understand item-specific data and inventory context within the activity-create process. (TGT-53503)

  * **Fixed an issue where removed promotions in recommendation activities reappeared after saving**: Customers reported that when [!UICONTROL front] or [!UICONTROL back] promotions were removed from [!DNL Recommendations] activities and the activity was saved, the promotions continued to appear upon reopening. This issue occurred in both staging and production environments and affected the updated activity-create process. The issue has been resolved. Promotions that are removed from an activity now persist correctly after saving. (TGT-53490)

+++

**Reports**

+++See details
* **Fixed an issue where the [!UICONTROL Automated Segments] report displayed null audience values**: Customers reported that [!UICONTROL Automated Segments] in activity reports were showing null for audience data, preventing accurate analysis of segment performance. This issue occurred when accessing the [!UICONTROL Reports] section and selecting [!UICONTROL Automated Segments], even though valid audience data was expected. [!UICONTROL Automated Segments] now correctly displays audience values, ensuring reliable reporting and segmentation insights. (TGT-52793)

+++

**Singe Page Applications (SPAs)**

+++See details
* **Fixed an issue where switching between [!UICONTROL Browse] and [!UICONTROL Design] modes reset SPA state in the updated UI**: Customers reported that switching between [!UICONTROL Browse] and [!UICONTROL Design] modes in the updated UI caused the web editor to reload, resetting the state of SPAs. This issue disrupted workflows and required customers to re-enter information. The issue has been resolved. SPA state is now preserved when toggling between modes, ensuring a smoother and more consistent experience during activity creation. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* **Fixed issue in the activity-create process that blocked progression to the [!UICONTROL Targeting] step in AP activities**: Fixed an issue in the activity-create process where customers were unable to proceed to the [!UICONTROL Targeting] step in [!UICONTROL Automated Personalization] (AP) activities unless two locations were added. This behavior differed from the previous experience, where a single location with multiple offers was sufficient. The requirement has been corrected, allowing customers to continue using single-location setups as part of their AP workflows. (TGT-53426)
* **Fixed an issue where the new activity-create process did not set the fmt=png-alpha parameter for transparent images**: In the updated UI, images inserted during the activity-create process no longer included the `fmt=png-alpha` parameter by default, resulting in loss of transparency. This behavior differed from the previous UI, which automatically appended the parameter to image URLs, preserving transparent backgrounds. The activity-create process now correctly applies the `fmt=png-alpha` parameter to image URLs when transparency is required, ensuring consistent rendering of transparent assets. (TGT-52615)
* **Fixed an issue that prevented customers from searching report suites in the updated UI**: In the updated UI, the [!UICONTROL Report Suites] drop-down list in the [!UICONTROL Goals & Settings] section did not allow customers to type and search, making it difficult to locate specific report suites, especially for tenants with a large number of entries. Unlike the previous UI, the list was not sorted and lacked input-based filtering. This issue has been resolved. Customers can now type to search and filter report suites, restoring the functionality available in the legacy UI. (TGT-53514)

+++

**[!UICONTROL Workspaces]**

+++See details
* **Fixed an issue where a customer restricted to a single workspace could view activities from other workspaces**: Customers with access limited to one workspace were unexpectedly able to view activities across all workspaces when selecting [!UICONTROL All Workspaces] in the activity-create process. This visibility posed a risk of unintended changes to live activities in other workspaces, potentially impacting website performance. Workspace access controls have been reinforced to ensure that customers can view and interact only with activities within their assigned workspace. (TGT-53101)
* **Fixed an issue where a customer could view activities from the [!UICONTROL Default Workspace] without having access:** A customer with access limited to the staging workspace was able to view activities from the [!UICONTROL Default Workspace] via the activity-create process. This behavior occurred despite correct backend configuration and access rights. Workspace access controls have been reinforced to ensure that customers can view activities only within their assigned workspace.(TGT-53297)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
