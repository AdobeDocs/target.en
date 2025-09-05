---
keywords: Release notes;prerelease notes;future enhancements;future fixes;future features;upcoming release
description: View a list of features, enhancements, and fixes included in previous releases of Adobe Target.
title: What Features Are Included in Previous Releases?
feature: Release Notes
exl-id: e4d261a1-d3aa-46ea-b1ce-efa76a90dc71
---
# Release notes for previous releases

Release notes for previous [!DNL Adobe Target] releases, including release notes for [!DNL Target Standard/Premium], the [!DNL Target] platform, and the [!DNL Target] Javascript library (at.js). 

Release notes are arraigned in descending order by month and year of release.

>[!NOTE]
>
>See [Target release notes (current)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) for information about the current month's Target releases (platform and Target Standard/Premium).

## Release notes - 2025

### [!DNL Target Standard/Premium] 25.8.4 (September 1, 2025)

This release contains the following updates and fixes:

**[!UICONTROL Activities]**

+++See details
* **Customers could not copy activity or document names from the [!UICONTROL Activity Overview]**: Previously, customers were unable to copy the name of an activity or the associated offer/document directly from the [!UICONTROL Activity overview] in the updated activity-create process. This limitation impacted usability, especially on smaller screens. Customers can now easily copy both activity and document names without workarounds. (TGT-51850)
* **Proactive ingestion of curated [!DNL Target] customer data during activity creation**: Improved the activity-create process by enabling the proactive collection of reports, content, and screenshots from [!DNL Target] customers. This enhancement addresses data gaps identified in existing use cases and helps ensure more accurate insights during activity and experiment setup. (TGT-52415)
* **AP activities did not fetch model-ready data in the [!UICONTROL Reports] section**: Customers viewing Automated Personalization (AP) activities in the [!UICONTROL Reports] section were unable to see model-ready indicators at the report group and offer level. This issue occurred because model-ready data was not being fetched correctly from the backend. The functionality has been restored, and model-ready data now appears as expected. (TGT-53600 & TGT-53601)
* **Activities scheduled for the future incorrectly displayed a "[!UICONTROL Live]" status in the [!UICONTROL Activity] overview**: Customers observed that activities scheduled to start in the future were incorrectly marked as "[!UICONTROL Live]" in the [!UICONTROL Activity] overview. This status mismatch was resolved, and scheduled activities now correctly display as "[!UICONTROL Scheduled]" without requiring a page refresh. (TGT-52835)

+++

**[!UICONTROL Recommendations]**

+++See details
* **Product list was not visible in the [!UICONTROL View Collection] dialog:** Previously, customers were unable to see the product list when viewing a collection in the [!UICONTROL Recommendations] tab. The [!UICONTROL View Collection] dialog now correctly displays the associated products, improving transparency and usability in the updated [!UICONTROL Recommendations] UI. (TGT-50531)
* **Fixed an issue that caused case-sensitive filtering in [!UICONTROL Product Catalog Search] advanced search**: The advanced search filtering in the [!UICONTROL Product Catalog Search] page now correctly ignores case sensitivity, aligning with the behavior of both the backend and GraphQL services. This update ensures consistent and accurate suggestion results for customers regardless of text casing. (TGT-53585)
* **Advanced search in the updated [!UICONTROL Product Catalog Search] UI did not provide suggestions**: Customers using the advanced search feature in the updated [!UICONTROL Product Catalog Search] UI were required to enter exact values with correct spelling, as no suggestions were displayed. This issue made it difficult to locate products efficiently. Suggestions now appear as expected during advanced search input. (TGT-52008)
* **Some approvers were unable to view products in [!UICONTROL Product Catalog Search]**: Customers with [!UICONTROL Approver] permissions were unable to see any products in [!UICONTROL Product Catalog Search], despite other users with identical roles having access. This issue was caused by a permissions inconsistency affecting catalog visibility. All approvers can now view products in the [!UICONTROL Recommendations] section as expected. (TGT-53617)

+++

**[!UICONTROL Reports]**

+++See details
* **Reports failed to load for the Desktop audience due to an invalid audience name error**: Customers encountered a GraphQL error when attempting to view reports for the one audience in the activity-create process. The system returned an "Invalid audience name: XXXXX" message, preventing access to reporting data. Reports now load correctly for the Desktop audience. (TGT-53371)
* **Switching audiences on the Reports page caused errors in the Target UI**: Customers encountered errors when selecting certain audiences in the [!UICONTROL Reports] section. This issue was caused by invalid audience handling in backend GraphQL calls, resulting in unexpected errors and missing data. The issue has been resolved, and desktop audiences now load without errors—even when no data is available. (TGT-53370)
* **[!UICONTROL Graph view] in the [!UICONTROL Reports] section did not display values from [!DNL Analytics]**: Customers accessing [!UICONTROL Graph view] in the Re[!UICONTROL ]ports section encountered missing data, with all values appearing as zero. This issue was caused by incorrect data retrieval from [!UICONTROL Analytics]. [!UICONTROL Graph view] now displays accurate values as expected. (TGT-52792)
+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* **Clicking "Accept Cookies" using the [!UICONTROL Enhanced Experience Composer] (EEC) failed due to a missing function**: Customers reported that attempting to accept cookies via the EEC resulted in a console error: `handleclickAcceptAllButton is not defined`. The cookie acceptance functionality now works as expected, ensuring a smoother experience during activity creation in the updated UI. (TGT-52794)
* **The new EEC UI failed to load certain pages that were previously supported in the legacy UI**: Customers reported that the new EEC could not load some pages, which were accessible in the legacy UI despite iframe-busting code present on the site. The updated activity-create process now supports loading these pages, restoring compatibility for activity creation workflows. (TGT-53061)
* **The VEC displayed a blank white screen when editing experiences**: Customers from a certain tenant reported that the VEC screen went blank when attempting to edit experiences in the updated VEC. This issue affected both newly created and older activities, preventing workflow continuity. The VEC now loads correctly, allowing customers to edit experiences without interruption. (TGT-53547)
* **The VEC crashed and displayed a blank screen when loading certain activities**: Customers from a certain tenant reported that the VEC failed to load specific activities. The experience editor remained stuck on "Applying initial modifications" before crashing and showing a blank screen. Console errors indicated a failure to read undefined properties. The editor now loads affected activities without errors in the updated VEC. (TGT-53548)
* **Clearing all date values using Backspace caused the page to crash**: Customers scheduling activities in the [!UICONTROL Goals & Settings] section experienced a crash when using Backspace to clear all values from the "[!UICONTROL Specified Date & Time]" fields. This issue was caused by a null reference error in the date-handling logic. The page now handles empty date inputs gracefully without crashing. (TGT-53624)
* **No products appeared in [!UICONTROL Product Catalog Search] due to an invalid payload**: Customers accessing the [!UICONTROL Recommendations] section in [!UICONTROL Product Catalog Search] encountered empty results caused by an invalid GraphQL payload. This backend error prevented product data from loading correctly. Products now display as expected in the updated UI. (TGT-53630)
* **[!DNL Scene7] images were saved with lower resolution in the updated VEC**: Customers editing experiences in the updated VEC noticed that [!UICONTROL Scene7] image URLs were saved without resolution parameters, resulting in lower-quality images being delivered (400×400 instead of the intended 800×800). Image URLs now retain the correct parameters to ensure proper resolution. (TGT-52631)
* **live activities could still be edited in the VEC**: Customers were able to access edit options for live activities in the updated VEC, which could lead to unintended changes. This issue has been resolved by disabling edit functionality for live activities. Edit buttons are now hidden in the activity list and overview for editors, while approvers and other roles remain unaffected. (TGT-53055)
* **Decommissioned the [!UICONTROL Failed] and [!UICONTROL Draft] activities section in the updated VEC**: The [!UICONTROL Failed] and [!UICONTROL Draft] activities options have been removed from the updated VEC. The new UI no longer supports draft states and failing campaigns are not stored in the backend. These options are no longer relevant. Related filters and backend fields (for example, `uiSyncFailed`, `errorMessage`) have also been removed to streamline activity management. (TGT-53150)
* **Unable to log in to the VEC for an activity**: Customers attempting to log in to their site through the VEC were repeatedly redirected to the login page, preventing access to activity editing. This issue was not reproducible internally and may have been related to site-side session handling. The login flow has been stabilized, and customers can now access the VEC without redirection errors. (TGT-53524)
* **Pressing the back button twice in [!UICONTROL Browse] mode caused the VEC to crash**: Customers navigating through [!UICONTROL Browse] mode in the VEC experienced crashes when pressing the browser's back button twice. This issue caused the editor to freeze and required a page refresh. The editor now handles back navigation reliably without crashing. (GT-53568)
* **Activities could not be edited due to undefined location mappings**: Customers encountered an error when attempting to edit activities, caused by undefined location IDs in the `LocationMapping.behaviorTargetedActivity` logic. This issue resulted in a 400 error and blocked activity updates. Activities can now be edited without location-related validation errors. (TGT-53607)
* **Saving activities triggered an invalid user input error**: Customers encountered an invalid user input error when attempting to save activities after making minor modifications in the updated VEC. The error was caused by mismatched location mappings in the backend validation logic. Activities can now be saved successfully without triggering location-related errors. (TGT-53603)

+++

### [!DNL Target Standard/Premium] 25.8.3 (August 21, 2025)

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

### [!DNL Target Standard/Premium] 25.8.2 (August 14, 2025)

This release includes the following fixes and updates:

**[!UICONTROL Activities]**

+++See details
* **Fixed activity-loading issue in updated [!DNL Target] UI**: Fixed an issue in the updated [!DNL Target] UI where certain activities failed to load when attempting to edit. This issue caused customers leaving users in an indefinite loading screen. This issue impacted multiple activities and was reported to occur inconsistently across customers. With this fix, affected activities now load properly, allowing seamless editing and reducing disruption to activity workflows. (TGT-53209)
* **Fixed save error in activity-create process due to `optionLocalId` validation**: Fixed an issue in the activity-create process that prevented customers from saving changes due to a backend validation error: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` This issue occurred when modifying specific elements within an activity, resulting in a failed save operation. The fix ensures that `optionLocalId` references are now correctly validated, allowing customers to save activities without encountering this error. (TGT-53293)
* **Fixed crash in activity-create process caused by invalid option references when switching pages**: Fixed an issue in the activity-create process that caused the UI to crash after switching pages three times during editing. The crash was triggered by invalid option references, resulting in console errors such as "Option with localId '7' not found." With this update, customers can now switch between pages and apply modifications without encountering system failures or interruptions. (TGT-53295)
* **Fixed save error in activity-create process caused by invalid user input when editing experiences**: Fixed an issue in the activity-create process where customers were unable to save changes to an activity due to an invalid user input error. The error occurred when modifying experiences in the updated UI, preventing updates from being committed. The activity can now be saved successfully, allowing customers to edit and publish without interruption. (TGT-53267)
* **Fixed loading issue in activity-create process that blocked editing in updated UI**: Fixed an issue in the activity-create process where customers were unable to edit activities in the updated UI due to a continuous loading screen. Customers can now open and modify activities without encountering loading failures. (TGT-53415)
* **Fixed experience requirement issue in activity-create process for AP activities in updated UI**: Fixed an issue in the activity-create process where [!UICONTROL Automated Personalization] (AP) activities required two locations instead of two experiences in the updated UI. This behavior blocked use cases where customers configured a single location with multiple offers, which was previously supported. The requirement has been corrected to match the original functionality, allowing customers to proceed with AP activities using two experiences regardless of location count. (TGT-53429)
* **Fixed tracked element field behavior in Click Track mode to prevent unsaved input and improve clarity**: Fixed an issue in the activity-create process where the [!UICONTROL Tracked Element] field in [!DNL Click Track] mode was editable but did not retain the entered name, causing confusion for customers. The field is now disabled to prevent unsaved input, and the naming of selected elements has been clarified to improve goal configuration and tracking accuracy.** (TGT-53458)
* **Fixed issue in activity-create process that blocked naming of tracked components in [!UICONTROL Click Track] mode**: Fixed an issue in the activity-create process where customers were unable to name tracked components in [!UICONTROL Click Track] mode. After entering a name, the field appeared editable but did not retain the input, defaulting to generic labels like "MY PRIMARY GOAL 0" in edit mode. The tracked element field is now disabled, and naming behavior has been clarified to improve goal setup and tracking accuracy. (TGT-51396)

+++

**Experience Fragments (XFs)**

+++See details
* **Fixed issue in activity-create process that allowed unintended HTML editing of AEM-exported fragments**: Fixed an issue in the activity-create process that allowed customers to edit the HTML of [!DNL Experience Fragments] (XFs) exported from [!DNL Adobe Experience Manager] (AEM) within [!DNL Target]. This behavior was unintended, as XFs should remain locked for editing once published from AEM. The fix ensures that the "Edit HTML" option is no longer available for AEM-exported fragments, preserving content integrity and expected governance. (TGT-53286)
* **Fixed intermittent preview issue for XF content in activity-create process within updated UI**: Fixed an issue in the activity-create process where XF content intermittently failed to render in preview mode within the updated UI. Although the content delivered correctly, the preview did not consistently display, making it difficult for customers to validate offer setup. XF previews now load reliably, improving confidence and efficiency during activity configuration. (TGT-53318)

+++

**QA mode**

+++See details
* **Fixed issue in activity-create process where leading spaces in URLs caused broken QA links**: Fixed an issue in the activity-create process where leading spaces in the activity URL were not trimmed properly when saving. This caused invalid QA links and incorrect formatting in the back-end. After the update, URLs are now saved cleanly, preventing broken links and improving the reliability of QA workflows for customers. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++See details
* **Fixed issue in catalog search UI where advanced search failed to provide suggestions**: Fixed an issue in the new [!UICONTROL Catalog Search] UI where the [!UICONTROL Advanced Search] feature failed to provide suggestions. Users were required to input exact values with precise spelling, making the search experience cumbersome and error-prone. With this fix, the [!UICONTROL Advanced Search] now offers relevant suggestions as users type, improving usability and reducing friction in locating products. (TGT-52008)
* **Resolved multiple UI and filtering issues to improve responsiveness and entity interaction**: Resolved several issues, including poor responsiveness of criteria details on small-screen devices, lack of results when selecting "All host groups" in the Environment filter, and inability to interact with entities that have no name. These fixes improve usability across screen sizes, ensure accurate filtering, and allow full interaction with all product entities, enhancing the overall experience for users. (TGT-52992)
* **Fixed missing product IDs in Recommendations detail view during activity creation**: Fixed an issue in the [!DNL Recommendations] activity-create process where product IDs were missing from the product detail screen, making it difficult for customers to copy or reference product IDs during workflows. Product IDs now appear clearly in the detail view, improving visibility and supporting more efficient product management for customers. (TGT-51964)
* **Fixed issue in activity-create process where product messages failed to display in recommendations view**: Fixed an issue in the activity-create process where the [!UICONTROL Message] column in the [!DNL Recommendations] view did not display product data, even though messages were present. Customers had to manually remove and re-add the column to temporarily reveal the content, which would often disappear again when scrolling or searching. This update restores consistent visibility of product messages, improving catalog navigation and review workflows. (TGT-52777)
* **Fixed issue in activity-create process where selecting 'All host groups' returned no results in recommendations view**: Fixed an issue in the activity-create process where selecting the "All host groups" environment in the [!DNL Recommendations] view returned no results. Customers can now view product data across all host groups as expected, improving visibility and filtering accuracy during activity setup. (TGT-53006)
* **Fixed issue in activity-create process where front-promotion toggle did not persist after saving**: Fixed an issue in the activity-create process where disabling the front promotion toggle in activity settings did not persist after saving. Customers attempting to remove the front promotion found the toggle re-enabled upon revisiting the activity, preventing proper customization. This update allows changes to be saved reliably, giving customers full control over promotion settings. (TGT-53215)
* **Fixed inconsistent sorting by [!UICONTROL Last Updated] column:** Fixed an issue in the activity-create process where sorting the catalog by the [!UICONTROL Last updated] column produced inconsistent results. Customers were unable to reliably organize product data based on update timestamps, making catalog review and management more difficult. Sorting now works as expected, improving accuracy and usability in the updated UI. (TGT-53116)

+++

**Visual Experience Composer (VEC)**

+++See details
* **Fixed activity loading and [!UICONTROL Cancel] button issues in activity-create process**: Fixed an issue in the activity-create process where certain activities failed to load, leaving customers unable to access modifications. Additionally, the [!UICONTROL Cancel] button was unresponsive, preventing customers from stopping the loading process or exiting the edit view. This fix ensures that activities now load reliably and the [!UICONTROL Cancel] button functions as expected, improving overall stability and user experience in the Visual Experience Composer. (VEC)(TGT-53218)
* **Fixed experience switching issue in updated VEC UI that blocked editing and disabled [!UICONTROL Cancel] button**: Fixed an issue in the updated VEC UI where modifications failed to load when switching between experiences in an Experience Targeting (XT) activity. Customers were unable to edit experiences beyond the one they initially entered, and the [!UICONTROL Cancel] button was either missing or unresponsive. This fix ensures that modifications now load correctly across all experiences and that the [!UICONTROL Cancel] button functions reliably, even without the Helper extension, improving editing workflows and reducing frustration. (TGT-53256)
* **Fixed white screen issue when switching between multiple experiences in activity-create process**: Fixed an issue where switching between multiple experiences caused a white screen. Also fixed an issue in the activity-create process where customers encountered a white screen when attempting to modify multiple experiences within an activity. This issue occurred after applying changes to two experiences and then selecting a third experience, preventing further edits. The update ensures smooth transitions between experiences, allowing customers to make modifications without interruption. (TGT-53266)
* **Fixed issue in VEC where custom code changes were not reliably saved across editing sessions**: Fixed an issue where custom code modifications made in the Visual Experience Composer (VEC) were not reliably saved in a single attempt. Customers reported that changes, such as styling updates or HTML edit, were intermittently missing from the website and QA URLs, even after using both the [!UICONTROL Edit Content] and final [!UICONTROL Save] buttons. This regression has been resolved, ensuring that all custom code changes persist as expected across editing sessions.** (TGT-53418)
* **Fixed missing `triggerViews` in updated UI during activity creation**: Fixed an issue in the activity-create process where `triggerViews` were not appearing in the updated UI, even though they were correctly implemented on the page. This impacted multiple customers and made it difficult to validate view-based triggers during activity setup. `TriggerViews` now display as expected, allowing customers to complete and test their configurations reliably. (TGT-53239)
* **Fixed view-loading issue in activity-create process for specific webpages in updated UI**: Fixed an issue in the activity-create process where views were not loading in the updated UI for specific webpages, despite being correctly implemented and visible in delivery or interact calls. This affected multiple customers and made it difficult to validate view-based targeting. Views now populate consistently across supported pages, improving reliability during activity setup. (TGT-53246)
* **Fixed intermittent view loading issue in activity-create process in updated UI**: Fixed an issue in the activity-create process where views intermittently failed to appear in the updated UI during activity editing. Although the correct view name was present in the network payload, it was not consistently recognized in the interface, impacting customers' ability to configure view-based personalization. Views now appear reliably, supporting smoother setup and validation workflows. (TGT-53223)
* **Fixed issue in activity-create process where tracked action names were not saved in updated UI**: Fixed an issue in the activity-create process where tracked action metrics could not be saved in the updated UI. After naming a tracked element and saving the activity, the name would reset to a default label when reopened, causing confusion and disrupting goal configuration. Tracked actions now retain their assigned names, allowing customers to set and manage conversion metrics accurately. (TGT-53453)

+++

### [!DNL Target Standard/Premium] 25.8.1 (August 7, 2025)

This release includes the following enhancements and fixes:

**Activities**

+++See details
* Fixed several issues with the updated UI, including errors when deleting page types due to spacing in input values, unreliable activity copying between workspaces, and malfunctioning page delivery rules in QA environments. (TGT-52703)
* Fixed an issue in the updated [!DNL Target] UI where users with the [!UICONTROL Editor] role were able to access and attempt to edit live activities, which should be restricted. The activity list and overview screens incorrectly displayed edit options for live activities, leading to potential unintended changes. (TGT-53055)
* Fixed an issue in the [!UICONTROL Advanced Search] UI where selecting the "value is present" or "value is not present" operators prompted users to enter an operand, which should not be required for these conditions. (TGT-51961) 
* Fixed an issue in the updated UI where attempts to copy activities from the staging to production workspace consistently failed, even in sandbox environments. Customers encountered various error messages, including "Anonymous audience already used by the activity" and "Invalid audience ID," despite using valid configurations and having appropriate workspace permissions. (TGT-52394)

+++

**Experience Fragments (XFs)**

+++See details
* Fixed an issue where Experience Fragment (XF) content fails to render in the [!UICONTROL Visual Experience Composer] (VEC) preview, despite working correctly in content delivery. (TGT-53318)

+++

**Localization**

+++See details
* Fixed a localization issue where the "Add Promotion" button in the "Promotions" section appeared unlocalized across multiple language environments in the QA tenant. (TGT-53263)

+++

**Offers**

+++See details
* Fixed an issue where editing an existing HTML offer via the Visual Experience Composer (VEC) caused all modifications to be removed from content delivery. The changes appear grayed out in the modification tab and are not reflected in QA previews, despite being correctly applied in the legacy UI. (TGT-52863)
* Fixed an issue in the updated [!DNL Target] UI where HTML offer modifications made in the [!UICONTROL Visual Experience Composer] (VEC) did not persist after navigating from the [!UICONTROL Targeting] tab back to [!UICONTROL Experiences]. (TGT-52874)
* Fixed an issue in the updated [!DNL Target] UI where inserting one HTML offer before and another after the same selector caused incorrect location generation. When customers returned from the [!UICONTROL Targeting] tab to the [!UICONTROL Experience] tab, only one selector was retained, resulting in lost modifications and broken content delivery. This behavior differed from the legacy UI, which correctly preserved both modifications with distinct location identifiers. (TGT-52891)
* Fixed an issue in the updated [!DNL Target] UI where clicking an added offer within the [!UICONTROL Modifications] rail caused the right-hand [!UICONTROL Configuration] panel to intermittently appear and disappear, making it difficult to interact with the offer settings. (TGT-53288) 
* Fixed an issue where HTML offers added to audience-specific variations within an activity did not consistently save or appear in the modification section. After switching between audiences during editing, previously applied offers sometimes disappeared or failed to render, disrupting validation and delaying activity readiness. (TGT-53440)
* Fixed an issue where copying an activity that included offers resulted in duplicate offers being created in the new activity. This behavior caused unnecessary clutter and confusion, particularly when moving activities between workspaces. The fix ensures that [!DNL Target] offers are now correctly copied into the destination workspace without duplication, streamlining activity management and improving workflow efficiency. (TGT-53454)

+++

**Single Page Applications (SPAs)**

+++See details
* Fixed an issue in the updated VEC that prevented customers from applying modifications to [!UICONTROL Single Page Application] (SPA) views. While activities created in the old UI supported view-specific targeting, the new UI failed to detect or allow edits to those views, with the view-switching controls appearing disabled. (TGT-52556)

+++

**Visual Experience Composer (VEC)**

+++See details
* Fixed an issue where modifications made to experiences within the [!UICONTROL Visual Experience Composer] were either not visible or appeared inconsistently in the UI. (TGT-TGT-53381)
* Fixed an issue in the updated VEC where the [!UICONTROL Manage Content] section failed to display alt text for experience thumbnails. This issue made it difficult for users to identify documents, especially when filenames were long or truncated. (TGT-52291)
* Fixed an error where customers encountered incorrect validation errors when configuring [!UICONTROL page delivery] rules in VEC activities. Specifically, operators like "equals any of" and "does not equal any of" triggered "Invalid input for the operator type" when entering text values, even though text should be supported. (TGT-52629)
* Fixed several issues that caused inconsistent behavior in the [!UICONTROL Modifications] panel of the updated UI when selecting offers using the "Select an offer" button. Instead of replacing the existing offer, the UI added a duplicate, and attempted to interact with either offer resulted in console errors such as `selectorNotFound`. Additionally, some offers do not display the "Select an offer" button, showing only editable properties. (TGT-53321)
* Fixed an issue in the updated [!DNL Target] UI where HTML code changes made during activity setup did not persist on variation pages, even though they saved correctly for control groups. Despite multiple attempts and recreating tests without page groupings, the variation pages consistently failed to retain modifications, impacting content delivery and QA validation. (TGT-53436)
* Fixed an issue in the updated VEC where the "equals any of" operator in page delivery rules fails to accept input values. When configuring customer parameters across all mboxes, selecting this operator resulted in an "Invalid Input" error, preventing rule creation. (TGT-52623)

+++

**Workspaces**

+++See details
* Improved the workflow when copying activities between workspaces. Copy activities between workspaces previously led to sync errors due to missing audiences and unassigned properties. This update introduces a smarter, more intuitive workflow that ensures copied activities are properly configured and ready for publishing. (TGT-47094)
* Fixed an issue where customers were unable to copy activities between workspaces due to a failure in the `copyActivityBatchOperations` mutation. Attempts to duplicate activities resulted in a server error (500) and a null response payload. (TGT-52405)
* Fixed an issue where activities failed to sync when offers referenced in the configuration were not accessible within the selected workspace. This caused publishing errors and left activities in a failed state. (TGT-52535)
* Fixed multiple issues when copying activities between workspaces in the updated [!DNL Target] UI. Customers encountered errors related to audience access, particularly with live activities, and incorrect privilege validation, even when the user had "[!UICONTROL Approver]" roles in both source and destination workspaces. (TGT-53002)
* Fixed an issue in the updated UI where copying activities within the same workspace unnecessarily duplicated associated offers and audiences. (TGT-53457)
* Fixed an issue to address cases where ad-hoc (anonymous) audiences were not correctly copied between non-default workspaces or from non-default to default workspaces. While earlier updates ensured proper duplication for default-to-non-default and same-workspace scenarios, this enhancement focused on preserving combined audience configurations that span multiple workspaces. The fix ensures consistent audience behavior and accurate targeting across all workspace transitions. (TGT-53268)

+++

### [!DNL Target Standard/Premium] 25.7.4 (August 1, 2025)

This release resolves recent issues, primarily caused by complex customer customizations, and includes the following fixes and improvements:

**Activities**

+++See details
* Fixed an issue where a customer encountered an "Invalid user input" error when attempting to save a live activity, even without making changes. The GraphQL response indicates a duplicate LocalId issue. (TGT-53329 & TGT-53373 & TGT-53195)
* Fixed an issue that prevented creating a redirect experience in the updated VEC. The redirect URL was ignored and the original page was shown instead. (TGT-53306)

+++

**Localization**

+++See details
* Fixed a localization issue in the [!UICONTROL Create Criteria] modal, when selecting the "between following values" option in the [!UICONTROL Choose Price Rule] drop-down list, the string "to" was unlocalized in the [!UICONTROL Inclusion Rules] section. (TGT-49754)
* Fixed a localization issue with the string "[!UICONTROL All host groups]" in the [!UICONTROL Environment] drop-down list of the Feeds Creation wizard is not localized correctly. (TGT-46737)

+++

**QA**

+++See details
* Fixed an issue where the QA environment fails to load data across multiple tabs, rendering the interface unusable. (TGT-53377)
* Fixed an issue that prevented creating an activity in the QA environment. The process redirected to the [!UICONTROL Activities] page instead of completing successfully. (TGT-53328)

+++

**Recommendations**

+++See details
* Fixed an issue where hovering over the "deep-learning" operand while creating a collection in [!DNL Recommendations] caused the page to crash. (TGT-53305)
* Fixed an issue where filter suggestions in [!UICONTROL Catalog Search] in the updated UI were inaccurate. (TGT-52007)
* Fixed an issue in the [!DNL Recommendations] UI where the Operands filter appears when using the "value is present" or "value is not present" operators—though it should be hidden. (TGT-53012)

+++

**Visual Experience Composer (VEC)**

+++See details
* Fixed an issue when a user clicks [!UICONTROL Manage Content] and then clicks [!UICONTROL Done] while editing an Automated Personalization (AP) activity, the page goes blank and becomes unresponsive. (TGT-53047 & TGT-52993)
* Fixed an issue where selecting the [!UICONTROL Viewed an mbox] conversion metric under [!UICONTROL Goals & Settings] caused the page to crash. (TGT-53346, TGT-53343, & TGT-53348)
* Fixed an issue where the [!UICONTROL Redirect to URL] feature fails to function as expected—no redirection occurs even with valid URLs. (TGT-53307)

+++

**Workspaces**

+++See details
* Fixed an issue when copying activities between workspaces caused duplicate "Audience Copy" entries and ID conflicts. Audiences are now copied with unique IDs, workspace context, and recursive handling for combined audiences (up to 5 levels). (TGT-53081)
* Fixed an issue when the workspace is set to "[!UICONTROL All Workspaces]," copying an activity that already exists in the default workspace results in an incorrect error:

  "At least one property should be included for non default workspaces."

  Since the copy is within the default workspace, no property should be required. Attempting to add a property and save results in a second error:

  "Invalid User Input"

+++

### [!DNL Target Standard/Premium] 25.7.3 (July 24, 2025)

Due to recent issues identified, primarily related to complex customer customizations, this release includes the following fixes and updates:

**Activities**

+++See details
* Fixed an issue where the `buildViews` method in the builder class incorrectly set `viewMaxLocalId` to the total count of views, rather than to the highest `viewLocalId` assigned. (TGT-53207)
* Fixed an issue in the updated [!DNL Target] UI where deleted offers in [!UICONTROL Automated Personalization] (AP) activities were shown as `Deleted option with ID: X` instead of their original names (for example, `Offer Name [Deleted]` as shown in the legacy UI). This fix restores meaningful labeling for deleted offers, improving clarity and making reporting more accurate and user-friendly. (TGT-52921)
*  Fixed an issue where some activities migrated from the [!DNL Target] frontend to [!DNL Target] Central had inconsistent metric configurations due to a previously fixed sync bug. Specifically, activities that originally used a conversion metric and were later updated to an analytics-based metric retained outdated values in the `primaryMetricType` and `successCriteria` fields. (TGT-52643)
* Fixed an issue where the entire content of a QA preview page became editable due to the unintended inclusion of the `contentEditable` attribute in HTML modifications. This allowed users to click and edit any text on the page, potentially causing layout issues and confusion during QA. (TGT-53247)
* Fixed an issue where moving a modification from [!DNL Page Load] to a [!UICONTROL View] caused the modification to be duplicated, remaining in [!UICONTROL Page Load] while also appearing in the [!UICONTROL View]. Additionally, removing the modification from the [!UICONTROL View] would incorrectly remove it from [!UICONTROL Page Load ]as well. (TGT-53270)

+++

**APIs**

+++See details
* Fixed an issue in the backend persistence layer where deleted options were correctly stored but not accessible via existing API endpoints. As a result, frontend applications couldn't retrieve meaningful names for deleted options, impacting historical reporting views. This fix ensures that preserved deleted option data can now be surfaced properly in the UI. (TGT-52973)
* Implemented a new migration endpoint to support the transfer of deleted activity options from JCR-based activities to [!DNL Target] Central. This functionality enables consistent tracking and reporting across systems. This feature ensures that deleted options are preserved and synchronized across the [!DNL Target] frontend and backend, improving historical reporting and data integrity. (TGT-53217)
* Introduced a new API endpoint that allows users to restore previously deleted activity options from a secondary database. This functionality leverages the existing infrastructure provided by the `RemovedCampaignElements` and `RemovedOptionInfo` classes, ensuring seamless reintegration of deleted options into active activities. (TGT-52903)
* Fixed an issue where [!DNL Recommendations] activities containing metric names longer than 25 characters could not be opened or edited due to API limitations. This fix ensures compatibility with metric names exceeding the character limit, restoring full access to affected activities. (TGT-52839)

+++

**Form-Based Experience Composer**

+++See details
* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] that caused the editor to crash after clicking the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ) when creating or editing an [!UICONTROL Automated Personalization] (AP) activity. (TGT-53047)

+++

**Recommendations**

+++See details
* Fixed an issue that prevented [!UICONTROL Catalog Search] from loading additional results when scrolling to the bottom of the list, restoring behavior consistent with the legacy UI. (TGT-53088)
* Fixed an issue that blocked deleting items from the [!UICONTROL Criteria Details] dialog box. (TGT-53245)
* Fixed an issue that prevented opening or interacting with products that had no name. This issue occurred when selecting environments that returned unnamed results, preventing access to product details. (TGT-53007)
* Fixed an issue that caused the [!UICONTROL Catalog Search] page to crash and display a blank screen when selecting certain products. (TGT-53087)
* Fixed an issue where users were unable to edit the site_cart_z1 [!DNL Recommendation] activity in the [!DNL Target] UI. Attempting to open the activity triggered an error on the [!UICONTROL Overview] page, blocking access to the editor. (TGT-53221)

+++

**Reporting**

+++See details
* Fixed an issue where the sandbox field in the activity database was not cleared when switching the reporting source from [!DNL Customer Journey Analytics] or [!DNL Analytics] to [!DNL Target]. Previously, the UI correctly sent sandbox: null, but the backend ignored this value, leaving outdated sandbox data in place. The backend now properly clears the sandbox field when null is received. (TGT-52798)
* Re-implemented the deleted options persistence layer in the Target backend to support accurate historical reporting in [!UICONTROL Automated Personalization] (AP) activities. Previously, when an option was deleted, its name was lost, making it difficult to interpret past performance data.

  **Key Improvements**:

  * Deleted options are now tracked using the existing `RemovedCampaignElements` and `RemovedOptionInfo` infrastructure.
  * When an option is removed from an AP activity, its metadata (for example, ID and name) is preserved.
  * The reporting UI can now display the original option name (for example, `Option Name [Deleted]`) alongside historical metrics, improving clarity and usability.

  This update ensures consistent and meaningful reporting, even after options are removed from an activity. (TGT-52986)

+++

**Visual Experience Composer (VEC)**

+++See details
* Fixed an issue in the VEC where applying a modification to a view caused duplication and triggered an 'Invalid user input' error. (TGT-52886)
* Fixed an issue with [!UICONTROL Undo] functionality for the [!UICONTROL Insert Before] and [!UICONTROL Insert After] options when configuring image offers in the VEC. 

  Previously, undoing an [!UICONTROL Insert Before] or [!UICONTROL Insert After] action on image offers resulted in inconsistent behavior or failure to properly revert the modification, especially in activities created in the legacy [!DNL Target] UI. This issue has been resolved to ensure undo actions now work reliably for these modifications. (TGT-52809)

* Fixed an issue where the `contentEditable` attribute was unintentionally set to true and persisted in saved HTML content. This update ensures cleaner, expected HTML output without unintended editing behavior. (TGT-52319)
* To prevent permanent loss of deleted options and to ensure consistent behavior across services, soft delete functionality has been implemented for options in the  UI and related microservices.

  **Key Changes**:

  * Options are no longer permanently deleted. Instead, they are marked with a new deleted: true flag in the parameters XML object.
  * This flag is used only by the updated [!DNL Target] UI to exclude deleted options from rendering and to prevent them from being sent to edge services.
  * Deleted options remain part of the activity payload during edits, ensuring traceability while avoiding delivery of non-existent options to customers.

  This update improves data integrity and aligns with best practices for managing deletions in distributed systems. (TGT-52726)

+++

**Workspaces**

+++See details
* Fixed an issue when copying an activity from a non-default to default workspace or between non-default workspaces. Offers are now duplicated with enhanced tracking and naming to prevent conflicts.

  **Key Improvements**:
  * Offers are recreated in the destination workspace with updated IDs and metadata.
  * Copied offers are renamed using the format: "Offer Name Copy" plus a random number or timestamp to ensure uniqueness.
  * The system updates offer and activity states to reflect the new IDs.
  * This functionality prevents errors caused by multiple identical "Offer Copy" names during repeated copy actions.
  * Offers might not immediately appear in the destination workspace's offer list but are processed and surfaced appropriately.

  This update improves reliability and traceability when managing offers across multiple workspaces. (TGT-53080)

+++

### [!DNL Target Standard/Premium] 25.7.2 (July 18, 2025)

Due to recent issues identified, primarily related to complex customer customizations, this release includes the following fixes and updates:

**Activities**

+++See details
* Added an additional confirmation warning when canceling activity edits with unsaved changes: "Do you really want to save this activity? If you don't save, all your changes will be lost." This message helps prevent accidental data loss. (TGT-52865)
* Restored legacy functionality to the [!UICONTROL Priority] slider in [!UICONTROL Goals & Settings], allowing customers to enter a numeric value directly, as supported in the legacy UI. (TGT-53185 & TGT-53219)

+++

**Audiences**

+++See details
* Fixed an issue that prevented saving or editing activities containing custom audiences. Customers encountered the error message "We cannot complete your request. Please contact [!DNL Adobe Client Care] if the problem persists." when attempting to save changes, or even save without changes, to certain activities. (TGT-53189)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details
* Fixed an issue when customers viewed reports for specific activities on the [!UICONTROL Goals & Settings] page, the [!UICONTROL View in Analytics] link incorrectly points to the QA environment instead of the production environment. (TGT-53163)

+++

**[!UICONTROL Experiences] and [!UICONTROL Offers]**

+++See details
* Fixed an issue where invoking `triggerView` via custom code caused an infinite loop. (TGT-52885)
* Fixed an issue causing mismatches between `LocalIds` defined for activities and those `LocalIds` used in experience definitions. (TGT-52669)
* Fixed an issue where metric names were missing on the activity [!UICONTROL Overview] page, displaying only 'Offer' instead of the correct metric name. (TGT-53054)

+++

**Form-Based Experience Composer**

+++See details
* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] that prevented activity saving and triggered the error message: "Cannot read properties of undefined (reading 'map')". (TGT-53145)

+++

**Recommendations**

+++See details
* Fixed an issue where clicking a product from [!UICONTROL Catalog Search] displayed the error 'Failed to retrieve product details' and opened a modal without a close option. (TGT-53082)
* Fixed an issue where [recommendations as offers ](/help/main/c-recommendations/recommendations-as-an-offer.md) in [!UICONTROL A/B Test] activities did not update correctly when changing collections or promotions. (TGT-52884)
* Fixed an issue in the production environment where clicking an entity in the updated UI displayed the error: "Failed to retrieve product details. Please contact [!DNL Adobe Client Care] if this problem persists." (TGT-53071)

+++

**Reports**

+++See details
* Fixed an issue where saving order details to a CSV file resulted in an empty file. (TGT-52225)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* Resolved an issue on the [!UICONTROL Goals & Settings] page where selectors used in multiple experiences were not consistently highlighted as selected. (TGT-53062)
*  Fixed an issue that prevented activity editing and triggered the error message: "Cannot read properties of undefined (reading 'map')". (TGT-53161)

+++

**Workspaces**

+++See details
* Improved handling of ad-hoc offers when switching workspaces.
  * When switching from the default workspace to a non-default workspace (or between non-default workspaces), ad-hoc offers are now copied correctly. During initialization, the workspace context is updated and a new ID is assigned to the offer to ensure uniqueness.
  * No changes occur when staying within the same workspace. (TGT-53079)
* Fixed an issue that prevented customers from [copying activities between different workspaces](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6). (TGT-52753 & TGT-47094)
* Fixed an issue when changing properties between workspaces. 
  * When switching between the default workspace to a non-default workspace, if the current property exists in the destination workspace, the property is preserved. 
  * If the [!UICONTROL Properties] list displays a warning (likely to indicate some properties may not be compatible) and the customer clicks [!UICONTROL Add] or [!UICONTROL Remove] and then clicks [!UICONTROL Save], all properties not in the destination workspace are removed. If the customer clicks [!UICONTROL Cancel], all properties remain, even if they don't exist in the destination workspace. (TGT-47094)
  * If staying in the same workspace or switching from a non-default workspace to the default or another workspace, everything remains as is. (TGT-53078)
* Updated entity validation logic to respect the original workspace context of the activity. Entities such as [!UICONTROL Experience Fragments] (XFs) are now validated based on the workspace in which the activity was originally created. For example, if an XF exists in the default workspace and the activity is copied from workspace X to workspace Y, validation still passes as long as the XF is valid in the original (default) workspace. (TGT-53196)
* Enhanced support for copying ad-hoc audiences during activity duplication.
  * Ad-hoc audiences, including metrics, reporting, page, and activity-only types, are now automatically copied in the following scenarios: 
    * When copying an activity from the default workspace to a non-default workspace.
    * When copying an activity within the same workspace. (TGT-53197)

+++

### [!DNL Target Standard/Premium] 25.7.1 (July 11, 2025)

Due to recent issues identified, primarily related to complex customer customizations, this release includes the following fixes and updates:

**Activities**

+++See details
* Fixed an issue where the [!UICONTROL Activity QA] URL included an unnecessary query parameter: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* Fixed an issue where Preview URLs incorrectly included additional audiences beyond the one explicitly typed by the user. This behavior has been corrected to ensure that only the specified audience is applied when generating a QA or preview link. (TGT-52912)
* Fixed an issue that prevented users from creating [!UICONTROL Auto-Target] (AT) activities if [!UICONTROL Auto-Allocate] (AA) is selected first during traffic allocation setup. This issue resulted in a backend validation error and prevents the activity from being saved. (TGT-53096)

+++

**Audiences**

+++See details
* Fixed an issue where users with the [!UICONTROL Approver] role were unable to add or save activity-only audience refinements. Attempting to do so resulted in a 403 Forbidden error, stating that the "[editor]" privilege was required, even though the user had sufficient permissions to approve and manage activities. (TGT-52984)
* Fixed an issue when an activity-specific audience is removed using the [!UICONTROL Remove Audience Refinement] option, the audience no longer appears in the audience list for re-selection within the same activity. This behavior prevented users from re-adding the same audience unless it is recreated from scratch. (TGT-52979)
* Fixed an issue where activity-only audience refinements disappeared from the UI immediately after being removed from a location, even before the activity was saved. This behavior contradicted the expected functionality and the tooltip guidance, which states: "All unused audiences from this library will be deleted once the activity is saved." (TGT-52982)
* Fixed an issue when attempting to assign an audience other than [!UICONTROL All Visitors] to an activity. Upon saving, the following error message displayed: "We cannot complete your request. Please contact [!UICONTROL Adobe Client Care] if the issue persists." (TGT-53008)
* Fixed an issue that blocked saving an activity after creating and assigning a new audience within the activity editor. The error message displayed was: "We cannot complete your request. Please contact [!UICONTROL Adobe Client Care] if the problem persists." (TGT-52977)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details
* Fixed an issue where copying an existing activity and changing the reporting source to [!DNL Adobe Analytics] (A4T) would result in an "Invalid user input" error. The error was triggered when certain metric actions incompatible with [!DNL Analytics] reporting, such as `restart_same_experience`, `restart_random_experience`, and `restart_new_experience`, were retained from the original activity. (TGT-52900)
* Fixed an issue that blocked customers from creating or saving an activity when selecting [!DNL Adobe Analytics] (A4T) as the reporting source in the [!UICONTROL Goals & Settings] step. The issue occurred specifically when selecting a [!UICONTROL Custom Event] metric (for example, "Custom Event 16"), resulting in the following error: "Invalid User Input." (TGT-52910)
* Fixed an issue where clicking the "[!UICONTROL View in Analytics]" link redirected users to the homepage instead of the intended [!DNL Analytics] dashboard. (TGT-53092 & TGT-53093)
<!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* Fixed an issue when viewing a [!DNL Recommendations] activity in the updated [!UICONTROL Overview] UI, the [!UICONTROL Goals & Settings] section fails to load when [!DNL Adobe Analytics] (A4T) is selected as the reporting source. The following error message was displayed: "Something went wrong. We cannot complete your request. Please contact Adobe Client Care if the problem persists." (TGT-52999)

+++

**[!UICONTROL Experiences] and [!UICONTROL Offers]**

+++See details
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* Fixed an issue where the [!UICONTROL Manage Content] feature did not properly validate the state of a location after all content options were removed. This issue could lead to inconsistent behavior or errors when attempting to save or proceed with the activity configuration. (TGT-52801)
* Fixed an issue where users encountered an "Invalid input" error when adding a new page and deleting specific elements within different experiences. The error is triggered by duplicate `LocalIds` being generated during element manipulation, particularly when switching between experiences and modifying shared page structures. (TGT-52720)
* Fixed an issue where using the [!UICONTROL Generate Adhoc Offer] feature resulted in undefined locations appearing in the [!UICONTROL Manage Content] panel. (TGT-53076 & TGT-53070)
* Clarified the behavior to the customer where modifications made using an HTML Offer might appear to be missing when navigating from the [!UICONTROL Targeting] step back to [!UICONTROL Experiences]. For this customer, the affected website dynamically generated multiple DOM selectors that changed with each page load. As a result, the selector originally used for the modification cannot be found when the editor is reopened, causing the modification to appear missing or invalid. This scenario is working as designed. To ensure that modifications persist visually in the editor, it is recommended that clients use stable, consistent selectors that do not change across page reloads. (TGT-52874)
* Fixed an issue where attempting to delete or deactivate an offer that was part of an excluded experience triggered an "Invalid user input" error. This issue occurred even though the offer was not actively used in the included experiences. (TGT-52917)

+++

**Form-Based Experience Composer**

+++See details
* Fixed an issue in form-based activities where duplicating an experience and editing the custom code in one of the duplicated experiences would unintentionally apply those changes to all duplicated experiences. Each experience now retains its own custom code independently after duplication. (TGT-51600)

+++

**Localization**

+++See details
* Updated localization strings in the new UI for French (fr_FR), German (de_DE), Italian (it_IT), Korean (ko_KO), and Simplified Chinese (zh_CN).

+++

**[!DNL Recommendations]**

+++See details
* Added a new [!DNL Recommendations] feed [status](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (KB-2215)
* Fixed an issue affecting the activity-create workflow when adding [!DNL Recommendations] with [!UICONTROL promotions]. When users selected "[!UICONTROL Promote by Attribute]" and added a filtering rule (for example, [!UICONTROL Parameter Matching]), the selected rule type and operand values were not retained after saving and re-editing the activity. Upon reopening, the filtering rule type would change unexpectedly, and operand values would be missing. (TGT-53059)
* Fixed an issue in the [!DNL Recommendations] UI where any promotion created with a single rule was incorrectly interpreted and displayed as a "List of items" promotion type, regardless of the rule's logic. (TGT-53063)
* Fixed an issue when using the updated [!UICONTROL Overview ]UI, the "[!UICONTROL Download Recommendations Data]" button was missing for [!UICONTROL Experience Targeting] (XT) activities that include [!DNL Recommendations]. (TGT-52730 & TGT-52756)
* Previously, the Recommendations UI displayed only the number of entities successfully imported from a feed. However, the backend message format includes both the number of imported entities and the total number of entities in the format:  `# of entities imported / # of total entities`. Due to this discrepancy, users were only seeing the first value (imported count) in the UI, which led to confusion. The UI now displays both numbers. (TGT-53073)
* Fixed an issue where customers were unable to save a filtering rule when configuring a "[!UICONTROL Promote by attribute]" promotion in a form-based A/B activity with recommendations. After saving and reopening the activity, the filtering rule was missing, and the activity could not be saved successfully. (TGT-53057)

  +++

**Reports**

+++See details
* Fixed an issue where selecting "[!UICONTROL Export order details to CSV]" from the [!UICONTROL Reports] page resulted in an empty file being downloaded. This issue occurred even when valid order data was present in the activity. (TGT-52225)
* Fixed an issue when attempting to save an activity after creating and assigning a new reporting audience. The error message returned was: "Access denied. To perform this operation, all of the following privileges are required: [editor]." This issue occurred despite the user having approver-level access. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* Resolved an issue where applying a modification to a view would result in the view being duplicated and the activity returning an "Invalid user input" error. This fix ensures that view modifications are applied correctly without triggering duplication or validation errors. (TGT-52886)
* Fixed an issue where custom code modifications were incorrectly displayed for the wrong experience. Specifically, changes intended for one experience were shown in a different experience, leading to confusion and potential misconfiguration of live activities. (TGT-52776)
* Fixed an issue that prevented editing or saving custom code modifications in the New VEC UI. Specifically:

  * After editing a custom code block and saving, the changes were not reflected in the UI or in the QA preview.
  * In some cases, modifications could not be deleted unless the activity was closed and reopened.
  * As a workaround, users had to copy the code, delete the modification, and recreate it manually with the updated content. (TGT-53072)

* Fixed an issue where editing and saving custom code caused the [!UICONTROL Modifications] panel to become unresponsive. (TGT-53075)
* Fixed an issue where modifications made to custom code in variant experiences were unintentionally reflected in the [!UICONTROL Control] experience. This caused unintended changes in delivery behavior. The [!UICONTROL Control] experience now remains isolated from custom code edits made to other experiences. (TGT-52413)
* Fixed an issue where modifications made to one experience (for example, Experience B) were unintentionally duplicated to another experience (Experience A) if the user clicked on the second experience before the editor fully loaded. This behavior could also result in modifications being lost if the initially selected experience had no changes. (TGT-52597)
* Fixed an issue where changes made in the [!UICONTROL Modifications] step of activity creation were not consistently saved. In some cases, after completing all steps and clicking [!UICONTROL Save], the custom script added in the [!UICONTROL Modifications] section would not reflect on the live site, despite no visible errors during the save process. (TGT-52661)
* Fixed an issue where custom code changes were not saving correctly and were unintentionally mirrored across multiple experiences within the same activity. Additionally, users encountered access issues when opening or refreshing certain activities, resulting in blank screens. These issues have now been resolved to ensure stable activity editing and accurate experience isolation. (TGT-52594)
* Fixed an issue where users were unable to browse to a different URL while in [!UICONTROL Browse Mode]. This prevented testers and editors from validating or previewing alternate pages within the same activity session. (TGT-53052)
* Fixed an issue where multiple [!UICONTROL Visual Experience Composer] (VEC) instances opened simultaneously during activity creation. This issue occurred when users disabled the [!UICONTROL Enhanced Experience Composer] (EEC) and removed the trailing slash from the website URL in the [!UICONTROL Page Delivery] step. (TGT-52782)
* Fixed an issue where the [!UICONTROL Revenue] metric dropdown in the [!UICONTROL Goals & Settings] step would incorrectly default to [!UICONTROL Revenue per Visit] (RPVISIT), even after the user selected a different metric.  The issue occurred when collapsing and re-expanding the metric configuration panel, causing the previously selected value to reset. (TGT-52811 & TGT-52878)
* Fixed several issues in the activity-create workflow related to offer naming and content translation in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Multivariate Testing] (MVT) activities:

  Key Issues Addressed:

  * Creating multiple HTML Offers with the same name (for example, "Experience") triggered a "Duplicate offer names are not allowed" error, but the UI did not clearly indicate which offers were causing the conflict.
  * Renaming offers via the right panel updated the name in the UI, but the change was not reflected in the [!UICONTROL Manage Content] tab or the [!UICONTROL Offers] tab, causing persistent validation errors.
  * In MVT activities, although the duplicate name error did not persist after renaming, the UI still failed to reflect updated offer names consistently across tabs. (TGT-52933)

  +++

### [!DNL Target Standard/Premium] 25.6.4 (June 27, 2025)

This release includes the following fixes and updates:

* Added the [!UICONTROL Rearrange] option to the updated [!UICONTROL Visual Experience Composer] (VEC) UI to align with functionality available in the legacy VEC. (TGT-46957 & TGT-52876)
* Fixed an issue where modifications made to variant experiences (for example, Experience B) in an [!UICONTROL A/B Test] activity were not being retained. After switching between experiences, the changes to the variant would disappear. This issue did not affect the Control experience. (TGT-52664)
* Fixed an issue where certain customers were unable to create or save activities, while others could perform the same actions without issue. The problem was inconsistent across accounts.(TGT-52842)
* Fixed an issue where in the updated VEC, users were unable to move modifications to the [!UICONTROL Page Load event], a capability that existed in the legacy UI. (TGT-52617)
* Fixed an issue in the updated UI where [!UICONTROL page load] events were not visible in [!DNL Target] when creating changes; updates only applied to views. (TGT-52604)
* Fixed an issue that prevented some activity modifications from displaying properly in the updated VEC. (TGT-52818)
* Fixed a null pointer exception that occurred when fetching reporting data for [!UICONTROL Automated Personalization] (AP) activities. (TGT-52362)
* Fixed an issue that prevented offer-level details from appearing in the .CSV file for [!UICONTROL Automated Personalization] (AP) activities. (TGT-52675)
* Fixed an issue when applying modifications in the updated VEC, changes initially appear correctly, including the expected [!UICONTROL Experience Fragment]. However, upon switching experiences or making additional edits, some modifications fail to apply due to selector issues. (TGT-52679)
* Fixed an issue where when a new activity was created by cloning an existing one, the QA links in the cloned activity incorrectly retained the page URLs from the original activity. (TGT-52775)
* Fixed an issue that unintentionally prevented [!UICONTROL On-device Decisioning] from being available in the updated VEC. (TGT-52371)
* Fixed an issue that prevented editing a product [!DNL Recommendations] activity. When attempting to access the VEC via the Target UI, an error appeared on the [!UICONTROL Overview] page, preventing any edits. (TGT-52823)
* Fixed an issue that prevented saving a [!DNL Recommendations] activity when experience names exceeded 50 characters. (TGT-52619)
* Fixed an issue where customers were unable to save a Recommendations activity after modifying the criteria in the new UI. The issue appears to be permission-related and does not affect all users with similar roles. (TGT-52816)
* Fixed an issue where users with the [!UICONTROL Editor] role were unable to edit a [!DNL Recommendations] activity. Attempting to change the design and save the activity resulted in a 403 Forbidden error, stating that the "[editor]" privilege was required, even though the user already had that role in the relevant workspace. (TGT-52836)

### [!DNL Target Standard/Premium] 25.6.3 (June 20, 2025)

This release includes the following fixes and updates:

* Fixed an issue where copying an activity from one workspace to another workspace triggered errors such as "must not be null" or "Something went wrong." (TGT-52474)
* Fixed an issue where [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes] reports were not generated for certain activities. (TGT-52904)
* Fixed an issue in the updated VEC where default content handling in [!UICONTROL Automated Personalization] (AP) activities did not match the legacy UI. The system now automatically adds a default `optionGroup` named "Default Content" with `optionGroupLocalId = 0` when no group is explicitly added. This group includes the default option (for example, `optionLocalId: 0`). If the default content is removed, the corresponding option group is also removed. (TGT-52651)
* Fixed an issue in [!UICONTROL Multivariate Test] (MVT) activities where reusing an `experienceLocalId` from previously removed experiences was incorrectly disallowed. (TGT-52672)
* Fixed an issue that prevented copying or editing activities containing an experience fragment. This triggered the error: `Enum "AemOfferType" cannot represent value: "html"`. (TGT-52635)
* Fixed an issue where URLs in activity locations failed to display query parameters due to invalid characters, such as slashes (/). (TNT52845)
* Improved the validation error message for [!DNL A/B Test] activity updates via the backend API. When duplicate location names are present, the message now clearly states: "Duplicate names are not allowed" for `locations.selectors`. (TGT-52589)
* Fixed an error that occurred when updating a live [!UICONTROL Recommendations] activity due to an unrecognized property in the request payload. The system now properly handles the "Invalid JSON. Unrecognized property name" error. (TGT-52723)
* Fixed an issue that prevented creating a [!DNL Recommendations] design. Clicking [!UICONTROL Create] triggered the message: "There should be at least 1 entity variable used inside the script." (TGT-52395 & TGT-52899)
* Fixed an issue where re-saving a [!DNL Recommendations] design without modifications was blocked. (TGT-52879)
* Fixed a backend validation error that caused a "400 Bad Request" error when saving a [!UICONTROL Recommendations] activity. (TGT-52716)
* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] where hovering over an mbox with special characters in the [!UICONTROL Location] drop-down caused the editor to go blank and triggered a "Failed to execute 'querySelector' on 'Element'." error. (TGT-52717)
* Improved feed-status accuracy with a new "PARTIALLY_IMPORTED" indicator. Previously, feeds were marked as "success" even when not all rows in a file were imported, which was misleading. (TGT-52892)
* Fixed an error where, after migrating to AP V2, certain API calls to `/admin/rest/ui/v1/campaigns` returned client-side errors (HTTP 4xx). (TGT-52721)

### [!DNL Target Standard/Premium] 25.6.2 (June 12, 2025)

This release includes the following fixes and updates:

* Added a [new FAQ article](/help/main/c-intro/updated-ui-faq.md) to address common questions about the updated [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC).
* Fixed an issue where the "[!UICONTROL URL - does not contain]" rule in [!UICONTROL Page Delivery] was not working, allowing content to be shown even when it should have been blocked. (TGT-52754)
* Fixed an issue where [!UICONTROL Page Delivery] incorrectly displayed the error message: "Duplicate page URLs are not allowed. (TGT-52765)
* Fixed an issue where audiences for [!UICONTROL Page Delivery] URLs containing experience fragments were created with # erroneously appended. (TGT-52786)
* Fixed an issue where copying an activity and editing settings on the [!UICONTROL Goals and Settings] page caused the [!DNL Target] UI to become unresponsive. (TGT-52797)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) that incorrectly allowed redirecting an additional page in an [!UICONTROL A/B Test] activity to the same URL. (TGT-51838)
* Fixed an issue where changes to metrics on the [!UICONTROL Goals and Settings] page were not saved when editing an activity. (TGT-52799)
* Fixed an issue where adding a new experience while the web editor was still loading caused the new experience to duplicate content from the previous experience. (TGT-51397)
* Restored the ability to use custom code outside the `<head>` tag, a feature previously available in the legacy Target UI. (TGT-52304 & TGT-52300)
* Removed unnecessary validation when selecting the default workspace during activity creation. Mandatory property validation no longer applies to the default workspace, but remains in place for non-default workspaces. (TGT-52449)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) where `triggerView()` calls were not being detected. (TGT-52575)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) that prevented users from adding modifications to [!UICONTROL Single Page Application] (SPA) views. (TGT-52556)
* Fixed an issue in the updated [!DNL Target] UI that prevented customers from viewing offer details. (TGT-52607)
* Fixed an issue where updates made to offers in the [!UICONTROL Offers Library] were not reflected in the updated [!UICONTROL Visual Experience Composer] (VEC). (TGT-52637)
* Fixed an issue that prevented the Offers section from displaying properly while creating an activity. (TGT-52773)
* Added validation to ensure that all `optionLocalIds` referenced in `optionGroups` exist in the options array. Invalid references are automatically removed during activity creation. (TGT-52687)
* Fixed an issue where reporting groups and exclusions were not retained after adding a new offer. (TGT-52728)
* Fixed an issue where activities without an [!UICONTROL Activity QA] button displayed an empty option selector. (TGT-52733)
* Fixed an issue where QA links failed to render content properly. (TGT-52718)
* Fixed an issue where replacing an element with an experience fragment did not reflect changes correctly in the QA environment. (TGT-52762)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) that caused an "Invalid Input" error when users attempted to add experience fragments. (TGT-52701)
* Fixed an issue where the "Edit Audience" modal appeared empty when editing audience targeting in the updated [!UICONTROL Visual Experience Composer] (VEC). (TGT-52749)
* Added a message to inform users when an entity is not accessible in the selected workspace. (TGT-52767)
* Fixed an issue where the UI failed to allow manual assignment of an environment ID to a criteria. Instead, it defaulted to the ID for the [!UICONTROL Product Catalog Search] host group. This fix ensures that criteria changes are now applied across all environments, not just the default. (TGT-52817)
* Fixed an issue where the "[!UICONTROL Download Recommendations data]" option was missing for [!UICONTROL Experience Targeting] (XT) activities with recommendations. (TGT-52730 & TGT-52756)

### [!DNL Target Standard/Premium] 25.6.1 (June 6, 2025)

This release includes the following fixes and updates:

* Fixed an issue where QA links did not deliver the correct experience for the associated activity. (TGT-52163 & TGT-52790)
* Fixed an issue where QA links were missing the associated audience ID. (TGT-52722)
* Fixed an issue to ensure that experiences are delivered only when their configured Page Delivery URL conditions are accurately met. (TGT-52696)
* Fixed an issue that prevented customers from creating a [!DNL Recommendations] design template. Attempting to create a template triggered the error: "There should be at least 1 entity variable used inside the script." (TGT-52395)
* Fixed an issue that prevented saving [!DNL Recommendations] designs using Velocity arrays. The error message "There should be at least 1 entity variable used inside the script" was incorrectly triggered. (TGT-52734)
* Fixed an issue where modifications were inaccessible in the [!UICONTROL Visual Experience Composer] (VEC) when the page failed to load for internal web pages. (TGT-52488 &TGT-52470)
* Fixed an issue where the [!UICONTROL Modifications] panel was not visible on smaller screen sizes in the VEC. (TGT-52470)
* Fixed an issue in the updated VEC where switching from [!UICONTROL Browse] mode back to [!UICONTROL Design] mode caused a console error and prevented further interaction. (TGT-52532)
* Fixed an issue in the VEC where clicking certain elements unintentionally expanded their size. (TGT-52497)
* Fixed an issue where certain page elements failed to load or be recognized in the VEC, preventing interactions such as selecting buttons or banners and disrupting accurate event tracking in activities. (TGT-52663)
* Fixed an issue that prevented customers from deleting or removing offers in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52690)
* Fixed an issue that caused inconsistent activity qualification behavior in multi-page activities. (TGT-52694)
* Fixed an issue that caused the activity's [!UICONTROL Overview] page to show an invalid URL for the [!UICONTROL Activity Location]. (TGT-52695)
* Fixed an issue in the updated [!DNL Target] UI that caused duplicate entries to appear for activity locations. (TGT-52693)
* Fixed an issue that triggered a `getAudiencesV3` error, preventing customers from editing or copying activities. (TGT-52709)
* Fixed an issue that caused an invalid payload error when adding [!UICONTROL Experience Fragments] or HTML offers to an activity. (TGT-52779 & TGT-52773)
* Fixed an issue in the updated [!DNL Target] UI where E[!UICONTROL xperience Fragments] failed to display correctly due to an invalid input error. (TGT-52701)
* Fixed an issue that prevented customers from editing activities in the [!UICONTROL Form-based Experience Composer] due to an invalid user error. (TGT-52470)
* Fixed a localization issue in the Korean language where previous translations used characters outside the Basic Multilingual Plane. The updated translation uses appropriate characters that accurately convey the intended meaning. (TGT-52508 & TGT-52509)
* Fixed a localization issue in the Korean language where the translation for "date" was inconsistent when selecting start and end dates for an activity. (TGT-52510)

### [!DNL Target Standard/Premium] 25.5.4 (May 29, 2025)

This release includes the following fixes and updates:

* Fixed an issue that prevented adding or editing URLs in QA mode. (TGT-51941)
* Added a QA Mode Traffic setting under [!UICONTROL Reports] > [!UICONTROL Report Settings] ( ![Report Settings icon](/help/main/assets/icons/Setting.svg) ) to align with functionality from the legacy [!DNL Target] UI. (TGT-52228 & TGT-52329)
* Fixed an issue where the Form-based activity generated incorrect QA links. The activity URL/location included an unintended "1" at the end, which has now been removed to ensure accurate linking. (TGT-52355 & TGT-52358)
* Fixed an issue where the Form-based activity generated incorrect QA links. The activity URL included an unintended `http://pid-ppc` at the beginning of the URL, which has now been removed to ensure accurate linking. (TGT-52557)
* Fixed an issue where [!DNL Target] generated invalid QA links for Form-based activities. (TGT-52528 & TGT-52603)
* Fixed an issue where saving a modified activity appeared to process but never completed, and no error message was shown in [!DNL Target]. (TGT-52461)
* Fixed an issue where the updated [!UICONTROL Visual Experience Composer] (VEC) failed to auto-detect the `at_property` value. (TGT-52347)
* Fixed an issue that caused two modifications being recorded when only one is expected after switching between [!UICONTROL Browse] and [!UICONTROL Design] modes in the VEC while interacting with a form element. (TGT-52455)
* Fixed an issue that prevented selecting the [!UICONTROL Clicked an Element] setting in the updated VEC due to an error stating that  the selector was invalid, already used, or not visible. (TGT-52467)
* Fixed an issue where adding a [!UICONTROL Recommendation Offer] box in the updated VEC caused duplicate (ghost) boxes to display. Switching between Experience A and B repeatedly added more ghost boxes. (TGT-52505 & TGT-52519)
* Fixed an issue in the updated [!DNL Target] UI where changes to an HTML Offer made via the [!UICONTROL Offer] menu were not reflected in the associated activity, and vice versa. This behavior now matches the legacy UI, where updates sync correctly between the [!UICONTROL Offer] menu and the activity. (TGT-52540 & TGT-52541)
* Fixed an issue where recent updates to [!UICONTROL Experience Fragments] in the [!UICONTROL Offers Library] were not reflected when attempting to use them within an activity. (TGT-52659)
* Fixed a localization issue in the Simplified Chinese translation of a confirmation message. The previous version lacked quotation marks around the location name and used informal language, contrary to the customer's style guide. The updated translation now uses proper punctuation and a formal tone. (TGT-52364) 

### [!DNL Target Standard/Premium] 25.5.3 (May 22, 2025)

This release includes the following fixes and updates:

* Fixed an issue where the search-by-name feature in the [!UICONTROL Activities] list did not work correctly with multi-word queries. (TGT-52529)
* Fixed an issue that prevented excluding experiences from [!UICONTROL Automated Personalization] (AP) activities. (TGT-52383)
* Fixed an issue where the "[!UICONTROL Contains]" option was missing from [!UICONTROL Filter Rules] when managing content in AP activities. (TGT-52384)
* Fixed a reporting inconsistency in [!UICONTROL Automated Personalization] (AP) activities, specifically related to how default offers are tracked and reported using `optionLocalId` values from [!DNL Target]'s internal system.
* Fixed an issue where QA links failed to deliver the intended activity experience. (TGT-52163)
* Fixed an issue where users with [!UICONTROL Approver] permissions were incorrectly blocked from editing live activities, receiving an "Access denied" error message. (TGT-52416)
* Fixed an issue where audience refinements failed to display for certain activities in the updated [!DNL Target] UI. (TGT-52057)
* Fixed an issue that caused audience refinements and activity audiences to be reversed in the updated UI. (TGT-52158)
* Fixed an issue where generating ad-hoc offers resulted in duplicate offers. (TGT-51938)
* Fixed an issue that blocked offer updates and incorrectly displayed an "Invalid user" error. (TGT-52361)
* Fixed an issue that prevented saving existing activities, triggering an "Invalid User Input" error. (TGT-52422)
* Fixed an issue that blocked editing existing HTML offers, triggering an "Invalid User Input" error on save, even when no code changes were made. (TGT-52351)
* Fixed an issue that prevented [!DNL Target] from recognizing the "#" character in a website's URL. (TGT-52093)
* Fixed an issue that prevented editing [!DNL Recommendations] activities to add or update promotions, which caused save failures and duplicate promotions. (TGT-52343)
* Fixed an issue that prevented changes to criteria or designs in [!DNL Recommendations] activities, resulting in an "invalid JSON: unrecognized property name" error. (TGT-52375)
* Fixed an issue where sequence criteria failed to display correctly in the [!UICONTROL Visual Experience Composer] (VEC) for [!DNL Recommendations] activities. (TGT-52435)
* Fixed an issue where views were not correctly identified on SPA pages when using the [!DNL Adobe Experience Platform Web SDK]. (TGT-52106)
* Fixed an issue where On-Device Decisioning (ODS) details were not saved correctly, despite being included in the batch operation payload. (TGT-52406)
* Added an `audienceMetadata` field to activities, enabling it to be read and updated during editing. (TGT-51004)
* Added an error message to alert users when an audience timeframe is invalid. (TGT52522)
* Updated the activity structure to support duplicate audiences of different types. (TGT-51200)

### [!DNL Adobe Target] [!DNL AI Assistant] release (May 16, 2025)

We are thrilled to announce the launch of the [!DNL AI Assistant] in [!DNL Adobe Target]! This powerful user interface feature is designed to help you navigate and understand [!DNL Target] concepts with ease. Available across multiple products in [!DNL Adobe Experience Cloud], including [!DNL Target], [!DNL AI Assistant] is here to revolutionize your experience.

[!DNL AI Assistant] in [!UICONTROL Target] is a conversational tool that you can use to accelerate your workflows with [!DNL Experience Platform] applications and services. Use [!DNL AI Assistant] to boost your overall productivity and amplify your understanding of product knowledge

In [!DNL Target], the first phase of [!DNL AI Assistant] provides invaluable product knowledge grounded in [!DNL Experience League] documentation. Whether you're setting up a profile script, troubleshooting errors, or considering an upgrade to the AEP Web SDK, [!DNL AI Assistant] has you covered.

For more information, see [Adobe Experience Platform AI Assistant overview](/help/main/c-intro/ai-assistant.md).

### [!DNL Target Standard/Premium] 25.5.2 (May 8, 2025)

This release includes the following fixes and updates:

* [!DNL Target] users with [!UICONTROL Product Administrator] and [!UICONTROL System Administrator] rights can now edit all settings on the [!UICONTROL Administration] pages, regardless of their role in [!DNL Target]. Users without these permissions have read-only access to these settings. This update ensures stricter access control over [Administration settings](/help/main/administrating-target/administrating-target.md). (TGT-48179)
* Fixed a caching issue that prevented saving activity [Site Preferences](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings). (TGT-52213) 
* Fixed an issue where customers couldn't enable selection by ID and class in the [!UICONTROL Site Preferences] section after loading the site in the VEC. The [!UICONTROL Site Preferences] setting automatically reverted to disabled even after being enabled. (TGT-52207)
* Fixed an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to display the correct page when [page delivery](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) URLs ended with a forward slash (/). (TGT-52237)
* Fixed an issue that prevented the removal of custom code modifications when changing experiences. (TGT-52240)
* Fixed an issue where HTML modifications in the VEC overlaid existing page elements. (TGT-52265)
* Fixed an issue that prevented editing custom code in the updated VEC due to the existing custom code not being visible in the editor. (TGT-52272)
* Fixed an issue that caused a "Duplicate names are not allowed" error message when saving a Recommendations activity. (TGT-52318)
* Fixed an issue in the updated VEC that prevented customers from editing text elements or removing container objects. (TGT-52348)
* Fixed an issue that blocked [!DNL Customer Journey Analytics] from displaying correctly on an activity [!UICONTROL Overview] page. (TGT-52359)
* Fixed an issue that prevented reporting groups from persisting in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52368)
* Fixed an issue that prevented saving activities that include offer decisioning. (TGT-52390)
* Fixed an issue where the default offer was selected, but other offer content displayed in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Multivariate Test] (MVT) activities. (TGT-52372)
* Fixed GET permissions logic to check with OR between full org access and specific org + user access. (TGT-52374)
* Fixed an issue where audience names did not display after selecting an audience for [!UICONTROL Managed Content] and [!UICONTROL Reporting Audiences], even though [!UICONTROL Show Only Selected] was enabled. (TGT-52393)

### [!DNL Target Standard/Premium] 25.5.1 (May 5, 2025)

This release includes the following fixes and updates:

* Fixed an issue preventing audience refinements from displaying for certain activities in the updated UI. (TGT-52057)
* Fixed an issue that prevented the use of combined audiences in activities. (TGT-52346)
* Fixed an issue that prevented the creation of a new activity in a non-default workspace using an activity-only audience from the same workspace. (TGE-52349)
* Fixed an issue that caused activity-only audiences to disappear from the updated UI after creating and selecting a new audience. (TGT=52091)
* Fixed an issue that prevented the use of duplicate audiences in activities. (TGT-51200 & TGT-52057)
* Fixed an issue that caused audience refinements and activity audiences to be reversed in the updated UI. (TGT-52158)
* Fixed an issue that prevented the creation of a new activity due to the user input error: "non-default workspace not allowed for this user." (TGT-52267)
* Fixed an issue that prevented offers from displaying in the updated UI for both default and non-default workspaces. [!DNL Target] now displays offers from both workspaces. (TGT-52339)
* Fixed an issue where [!DNL Target] did not warn customers when editing an activity and changing a modified website element. (TGT-52100)
* Fixed an issue where editing an offer with ad-hoc offers created a new offer instead of updating the existing one. (TGT-52135)
* Fixed Fixed an issue that caused an invalid payload error when moving offers to folders. (TGT-52325)
* Fixed Fixed an issue that caused an user input error when moving offers to folders. (TGT-52296)
* Added an `audienceMetadata` field for each activity, and ensured it is read and updated when editing the activity. (TGT-51004)

### [!DNL Target Standard/Premium] 25.4.5 (April 25, 2025)

This release includes the following fixes and updates:

* Fixed an issue that caused discrepancies in audience listings between the [!UICONTROL Activity] settings page and the [!UICONTROL Reporting] overview page. (TGT-52203)
* Fixed an issue that prevented adding a new page to an activity due to an invalid user input error. (TGT-52263)
* Fixed an issue that caused `OptionLocalIDs` to incorrectly increment when the option remains unchanged. (TGT-52187)
* Fixed an issue that caused `location` and `OptionLocalIDs` to incorrectly increment when the option remains unchanged. (TGT-52188)
* Fixed an issue that caused the location on the activity's [!UICONTROL Overview] page to be incorrect. (TGT-52182)
* Fixed an issue where an invalid selector warning was not displayed for an invalid location. (TGT-52110)
* Fixed an issue so that downloaded reporting files correctly show data present in the reporting UI. (TGT-52068)
* Fixed an issue so that batch operations do not fail after adding page-delivery rules. (TGT-52097)
* Fixed an issue that caused [!DNL Target] to trim all query parameters from the website's URL. (TGT-52100)
* Resolved a console error that prevented customers from creating activities in both the legacy and updated [!DNL Target] UI. (TGT-52181)
* Fixed an issue that blocked customers from adding new pages, causing an invalid user input error. (TGT-52258)
* Fixed an issue that caused modifications to disappear after adding additional pages then navigating back to the [!UICONTROL Experiences] tab. (TGT-52264)
* Fixed an issue that blocked customers from changing the audience in an [!UICONTROL Experience Targeting] (XT) activity. (TGT-52191)
* Fixed an error that prevented editing of an XT activity due to an unsupported UI rule. (TGT-52273)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) where breadcrumbs were not always displayed at the bottom of the editor, causing difficulties in precisely selecting elements. (TGT-52169)
* Fixed an issue where the [!UICONTROL Audience] drop-down list failed to display all audiences due to pagination. (TGT-52204)
* Fixed an issue that caused an invalid user input message when adding new offers in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52210)
* Fixed an issue where [!UICONTROL Analytics for Target] (A4T) was incorrectly selected as the reporting source, even though the customer did not have access to A4T. (TGT-52226)
* Fixed an issue that prevented saving an activity with the [!UICONTROL View a Page] URL metric. (TGT-52260)
* Fixed an issue that blocked customers from selecting workspaces while creating offers within an activity. (TGT-52289)
* Fixed an issue that blocked customers from creating activities across all workspaces. (Tgt-52218)
* Fixed an issue where modifications from one experience were incorrectly displayed when switching to another experience. (TGT-52184)
* Fixed an issue where the default offer was incorrectly displayed in the [!DNL Target] UI when opening the activity. (TGT-52198)

### Target permissions update (April 22, 2025)

This future update enhances organizational control over [!DNL Target] instance configurations, preventing accidental updates that could affect activity delivery across various testing and personalization teams.

Effective April 22, 2025, only [!UICONTROL Product] and [!UICONTROL Solutions] admins will be able to update settings in the [!UICONTROL Administration] sections, regardless of their roles in [!DNL Target] workspaces. Users without this permission will have read-only access to the [!UICONTROL Administration] sections.

For more information, see [Administer Target](/help/main/administrating-target/start-target.md).

### [!DNL Target Standard/Premium] 25.4.4 (April 17, 2025)

This release includes the following fixes and updates:

* Added an error message to guide users on resolving duplicate options in an activity. (TGT-51927)
* Fixed an issue where `ClickTrack` selectors were not removed when deleting pages or experiences with redirect offers. (TGT-51952)
* Fixed an issue caused by allowing empty `ClickTrack` selectors. [!DNL Target] now requires that the selector field must not be blank. (TGT-52107)
* Fixed an issue that incorrectly allowed metrics with duplicate names. Metrics now require unique names. (TGT-52201)
* Fixed an issue where audience definitions were not visible when editing offer-level targeting in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52148)
* Fixed an issue that prevented customers with [!UICONTROL Editor] rights from saving activities. (TGT-52227)
* `OptionLocalIDs` no longer increment incorrectly when the option remains unchanged. (TGT-52139)
* Fixed an issue that caused an "Invalid `optionLocalIds`" message when trying to create an activity. (TGT-52154)
* Discrepancies between `OptionLocalIDs` defined for an activity and those used to define experiences have been fixed. (TGT-52215)
* Fixed an issue that caused a validation failure that occurred when trying to create an A/B activity. (TGT-51923)

### [!DNL Target Standard/Premium] 25.4.3 (April 11, 2025)

This release includes the following fixes and updates:

* Fixed an error that prevented customers from opening the audience information pop-up for certain [!UICONTROL Experience Targeting] (XT) activities. (TGT-52049)
* Fixed an issue where the audience setting reverted to "[!UICONTROL All Visitors]" following changes made in the [!UICONTROL Visual Experience Composer] (VEC). (TGT-52132)
* Fixed an issue where audience refinements were not displayed for specific activities (TGT-52057) 
* Fixed an issue that prevented customers from inserting an [!UICONTROL Experience Fragment] in the default workspace. (TGT-52073)
* Fixed an issue where an offer showed as "Content not found" and did not display on the [!UICONTROL Offers] page for an [!UICONTROL Automated Personalization] (AP) activity. (TGT-52150)
* Added the ability to allow duplicate audiences within an activity. (TGT-51200)
* Fixed an issue where the wrong mbox name displayed on the [!UICONTROL Goals & Settings] page for an XT activity after editing. (TGT-52026)
* Fixed an issue where `defaultContent` displayed in options despite not being in `experiences/optionLocations`. (TGT-52036)
* Fixed an issue to ensure that empty strings are not converted to null values. (TGT-52037)
* Fixed an issue requiring customers to reconfigure the [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] on the [!UICONTROL Goals & Settings] page after edits. (TGT-52071)
* Fixed an issue where an activity with no page-delivery rules displayed multiple rules on the [!UICONTROL Overview] page. (TGT-52084)
* Added an error message for users attempting to save an offer with characters outside the basic multilingual plane, such as emojis. (TGT-52105)
* Fixed an issue where opening an activity triggered the error message: "This Activity is using one or more audiences deleted at source." (TGT-52120)
* Fixed an issue where ClickTrack metrics were not displayed in the updated [!UICONTROL Visual Experience Composer] (VEC) during editing. (TGT-52152)
* Fixed an issue where a URL with a query parameter as the activity location did not display the query parameter on the activity's [!UICONTROL Overview] page. (TGT-51635)
* Fixed an issue that prevented the entire experience URL from displaying in [!UICONTROL Browse mode] within the [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* Fixed an issue where editing an activity caused page delivery to add a "/" to the end of the URL, rendering it invalid. (TGT-52114)
* Fixed an issue where the [!UICONTROL Activity QA] link in the [!UICONTROL Form-Based Experience Composer] incorrectly redirected to the [!DNL Adobe Experience Cloud] homepage. (TGT-52055)
* Fixed an issue where additional pages added to the [!UICONTROL A/B Test] activity were not retained after saving and reopening. (TGT-51994)
* Fixed an issue that prevented customers from deleting styles in the inline style section. (TGT-52070)
* Restored access to [audience definition cards](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) in the [!UICONTROL Activity QA] dialog box, similar to the legacy UI. (TGT-52056)
* The updated UI did not save pages or audiences without modifications. If customers added new pages or audiences to an activity but make no changes to them, [!DNL Target] discarded the unmodified audiences upon saving. Notifications have added in relevant places to inform users of this behavior. (TGT-52104)

### [!DNL Target Standard/Premium] 25.4.1 (April 2, 2025)

This release includes the following fixes and updates:

* Fixed an issue that caused experience audiences to disappear from activities. (TGT-52003)
* Fixed an issue that caused unexpected elements during delivery. (TGT-52011)
* Fixed an issue that blocked customers from viewing the audience in the targeting graph on the Ove[!UICONTROL r]view page and during activity editing. (TGT-52050)
* Fixed an issue that prevented customers from reordering experiences in order of priority in [!UICONTROL Experience Targeting] (XT) activities. (TGT-52054)
* Fixed an issue that caused incorrect rendering when undoing text style changes. (TGT-51876)
* Fixed an issue that when modifying a redirect offer, [!DNL Target] also removes any [!UICONTROL ClickTrack] selectors associated with that offer. (TGT-51936)
* Fixed an issue that caused [!DNL Target] to incorrectly save the selector when cancelling [!UICONTROL ClickTrack]. (TGT-51937)
* Fixed an issue that triggered an invalid name error after opening and closing the mbox picker on the [!UICONTROL Goals & Settings] page without making any changes. (TGT-51983)
* Fixed an issue that blocked editing ad hoc offers created in the legacy [!DNL Target] UI. (TGT-51984)
* Fixed an issue that blocked editing activities that have ad-hoc offers that contain custom code. (TGT-51995)
* Fixed an issue that caused exclusion rules to display as inclusion rules when editing combined audience definitions. (TGT-51999)
* Fixed an issue that prevented custom code from displaying correctly during experience editing. (TGT-52005)
* Fixed an issue that made the [!UICONTROL Insert Before] option unavailable for inserting content before the navigation bar. (TGT-52031)
* Fixed an issue that prevented correct highlighting of the default experience in reporting. (TGT-51716)
* Fixed an issue that triggered a `default message [Invalid optionLocalIds: xx]]` message when creating an activity. (TGT-52038)

### at.js version version 2.11.8 (March 31, 2025)

* Resolved CodeQL-identified vulnerability in string suffix validation to prevent edge cases during resize and move operations. (TNT-51516)

### [!DNL Target Standard/Premium] 25.3.8 (March 28, 2025)

This release includes the following fixes and updates:

* Resolved an issue that caused the [!UICONTROL Activities] page to load slowly. (TGT-51151)

### [!DNL Target Standard/Premium] 25.3.7 (March 26, 2025)

This release includes the following fixes and updates:

* Resolved an issue that blocked saving multi-page activities if a page was deleted after modifications. (TGT-51988)
* Resolved an error that occurred when editing an activity: `default message [Invalid optionLocalIds: xx]]`. (TGT-51985)
* Resolved an issue where adding new modifications to an activity removed existing modifications. (TGT-51981)
* Resolved an issue where replacing an audience with "[!UICONTROL All visitors]" during activity creation or editing caused a "Duplicate audiences are not permitted" error. (TGT-51978)
* Resolved an issue that caused an "Invalid user input" error when saving an [!UICONTROL A/B Test] activity. (TGT-51976)
* Resolved an issue that prevented calculated metrics from displaying correctly on the [!UICONTROL Goals & Settings] page. (TGT-51975)
* Resolved an issue that prevented matching `companyName` and `reportSuite` in the [!DNL Analytics] configuration for the `pageviews` metric. (TGT-51965)
* Resolved an issue where switching experiences in an activity removed modifications. (TGT-51945)
* Resolved an issue where removing a page audience also removed [!UICONTROL ClickTrack] selectors. (TGT-51935)
* Resolved an issue that made an activity uneditable after opening its [!UICONTROL Overview] page. (TGT-51931)
* Resolved an issue that caused an `[Unused optionLocalIds: 0]]` error during activity creation. (TGT-51920)
* Resolved an issue where some changes were not translated correctly after removing text style changes. (TGT-51876)
* Resolved an issue that prevented targeted audiences from updating correctly in the [!UICONTROL Form-Based Experience Composer]. (TGT-51845)
* Resolved an issue where the URL in the [!UICONTROL Visual Experience Composer] did not update correctly during activity navigation. (TGT-51832)
* Resolved an issue that prevented offers from appearing in the [!UICONTROL Offers] UI, despite displaying correctly when creating an activity and adding offers. (TGT-51805)
* Resolved an issue where some activities lacked a fallback screen to display default content when personalized or targeted content could not be delivered. (TGT-51638)
* Resolved an issue that prevented live offers and certain folders from displaying correctly in the [!UICONTROL Offers] UI. (TGT-51628)
* Resolved an issue that prevented some URL strings and goURLs from being localized correctly. (TGT-35741)
* Fixed an issue that prevented roles ([!UICONTROL Approver], [!UICONTROL Editor], and [!UICONTROL Observer]) from being localized correctly in the [!DNL Target] UI. (TGT-29925)

### [!DNL Target Standard/Premium] 25.3.6 (March 14, 2025)

This release includes the following fixes and updates:

* Resolved "Invalid user input" error in [!UICONTROL Visual Experience Composer] (VEC) activities with [!UICONTROL Click Tracking] enabled when the same [!UICONTROL ClickTrack] selector is used multiple times. (TGT-51921)
* Fixed "Invalid user input" error in VEC activities with shared locations (for example, HEAD selector) and identical offers. (TGT-51879)
* Fixed an issue that caused experience modifications to be shared across audiences. (TGT-51815)
* Resolved validation errors when creating activities due to segment ID conflicts. The errors occurred when [!DNL Target] detected existing activities using anonymous segments. (TGT-51784)
* Resolved issue preventing [!DNL Target] from saving activities with exclusion rules in an audience. (TGT-51581)
* Resolved issue preventing customers from creating, deleting, or moving folders without access to the default workspace. (TGT-51499)
* Resolved issue causing GET requests to fail when retrieving [!DNL Analytics] metrics list. (TGT-51106)

### [!DNL Target Standard/Premium] 25.3.5 (March 11, 2025)

This release includes the following fixes and updates:

* Resolved an issue that prevented users from changing offers in the [!UICONTROL Modifications] panel. (TGT-51800)
* Resolved an issue where actions were incorrectly displayed in the left panel for experiences and audiences, including in [!UICONTROL ClickTrack] mode. (TGT-51895)
* Resolved an issue where [!UICONTROL ClickTrack] selectors were not applied to the correct audience page. (TGT-51871)

### [!DNL Target Standard/Premium] 25.3.4 (March 7, 2025)

This release includes the following fixes and updates:

* Resolved an issue where activity-only audiences were not visible in the [!UICONTROL Audiences] panel, preventing their editing or reuse. (TGT-51860)
* Fixed an issue that blocked [!DNL Target Standard] customers from creating activities using [!UICONTROL Analytics for Target] (A4T) reporting. (TGT-51854)
* Fixed an issue that excluded local ID counters from the payload during batch create and edit operations. (TGT-51867)

### [!DNL Target Standard/Premium] 25.3.2 (March 6, 2025)

This release includes the following fixes and updates:

* Fixed an issue where copying an activity with an activity-only audience failed to create a new activity, mistakenly using the original activity's audience instead. (TGT-51855)
* Fixed an issue that prevented editing of [!UICONTROL Experience Targeting] (XT) activities with activity-only audiences. (TGT-51846)
* Fixed an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to apply modifications to an experience correctly on the first edit. (TGT-51843)
* Fixed an issue that triggered an 'ID' error when clicking on certain elements within the VEC. (TGT-51814)
* Updated error handling in the VEC during activity creation. (TGT-51759)
* Fixed an issue where a missing view in the [!UICONTROL Modifications] panel caused an 'invalid user input' error when saving the activity. (TGT-51827)
* Fixed an issue that prevented the creation of recommendations criteria. (TGT-51834)
* Added a confirmation message before redirecting to a different URL. (TGT-51703)
* Fixed issues with GraphQL integration tests within offers and folders. (TGT-51839)

### [!DNL Target Standard/Premium] 25.3.1 (March 3, 2025)

This release includes the following fixes and updates:

* A combined audience can include subgroups, each containing multiple audiences. This release fixed an issue that prevented subgroup audiences from displaying in the [!UICONTROL Rules] dialog box. (TGT-51813)
* Resolved an issue where some experience audiences were replaced with [!UICONTROL All Visitors] when opening older activities. (TGT-51812)
* Resolved an issue that prevented editing activities with activity-only audiences. (TGT-51807)
* Resolved an issue that prevented editing page head modifications in the updated [!DNL Target] UI. (TGT-51797)
* Resolved a null error that occurred when duplicating an experience, deleting another experience, and then trying to save the activity. (TGT-51796)
* Resolved an issue that prevented audience exclusion rules from displaying in the audience's info panel during the [!UICONTROL Targeting] step of creating activities. (TGT-51579)
* Updated error messages localized in Korean. (TGT-51701 & TGT-51699)

### [!DNL Target Standard/Premium] 25.2.3 (February 26, 2025)

This release includes the following updates:

* Resolved an issue preventing activity updates post [!DNL Target] 25.2.1 release for some activities. (TGT-51781)
* Resolved an issue where all in-state audience changes were removed upon canceling the activity-creation process (selecting [!UICONTROL Cancel] instead of [!UICONTROL Add Audience]). (TGT-51769 & TGT-51770)
* Resolved an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to load for some activities, particularly when custom code was used.  issue led to the VEC displaying a blank screen or the [!DNL Target] UI reverting to its older version. (TGT-51758)
* Resolved an issue where modifications were discarded after editing page delivery for audiences. (TGT-51756)
* Resolved an issue where all non-metric audiences (page and experience audiences) were removed from activities upon changing a metric type on the [!UICONTROL Goals & Settings] page. (TGT-51753)
* Resolved an issue where clicking [!UICONTROL Cancel] while editing an activity navigated the Target UI to the [!UICONTROL Activities List] instead of the [!UICONTROL Activity Details] page. (TGT-51731)
* Resolved an issue preventing customers from downloading reports via the [!UICONTROL Export Reports to CSV] option. (TGT-51708)
* Resolved an issue in the Form-Based Experience Composer where [!DNL Target Standard] customers were incorrectly shown as using [!UICONTROL Properties], a [!DNL Target Premium] feature. (TGT-51678)
* Fixed an issue that blocked [!DNL Adobe Experience Platform] attributes from displaying when creating new offers. (TGT-51665)
* Moved all active filters for [!DNL Recommendations] inventory to the quick search, aligning the UI with [!UICONTROL Catalog Search] instead of the [!UICONTROL Filter] rail. (TGT-50723)

### at.js version version 2.11.7 (February 26, 2025)

This release includes the following update:

* Fixed Telemetry logging when `localStorage` is not available. Telemetry was causing an issue for some customers that had `localStorage` disabled in their browsers.

For information about this and previous at.js releases, see [at.js version details](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}.

### Target Standard/Premium 25.2.1 (February 17, 2025) {#ui-update-2}

This release includes the following updates:

* [!UICONTROL Activities] user interface update
* [!DNL Recommendations] user interface update

#### [!UICONTROL Activities] user interface update

As the [!DNL Adobe Target] UI modernization effort continues, we are pleased to announce the general availability of the updated [!UICONTROL Activities] User Interface.

>[!NOTE]
>
>Starting February 17, customers will gradually have access to the new [!UICONTROL Activities]  UI. To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage will upgrade the initial group of [!DNL Target] customers to the new [!UICONTROL Activities] UI. Subsequent stages will upgrade the remaining customers.

>[!IMPORTANT]
>
>For important information about the [!DNL Target] UI version toggle end-of-life plan, see [[!DNL Target] UI version toggle deprecation](/help/main/r-release-notes/release-notes.md#toggle).

Based on the latest [!DNL Adobe Spectrum] design system, the update standardizes previously inconsistent design patterns, while adding new enhancements, such as:

* [Redesigned reporting](/help/main/administrating-target/reporting.md) for better insights into activity results.
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) page, now getting the information from the [[!DNL Audit Query API]](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} for real-time insights.
* [Customizable list views](/help/main/c-activities/activities.md) for better flexibility across different team needs.
* [Enhanced quick info and detail screens](/help/main/c-activities/activities.md) for easier access to information.
* [Session-persistent search and filter options](/help/main/c-activities/activities.md).
* Completely [rebuilt [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) with support for latest security updates from browser providers and a modern user interface.

  For information about how the updated VEC differs from the previous version, see:
  
  * [Visual Experience Composer changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md) 
  * [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [Updated [!DNL Chrome] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) supporting Manifest V3 for increased security and improved support for first-party cookies.

![Activities refresh](/help/main/r-release-notes/assets/activities-refresh.png)

#### [!DNL Recommendations] user interface update

As the [!DNL Adobe Target] UI modernization effort continues, we are pleased to announce the general availability of the updated [!DNL Recommendations] User Interface. 

>[!NOTE]
>
>Starting February 17, customers will gradually have access to the new [!UICONTROL Recommendations]  UI. To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage will upgrade the initial group of [!DNL Target] customers to the new [!UICONTROL Activities] UI. Subsequent stages will upgrade the remaining customers.

Based on the latest [!DNL Adobe Spectrum] design system, the update standardizes previously inconsistent design patterns, while adding new enhancements, such as:

* The [product catalog search](/help/main/c-recommendations/c-products/catalog-search.md) now features an updated database allowing a real-time synchronization of products.
* [!UICONTROL Recommendations] objects ([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections], and [!UICONTROL Exclusions]) [created over API are now available in the UI](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [Recommendations settings](/help/main/administrating-target/recommendations-settings.md) have been consolidated under the [!UICONTROL Administration] section.
* Customizable list views for better flexibility across different team needs.
* Refreshed HTML and JSON code editors with [syntax highlighting and line numbering](/help/main/c-experiences/c-manage-content/create-json-offer.md). 
* Enhanced quick info and detail screens for easier access to information.
* Session-persistent search and filter options.

![Recommendations UI refresh](/help/main/r-release-notes/assets/recs-ui-refresh.png)

### Target Standard/Premium 25.1.1 (January 9, 2025) {#ui-update-1}

This release includes the following updates:

#### [!UICONTROL Offers Library] user interface update

To enhance the user experience for [!DNL Adobe Target] users, this release updates the [!UICONTROL Offers Library] user interface. 

>[!NOTE]
>
>To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage upgraded the initial group of Target customers to the new Offers UI. Subsequent stages will upgrade the remaining customers.

>[!IMPORTANT]
>
>For important information about the [!DNL Target] UI version toggle end-of-life plan, see [[!DNL Target] UI version toggle deprecation](/help/main/r-release-notes/release-notes.md#toggle).

Using the latest [!DNL Adobe Spectrum] design system, this update standardizes inconsistent design patterns and introduces new enhancements, including the following:

* **Bulk offer management**: Select and delete or move multiple offers simultaneously.

* **[!UICONTROL Code Editor] upgrades**: Refreshed HTML and JSON editors with syntax highlighting and line numbering.

* **Improved offer cards**: Enhanced quick information and detail cards for easier information access.

* **Persistent search and filters**: Adds session-persistent search and filter options.

For more information see [Offers](/help/main/c-experiences/c-manage-content/manage-content.md) and the sub-articles in this section. All Offers articles in this section have been updated to reflect these UI changes.

Here's a short video that highlights the changes in this release:

![Offers UI refresh video](/help/main/r-release-notes/assets/offers-video-v2.gif)

## Release notes - 2024

### [!DNL Adobe Experience Platform Web SDK] `__view__` scope optimization (October 22, 2024)

Between July 22, 2024 and August 15, 2024, the [!DNL Target] team optimized the `__view__` scope, enhancing the accuracy of activity impression, visit, and visitor reporting. This optimization aims to automatically capture reporting data for auto-rendered propositions and should be transparent to most accounts.

All new [!DNL Adobe Experience Platform Web SDK] customers will have this optimization enabled. However, customers who migrated from at.js and have not followed the implementation steps below have the optimization disabled. We urge these customers to review their implementations by February 3, 2025. After this date, we will enable the optimization for all customers. Failure to review and adjust implementations by then might impact reports, as mentioned below. Please contact [!DNL Adobe Customer Care] if you need to confirm whether your implementation is affected or if you require more time to adjust your implementation.

>[!IMPORTANT]
>
>If you cannot complete your implementation review and resolve any issues by February 3, 2025, you can request a one-time, six-month extension. Ensure that your request is submitted by January 31, 2025. Adobe will review and decide on your request.

To benefit from this optimization in case of manual proposition rendering, review your [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} to ensure that you are sending notifications after manually rendering experiences or when using the `applyPropositions` method (or the corresponding [!DNL Launch] action as a helper) to render experiences.

The most-common scenarios when experiences are manually rendered include:

* Using JSON offers
* Using a custom decision scope in an activity created in the [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)
* Not using `renderDecisions: true` when fetching an activity created using the [!UICONTROL Form-Based Experience Composer] that uses the global `__view__` scope

If notifications are not implemented as documented in [Render personalized content](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} in the *Data Collection* guide, reporting data might be missing in [!DNL Target] and in [Analytics for Target reporting](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In certain scenarios, you might notice an incorrect traffic split because the reporting data is not captured. Or, in other scenarios, reporting the same event repeatedly.

Depending on your implementation, check for [!DNL Analytics] and A4T reporting impacts. 

The [!DNL Platform Web SDK] supports two implementation types for rendering experiences and personalizations:

* **Single call for personalization and measurement.**

  Initially recommended, the single-call approach for the [!DNL Platform Web SDK] is scheduled to be deprecated in favor of the split-call approach. Adobe advises all new implementations to use the new split-call approach and recommends that existing customers transition to the split-call method as well. 
  
  If you continue to use the single-call approach, you might notice the following unexpected changes in your [!DNL Analytics] reports:

  * A dip in bounces.
  * A4T and [!UICONTROL Page View] hits not stitched together, making it challenging to perform certain breakdowns and correlations of your A4T reports using [!DNL Analytics] eVars and events.

* **Split calls (also known as top and bottom of page events).**

  This implementation type is the new [split-call implementation approach](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank} recommended by [!DNL Adobe]. With this approach, the new optimization does not impact [!DNL Analytics] or A4T reports.

If you have questions, contact [Adobe Customer Care](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

### at.js version 2.11.6 (September 29, 2024)

* Fixed an issue that prevented [!DNL Target] from operating correctly with redirect offers within the [!UICONTROL Visual Experience Composer] (VEC) or [!UICONTROL Form-Based Experience Composer].

For more information about at.js releases, see [at.js version details](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank} in the *Adobe Target Developer Guide*.

### [!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics] (May 8, 2024)

The integration between [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} and [!DNL Target] provides powerful analysis and timesaving tools for your optimization program.

The primary benefits of using [!DNL Customer Journey Analytics] as the reporting source for [!DNL Target] are:

* Marketers can dynamically apply [!DNL Customer Journey Analytics] success metrics to [!DNL Target] activity reports at any time. It is not required to specify everything before running the activity. 
* Marketers can take advantage of [!DNL Customer Journey Analytics] features, such as the [Experimentation Panel](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, to further analyze their website personalization.  

For more information, see [Target reporting in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

### [!UICONTROL Visual Experience Composer] helper extension (April 23, 2024)

The legacy [!DNL Target] Visual Experience Composer helper extension was created using Manifest V2. [!DNL Google] announced that it will no longer allow extensions created using Manifest V2 starting in June 2024. For more information, see [[!UICONTROL Visual Experience Composer] helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] recommends that customers move to the newer [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) as soon as feasible.

### Updates for `Browser:iPad` and `Browser:iPhone` in [!UICONTROL Browser] audience attributes (April 30, 2024)

|Updates|Details|
|--- |--- |
|[!UICONTROL Browser:iPad] and [!UICONTROL Browser:iPhone] updated in [Browser attributes](/help/main/c-target/c-audiences/c-target-rules/browser.md) used when creating audiences.|[!DNL Adobe Target] lets you [target on any of several category attributes](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), including visitors who use a specific [browser or browser options](/help/main/c-target/c-audiences/c-target-rules/browser.md) when they visit your page.<P>Starting with the [!DNL Target] Standard/Premium 24.3.1 (March 4-6, 2024), built-in audiences created using the Target UI, such as `Browser:iPad` and `Browser:iPhone` will be updated to perform proper targeting for [!DNL iPad] and [!DNL iPhone] using `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` and `profile.mobile.isTablet`.<P>This update requires no action on the customers' side.<p><B>Important</b>: For customers to perform proper targeting for [!DNL iPad] and [!DNL iPhone] in profile scripts (and JavaScript segments), manual changes must be made by the customer by **April 30, 2024**. For examples of alternate settings that must be manually changed, see [Updates for [!DNL iPad] and [!DNL iPhone] in [!UICONTROL Browser] audience attributes](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates).|

### [!UICONTROL Visual Editing Helper] extension (March 14, 2024)

This release contains the following enhancements and fixes for the [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) extension for [!DNL Google Chrome]:

* Enhanced the iFrame loading mechanism when performing authoring in customers' websites.
* Fixed an issue that caused the extension to duplicate cookies while performing authoring in the [!UICONTROL Visual Experience Composer] (VEC).

### [!DNL Target] Standard/Premium 24.3.1 (March 4-6, 2024)

This release contains the following enhancements and fixes:

* Fixed the logic that computes the number of unique selectors in an activity. (TGT-47878)
* Fixed an issue that caused [!UICONTROL Multivariate] (MVT) activities configured with [!UICONTROL Analytics for Target] (A4T) reporting to not display properly. (TGT-47490)
* Improved the warning message displayed in reporting when an experience with no traffic is used as the control experience. (TGT-47537)
* Added many backend and localization fixes.

### [!DNL Target] Standard/Premium 24.1.1 (January 22, 23, & 25, 2024)

This release contains the following enhancements and fixes:

* [!UICONTROL Analytics for Target] (A4T) activities with revenue goal metrics did not display "Revenue" as the column name and the revenue metric did not display in ($) format in reporting. This was a cosmetic issue that has been remedied. (TGT-46995)
* Fixed an issue that caused reporting date intervals to not work correctly. (TGT-47396)
* Fixed an issue that caused the incorrect status to display on the [!UICONTROL All Activities] page after customers activated or deactivated an activity using the [!UICONTROL More Actions] icon. (TGT-47367)
* Fixed an issue that caused the [!UICONTROL Important Attributes] report to not display for a single customer. (TGT-47272)
* Fixed an issue that caused an "Invalid payload" message to display when a single customer tried to enable "Require Authentication." (TGT-47195)
* Updated numerous localized strings in the [!DNL Target] UI.

## Release notes - 2023

### [!DNL Target] Standard/Premium 23.11.1 (November 13 & 14, 2023)

This release is scheduled for the following days:

* **November 13**: Asia-Pacific (APAC) region
* **November 14**: Americas region
* **November 14**: Europe, Middle East, and Africa (EMEA) region

This release contains the following enhancements and fixes:

* Enhanced the [Activity QA](/help/main/c-activities/c-activity-qa/activity-qa.md) feature to support [disallowing duplicate offers](/help/main/c-activities/t-automated-personalization/managing-exclusions.md) for experiences in [!UICONTROL Automated Personalization] activities. (TGT-46627)
* Added a tooltip in the [!DNL Target] UI to help customers understand why there might not be data available in activity reports if no traffic is allocated to the control experience. A link to more information is included in the tooltip: [Why is there no data available for my activity's report?](/help/main/c-reports/reporting-frequently-asked-questions.md#section_E4722F6445884130951DF79981C8289B). (TGT-46610)
* Fixed an issue that prevented activities from displaying properly on the [!UICONTROL Activities] page for a few customers. (TGT-46830)
* Fixed the following issues that affected activities that use [[!UICONTROL Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) as the reporting source: 
  * Fixed an issue that prevented some customers from viewing reporting data. (TGT-46557)
  * Fixed an issue that sometimes caused the [!UICONTROL View in Analytics] link on activity reporting pages to not function properly. (TGT-46731)
  * Fixed an issue that prevented data for [!UICONTROL Lift] and [!UICONTROL Confidence] to display properly in the [!DNL Target] UI. (TGT-46592, TGT-46554, & TGT-46586)

### [!UICONTROL Activities] page user interface refresh (October 25, 2023)

As part of the [!DNL Adobe Target] team's ongoing effort to improve the user-experience for [!DNL Target] users, this release refreshes the [!UICONTROL Activities] page in the [!DNL Target] UI. This update unifies and standardizes design patterns that were previously inconsistent, while adding new enhancements.

Starting Wednesday, October 25, a percentage of customers will have access to the new UI with additional customers getting access in the next several days.

For more information see [Activities](/help/main/c-activities/activities.md).

### [!DNL Target] Standard/Premium 23.10.2 (October 24, 2023)

This release contains the following enhancements and fixes:

* Enhanced the new [!UICONTROL Activities] UI so that the [!UICONTROL Visual Experience Composer] (VEC) opens with the default settings for `selectorCriteria` when creating a new activity. (TGT-46586)
* Fixed an issue that prevented some customers from editing elements in [!UICONTROL Composer] mode when using the VEC. (TGT-46470)
* Added the ability to specify a generic preferred selector when using custom attributes. (TGT-46545)
* Fixed an issue that sometimes prevented an [!UICONTROL Auto-Target] report that uses [!UICONTROL Analytics for Target] (A4T) from displaying in the [!DNL Target] UI, even though the report displayed correctly in [!DNL Adobe Analysis Workspace]. (TGT-46494)
* Updated various localized strings in the Target UI. (TGT-18899)

### [!DNL Target] Standard/Premium 23.9.4 (October 4-6, 2023)

This release contains the following enhancements and fixes:

|Feature|Details|
| --- | --- |
|[!DNL Recommendations] implementation pattern|The *Recommendations implementation pattern using at.js* articles help you understand and create your [!DNL Adobe Target Recommendations] implementation when using the at.js JavaScript library.<P>For more information, see [Recommendations implementation pattern using at.js overview](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html){target=_blank} in the *Adobe Target Developer Guide*.|

* Added [!UICONTROL Visual Experience Composer] (VEC) enhancements for dynamic frameworks. (TGT-44064)
* Fixed an issue that caused the selected date in the `getViewInAnalyticsId` request to not update properly. This fix helps recompute the [!DNL Analytics] link in reporting when the date range and metrics report settings are changed. (TGT-46246)

### [!DNL Target] Standard/Premium 23.9.3 (September 18, 2023)

This release contains the following enhancements and fixes:

* Enhanced the [!UICONTROL Visual Experience Composer] (VEC) to support Lightning Web Components (Light DOM). (TGT-45422)
* Fixed an issue that caused VEC actions to be applied in the incorrect order. In some cases, the VEC applied some modifications asynchronously and adding extra modifications to an element caused errors if that element displays after an [!UICONTROL Insert] action. Also fixes the VEC URL that now updates when clicking anchor links. (TGT-45983)
* Fixed an issue with the VEC [!UICONTROL Overlay] feature, which now supports elements in Shadow DOMs. (TGT-45202 & TGT-45262)
* Fixed an issue when opening a Single Page Application (SPA) page in the VEC and then going to [!UICONTROL Browse] mode caused the Back and Forward arrows to not function correctly. (TGT-45956)
* Fixed an issue that prevented some web pages from loading in the VEC. (TGT-45983)

### [!DNL Target] Standard/Premium 23.9.2 (September 12-14, 2023)

This release contains the following enhancements and fixes:

* Changed the [!DNL Analytics] API to the new [!DNL Analytics] API version 2.0. (TGT-45345)
* Fixed issues that impacted [!UICONTROL Automated Personalization] (AP) activities for some customers, including timely syncing the activity on the [!DNL Target] backend and delivering the expected experience in preview links. (TGT-46202)

### [!DNL Target] Standard/Premium 23.9.1 (September 6-11, 2023)

This release contains the following enhancements and fixes:

* Fixed an issue that caused inconsistent reporting data in the [!DNL Target] UI and the [!DNL Adobe Analytics] UI for [!UICONTROL Auto-Allocate] activities that use [!UICONTROL Analytics for Target] (A4T) as the reporting source. (TGT-46112)
* Increased the timeout for PUT calls to the Target Delivery API to 15 seconds to avoid timeout errors. (TGT-46091)
* Fixed an issue that prevented the URL from consistently updating when browsing through a Single Page Application (SPA) website. (TGT-45417)

### [!DNL Adobe Target] Edge planned infrastructure upgrade {#edge}

The planned edge infrastructure upgrade requires additional IP or domains to be allow-listed. Review and allow-list the NAT and IP/domains for edge deployments 41-48. Infrastructure upgrades begin August 9, 2023.

For more information, see [Allowlist Target edge nodes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank} in the *Adobe Target Developer Guide*.

### [!DNL Target] Standard/Premium 23.8.1 (August 9, 2023)

This release contains the following enhancements and fixes:

* Fixed an issue that sometimes prevented activities from syncing properly, as shown in the "[!UICONTROL Status]" column on the [!UICONTROL Activity] list page. (TGT-46010 & TGT-44831)
* Fixed an issue that sometimes prevented the "[!UICONTROL View in Analytics]" link from displaying on the [!UICONTROL Reports] page of activities that use [!UICONTROL Analytics for Target] (A4T) as the reporting source. (TGT-45808)
* Adjusted the presentation of values in tables to display as percentages instead of numbers with decimals. For example, 8% instead of .08. (TGT-45548)
* Fixed an issue that prevented customers from using keyboard focus to move to the next element in the [!UICONTROL Goals & Settings] page for [!UICONTROL Experience Targeting] (XT) activities. (TGT-44526)
* Fixed an issue that caused keyboard loss of focus after opening the "[!UICONTROL Add audiences]" dialog while creating an activity. (TGT-44525)

### [!DNL Target] Standard/Premium 23.7.1 (July 24-26)

This release contains the following enhancements and fixes:

* Improved search when [navigating elements using the DOM path](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in the [!UICONTROL Visual Experience Composer] (VEC) to include shadow DOM elements. (TGT-45262)
* Fixed an issue that prevented the [Change Overlay](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) setting from working properly. (TGT-45202)
* Fixed an issue that prevented some customers from downloading activity reports after receiving the following error message: "User is not authorized to access the report." (TGT-45724 & TGT-45747)

### [!DNL Target] Standard/Premium 23.6.1 (June 27-29)

This release contains the following enhancements:

|Feature|Details|
|--- |--- |
|[!UICONTROL QA mode] for [!UICONTROL Automated Personalization] activities|[!DNL Adobe Target] [!UICONTROL QA mode] is now available for [!UICONTROL Automated Personalization] activities, replacing [!UICONTROL Preview links] functionality.<P>For more information, see [Activity QA](/help/main/c-activities/c-activity-qa/activity-qa.md).|

* Performance enhancements to disallow duplicates functionality (including reduction in load time) while [managing exclusions](/help/main/c-activities/t-automated-personalization/managing-exclusions.md#concept_4EF78013F80E48EFA024AE0274C9F037) in [!UICONTROL Automated Personalization] activities.

### [!DNL Target] Standard/Premium 23.5.2 (May 31, 2023)

This release contains the following enhancements and fixes:

* Fixed an issue that caused a blank page to display while generating a Profile API authorization token. (TGT-45387 & TGT-45423)
* Fixed an issue that prevented an image from displaying in the [!UICONTROL Create Design] panel if the image name contains GB 18030 characters. (TGT-44614)
* Fixed an issue in which some GB 18030 symbol characters were incorrectly escaped in Text/HTML in experiences. (TGT-44600)
* Fixed an issue that caused reports for [!UICONTROL Auto Personalization] activities to freeze during analysis. (TGT-44820)
* Fixed an issue that prevented searching for an activity on the [!UICONTROL Activity] page if the activity name contains a square bracket ( [ or ] ). (TGT-44777)
* Fixed an issue that prevented an activity from syncing if the activity's objective contains special characters. (TGT-44982)
* Fixed an issue that caused no activities to display in the [!DNL Target] UI for the Default workspace for certain customers. (TGT-45286)
* Updated the behavior of the "Disallow Duplicates" flag. Excluded repeating offers flags are updated to allow repeating offers if they are the default content offer (for APIs v3, v4) and allow duplicate options if the options reference the default content offer and have no templates defined. (TNT-46617)
* Fixed an issue in which a query parameter was added to a URL that prevented the page from loading in the [!UICONTROL Visual Experience Composer] (VEC). (TGT-44873)
* Made various localization fixes throughout the [!DNL Target] UI.

### Real-Time CDP Profile Attributes shared with [!DNL Target] [!UICONTROL Real-Time CDP Profile Attributes] (June 13, 2023)

This release contains the following enhancement:

|Feature|Details|
|--- |--- |
|Real-Time CDP Profile Attributes shared with [!DNL Target]|[!UICONTROL Real-Time CDP Profile Attributes] can be shared with [!DNL Target] for use in HTML and JSON offers.<P>For more information, see [Share Real-Time CDP Profile Attributes with [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes).|

### [!DNL Target] Standard/Premium 23.5.1 (May 23-25, 2023)

This release contains the following new enhancements and fixes:

* Fixed an issue that prevented certain customers from creating audiences with visitor profiles using "greater than" or "less than" operators. (TGT-45271)
* Made various localization fixes throughout the [!DNL Target] UI.
* Updated the Target UI in various places for an upcoming UI refresh (changes are behind a feature flag until the updates are released).

### [!DNL Target] Standard/Premium 23.4.1 (April 25-27, 2023)

This release contains security updates and the following new features:

|Feature|Details|
|--- |--- |
|AEM [!UICONTROL Content Fragments] for headless personalization and experimentation|Use [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Content Fragments] in [!DNL Target] activities. Combine the ease-of-use and power of AEM with powerful Artificial Intelligence (AI) and Machine Learning (ML) capabilities in [!DNL Target] to aid headless personalization and experimentation.<P>For more information, see [AEM [!UICONTROL Content Fragments]](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md).|
|[*Adobe Target Developer Guide*](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}|The *Adobe Target Developer Guide* has been relocated to *[!UICONTROL Adobe Experience League]*. The move to *[!UICONTROL Experience League]* aids in localization of text in additional languages, unifies search within *Experience League* to span and offer search results from both the *[!UICONTROL Adobe Target Business Practitioner Guide]* and the *[!UICONTROL Adobe Target Developer Guide]*, and provides additional benefits.<P>You will be redirected from the previous location to *[!UICONTROL Experience League]* automatically. Please update your bookmarks as necessary.|

### [!DNL Target] Standard/Premium 23.3.1 (March 28-30, 2023)

This release contains the following new features, enhancements, and fixes:

|Feature|Details|
|--- |--- |
|Optimized A4T metrics for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]<p>(Release date March 30, 2023)|[!DNL Target] lets you choose metrics based on binomial events or metrics based on continuous events when using [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities.<P>Be aware of the following change in supported metrics:<ul><li>[!DNL Target] preserved the previous behavior for existing activities until September 9, 2023. After this date, activities using non-supported metrics will be discontinued to force existing activity migration to the new behavior.</li></ul>For more information, see "Supported goal metrics" in [A4T support for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported).<br>With this feature, the following tutorials have been updated:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Target] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul>|

* Enhanced audience and activity synchronization so that items created in [!DNL Adobe Experience Platform] and [!DNL Adobe Audience Manager] are available in the [!DNL Target] UI quicker. (TGT-44568)
* Enhanced UI to let users remove the [!UICONTROL Default URL] under [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer] > [!UICONTROL Default URL]. This change lets customers change the default URL back to an empty string, which was previously not possible after initial configuration. (TGT-44577)
* Removed restrictions that prevented customers from editing or deleting out-of-the box audiences (audiences with reserved names). (TGT-44655)
* Disabled the "[!UICONTROL Done]" option while loading spinners were visible in the [!DNL Target] UI when creating [combined audiences](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* Fixed the [!UICONTROL Language] link at the bottom of the [!UICONTROL Audiences] page so that it correctly links to the "[!UICONTROL Account communication preferences]" page. (TGT-43562)
* Resolved an issue that sometimes prevented customers from creating [!UICONTROL A/B Test] activities after selecting the [!UICONTROL Adobe Analytics] option under [!UICONTROL Administration] > [!UICONTROL Reporting] > [!UICONTROL Reporting Experience Cloud Solution]. (TGT-44844)
* Fixed an issue that prevented customers from viewing the last experience in a [!UICONTROL Multivariate Test] activity with many experiences from within the [!UICONTROL Visual Experience Composer] (VEC). The [DOM path](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) at the bottom of the VEC sometimes prevented customers from seeing the last experience. (TGT-44578)
* Fixed an issue that caused the Browse URL in the VEC to not reflect the current page that is visible in a normal browser session if the page requires authorization or invokes redirects. (TGT-44350)
* Fixed an issue that prevented customers from changing the [!UICONTROL Filter Incompatible Criteria] setting in [!UICONTROL Recommendations] > [!UICONTROL Settings]. (TGT-44398)
* Fixed an issue that caused POST requests to create [!DNL Recommendations] feeds to fail when using [!UICONTROL Analytics Classifications] with report suites with dots in their names. (TGT-44598)
* Updated links in the [!DNL Target] UI to point to the new [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* Enhanced security to prevent Server-Side Request Forgery (SSRF) attempts in [!DNL Recommendations] feeds. (TGT-43769)
* Made various localization fixes throughout the [!DNL Target] UI.

### at.js version 2.10.2 (March 7, 2023)

* Fixed an issue that caused the `trackEvent` function to always return an error.

For information about all at.js releases, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} in the [Adobe Target Developer Guide](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.

### [!DNL Target] Standard/Premium 22.15.1 (March 8 & 9, 2023)

This release will be available according to the following staggered schedule:

* **March 8**: Americas region
* **March 9**: Europe, Middle East, and Africa (EMEA) region
* **March 9**: Asia-Pacific (APAC) region

This release contains the following fixes:

* Updates for custom web components authoring with the [!UICONTROL Visual Experience Composer] (VEC):

  * Fixed Shadow DOM elements selection in the VEC by improving the authoring process so there is no dependency on the [!DNL Target] implementation type when authoring the shadow root. Now, selecting Shadow DOM elements in the VEC should work for any website.
  * Fixed an issue that prevented loading HTML elements using #Shadow DOM in the VEC. (TGT-35801)
  * Fixed VEC issues with SPA websites using ShadowDOM. (TGT-43169)
  * Fixed an issue with the Optimization Goal: "clicked an element" that did not properly identify the CSS selector in ShadowDOM.

>[!NOTE]
>
>To ensure delivery of the changes authored in the VEC, ensure that you are using a [!DNL Target] SDK ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js)) with a version greater than 2.8.

**Known issue**: Click-tracking on a shadow root element when using [!DNL Adobe Experience Platform Web SDK] is not working correctly. (TNT-47012)

### at.js version 2.10.2 (March 7, 2023)

* Fixed an issue that caused the `trackEvent` function to always return an error.

For information about all at.js releases, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} in the [Adobe Target Developer Guide](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.

### [!DNL Target] Standard/Premium 22.14.5 (February 13-15, 2023)

This release will be available according to the following staggered schedule:

* **February 13**: Americas region
* **February 15**: Europe, Middle East, and Africa (EMEA) region
* **February 15**: Asia-Pacific (APAC) region

This release contains the following fixes:

* Fixed an issue that caused the following error message even though a property was specified in Automated Personalization (AP) activities: "Errors: At least one property has to belong to a non-default workspace" (TGT-44607)
* Fixed a potential security issue impacting server-side Recommendations feeds. (TGT-43769) 

### at.js version 2.10.1 (February 2, 2023)

* Fixed a bug in which activities involving audience rules containing parameters with dots in their names were not returning the expected experience, for on-device decisioning.
* Fixed a bug introduced in at.js 2.6.0 in which at.js was firing a delivery call, even when `mboxDisable` was enabled.

For information about all at.js releases, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} in the [Adobe Target Developer Guide](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.

### [!DNL Target] Standard/Premium 22.13.3 (January 25-26, 2023)

This release will be available according to the following staggered schedule:

* **January 25**: Europe, Middle East, and Africa (EMEA) region
* **January 25**: Asia-Pacific (APAC) region
* **January 26**: Americas region

This release contains the following new features, enhancements, and fixes:

|Feature|Details|
| --- | --- |
|[JSON offer](/help/main/c-experiences/c-manage-content/create-json-offer.md) support in Automated Personalization (AP)|Added support for JSON offers in [!UICONTROL Automated Personalization] (AP) activities using the Form-Based Experience Composer. (TGT-41460)|
|[AEM experience fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)|Added the ability to distinguish between [!DNL Adobe Experience Manager] fragment (AEM XF) types that are exported to [!DNL Target]. Instead of the "Experience Fragment" option, [!DNL Target] now lets you filter and search by "HTML XF" and "JSON XF." (TGT-44132)|

* Fixed an issue that caused a "500 error" in [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] (XT) activities that contain recommendations. This issue was caused when [!DNL Target] failed to properly delete criteria objects from the [!DNL Target] UI and [!DNL Recommendations] backend that are no longer in use. (TGT-44383)
* Removed the location from the displayed offer name in the [!UICONTROL Offer Level] report for [!UICONTROL Automated Personalization] activities. This change makes the report more readable. (TGT-44294)
* Removed the 45-day and 90-day calendar options from the AP and [!UICONTROL Auto-Target] [!UICONTROL Personalization Insights] and [!UICONTROL Important Attributes] reports in the [!DNL Target] UI. Because of usage patterns and to improve performance, these date ranges have been deprecated. The UI has been updated to reflect the currently allowed ranges: 15, 30, and 60 days. (TGT-39357)
* Disallowed the ability to change the [!UICONTROL Same as Optimization Goal] setting on the [!UICONTROL Goals & Settings] page after the activity is live. (TGT-43923)
* Fixed an issue that caused issues with the default workplace in the [!DNL Target] backend when upgrading from [!DNL Target Standard] to [!DNL Target Premium]. (TGT-44081 & TGT-44306)
* Made a change to allow [!DNL Analytics] report suites that contain a dot character "." in their names to be used in the [!DNL Target] UI to create [!DNL Analytics] classification feeds.
* Changed the link on the [!UICONTROL Implementation] page ([!UICONTROL Administration] > [!UICONTROL Implementation]) for "Implementation Methods with On-Device Decisioning" to point to the page that explains how to use on-device decisioning for all supported SDKs: Node.js, Java, .NET, and Python. For more information, see [Getting Started with Target SDKs](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/getting-started.html){target=_blank} in the [Adobe Target Developer Guide](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.
* Fixed an issue that caused file-upload issues when using [!DNL Scene7] and [!DNL Target].
* Enhanced the accessibility of the [!DNL Target] UI for persons with disabilities by using results from an internal usability audit. These accessibility enhancements include access to features that were previously not accessible via the keyboard, alt text enhancements, the ability to zoom parts of the UI to be more usable, improved keyboard focus, and more.   (TGT-42759) 
* Made various localization fixes throughout the [!DNL Target] UI.

## Release notes - 2022

### Models API release (November 23, 2022)

The new [!DNL Adobe Target] Models API, also called the Blocklist API, lets users view and manage the list of features used in machine learning models for [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] (AT) activities.

For more information, see [Models API Overview](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html){target=_blank} in the *Adobe Target Developer Guide*.

### [!DNL Target] Standard/Premium 22.10.3 (staggered release October 25-27, 2022)

This release contains the following fixes:

* Added tooltips in the [!DNL Target] UI to help customers navigate the audience builder more efficiently and to learn how to use features that might be unfamiliar. (TGT-44139)
* Added functionality to prevent customers from editing an activity that was disabled by [!DNL Target] because it uses unsupported metrics. A message in the UI directs customers to duplicate the activity and then update the conversion metric.

  With this release `averagetimespentonsite`, `bouncerate`, and `entries` metrics in [!DNL Target] activities will be deprecated for new activities. Existing activities can continue using these metrics until May 2023.

* Added a tooltip in the [!DNL Target] UI to help customers select an optimization criteria while creating or editing an [!UICONTROL Auto-Target] activity that uses A4T. 

### [!DNL Target] Standard/Premium 22.10.1 (staggered release October 10-13, 2022)

This release contains the following new features, enhancements, and fixes:

|Feature|Details|
| --- | --- |
|[!DNL Adobe Experience Manager] (AEM) experience fragments|Updates to the AEM experience fragments functionality include the following:<ul><li>Added the ability to filter AEM experience fragments by type (HTML or JSON) in the [!UICONTROL Offers] list. (TGT-43121)</li><li>Fixed an issue that allowed customers to insert JSON [!UICONTROL Experience Fragment] offers when using the VEC, which is not supported. JSON offers can be inserted only when using the [!UICONTROL Form-Based Experience] composer. (TGT-43846)</li></ul>For more information, see AEM [experience fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).|
|New [!UICONTROL Visual Experience Composer] extension for Google Chrome|A new [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) extension for Chrome is available in the Chrome Web Store.<br>Starting in January 2023, the current [!DNL Target] VEC Helper extension will stop working in Google Chrome because Google won't allow extensions using Manifest V2. Download the new extension to continue to visually author your websites in [!DNL Target] starting with the new year.<br>The following links show the two extensions in the Chrome Web Store:<ul><li>[New extension](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Old Extension](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>For more information, see [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).|
 
* Fixed an issue that prevented audience rule information from displaying properly in the [!UICONTROL Audiences Refinements] information window. (TGT-43917)
* Improved the performance of the [!DNL Target] UI when loading audiences that approach the [recommended limit of targeting rules](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* Fixed an issue that caused some components to not display properly in the [!UICONTROL Modifications] panel on the [!UICONTROL Experiences] page when creating or editing activities in the VEC after switching from [!UICONTROL Compose] to [!UICONTROL Browse] mode. (TGT-43300)
* Fixed an issue that prevented some customers from archiving [!UICONTROL A/B Test] activities that use [!UICONTROL Auto-Target]. (TGT-40978)
* Added the ability to automatically use a single offer in multiple locations within a single reporting group. (TGT-40689)

### [!DNL Target] Standard/Premium 22.9.1 (staggered release September 13-15, 2022)

This release will be available according to the following staggered schedule:

* **September 13**: Europe, Middle East, and Africa (EMEA) region
* **September 14**: Americas region
* **September 15**: Asia-Pacific (APAC) region

This release contains the following enhancements and fixes:

* Added a [!UICONTROL Cross-Domain] option when downloading at.js 2.10.0 (and later) to allow or disable setting 3rd-party cookies. (TGT-43674)
* Updated notifications in the [!DNL Target] UI to inform customers if the import of [!DNL Recommendations] feeds fails. (TGT-35811)
* Fixed an issue that caused [!UICONTROL Decision Offers] to not work properly within the [!UICONTROL Visual Experience Composer] (VEC). (TGT-43866)
* Fixed an issue that caused an error message to display when selecting the [!UICONTROL Clicked an Element] conversion goal while creating an [!UICONTROL Multivariate Testing] (MVT) activity. (TGT-43842)
* Fixed an issue that prevented the [!UICONTROL Impressions] column from displaying in the downloaded CSV report file for [!UICONTROL Automated Personalization] (AP) activities. (TGT-43780)
* Fixed an issue that prevented customers from editing HTML/JSON offers after duplicating experiences when using the [!UICONTROL Form-Based Experience Composer]. (TGT-43633)
* Fixed an issue that prevented customers from copying an [!UICONTROL A/B Test] activity from a non-default workspace to another non-default workspace. (TGT-41910)
* Fixed an issue to ensure that customers can properly display usages of [!DNL Recommendations] objects (designs, criteria, collections, and so forth) in [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] (XT) activities that contain recommendations and also delete criteria objects that are no longer in use from [!DNL Target] UI and [!DNL Recommendations] backend. (TGT-42331)
* Fixed an issue that causes a network timeout alert to appear in the [!DNL Target] UI when fetching parameters. (TGT-43737)
* Made UI updates to ensure that certain drag-and-drop actions are accessible by keyboard. (TGT-42969)
* Made UI updates to ensure that text stings are properly localized.

### at.js version 2.10.0 (September 13, 2022)

* Added a [!UICONTROL Cross-Domain] option when downloading at.js 2.10.0 (and later) to allow or disable setting 3rd-party cookies. (TGT-43674)

### [!DNL Target Standard/Premium] 22.8.1 (staggered release August 17-18, 2022)

This maintenance release includes backend and localization fixes.

### [!DNL Target] platform release (July 20, 2022)

This release contains the following features, enhancements, and fixes:

|Feature|Description|
| --- | --- |
|Improved audience evaluation accuracy and reduced end-user latency through IPv6 support (TNT-43364, TNT-44692) |Visitors' geo-locations are now determined by IPv6 addresses, if available, as opposed to only IPv4 addresses. Delivery APIs also support IPv6 input parameters. Filtering and allow-listing support both IPv4 and IPv6 addresses. The IPv6 support in this release means visitors will be more accurately included in audiences (more accurately qualify for activities or be included in filtering criteria). It also improves data latency, as IPv6 clients will route directly, avoiding the overhead of the the IPv6-to-IPv4 gateway.|
|Fixed A4T client-side payload handling issue (TNT-44926)|With A4T server-side integration, if Adobe Target identifies a request as coming from a bot, it does not forward the payload to Analytics, and there is no mod_stats event in recorded in the [!DNL Target] logs. With this release, A4T client-side logging has been enhanced so that the behavior regarding the A4T payload is the same as with A4T server-side: Visitors that are identified as bots are excluded from [!DNL Target] counting/reporting. (Note the issue in question was limited to implementations that used client-side payload handling; server-side was not impacted. With this release, the behavior is now consistent for both server-side and client-side payload handling.)|

### [!DNL Target Standard/Premium] 22.6.2 (June 30, 2022)

This release contains the following features, enhancements, and fixes:

|Feature|Description|
| --- | ---  |
|In-product notifications|Get the following relevant in-product notifications:<ul><li>**Activities**: Notifications for all activity types when an activity is approved or deactivated, either manually or when it reaches its start or end date. The notification includes the name of the activity with a link to the activity's overview page.</li><li>**Profile scripts** Notifications when a profile script is activated or deactivated, either manually or by Target.</li><li>**Recommendations feeds**: Notifications when a Recommendations feed is activated or deactivated, either manually or by Target. Notifications are also sent when a Recommendations feed fails.</li></ul> By default, notifications are received by product admins, publishers, and approvers. Notifications are configurable inside Experience Cloud preferences.<br>For more information see [Notifications and announcements](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements).|
|*Adobe Target Developer Guide*|The *Adobe Target Developer Guide* consolidates all [!DNL Target] developer content in one convenient guide. The guide includes information about implementing [!DNL Target] and [!DNL Recommendations], [!DNL Target] SDKs, and [!DNL Target] APIs.<br>For more information, see [Adobe Target Developer Guide](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.|

* Users with the [!UICONTROL Editor] role can no longer edit audiences in live activities. (TGT-43582)
* A warning message displays if a customer attempts to save an audience with an exclamation mark ( ! ) as the first character of the audience's name (for example !London). (TGT-43643)
* Fixed an issue that caused audiences definition details cards for some customers to indicate that an ended activity is still live. (TGT-43527)

### [!DNL Target Standard/Premium] 22.6.1 (staggered release: June 7-9, 2022)

This release will be available according to the following staggered schedule:

* **June 7**: Asia-Pacific (APAC) region
* **June 8**: Americas region
* **June 9**: Europe, Middle East, and Africa (EMEA) region

This release contains the following enhancements and fixes:

* An enhancement was delivered for the new [!UICONTROL Audiences] page to prevent an inconsistent state between the old database where the audiences were stored in the past and the new architecture that is retrieving the information directly from the backend. (TGT-43552)
* Fixed an issue that prevented some customers from saving combined audiences caused by the Target UI creating "empty" containers. (TGT-43588)

### Target platform release (May 25, 2022)

This release contains the following enhancements and fixes:

* Added [User Agent Client Hints](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/user-agent-and-client-hints.html){target=_blank} support.
* Fixed an issue that intermittently caused timeouts when rendering [!UICONTROL Offer Decisions] in [!UICONTROL Experience Targeting] (XT) activities. (TNT-44611)

### at.js version 2.9.0 (May 27, 2022) 

* Added [User Agent Client Hints](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/user-agent-and-client-hints.html){target=_blank} support.
* Fixed a bug where multiple mbox requests on the same page have different impression IDs.

### [!DNL Target Standard/Premium] 22.5.1 (staggered release; May 11-13, 2022)

This release will be available according to the following staggered schedule:

* **May 11**: Asia-Pacific (APAC) region
* **May 12**: Americas region
* **May 13**: Europe, Middle East, and Africa (EMEA) region

This release contains the following enhancements and fixes:

* Fixed an issue that caused a JavaScript error and prevented some customers from accessing the activity details for certain [!UICONTROL Automated Personalization] (AP) activities. (TGT-43526)
* Fixed an issue that prevented some customers from adding (or editing) a specific offer to an AP activity. (TGT-43503)
* Fixed an issue in the [!DNL Target] UI that displayed the following error message: "Your global mbox may not be in sync. Please try resaving it." This issue was a UI issue and did not impact customers' implementations. (TGT-43475)
* Fixed an issue that prevented one customer from editing experience-level refinements and audiences for an activity if the refinements and audiences were created before the new [!UICONTROL Audiences] UI was deployed. (TGT-43433)
* Fixed an issue that allowed customers to select duplicate [!DNL Adobe Audience Manager] (AAM) audiences while editing reporting audiences for an activity. (TGT-43430)
* Fixed an issue that prevented customers from creating duplicate audiences, but in different workspaces. (TGT-43423)
* Fixed an issue that prevented customers from deleting locations that have ad-hoc offers in activities created in the [!UICONTROL Form-Based Experience Composer]. (TGT-43315)
* Fixed an issue that prevented customers from accessing code offers after clicking image offers and then refreshing the UI. (TGT-43566)
* Fixed an issue that caused edits to profile scripts to revert to the original, unedited script after the script is edited, activated, and then deactivated. The profile script now remains in its edited state. (TGT-43249)
* Fixed an issue that caused the following error when attempting to move an audience to another workspace: "We cannot complete your request. Please contact Adobe Client Care if the problem persists". (TGT-43212)
* Fixed an error that caused an error when cloning custom code modifications for Single Page App (SPA) pages. (TGT-43137)
* Fixed an issue that caused the original promotion to be affected after duplicating an experience and then editing the promotion. (TGT-41775)

### [!DNL Target Standard/Premium] 22.4.1 (April 28, 2022)

This release contains the following fix:

* Fixed an issue that caused three cart-based algorithms to use the same Bought/Bought condition on the [!DNL Target] backend. (TGT-43456)
* Enabled [!DNL Target] UI token refresh for organizations enabled with [Business ID accounts](https://helpx.adobe.com/enterprise/using/identity.html){target=_blank} and Policy Based Authentication (PBA). (TGT-42590)

### [!DNL Target] platform release (April 27, 2022)

This release contains the following change:

* With this release you can prefetch content for [!UICONTROL Auto Personalization] (AP) and [!UICONTROL Auto-Target] (AT) activities (previously not returned by [!DNL Target]). This might change the experiences the end users see in case of a pre-fetch call (no changes to the "execute" flow) if an AP/AT activity is on the delivery path and is higher in priority than other AB/XT activities that use the same location for content delivery.

### [!DNL Target] platform release (March 30)

This release contains the following enhancement:

* Click-track metrics will include analytics payload in Delivery API requests for activities that use Analytics as the reporting source (A4T) and process events on client-side. (TNT-43073)

### [!DNL Target Standard] Audiences refresh (March 28)

This release contains the following update:

* The new [!UICONTROL Audiences] UI will be enabled for all [!DNL Target Standard] customers.

### Target Standard/Premium customer engineering fixes (March 22, 2022)

This maintenance release contains the following enhancements:

* Added functionality to return [!DNL Analytics] payload data for `prefetch` views and `pageLoad` click metrics when using the [!UICONTROL Delivery API] with activities that use [!UICONTROL Analytics as the reporting source] (A4T). (TNT-43198)
* Updated the bot filtering user agent list to allow a browser type commonly used in Japan. (TNT-43867)

### Target Standard/Premium 22.2.1 (February 1, 2022)

This maintenance release contains the following fixes and enhancements for the new [!UICONTROL Audiences] UI announced in the Target Standard/Premium 22.1.2 release that is rolling out to customers across all regions in the next six weeks. These fixes align the functionality of audiences created in [!DNL Adobe Target Standard/Premium].

* Fixed an issue that prevented imported audiences from [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud], and [!DNL Adobe Target Classic] from being assigned as reporting audiences. (TGT-43140)
* Added a [!UICONTROL Delete] option in the [!UICONTROL Audiences] list for imported audiences from [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud], and [!DNL Adobe Target Classic]. Also added bulk-delete functionality. (TGT-42914)

### at.js version 2.8.1 (January 28, 2022)

* Fixed `pageLoad` not being mapped to target-global-mbox in [!UICONTROL On Device Decisioning] (ODD) hybrid execution mode.
* Fixed an issue with analytics details for mbox request.
* Upgraded dev dependencies to fix security vulnerabilities.

### [!DNL Target Standard/Premium] 22.1.2 (January 26, 2022)

|Feature|Details|
| --- | --- |
|[!DNL Adobe Experience Platform] audiences in [!DNL Target]|You can now consume and use [!DNL Adobe Experience Platform] audiences in [!DNL Target]. The [!DNL Target] team, [!DNL Experience Platform] [!DNL Destinations] team and the [!DNL Unified Profile Service] team is pleased to announce the general availability of the "Same Page/Next Page Personalization" use cases.<br>Using audiences created in [!DNL Adobe Experience Platform] provide richer customer data that leads to more impactful personalization. The [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCP), built on [!DNL Adobe Experience Platform] helps companies bring together known and anonymous data from multiple enterprise sources to create customer profiles that can be used to provide personalized customer experiences across all channels and devices in real time.<br>For more information, see [Use audiences from Adobe Experience Platform](/help/main/c-target/c-audiences/audiences.md#aep) in *Create audiences*.<br>Be sure to read the Adobe blog and watch the video: [[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] and [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}.|
|[!UICONTROL Audiences] UI refresh|As part of the [!DNL Adobe Target] team's ongoing effort to improve the user-experience for [!DNL Target] users, this release refreshes the [!UICONTROL Audiences] and [!UICONTROL Profile Scripts] pages in the [!DNL Target] UI. This update unifies and standardizes design patterns that were previously inconsistent, while adding new enhancements, such as:<ul><li>The ability to select and delete multiple audiences simultaneously</li><li>A refreshed [audience builder design](/help/main/c-target/c-audiences/create-audience.md)</li><li>Exclusion rule support in the [!UICONTROL Audience] library rule builder</li><li>A new "Audience Source" filter, to allow for faster audience discovery</li><li>Session persistent search and filter options</li><li>The ability to move audiences between workspaces for [!DNL Target Premium] customers.</li></ul>For more information, see [Audiences](/help/main/c-target/target.md).<br>**NOTE**: This feature will be rolled out to customers in different regions in the next eight weeks.|
|[!UICONTROL Profile Scripts] UI refresh|The [!UICONTROL Profile Scripts] library was also updated, and includes a refreshed interface along and several productivity updates:<ul><li>The ability to select and delete multiple profile scripts simultaneously</li><li>A new code editor for profile scripts</li><li>Syntax highlighting and error checking inside the code editor</li><li>Auto-complete tokens (mbox or profile) parameters through keyboard shortcuts</li></ul>For more information, see [Visitor Profiles](/help/main/c-target/c-visitor-profile/visitor-profile.md).<br>**NOTE**: This feature will be rolled out to customers in different regions in the next eight weeks.|

### [!DNL Target Standard/Premium] 22.1.1 (January 12, 2022)

This release includes bug fixes and pre-requisite capabilities for future integrations.

### Target Platform release (April 13, 2022)

This release contains the following update:

* Fixed issue to ensure that the last octet of IP addresses are properly obfuscated when captured using profile scripts. (TNT-44076)

### [!DNL Target Standard/Premium] 22.3.1 (April 5, 2022)

This release contains the following changes and enhancements:

* Fixed an issue that caused the [!UICONTROL Include] and [!UICONTROL Exclude] options to be disabled for combined audiences when editing an activity. (TGT-43422)
* Fixed an issue that prevented some customers from seeing the list of available audiences while editing an activity. (TGT-43404)
* Fixed an issue that prevented some customers from deleting an IP address from the "[!UICONTROL IPs to exclude from [!DNL Target] reporting data]" list in [!UICONTROL Administration] > [!UICONTROL Reporting]. (TGT-43384)
* Fixed an issue that prevented the use of negative numbers in audience criterion that check that any variable is "greater than," "greater than or equal to," "less than," or "less than or equal to." (TGT-43367)
* Fixed an issue that prevented customers from seeing the [!UICONTROL Audience Details] card when creating combined audiences. (TGT-43303)

### at.js version 2.8.0 (January 7, 2022)

The [!DNL Target] at.js JavaScript library now collects feature usage and performance telemetry data. Personal data is not collected. Opt-out for this feature is available by setting `telemetryEnabled` to false in `targetGlobalSettings`. For more information, see [telemetryEnabled in targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}.

## Release notes - 2021

### at.js version 2.7.0 (October 28, 2021)

This release contains the following enhancement:

* Added support for [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components). This version of at.js is required to create and test personalized experiences and offers on custom elements and on elements inside custom elements. This functionality is included in the [!DNL Target Standard/Premium] 21.10.5 release.

### [!DNL Target Standard/Premium] 21.10.5 (October 28, 2021)

This maintenance release contains the following enhancement:

|Feature|Details|
| --- | --- |
|[!UICONTROL Visual Experience Composer] (VEC)|Added support for [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Personalized experiences and offers can be created and tested on custom elements and on elements inside custom elements.<br>For more information, see [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#custom).|

### [!DNL Target Standard/Premium] 21.10.4 (October 21, 2021)

This maintenance release contains the following enhancement:

|Feature|Details|
| --- | --- |
|Cart-based Recommendations|Added a new family of algorithms to deliver recommendations based on the contents of the visitor's cart.<br>For more information, see "Cart-Based" in [Create criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md), "Cart adds/cart views/checkout pages" and "Exclude items already in the visitor's cart" in [Plan and implement Recommendations](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}, and "Cart-Based" in [Base the recommendation on a recommendation key](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).|

### [!DNL Target Standard/Premium] 21.10.3 (October 19, 2021)

This maintenance release contains the following enhancements, fixes, and changes:

* Fixed issues that prevented customers from opening the [!UICONTROL A4T] panel in [!DNL Analysis Workspace] by clicking the [!UICONTROL View in Analytics] button in [!DNL Target] activity reporting. (TGT-42099, TGT-42100)
* Fixed an issue that caused the [!UICONTROL Edit Design] button to not display while editing [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] (XT) activities using the [!UICONTROL Form-Based Experience Composer]. (TGT-41980)
* Fixed an issue that prevented the [!UICONTROL Compatible] checkbox from displaying in criteria selection while creating a new [!UICONTROL Recommendations] activity. (TGT-42053)
* Fixed an incorrect error message that displayed when not being able to select [!DNL Analytics] as the reporting source (A4T) because of lack of [!DNL Analytics] permissions. (TGT-41954)
* Implemented multiple accessibility fixes to improve keyboard navigation across the [!DNL Target] UI.

### [!DNL Target Standard/Premium] 21.10.2 (October 13, 2021)

The following enhancements have been added when using [!DNL Target] [!UICONTROL Audiences] with the [!DNL Adobe Experience Platform Web SDK]:

* Added warning icons, popovers, and messages in various places in the [!DNL Target] UI to indicate that the audience was deleted at the source and is no longer available for use in [!DNL Target] activities.

  The following illustrations show some of the places the icons, popovers, and messages display:

  * [!UICONTROL Activity] list page

    ![Audience deleted at source message on Activities list page](assets/deleted-at-source-audiences-list.png)

  * Activity [!UICONTROL Overview] pages:

    ![Audience deleted at source message on overview page](assets/deleted-at-source-overview.png)

  * [!UICONTROL Experiences] step of the activity-creation workflow:

    ![Audience deleted at source message on [!UICONTROL Experiences] page](assets/deleted-at-source-experiences.png)

  * [!UICONTROL Targeting] step of the activity-creation workflow:

    ![Audience deleted at source message on [!UICONTROL Targeting] page](assets/deleted-at-source-targeting.png)

  * [!UICONTROL Goals & Settings] step of the activity-creation workflow:

    ![Audience deleted at source message on the [!UICONTROL Goals & Settings] page](assets/deleted-at-source-goals-settings.png)

  * Audience refinements ([!UICONTROL Replace Audience] on the [!UICONTROL Targeting] step of the activity-creation workflow):

* If you attempt to use the Combine Audiences feature and one of audiences was deleted at the source, [!UICONTROL Save] is disabled. 

### [!DNL Target Standard/Premium] 21.10.1 (October 6, 2021)

This release contains the following new features:

|Feature|Details|
| --- | --- |
|[!UICONTROL Audiences] UI refresh|As part of the [!DNL Adobe Target] team's ongoing effort to improve the user-experience for [!DNL Target] users, this release refreshes the [!UICONTROL Audiences] and [!UICONTROL Profile Scripts] pages in the [!DNL Target] UI. This update unifies and standardizes design patterns that were previously inconsistent, while adding new enhancements, such as:<ul><li>The ability to select and delete multiple audiences simultaneously</li><li>A refreshed [audience builder design](/help/main/c-target/c-audiences/create-audience.md)</li><li>Exclusion rule support in the [!UICONTROL Audience] library rule builder</li><li>A new "Audience Source" filter, to allow for faster audience discovery</li><li>Session persistent search and filter options</li></ul>For more information, see [Audiences](/help/main/c-target/target.md).|
|[!UICONTROL Profile Scripts] UI refresh|The [!UICONTROL Profile Scripts] library was also updated, and includes a refreshed interface along and several productivity updates:<ul><li>The ability to select and delete multiple profile scripts simultaneously</li><li>A new code editor for profile scripts</li><li>Syntax highlighting and error checking inside the code editor</li><li>Auto-complete tokens (mbox or profile) parameters through keyboard shortcuts</li></ul>For more information, see [Visitor Profiles](/help/main/c-target/c-visitor-profile/visitor-profile.md).|
|[!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="See what's included in Target Premium."} Recommendations Criteria create and edit|The [!UICONTROL Recommendations Criteria] creation and editing workflow has been streamlined to simplify choosing the right recommendations algorithm and settings to achieve your goals.<br>For more information, see [Create criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).|
|![Premium badge](/help/main/assets/premium.png) Recommendations lookback window and algorithm refresh rate improvements|You can now run "Most Viewed" and "Top Sellers" algorithms with a six-hour lookback window to capture the content that's trending most recently. When the six-hour lookback window is selected, your recommendations results are updated every 3-6 hours throughout the day.<br>For more information, see [Data Source](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in *Create criteria*.|

### [!DNL Target Standard/Premium] 21.9.1 (September 14, 2021)

This maintenance release contains the following enhancements, fixes, and changes.

* Fixed issues that prevented customers from logging in to the [!UICONTROL Visual Experience Composer] (VEC) due to new security policies for third-party cookies in some web browsers. This issue was discussed in "Pages not loading in the Visual Experience Composer (VEC) or Enhanced Experience Composer (EEC) when using Google Chrome version 80+" in [Troubleshooting Issues Related to the Visual Experience Composer and Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).
* Fixed an issue that caused offer names in the VEC to display the offer's path instead of the offer's friendly name. (TGT-41300)
* Experience names are now reflected in [!DNL Analysis Workspace] for A4T activities (TGT-38674) 
* Fixed an issue in [!DNL Recommendations] that erroneously applied entity ID changes in a promotion in a duplicated activity to the original activity. (TGT-41482)
* Fixed an issue that prevented the "Edit Criteria" button from displaying properly on the [!UICONTROL Experiences] page for [!DNL Recommendations] activities in the VEC. (TGT-39512)
* Fixed an issue that prevented synchronization of activities when duplicated and copied to a test workspace. (TGT-40686)
* Fixed an issue that prevented modifications to a selector with [experience fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) when using "[!UICONTROL Insert After]" in the VEC. (TGT-41802)
* Fixed an issue that prevented empty JSON content in an offer from being sent to the backend. [!DNL Target] now sends the JSON object even though it is empty. (TGT-41555)
* Fixed an issue that caused legacy [!DNL Analytics] reporting to open instead of [!DNL Analysis Workspace] when customers clicked "[!UICONTROL View in Analytics]" while viewing a report. (TGT-41867)
* Added additional clarification to the displayed UI message when a customer attempts to select [!DNL Analytics] as the reporting source (A4T) for an [!UICONTROL Automated Personalization] activity. The message states that, "[!DNL Target] is the only supported source for [!UICONTROL Automated Personalization] activities." (TGT-41954)
* Added additional clarification to the error message when customers attempt to separate hosts with "newline" instead of commas. (TGT-40671) 
* Fixed an issue that caused some activities' "[!UICONTROL Last Updated]" dates to differ from the English UI for Spanish and Japanese customers (when viewing the UI in Spanish and Japanese). (TGT-38980) 

### at.js 2.6.1 (August 16, 2021)

* Bug fix for "No cached artifact available for hybrid mode" when using on-device decisioning.

### [!DNL Target] node.js SDK 2.2.0 (August 11, 2021)

* Added SDK telemetry data collection
* Automated Delivery API client openapi codegen

For more information about this and previous releases, see the [Change log](https://github.com/adobe/target-nodejs-sdk/blob/main/CHANGELOG.md) in the [Target node.js SDK documentation](https://github.com/adobe/target-nodejs-sdk) on Github.

### [!DNL Target Standard/Premium] 21.8.1 (August 10, 2021)

This maintenance release contains many backend enhancements, including the following customer-facing change:

* Fixed an issue that caused reports for [!UICONTROL Auto Personalization] activities created in the [!UICONTROL Form-Based Experience Composer] to reference deleted offers in reports. This issued caused the following error message to display, "We are having trouble retrieving data for this report. Please contact Adobe Client Care if the problem persists." (TGT-41028)

### Target Delivery API (August 3, 2021)

This release contains the following enhancements:

* The limit for mbox parameters has been increased to 100 parameters. The previous limit was 50 parameters. (TNT-41717)
* The limit for `categoryId` has been increased to 256 characters. The previous limit was 128 characters.
* The following [!DNL Adobe Audience Manager] (AAM) details have been added to the Delivery API:    

  * AAM UUID: The internal AAM ID used to uniquely identify a user. 
  * dataPartnerId: The ID for a data partner.
  * dataPartnerUserId: The user ID provided by a data partner.
  
  Previously, the Delivery API included `dcsLocationHint` and `blob` only. (TNT-41644)

### [!DNL Target Standard/Premium] 21.6.1 (June 30, 2021)

This release contains the following new features and enhancements. The issue numbers in parentheses are for internal [!DNL Adobe] use.

|Feature|Details|
| --- | --- |
|[!UICONTROL Analytics for Target] (A4T)|Clicking the "[!UICONTROL View in Analytics]" link on the [!UICONTROL Reports] page from an activity that uses [!DNL Analytics] as the reporting source (A4T), [!DNL Analysis Workspace] now opens. Previously, the link opened [!DNL Analytics] reporting. (TGT-36959)|

### Python SDK 1.0.0 (June 16, 2021)

The new [!DNL Adobe Target] Python SDK with on-device decisioning capabilities is now available. This newest addition bolsters the [!DNL Target] suite of server-side SDKs. These SDKS help you integrate with [!DNL Target] and expedite your time to value, in the language of your choice. Server-side integrations are becoming a popular choice given that the market is shifting to a cookie-less world in which first-party data is valuable. Target SDKs are available in the most popular programming languages in the market (Python, Java, JavaScript, C# / .Net).

For more information, see the [Python SDK documentation](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/python/overview.html){target=_blank} in the [Adobe Target Developer Guide](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.

### Target Standard/Premium 21.5.1 (June 7, 2021)

This release includes the following enhancements:

|Feature|Details|
| --- | --- |
|![Premium badge](/help/main/assets/premium.png) [!DNL Recommendations] [!UICONTROL Catalog Search] API|Search your [!DNL Recommendations] product and content catalog programmatically via API to identify items that match a search criteria and simplify administration of your catalog.<br>**Limitations and notes**:<ul><li>Catalog search via API is not supported for environments with more than 2,000,000 items.</li><li>Catalog search results via API are updated more rapidly than catalog search results via the [!DNL Target] UI. The catalog search in the [!DNL Target] UI can take additional time to reflect the latest results.</li></ul>For more information, see [Searching Entities](https://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) in the *[!DNL Adobe Target] [!DNL Recommendations] API* guide.|

This release maintenance release contains the following fixes.

* Fixed an issue that caused the default workspace to change to another workspace when refreshing the [!UICONTROL Audiences] page. (TGT-38871)
* Fixed an issue in [!UICONTROL Administration] > [!UICONTROL Implementation] that sometimes caused an error message stating, "Your global mbox may not be in sync. Please try resaving it."

### ![Adobe Experience Platform Web SDK badge](/help/main/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] version 2.5.0 (June 1, 2021)

This release of the [!DNL Platform Web SDK] includes support for the following:

|Feature|Details|
| --- | --- |
|Redirect support with [!UICONTROL Analytics for Target] (A4T)|The Platform Web SDK now supports [!DNL Target] redirects when using [A4T](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>For more information, see see [Analytics for [!DNL Target] implementation](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).|

### at.js version 2.5.0 (May 13, 2021)

This release of at.js includes the following enhancements and changes:

* [On-device decisioning](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html){target=_blank} support for at.js.
* [Preview links](/help/main/c-activities/c-activity-qa/activity-qa.md) support for Automated Personalization activities

This release also removes support for Microsoft Internet Explorer 10, Internet Explorer 11, and all older versions. Microsoft Edge continues to be supported in at.js 2.5.0 and later.

### Target Standard/Premium 21.4.1 (April 19, 2021)

This release contains the following new features and enhancements. The issue numbers in parentheses are for internal [!DNL Adobe] use.

|Feature|Details|
| --- | --- |
|On-device decisioning support for at.js<br>(Date to be announced)|On-device decisioning lets marketers and developers deliver experimentation and personalization on a user's browser at near-zero latency.<br>For more information, see [On-device decisioning for at.js.](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html){target=_blank}|
|![Premium](/help/main/assets/premium.png) List-based operators for entity filtering rules|[!DNL Target Recommendations] supports new list-based operators for entity filtering rules. (TGT-39234)<br>Newly added operators include:<br><ul><li>Is Contained In List</li><li>Is Not Contained In List</li><li>List Contains An Item In</li><li>List Does Not Contain An Item In</li><li>List Contains All Items In</li><li>List Does Not Contain All Items In</li></ul>For more information, see "Available operators" in [Use dynamic and static inclusion rules](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators).|

This release contains the following fixes.

* Fixed an issue that prevented an activity from syncing after changing the audience to [!UICONTROL All Visitors]. (TGT-40259)
* Fixed an issue that prevented offers from being duplicated when used in different locations in [!UICONTROL Automated Personalization] activities even though the [!UICONTROL Disallow Duplicates] option is enabled. (TGT-39567)
* Fixed an issue that prevented the [!UICONTROL Administration] > [!UICONTROL Scene7 configuration] page from loading properly. (TGT-39918)
* Fixed an issue that caused properties to be mapped to the incorrect workspace. (TGT-39869)
* Fixed an issue that caused infinite loading if the request fails after changing the environment while creating a recommendations exclusion. (TGT-39948)

### at.js 2.4.1 (March 23, 2021)

This release of at.js is a maintenance release and includes the following enhancements and fixes:

* Fixed an issue with `targetPageParams` being included in mbox requests. `targetPageParams` should be included in `pageLoad` requests only. (TNT-40247)
* Fixed an issue with document and window global objects in the [!DNL Adobe Experience Platform Launch] extension by replacing the Platform Launch global object dependencies with direct references to them. (TNT-37124)

### IP address changes for Recommendations feed-processing servers (March 16, 2021)

The [!DNL Target Recommendations] feed-processing server IP addresses were updated on March 16, 2021. For more information, see [IP addresses used by Recommendations feed-processing servers](/help/main/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md).

### Target Standard/Premium 21.2.1 (March 9, 2021)

This maintenance release contains the following enhancements, fixes, and changes.

The issue numbers in parentheses are for internal [!DNL Adobe] use.

* Increased the allowable offer size (TGT-38304):

  |Type|Previous Limit|New Limit|
  | --- | --- | --- |
  |HTML|256 KB|1024 KB|
  |Visual offers from the Target UI|64 KB|1024 KB for each experience|
  |Via API|512 KB|1024 KB|

* [!UICONTROL Personalization Insights] reports for [!UICONTROL Auto-Target] (AT) and [!UICONTROL Automated Personalization] (AP) activities are now produced daily. You can choose a report providing [!UICONTROL Automated Segments] or [!UICONTROL Important Attributes] for the last 15, 30, and 60 days. The 45-day and 90-day options have been removed to enable the other lookback window settings to run daily. (TGT-39472)
* Fixed an issue that caused the current dependency to not display when customers click [!UICONTROL Edit Dependency] on an activity's [!UICONTROL Goals & Settings] page. (TGT-39340)
* Fixed an issue when refreshing a workspace's [!UICONTROL Audience Library]. Before the refresh, the audiences for the currently selected workspace displayed. After the refresh, the [!UICONTROL Default Workspace] and its audiences displayed. The current workspace and its audiences now persist after the refresh. (TGT-38871) 
* Fixed an issue when copying a [!UICONTROL Recommendations] activity and later editing the original activity by changing its criteria sequence. The change in the criteria sequence in the original activity was also incorrectly applied to the copied activity. (TGT-39155)
* Fixed an issue that caused the incorrect number of products to display for [!UICONTROL Recommendations] exclusions. (TGT-39599)

### Target Standard/Premium 21.1.1 (January 19, 2021)

This maintenance release contains the following enhancements, fixes, and changes.

The issue numbers in parentheses are for internal [!DNL Adobe] use.

* Added a warning when selecting an [!DNL Adobe Analytics] metric when using [!UICONTROL Analytics as the reporting source] (A4T) in an [!UICONTROL Auto-Target] activity. [!UICONTROL Auto-Target] models are optimized to work with binary (conversion-based) metrics. Selecting a continuous metric, such as revenue, might have sub-optimal outcomes and the [!UICONTROL Personalization Insights] reports might not be accurate. (TGT-38926)
* Added a status icon in the [!UICONTROL Auto-Target Summary] report for [!UICONTROL Auto-Target] activities that use A4T. The green check icon next to each experience in the report indicates that a personalized machine-learning model has been generated for that experience. The clock icon indicates that not enough traffic has been served to build the model. (TGT-38925)
* The [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes] reports for [!UICONTROL Auto-Target] activities that use A4T and [!DNL Analytics] conversion metrics are generated and look the same as when using [!DNL Target] as the reporting source. (TGT-38931)
* Added an environment filtering option to the [!UICONTROL Recommendations] [!UICONTROL Collections] list. (TGT-38353)
* Fixed an issue that caused the incorrect product count to display in [!UICONTROL Recommendations] collections. (TGT-39162)
* Added a [!UICONTROL Last Updated] filter to the [!UICONTROL Recommendations] [!UICONTROL Catalog Search]. (TGT-38340)
* Fixed an issue in [!UICONTROL Recommendations] that caused the [!UICONTROL Create Sequence] page to hang after changing the industry vertical. (TGT-38160)
* Fixed an issue that prevented users from removing an audience from an offer in an [!UICONTROL Automated Personalization] (AP) activity. (TGT-39058)
* Fixed an issue that caused the incorrect time frame (start and end dates) to display in [!UICONTROL Audience Info] cards for some customers. (TGT-39150)
* Fixed an issue that prevented some customers from seeing the list of activities in the [!UICONTROL Default Workspace]. (TGT-38526)

### at.js 2.4.0 (January 14, 2021)

This release of at.js is a maintenance release and includes the following fixes:

* Adds support for unified profile/platform id to delivery API customerIds.
* Fixes invalid style tag injection.

## Release notes - 2020

### Target Standard/Premium 20.10.1 (October 27, 2020)

This release contains the following new features:

|Feature|Details|
| --- | --- |
|On-device decisioning|On-device decisioning lets both marketers and product developers deliver experimentation and Machine Learning-driven personalization from within a user's device, across channels, at near-zero latency.<br>Speed and performance matters--in customer insights and user satisfaction.<br>On-device decisioning lets you compile key personalization and experimentation instructions in A/B Test and Experience Targeting (XT) activity types into "optimization artifacts:" JSON objects that are loaded onto customer devices via the CDN. And because on-device decisioning connects natively with [!DNL Adobe Experience Cloud] products, [!DNL Target] users get rapid analysis and faster experience iterations.<br>For more information, see *[On-device decisioning for at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html){target=_blank} and [Introduction to on-device decisioning](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html){target=_blank} for server-side.|

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that prevented [!UICONTROL Average Lift Confidence Interval] and [!UICONTROL Confidence] from displaying in [!DNL Auto-Target] reporting for the [!UICONTROL Total] row. Measurements displayed correctly for all individual experiences. (TGT-37301)
* Fixed an issue that impacted [!DNL Adobe Target Premium] users' [!UICONTROL Auto-Target] reporting from September 15, 2:30 p.m. (PDT) to October 6, 9:25 a.m. (PDT). When viewing reports for the impacted conversion metrics (configured using either the "[!UICONTROL Viewed a page]" or "[!UICONTROL Clicked on mbox]" option), the conversions rates are incorrectly reported. There is no known delivery issue at this time.
* Added a selectable [!UICONTROL Last Updated At] column in the [!UICONTROL Catalog Search] table and a [!UICONTROL Last Updated At] filter. This enhancement saves time and effort because you don't have to open each individual item to see when it was last updated and you can filter by date the items were last updated.

  ![Last Updated at column and filter illustration](/help/main/r-release-notes/assets/column-and-filter.png)

* Updates were made to help make the Target UI compliant with [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Level A and AA Success Criteria (WCAG 2.0 AA). (TGT-34384 & TGT-24679)
* Made Content Security Policy (CSP) improvements. (TGT-37035)
* Introduced a way to specify the client code as a parameter for customers using CNAME. (TNT-38571)
* [!DNL Adobe Experience Cloud] documentation is moving to [!DNL Experience League]. During October, all release notes, articles, videos, and tutorials will move from their current location at `docs.adobe.com` to [!DNL Experience League]. This move ensures that all learning, self-help, enablement, and community content is served from a single location. When this change occurs, there is nothing you need to do, as all links will be redirected to [!DNL Experience League]. We will update the release notes when the cutover begins.

### Target Standard/Premium 20.9.1 (September 30, 2020)

This maintenance release contains the following enhancements, fixes, and changes:

* Improved navigation and functionality for keyboard-only users. (TGT-34487, TGT-34516, TGT-34517, TGT-34514)
* Added labels in the UI to aid users using assistive technologies. (TGT-34500, TGT-34501, TGT-34502, TGT-24504)
* Improved text and color contrast for images and text in UI. (TGT-34513)

### Target Standard/Premium 20.8.3 (September 15, 2020)

|Feature|Details|
| --- | --- |
|![Premium badge](/help/main/assets/premium.png) Analytics for Target (A4T) support for Auto-Target activities|[!UICONTROL Auto-Target] activities now support [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>This integration allows you to use the [!UICONTROL Auto-Target] ensemble machine learning algorithm to choose a best experience for each visitor based on their profile, behavior, and context.<br>If you've already [implemented A4T](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md) for use with A/B Test and Experience Targeting activities, you're all set!<br>For more information, see [A4T support for Auto-Allocate and Auto-Target activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).|

### Target Standard/Premium 20.8.2 (September 10, 2020)

|Feature|Details|
| --- | --- |
|![Premium badge](/help/main/assets/premium.png) Control recommendations slots within criteria sequences|Criteria Sequences now allow you to control the number of slots taken up by each recommendations criteria, enabling you to mix and match different types of items or different algorithm logic.<br>See [Create criteria sequences](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) to learn more.|

### Target Standard/Premium 20.8.1 (September 2, 2020)

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that caused errors to display when loading the new [!UICONTROL Administration] pages after switching organizations. (TGT-37730)
* Fixed a display issue that caused the incorrect client code to display on the [!UICONTROL Administration > Implementation] page. (TGT-37849)
* Fixed an issue that sometimes prevented users from using the editing features in the [!UICONTROL Visual Experience Composer] (VEC) after successfully loading the VEC. (TGT-37162)
* Fixed an issue that prevented pages from loading in the VEC and Enhanced Experience Composer (EEC) even though the VEC Helper extension was installed. This was due to changes in Google Chrome 80+. Download the [updated VEC Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md). (TGT-37893) 
* Fixed an issue that sometimes prevented users from downloading at.js from the [!UICONTROL Administration > Implementation] page after switching organizations. (TGT-37668)
* The at.js download button is now disabled while loading to prevent [!DNL Target] from sending multiple requests if users click the download button multiple times. (TGT-37633)
* Fixed an issue in [!UICONTROL Experience Targeting] (XT) activities that caused experiences to display "fetching results" for an extended period of time. (TGT-37684)
* Improved navigation and functionality for keyboard-only users. (TGT-34479 & TGT-34473)
* Added labels in the UI to aid users using assistive technologies. (TGT-34480)
* Improved the error message when deleting a mobile viewport that is currently used in an activity. The error message now reads: "This viewport is currently associated to one or multiple activities. You need to remove the viewport from those activities before being able to delete it." (TGT-37030)
* Added support in the VEC to allow click tracking on a css selector that matches more than one element in the page. (TGT-37323)
* Fixed an issue that prevented certain users from displaying the [!UICONTROL Activity] list. The following error message was displayed: "Unable to fetch URLsuggestions." The error occurred for users using carriage returns in their FirstName (FirstName/r/n) in the Adobe Backend system. (TGT-37330)
* Fixed an issue that prevented users from displaying the [!UICONTROL Activity] page if the workspace name (specified in the [!UICONTROL Adobe Admin Console for Enterprise]) contains an apostrophe. (TGT-37709)
* Fixed an issue in [!UICONTROL Auto-Allocate] activities while selecting optimization and conversion metrics where an error message incorrectly informed users to select a report suite, even though a report suite was already specified. (TGT-37689)
* Fixed an issue that sometimes caused metrics on the [!UICONTROL Goals and Settings] page to be blank after navigating to the [!UICONTROL Targeting] page and then back. (TGT-37691)
* Fixed an issue that caused an incorrect last-modified value for [!DNL Recommendations] criteria. (TGT-37666)
* Fixed an issue that caused mbox IDs to display in the Mboxes drop-down list instead of mbox names. (TGT-37739)

### at.js 2.3.2 (July 24, 2020)

This release of at.js is a maintenance release and includes the following fix:

* Fixed a bug when a script or code adds default property to the window or document.

### Target Standard/Premium 20.7.1 (July 27, 2020)

This release includes the following changes:

#### [!UICONTROL Administration] section UI refresh

We are gradually rewriting the entire [!DNL Target] UI using a new tech stack to be able to offer improved performance, reduce the maintenance time required when releasing new features, and to improve the user experience across the product. The first section refreshed is the [!UICONTROL Setup] section, which has been renamed [!UICONTROL Administration].

As part of this refresh, you will be able to easily perform many actions using the pages in the [!UICONTROL Administration] section, such as:

* Download the latest at.js file from the [!UICONTROL Implementation] tab (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Customize your at.js settings and be able to easily review your changes (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Modify enhanced reporting settings, such as the default currency and time zone, IPs to exclude from reporting, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]**)
* Obfuscate visitor IP addresses for privacy reasons (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* View the existing list of users per workspace and their roles, before managing them in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**).
* Search and filter all tables in the [!UICONTROL Administration] section.

For more information, see [Administer Target Overview](/help/main/administrating-target/administrating-target.md).

#### Enhancements, fixes, and changes

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that prevented site preferences from being retained after refresh. (TGT-37239)
* Fixed an issue that prevented [!UICONTROL Insert After] > [!UICONTROL Image] from functioning properly with Scalable Vector Graphics (SVG) images. (TGT-37242)
* Fixed an issue for users with the [!UICONTROL Publisher] role that prevented the deletion of draft activities. (TGT-37358)
* Fixed an issue that prevented users from editing an activity when [!UICONTROL All My Workspaces] is selected. (TGT-37276)

### Target Standard/Premium 20.5.1 (June 17, 2020)

|Feature / Enhancement|Description|
| --- | --- |
|Analytics for Target (A4T) support for [!UICONTROL Auto-Allocate] activities|[!UICONTROL Auto-Allocate] activities now support [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>This integration allows you to use the [!UICONTROL Auto-Allocate] multi-armed bandit capability to drive traffic to winning experiences, while using an [!UICONTROL Adobe Analytics] goal metric and/or [!UICONTROL Adobe Analytics] reporting and analysis capabilities.<br>If you've already [implemented A4T](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md) for use with A/B Test and Experience Targeting activities, you're all set!<br>For more information, see [A4T support for Auto-Allocate and Auto-Target activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).|
|Response tokens for Traffic Allocation Method for Auto-Target and Automated Personalization activities|Two [response tokens](/help/main/administrating-target/response-tokens.md) have been added to [!UICONTROL Auto-Target] and [!UICONTROL Automated Personalization] activities to enable determination of whether a visitor received a particular experience as a result of being assigned to "control" or to "targeted" traffic.<ul><li>`experience.trafficAllocationId` will return 0 if a visitor received an experience from being in "control" traffic and 1 if a visitor received an experience from the "targeted" traffic distribution.</li><li>`experience.trafficAllocationType` will return "control" or "targeted."</li></ul>For more information on control vs. targeted traffic, see [Select the control for your Automated Personalization or Auto-Target activity](/help/main/c-activities/t-automated-personalization/experience-as-control.md).|
|[!UICONTROL Publisher] role|This new role is similar to the current [!UICONTROL Observer] role (can view activities, but cannot create or edit them). However, the [!UICONTROL Publisher] role has the additional permission to activate activities.<br>For more information, see: <ul><li>**Target Standard users**: [Specify roles and permissions](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Users*.</li><li>**Target Premium users**: [Step 6: Specify roles and permissions](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configure enterprise permissions*.</li></ul>|
|A4T support in [!DNL Analysis Workspace]<br>June 25, 2020|[!UICONTROL Anaytics for Target] (A4T) is now supported in [!DNL Analysis Workspace]. The [!UICONTROL Analytics for Target (A4T) panel] lets you analyze your [!DNL Adobe Target] activities and experiences in [!DNL Analysis Workspace].<br>For more information, see [Reports in Analytics](/help/main/c-integrating-target-with-mac/a4t/reporting.md) in *A4T reporting* and [Analytics for Target (A4T) panel](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) in the *Analytics Tools Guide*.|

**Enhancements, fixes, and changes**

* Fixed an issue that caused the "visitors" metric to be stored in the activity's definition instead of "UniqueVisitors." (TGT-37098)
* Fixed an issue in the [!DNL Target] UI that caused the vertical scrollbar to not function correctly on the [!UICONTROL Audiences] page. (TGT-36968)

### at.js 1.8.2 and at.js 2.3.1 releases (June 15, 2020)

The following improvements and fixes have been made in the [!DNL Target] at.js libraries:

|Feature / Enhancement|Description|
| --- | --- |
|at.js 1.8.2|This release of at.js is a maintenance release and includes the following fix:<ul><li>Fixed an issue when using CNAME and edge override, at.js 1.*x* might incorrectly create the server domain, which resulted in the [!DNL Target] request failing. (TNT-35064)</li></ul>For more information, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.|
|at.js 2.3.1|This release of at.js is a maintenance release and includes the following enhancements and fixes:<ul><li>Made the `deviceIdLifetime` setting overridable via [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}. (TNT-36349)</li><li>Fixed an issue when using CNAME and edge override, at.js 2.*x* might incorrectly create the server domain, which resulted in the [!DNL Target] request failing. (TNT-35065)</li><li>Fixed an issue when using the [!DNL Target] [!DNL Launch] extension v2 and the [!DNL Adobe Analytics] [!DNL Launch] extension, [!DNL Target] delayed the [!DNL Analytics] `sendBeacon` call. (TNT-36407, TNT-35990, TNT-36000)</li></ul>For more information, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.|

### Profile Batch Status API v2 changes (May 14, 2020)

With the May 20 release, Profile Batch status will return only row-level failure data going forward (success data will not be returned). Failed profile IDs will be returned by the API going forward. 

The previous and new API responses are as follows:

`ProfileBatchStatus Api`
`http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**Currently we see the response as:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>1514187733806-729395</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>1573612762055-214017</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

**After May 4, the response will be:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

### Target Standard/Premium 20.4.1 (May 6, 2020)

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that incorrectly qualified a device and browser type for an audience. (TGT-36266)
* Fixed an issue that prevented report data from displaying when viewed on screens less than 963 pixels wide. (TGT-36549)
* Fixed an issue that caused Auto Personalization reports to not render correctly. (TGT-36619)
* Fixed an issue that allowed incompatible metrics to be selected in Auto-Allocate and Auto-Target activities that use Analytics for Target (A4t). (TGT-36646)
* Fixed an issue that caused certain options in the Visual Experience Composer (VEC) to not display correctly. (TGT-36571)
* Fixed an issue in the Target UI that caused other Recommendations offer previews to display the edited content after a user replaced the content in a single experience. (TGT-36053 & TGT-36894)
* Fixed an issue that prevented some users from deleting items from a Recommendations catalog. (TGT-36455)
* Fixed an issue that prevented users from saving Recommendations criteria on a multi-page activity. (TGT-36249)
* Fixed an issue that caused the behavioral data source radio buttons to disappear when editing the criteria for a second consecutive time. (TGT-36796)
* Fixed a display issue that caused a Recommendations algorithm to display "fetching results" for an extended period. (TGT-36550 & TGT-36551)
* Updated many UI strings localized in various languages.

### Target at.js (March 25, 2020)

The following new versions of the Target at.js JavaScript libraries are available:

* at.js version 2.3.0
* at.js version 1.8.1

For more information, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

### Target Standard/Premium 20.2.1 (March 23, 2020)

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that prevented customers from selecting a collection when performing a catalog search. (TGT-36230)
* Fixed an issue in which a criteria created via API, but not referenced by an activity created in the Target UI, could be erroneously deleted from the UI. (TGT-35917)
* Implemented security improvements to the Content Security Policy (CSP). (TGT-36190)
* Fixed an issue that caused "NaN%" to display when sliding the Attribute Weighting percentage bar to the far left. (TGT-36211)
* Resolved localization issues so that UI text in various languages displays correctly.
* We've standardized the list of available metrics from Adobe Analytics for Target (A4T) activities by deprecating Adobe Analytics metrics not supported in the current version of Adobe Analytics APIs. This will enable us to extend our A4T support in future Adobe Target releases. 

  The following changes have been made:

  * "Average Time Spent on Page" has been replaced by "Average Time Spent on Site." Any activities using this as metric the Primary Goal Metric will have "Average Time Spent on Site" (note: measured in minutes rather than seconds) selected as the Primary Goal Metric the next time the activity is edited.
  * "Visitors" has been replaced by "Unique Visitors." Any activities using this metric as the Primary Goal Metric will have "Unique Visitors" selected as the Primary Goal Metric the next time the activity is edited.

* The following metrics have been deprecated and can no longer be selected as the Primary Goal Metric when creating a new A4T activity.

  |Deprecated Metric(s)|Suggested Replacement Metric(s)|
  |--- |--- |
  |Daily Visitors, Hourly Visitors, Monthly Visitors, Quarterly Visitors, Weekly Visitors, Yearly Visitors|Unique Visitors|
  |Average Visit Depth|n/a. Not suggested as a primary goal metric|
  |Bots|n/a. Not suggested as a primary goal metric|
  |Mobile Crash Rate, Mobile Avg Prev Session Length, Mobile App Store Avg Rank, Mobile App Performance Crash Rate, Mobile App Store Avg Rating|n/a. Not suggested as a primary goal metric|

### Adobe Experience Cloud navigation (February 22, 2019)

* When you log in to the [!DNL Adobe Experience Cloud], you will be taken to the new header navigation. It looks very similar to the previous navigation with the black bar at the top, but it provides the following improvements:

  * Easier switching between [!DNL Identity Management System] (IMS) organizations or to a different solution.
  * Improved user help: Search results include results from the [!DNL Target] product documentation, as well as community forums and more video content, giving you easier access to more content to help get the most out [!DNL Target]. We've also added a feedback mechanism right in the [!UICONTROL Help] menu, making it easier to report issues or to share your ideas.

  * Improved Net Promoter Score (NPS) feedback functionality, so the survey modal doesn't disturb your flow of work.
    
  * Notifications for [!DNL Target] are not currently available in the [!UICONTROL Notifications] drop-down in the header.

  >[!NOTE]
  >
  >As part of the rollout of the new navigation bar, you will also notice some URL changes. All previous bookmarked links continue to work but we encourage you to bookmark new links for faster opening.

### Target Standard/Premium 20.1.1 (February 4, 2020)

The Target Standard/Premium 20.1.1 release is a maintenance release and includes backend enhancements and improvements. In addition, the following fixes are included:

* Fixed an issue that caused the Adobe Analytics tracking server field to be blank on the Goals and Settings page for existing Adobe for Target (A4T) activities. (TGT-35960)
* Fixed an issue in the user interface that caused your selection in the second drop-down list to not display while creating an audience for category affinity. (TGT-36098)

## Release notes - 2019 {#releases-2019}

### Target Java SDK version 1.1.0 (December 16, 2019)

* Support for proxy config added due to an open source contribution made by @hisham-hassan.

### Target Java SDK version 1.0.1 (November 11, 2019)

The following issue was fixed in version 1.0.1:

* Send supplemental data ID in a Target request even when there is no Visitor API cookie present.

### Target platform (October 31, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|Java SDK|The [!DNL Target] Java SDK lets you deploy [!DNL Target] server-side. This Java SDK helps you easily integrate [!DNL Target] with other [!DNL Adobe Experience Cloud] solutions, such as the [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics], and [!DNL Adobe Audience Manager].<br>The Java SDK introduces best practices and removes complexities when integrating with [!DNL Target] via our delivery API so that your engineering teams can focus on business logic. The following are notable features that we are introducing in the latest version:<ul><li>Support for prefetching and notifications that allows you to optimize for performance via caching.</li><li>Support for optimizing performance when you have a hybrid integration of [!DNL Target] on both your web pages and server-side. We are introducing a setting called `serverState` that is populated by experiences retrieved via the server-side so that at.js 2.2 will no longer make an additional server call to retrieve the experiences. This approach optimizes page load performance.</li><li>Support for retrieving VEC-created activities via the Java SDK, which is made possible by the new Delivery API.</li><li>Open sourced so your developers can contribute to the [Target Java SDK](https://github.com/adobe/target-java-sdk).</li></ul>Learn more about the Target Java SDK on the Adobe Tech Blog - [Server-Side Optimization with the new Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).|

### Target Standard/Premium 19.10.2 (October 31, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|![Premium badge](/help/main/assets/premium.png) Multi-value attribues|Sometimes you want to work with a multi-value field. Consider the following examples:<ul><li>You offer movies to users. A given movie has multiple actors.</li><li>You sell tickets to concerts. A given user has multiple favorite bands.</li><li>You sell clothing. A shirt is available in multiple sizes.</li></ul>To handle recommendations in these scenarios, you can pass multi-value data to Target Recommendations and use special multi-value operators.<br>For more information, see [Work with multi-value attributes](/help/main/c-recommendations/c-algorithms/work-with-multi-value-attributes.md).|

### Target Standard/Premium 19.10.1 (October 22, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|![Premium badge](/help/main/assets/premium.png) User-Based Recommendations<br>(October 24, 2019)|Recommends items based off of each visitor's browsing, viewing, and purchasing history. These items are generally referred to as "Recommended for You."<br>This criteria lets you deliver personalized content and experiences to both new and returning visitors. The list of recommendations is weighted towards the visitor's most-recent activity and is updated in-session and becomes more personalized as the visitor browses your site.<br>For more information, see "User-Based Recommendations" in [Criteria/Algorithms](/help/main/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms).|

**Adobe Experience Cloud navigation**

* When you log in to the [!DNL Adobe Experience Cloud], you will be taken to the new header navigation. It looks very similar to the previous navigation with the black bar at the top, but it provides the following improvements:

  * Easier switching between [!DNL Identity Management System] (IMS) organizations or to a different solution.
  * Improved user help: Search results include results from the [!DNL Target] product documentation, as well as community forums and more video content, giving you easier access to more content to help get the most out [!DNL Target]. We've also added a feedback mechanism right in the [!UICONTROL Help] menu, making it easier to report issues or to share your ideas.

  * Improved Net Promoter Score (NPS) feedback functionality, so the survey modal doesn't disturb your flow of work.
      
  * Notifications for [!DNL Target] are not currently available in the [!UICONTROL Notifications] drop-down in the header.

  >[!NOTE]
  >
  >These features will not be rolled out at once, nor will they be rolled out to all customers together. We will be rolling out these features over the course of the next few weeks, starting with the [!DNL Target Standard/Premium] 19.10.1 (October 22, 2019) release.
  >
  >As part of the rollout of the new navigation bar, you will also notice some URL changes. All previous bookmarked links continue to work but we encourage you to bookmark new links for faster opening.

### at.js versions 2.2 and 1.8 (October 10, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|at.js version 2.2<br>and<br>at.js version 1.8|These versions of at.js provide:<ul><li>Improved performance when using both Experience Cloud ID Service (ECID) v4.4 and at.js 2.2 or at.js 1.8 on your web pages.</li><li>Previously, the ECID made two blocking calls before at.js could fetch experiences. This has been reduced to a single call, which significantly improves performance.</li></ul> In order to take advantage of these performance improvements, upgrade to at.js 2.2 or at.js 1.8 along with ECID Library v4.4.<br>at.js 2.2 provides:<ul><li>**serverState**: A setting available in at.js v2.2+ that can be used to optimize page performance when a hybrid integration of Target is implemented. Hybrid integration means that you are using both at.js v2.2+ on the client-side and the delivery API or a Target SDK on the server-side to deliver experiences. `serverState` gives at.js v2.2+ the ability to apply experiences directly from content fetched on the server side and returned to the client as part of the page being served.<br>For more information, see "serverState" in [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}.</li></ul>|

### Target platform (October 9, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|Node.js SDK version 1.0|The Target Node.js SDK lets you deploy Target server-side.<br>This Node.js SDK helps you easily integrate Target with other Experience Cloud solutions, such as the Adobe Experience Cloud Identity Service, Adobe Analytics, and Adobe Audience Manager.<br>The Node.js SDK introduces best practices and removes complexities when integrating with Adobe Target via our delivery API so that your engineering teams can focus on business logic. The following are notable features that we are introducing in the latest version:<ul><li>Support for prefetching and notifications that allows you to optimize for performance via caching.</li><li>Support for optimizing performance when you have a hybrid integration of Target on both your web pages and server-side. We are introducing a setting called `serverState` that will be populated by experiences retrieved via the server-side so that at.js 2.2 will no longer make an additional server call to retrieve the experiences. This approach optimizes page load performance.</li><li> Support for retrieving VEC-created activities via the Node.js SDK, which is made possible by the new Delivery API.</li><li>Open sourced so your developers can contribute to the Node.js SDK.</li></ul>|
|Delivery API|An entirely new delivery API endpoint (/v1/delivery) is available in production. Notable features are:<ul><li>One endpoint to retrieve experiences for one or more mboxes.</li><li>Retrieve VEC-created activities via the API.</li><li>Support for an entirely new object called Views that is used for Single Page Applications (SPAs) and Mobile applications.</li></ul>|

### Target Standard/Premium 19.9.2 (September 30, 2019)

This maintenance release includes the following enhancement:

* Several security fixes, including a security update to the Rich Text Editor (RTE) in the Visual Experience Composer (VEC). (TGT-35383)
* Recommendations Offers can now be added to elements other than DIV (e.g. P, UL, H1), in addition to DIV, in A/B Test and Experience Targeting activities. (TGT-34333)
* Event notifications (the bell icon in the Target UI) is no longer available. A new look for notifications is coming soon.

### Target Standard/Premium 19.9.1 (September 10, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|![Premium badge](/help/main/assets/premium.png) Enterprise Permissions|With the Target September 2019 release, Enterprise Permissions provides customers with the following access controls:<UL><li>You can choose the workspaces to which the integration can be applied.</li><li>You can apply a role to the Adobe I/O integration: Approver, Editor, or Observer.</li></ul>For step-by-step instructions and more information, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/main/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).|

### Target Standard/Premium 19.7.1 (July 24, 2019) {#tgt-19-7-1}

This release includes the following new features and enhancements:

(The issue numbers in parentheses are for internal Adobe use.)

|Feature / Enhancement|Description|
| --- | --- |
|![Premium badge](/help/main/assets/premium.png)<br>Recommendations in A/B Test and Experience Targeting (XT) activities|The Recommendations offer (algorithm) status displays on the Overview page for A/B Test and XT activities that contain Recommendations offers. Statuses include: Results Ready, Results Not Ready, and Feed Failure. (TGT-33649)<br>See [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md#status).|
|Cross-domain tracking support for at.js 2.0+ via the Experience Cloud ID  (ECID) library|Previously, cross-domain tracking was not supported in at.js 2.*x*. With this release, customers using at.js 2.0 or above can now utilize cross-domain tracking through the ECID library. The ECID library must be installed on the page in conjunction with at.js 2.0 or above in order for cross-domain tracking to work. [Experience Cloud ID library 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) must be used.<br>See [Cross-domain tracking support in at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.|
|Target support for Apple's ITP 2.1 and ITP 2.2 via the Experience Cloud ID (ECID) library 4.3|Today, Target customers can mitigate Apple's ITP 2.1 and ITP 2.2 by leveraging Adobe's CNAME certification program.<br>With this release, Target introduces a seamless integration with the ECID library 4.3, which leverages a server-side cookie to mitigate ITP 2.1 and ITP 2.2. It is highly recommended that Target customers deploy [ECID library 4.3+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) in conjunction with Target's JavaScript library to mitigate any future ITP releases. The ECID library will continue to roll out enhancements that provide a robust solution to the ever-changing cookie policies introduced by browsers.<br>See [Apple Intelligent Tracking Prevention (ITP) 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/apple-itp-2x.html){target=_blank}.|

**Enhancement, fixes, and changes**

* Fixed an issue that prevented exclusion values in Recommendations activities from being cleared when adding duplicate values. (TGT-34996)
* You can now remove a design in a Recommendations activity from the Targeting page (Step 2 of the three-part guided workflow). Note that to remove a design, there must be more than one design selected. (TGT-35118)
* Fixed an issue that prevented custom criteria cards for some customers to load properly in the Target UI or to be editable. (TGT-35170)

### at.js version 2.1.1 (July 24, 2019)

This release of at.js is a maintenance release and includes the following enhancements and fixes:

(The issue numbers in parentheses are for internal Adobe use.)

* Fixed an issue that caused multiple beacons to fire when using the Click Tracking metric on the Goals & Settings page in the Visual Experience Composer (VEC). (TNT-32812)
* Fixed an issue that caused `triggerView()` to not render offers more than once. (TNT-32780)
* Fixed an issue with `triggerView()` to ensure that the request contains Marketing Cloud ID (MCID) information. (TNT-32776)
* Fixed an issue that prevented the `triggerView()` notification to fire even if there are no saved views. (TNT-32614)
* Fixed an issue that caused an error due to the use of decodeURIcomponent that caused issues when the URL contains a malformed query string parameter. (TNT-32710)
* The beacon flag is now set to "true" in the context of delivery requests sent via the `Navigator.sendBeacon()` API. (TNT-32683)
* Fixed an issue that prevented Recommendations offers from displaying on websites for a few customers. Customers could see the offer content in the delivery API call but the offer was not applied on the website. (TNT-32680)
* Fixed an issue that caused click-tracking across multiple experiences to not work as expected. (TNT-32644)
* Fixed an issue that prevented at.js from applying the second metric after the rendering of the first metric fails. (TNT-32628)
* Fixed an issue when passing `mboxThirdPartyId` using the `targetPageParams` function that caused the request payload to not be present in either the query parameters or in the request payload. (TNT-32613)
* Fixed an issue that caused display and click notification responses to be blocked in Chromium-based browsers (including Google Chrome). (TNT-32290)

For information about this and previous versions of at.js, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

### Target Standard/Premium 19.6.1 (June 26, 2019) {#tgt-19-6-1-historical}

This release includes the following new features and enhancements:

(The issue numbers in parentheses are for internal Adobe use.)

|Feature / Enhancement|Description|
| --- | --- |
|Visual Experience Composer (VEC)|**New VEC menu options**: When you click a page element in the VEC, a menu shows the options that are available for that element type.<ul><li>You can now use the [!UICONTROL Styles > Background] option to change the background image and color for the selected element. (TGT-15001)</li></ul>See *Styles* in [Visual Experience Options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**Click-tracking improvements**: We have improved the process for configuring click tracking within the VEC and the Single Page Application (SPA) VEC.<ul><li>While selecting elements to use in click tracking, the names of all available elements display in the Modifications panel on the right side, making it quick and easy to select the desired elements.</li><li>The [!UICONTROL Goals & Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. You can hover over this number to see the names of all selected elements. (TGT-33878)</li></ul>See [Click tracking](/help/main/c-activities/r-success-metrics/click-tracking.md).|
|Single Page App Visual Experience Composer (SPA VEC)|**Guided workflow**: A new guided workflow helps you understand how page-delivery-rule settings should be configured to execute and run an activity successfully for your Single Page App. (TGT-33718)<br> See [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**Clone modifications**: You can now define a modification using the SPA VEC and then clone that modification for use in other views in your Single Page App. (TGT-33882)<br>See [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md).|
|![Premium badge](/help/main/assets/premium.png) Automated Personalization (AP) & Auto-Target|**Specific experience as control**: You can select an experience to be used as control while creating an AP or Auto-Target activity. This feature lets you route the entire control traffic to a specific experience, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against control traffic to that one experience. The current control option (randomly served experiences) will continue to be available. (TGT-32801, TGT-26572, & TGT-26571)<br>See [Select the control for your Automated Personalization or Auto-Target Activity](/help/main/c-activities/t-automated-personalization/experience-as-control.md).<br>**Personalization Insights reports**: The marketer-friendly naming for attributes when a visitor sees a specific piece of content in a specific location provides more meaningful information. (TGT-33421 & TGT-34957)<br>See [Data collection for the Target personalization algorithms](/help/main/c-activities/t-automated-personalization/ap-data.md).|
|![Premium badge](/help/main/assets/premium.png) Recommendations|You can use the Recommend Previously Purchased Items toggle while creating Recently Viewed Items logic. (TGT-34030)<br>For more information, see [Recently Viewed Items](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#previously-purchased) in "Create criteria."|
|Google Chrome SameSite cookie policies|Google recently announced that starting with Chrome 76, which is slated for a July 30, 2019 release, developers must explicitly specify which cookies can work across websites and which cookies can track users.<br>As the industry makes strides to create a more secure web for consumers, Target is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors.<br>See [Google Chrome SameSite cookie policies](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/google-chrome-samesite-cookie-policies.html){target=_blank}.|

### at.js version 2.1.0 (June 3, 2019) {#atjs-210}

We are thrilled to announce the following exciting features in at.js 2.1.0:

|Feature / Enhancement|Description|
| --- | --- |
|Adobe Opt-in support|Adobe Opt-In is a way to simplify Adobe solutions integrations with consent management platforms.<br>For more information about Adobe Opt-in, see [Privacy and General Data Protection Regulation (GDPR)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation.html){target=_blank}.|
|Industry-standard CSP compliant|at.js no longer uses eval() to execute JavaScript.|
|Client-side analytics logging|Gives customers full control on how they want to send analytics data to Adobe Analytics, whether on the client-side or server-side.<br>For more information, see [Client-side Analytics logging](/help/main/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Before you implement*.|
|Send notifications|Allows developers to send notifications when an experience is rendered by their code instead of using `applyOffer()` or `applyOffers()`.<br>For more information, see [adobe.target.sendNotifications(options)](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-sendnotifications-atjs-21.html){target=_blank}.|
|Reduced file size|The size of at.js is reduced by ~24%. The smaller file size improves page load performance and reduces the time to download at.js on the page.|
|at.js documentation updates|For a full list of all articles updated due to the at.js 2.1.0 release, see the June 3, 2019 entries in [Documentation changes](/help/main/r-release-notes/doc-change.md).|

### [!DNL Target] Standard/Premium 19.5.1 (May 21, 2019) {#tgt-19-5-1-historical}

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

#### Feature updates

|Feature / Enhancement | Description |
| --- | --- |
|Single Page App Visual Experience Composer (SPA VEC)|The SPA VEC includes the following enhancements to make your work quicker and more efficient:<ul><li>Clicking an action in the SPA highlights the element on the site where this action will be applied. Each VEC action created under a View has four corresponding icons: Information, Edit, Move, and Delete. New "Move" functionality in this release lets you move the action to a Page Load Event or any other View that already exists in the modifications panel. (TGT-33746)</li><li>You can perform many actions before the page loads in the VEC, or even if the page fails to load altogether (for example, custom code is no longer operational). Actions that cannot be edited before the site loads are disabled in the Target UI. (TGT-33851 & TGT-34149)</li></ul>For more information, see [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md).|

#### Enhancement, fixes, and changes

* Toolbar icons display appropriately after you cancel loading of a page within the VEC. If specific actions cannot be performed until after the page is fully loaded, the associated toolbar icons are disabled. (TGT-33811)

### [!DNL Target] Standard/Premium 19.4.2 (April 30, 2019) {#release-19-4-2}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

#### Feature updates

|Feature / Enhancement | Description |
| --- | --- |
|[!UICONTROL Visual Experience Composer]|The [!UICONTROL Visual Experience Composer] (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>The DOM path feature is now available when setting up click tracking.<br>For more information, see [click tracking](/help/main/c-activities/r-success-metrics/click-tracking.md#considerations).</li><li>Use the Styles panel to view or edit the value of existing styles for the selected element. You can also add additional styling.<br>To access the Styles panel, click a page element from within the VEC, then click [!UICONTROL Edit] > [!UICONTROL Styles].<br>The Styles panel displays on the right side of the VEC. The panel contains a list of styles that lets you edit or add to the selected element. A real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.<br>For more information, see [Styles](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in *Visual Experience Composer Options*.</li><li>The Rich Text Editor now supports nested HTML5 elements.<br>HTML5 specifications allow new combinations of tags for nesting. The previous version of the rich text editor did not support new nesting of tags as allowed by the HTML5 specification. As a result, any nested elements selected in the VEC were not handled properly, which led to unwanted HTML changes. (TGT-33618)<br>For more information, see [Edit Text/HTML](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) in *Visual Experience Composer options*.</li>|

#### Enhancement, fixes, and changes

* We improved the workflow when you delete assets using the VEC. Deleted assets are now removed from the [!UICONTROL Offers library] and from [!DNL Scene7] (if applicable). Deleted assets no longer display in search results. (TGT-31981)
* You can now delete asset folders even if they contain images (non-empty folders). (TGT-33265)

  Previously, you could not delete a non-empty folder from the Target image offers library ([!UICONTROL Offers] > [!UICONTROL Image Offers]). You would get a "Folder is not empty!" notification when trying to delete the folder from the UI.  With this feature, we are adding the capability to let you perform the folder deletion to remove an entire folder containing any number of assets and sub-folders inside. This feature is available in the Target UI as well in the Adobe Experience Cloud Assets UI.

  * Non-empty folders in the Image Offer library can be deleted. If all images within the folder are not referenced in any activity, the entire folder and its contents are deleted. If some images within the folder are referenced in any activity, all unreferenced images are deleted, but referenced images and folders containing those images are retained.
  * Rendering of image offers in the Image Asset picker is made faster and more efficient. 
  
  For more information, see [Work with content in the library](/help/main/c-experiences/c-manage-content/assets-working.md). (TGT-32897) 

* We improved the rendering of image offers in the Assets picker. Displaying and selecting image offers is now quicker and more efficient. (TGT-32897)
* We improved the handling of redirects to URLs when you cancel loading of a page within the VEC. (TGT-33815)
* After you select a [!UICONTROL Recommendations] collection from the Collections picker, you must now click the [!UICONTROL Save] button. This workflow is consistent with other workflows within [!DNL Target]. (TGT-33205)
* Fixed an issue that caused a small set of Insights reports to return 0% conversion rates instead of the actual conversion rates. (TNT-32125)

### [!DNL Target] Standard/Premium 19.4.1 (April 15, 2019) {#release-19-4-1}

This release is a maintenance release and includes the following change:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

* Updated the [!DNL Adobe Experience Cloud] UI to reflect branding and product changes. (TGT-33546, TGT-33272, and TGT-33331)

#### [!DNL Target] Standard/Premium 19.3.1 (March 29, 2019) {#release-19-3-1}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

| Feature / Enhancement | Description |
| --- | --- |
|Visual Experience Composer|The Visual Experience Composer (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>You can now cancel the loading of a website in the VEC to unblock editing of an activity. This enhancement is useful, for example, if you want to make a small edit to the activity, review its settings, or add custom code and you don't want to wait for the site to load. (TGT-31288)<br>See [Cancel loading of a page within the VEC](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading).</li><li>You can perform many actions before the page loads in the VEC, or even if the page fails to load altogether (for example, custom code is no longer operational). Actions that cannot be edited before the site loads are disabled in the Target UI. (TGT-31288, TGT-31611, and TGT-32602)<br>See [Edit a page while the page is loading or after the page fails to load](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading).</li><li>The VEC displays the DOM path so you can easily select the proper element while creating or editing experiences. (TGT-13422)<br>See [Navigate elements using the DOM path](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).</li></ul>|

### at.js version 2.0.1 (March 19, 2019) {#atjs201}

This is a maintenance release and includes the following enhancements and fixes:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

* Fixed a race condition in the DOM polling code that caused JavaScript exceptions for certain customers. (TNT-31869)
* Notifications that views were rendered have been decoupled from click-tracking event handlers. Initially, Target did not send notifications if click-event handlers belonging to a rendered view could not be attached. Target now sends a view notification even when click elements are not found. (TNT-31969)
* Fixed an issue that caused the request-succeeded event redirect flag to always be set to true. (TNT-31907)
* Fixed an issue that caused the VEC rearrange action to be logged as success, even when elements were missing. (TNT-31924)
* Fixed an issue that caused notifications for certain customers to not contain the Enterprise Permissions property token. (TNT-31999)

>[!NOTE]
>
>If you require [!DNL Adobe] Opt-in support for the General Data Protection Regulation (GDPR), you should implement at.js 1.7.1. Opt-in support is not currently supported in at.js 2.*x*.

### at.js version 1.7.1 (March 19, 2019) {#atjs171}

This is a maintenance release and includes the following fix:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

* Fixed a race condition in the DOM polling code that caused JavaScript exceptions for certain customers. (TNT-31869)

### Platform Changes (February 19, 2019) {#atjs2}

|Feature/Enhancement|Description|
| --- | --- |
|at.js version 2.0.0<br>February 19, 2019|at.js 2.x is now available.<br>The newest version of at.js provides rich feature sets that equip your business to execute personalization on next generation client-side technologies. This new version is focused on upgrading at.js to have harmonious interactions with single page applications (SPAs).<br>Here are some benefits of using at.js 2.x that are not available in previous versions:<ul><li>The ability to cache all offers on page load to reduce multiple server calls to a single server call.</li><li>Tremendously improve your end-users' experiences on your site because offers are shown immediately via the cache without any lag time that traditional server calls introduce.</li><li>Simple one-line of code and one-time developer setup to enable your marketers to create and run A/B and Experience (XT) activities via the Visual Experience Composer (VEC) on your single page applications.</li></ul>at.js 2.x introduces the following new functions:<ul><li>getOffers()</li><li>applyOffers()</li><li>triggerView()</li></ul>The following functions have been deprecated with the introduction of at.js 2.x:<ul><li>mboxCreate()</li><li>mboxDefine</li><li>registerExtension()</li></ul>For more information, see [Upgrading from at.js 1.x to at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} and [at.js functions](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.<br>**Note**: If you require Adobe Opt-in support for the [General Data Protection Regulation](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation.html){target=_blank} (GDPR){target=_blank}, you must currently use at.js 1.7.0. Opt-in support is not supported in at.js 2.x.|
|at.js version 1.7.0<br>February 14, 2019|at.js 1.7.0 is available.<br>This release brings Adobe Opt-In support. Adobe Opt-In is a way to simplify Adobe solutions integrations with consent management platforms.<br>For more information about Adobe Opt-in, see [Privacy and General Data Protection Regulation](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation.html){target=_blank} (GDPR){target=_blank}.<br>This release also fixes an issue where Target might override redirect URL parameters with parameters that are coming from the redirect URL.<br>**Note**: If you require Adobe Opt-in support for GDPR, you must currently use at.js 1.7.0. Opt-in support is not supported in at.js 2.x.<br>For a list of all versions, see [at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.|

### [!DNL Target] Standard/Premium 19.2.1 (February 19, 2019) {#target-19-2-1}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

| Feature / Enhancement | Description |
| --- | --- |
|Single Page App Visual Experience Composer|The Visual Experience Composer (VEC) for Single Page Apps (SPAs) lets marketers create tests and personalize content on SPAs in a do-it-yourself fashion without continuous development dependencies. The VEC can be used to create activities on most popular frameworks, such as React and Angular. (TGT-27916)<br>For more information, see [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md) and [Single Page Application integration](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/target-atjs-single-page-application.html){target=_blank}.<br>In addition to the above article, there are many topics related to SPAs and at.js that address this feature and how to implement it. For more information see [Documentation changes](/help/main/r-release-notes/doc-change.md).|
|Visual Experience Composer|The Visual Experience Composer (VEC) includes the following enhancements to make your work quicker and more efficient:<ul><li>You can now use the Insert Before and Insert After options in the VEC while inserting [AEM experience fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). See [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md). (TGT-32385)</li><li>The [!DNL Adobe Target] VEC Helper browser extension for Google Chrome lets you load websites reliably within the VEC to rapidly author and QA web experiences. See [Visual Experience Composer helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). (TGT-32746)</li></ul>|
|![Premium badge](/help/main/assets/premium.png)<br>Recommendations in [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] activities|You can now include recommendations inside [!UICONTROL A/B Test] (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) and [!UICONTROL Experience Targeting] (XT) activities. This opens up entirely new capabilities, such as:<ul><li>Test and target recommendations and non-recommendations content within the same activity.</li><li>Easily experiment with placement of recommendations on the page, including the order of multiple recommendations.</li><li>Automatically push traffic to the best-performing recommendations experience using [!UICONTROL Auto-Allocate].</li><li>Dynamically assign visitors to tailored recommendations experiences based on their individual profiles using [!UICONTROL Auto-Target].</li></ul>To get started, create an [!UICONTROL A/B Test] or [!UICONTROL Experience Targeting] activity using the VEC and use the [!UICONTROL Insert Before], [!UICONTROL Insert After], or [!UICONTROL Replace With] action to add recommendations to an experience. (RECS-6166)<br>For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).|
|![Premium badge](/help/main/assets/premium.png)<br>Enterprise Permissions support in Target APIs|[Adobe Target Admin APIs](https://developers.adobetarget.com/api/#admin-apis) will now take full advantage of the same Enterprise Permissions capabilities found in the Target UI. Starting **Feb 21, 2019**, system administrators can programmatically access report data as well as create and manage activities, offers, and audiences within any workspace. These actions were previously limited to the default workspace only. Support for Automated Personalization (AP) activities will come in a future release.|

**Enhancement, fixes, and changes**

* To improve security, [!DNL Target] now prevents accessing Amazon Web Services (AWS) metadata endpoints while loading the VEC. (TGT-33129)

### Platform Changes (January 2019) {#platform-19-1-previous}

| Feature / Enhancement | Description |
| --- | --- |
|Targeting<br>January 25, 2019|Made changes to how targeting matches function for "equals" comparisons with non-decimal and decimal values returned by profile scripts or any other source of input, such as mbox parameters, profile parameters, etc.<br>For more information, see [Targets and audiences](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) FAQ.|
|Profile scripts<br>January 17, 2019|For performance reasons, we recommend a return value that is no longer than 256 characters.<br>For a String return value, if the size of the return value exceeds 2048 characters, the script is disabled by the system.<br>For an array return value, if the size of the concatenated values of the array exceeds 2048 characters, the script is disabled by the system.<br>For more information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Target, see [Limits](/help/main/r-troubleshooting-target/target-limits.md).|
|at.js<br>January 16, 2019|at.js 1.6.4 is a maintenance release and addresses the following issues:<ul><li>Fixed a race condition manifesting in Microsoft Internet Explorer 11 that caused duplicate offers to be applied. (TNT-31374)</li><li>Fixed an issue that affected click tracking when there is a default offer with a click-token and html offers. (TNT-31493)</li><li>Extended the mboxEdgeCluster cookie with each Target request. This is used only when mboxEdgeOverride is enabled. (TNT-31485)</li></ul>|

### [!DNL Target] Standard/Premium 19.1.1 (January 22, 2019) {#release-19-1-1-previous}

This release includes the following features, changes and enhancements:

(The issue numbers in parentheses are for internal Adobe use.)

| Feature / Enhancement | Description |
| --- | --- |
| ![Target Premium badge](/help/main/assets/premium.png)<br/>[!UICONTROL Enterprise Permissions] support in [!DNL Target] APIs |[Adobe Target Admin APIs](https://developers.adobetarget.com/api/#admin-apis) will now take full advantage of the same Enterprise Permissions capabilities found in the Target UI. Starting **Feb 21, 2019**, system administrators will be able to programmatically access report data as well as create and manage activities, offers, and audiences within any workspace. These actions were previously limited to the default workspace only. Support for Automated Personalization (AP) activities will come in a future release. |
| ![Target Premium badge](/help/main/assets/premium.png)<br/>[!UICONTROL Recommendations]: filter collections and exclusions by environment (host group) | You can now preview the contents of [!UICONTROL Recommendations] collections and exclusions for a selected environment (host group).<br/>Previously, when you viewed a collection or exclusion, the displayed items contained were results for the default host group (specified in [!UICONTROL Recommendations > Settings > Default Host Group]).<br/>Now, when creating or updating a collection or exclusion, you can use the [!UICONTROL Environment] selector to choose the environment to preview results for. The new [!UICONTROL Environment] filter saves you time and effort because you no longer need to navigate to the [!UICONTROL Settings] page to select the appropriate default host group before creating or editing collections and exclusions.<br/>**Note:** After changing the selected environment, you must click [!UICONTROL Search] to update the returned results.<br/>The new [!UICONTROL Environment] filter is available from the following places in the [!DNL Target] UI:<ul><li>[!UICONTROL Catalog Search] ([!UICONTROL Recommendations > Catalog Search])</li><li>[!UICONTROL Create Collection] dialog box ([!UICONTROL Recommendations > Collections > Create New])</li><li>[!UICONTROL Update Collection] dialog box ([!UICONTROL Recommendations > Collections > Edit])</li><li>[!UICONTROL Create Exclusion] dialog box ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>[!UICONTROL Update Exclusion] dialog box ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul><br>For more information, see the following topics:<uL><li>[Collections](/help/main/c-recommendations/c-products/collections.md)</li><li>[Exclusions](/help/main/c-recommendations/c-products/exclusions.md)</li><li>[Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md)</li><li>[Settings](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}</li><li>[Recommendations: filter collections and exclusions by environment (host group)](/help/main/administrating-target/hosts.md)</li></ul>(TGT-20622)</ul>|

**Enhancement, fixes, and changes**

* Fixed an issue that caused the Save button to remain disabled when the user logs in through the login pop dialog box on session expiry while editing an audience. (TGT-32722)

## Release notes - 2018 {#reference_36ACC83E135A41F28104C44755C26D5B}

### Platform (November 15, 2018) {#section_484A56774E004282B98FFFF851E4E670}

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js 1.6.3 </p> </td> 
   <td colname="col2"> <p>at.js version 1.6.3 is now available. </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Selectors are now CSS-escaped if they contain IDs or CSS classes that start with a digit, two hyphens, or a hyphen followed by a digit (for example #-123). (TNT-31061) </p> </li> 
      <li id="li_6504E90D7C534A1BB9A2DE8510CE3B90"> <p>Fixed an issue introduced with at.js 1.6.2 where Visual Experience Composer (VEC) offers from different activities that apply to the same CSS selector did not respect activity priority. (TNT-31052) </p> </li> 
      <li id="li_D347CA513F1240E4BF79D757287AB30C"> <p>Fixed an issue with timing out a promise in environments where there was no native support for promises. (TNT-30974) </p> </li> 
      <li id="li_17F41A84CCFF41D7993E35DE10F87066"> <p>Issues are now correctly captured and reported via the content-rendering failed event. Previously, JavaScript might have been reported to have run successfully, even if that wasn't the case. (TNT-30599) </p> </li> 
     </ul> </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.11.1 (November 12, 2018) {#section_6BBA8B1EE9D241C28E12856A375E97F6}

The [!DNL Target] Standard/Premium release on November 12 includes back-end enhancements, fixes, and changes. The [!UICONTROL Personalization Insights] reports will be available November 14.

<table id="table_EF529199D1C741F7BDBC9C41A37B7D26"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Personalization Insights reports </p> <p> <p>Note:  Available November 14, 2018. </p> </p> </td> 
   <td colname="col2"> <p>Two specialized reports are available to users of <span class="wintitle"> Automated Personalization (AP)</span> and <span class="wintitle"> Auto-Target (AT)</span> activities: </p> <p> 
     <ul id="ul_C338AC34C57C49E1A8DFA471167EC40A"> 
      <li id="li_2329BFC8CC524EBBA99C2F8EDC745B90"> <p><b><span class="wintitle"> Automated Segments</span>:</b> Different visitors respond differently to the offers/experiences in your AP/AT activity. This report shows how different automated segments defined by Target's personalization models responded to the offers/experiences in the activity. </p> </li> 
      <li id="li_48556C9BAD48476DA00DD666F5265E2B"> <p><b><span class="wintitle"> Important Attributes</span>:</b> In different activities, different attributes are more, or less, important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance. </p> </li> 
     </ul> </p> <p>See <a href="/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> Personalization Insights reports</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.10.1 (October 24, 2018) {#section_FA37BF4E840B424E8BC4791D7234FE2A}

This release includes the following features and enhancements:

(The issue numbers in parentheses are for internal Adobe use.)

<table id="table_B1911F55CCE1428881D258380A8254A9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experiences </p> </td> 
   <td colname="col2"> <p>You can now copy an experience in an Experience Targeting (XT) activity so you can make minor changes to it without having to re-create the experience from scratch. This capability was already available for A/B Tests. (TGT-31504) </p> <p>See <a href="https://experienceleague.adobe.com/docs/target/using/activities/experience-targeting/create-targeting/xt-add-experience.html" format="html" scope="external"> Create experience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Offers in Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p>In the September 2018 release, we added an enhancement that lets you filter offers by reporting groups. You can now filter for Unassigned Offers so you can assign a reporting group to an offer that is not currently assigned to any reporting group. (TGT-31882) </p> <p>See <a href="https://experienceleague.adobe.com/docs/target/using/activities/automated-personalization/create-ap-activity.html" format="html" scope="external"> Create an Automated Personalization activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting source for activities </p> </td> 
   <td colname="col2"> <p>In <span class="wintitle"> Administration </span> &gt; <span class="wintitle"> Visual Experience Composer </span>, you can select the reporting source for your activities, either <span class="keyword"> Target </span> or <span class="keyword"> Adobe Analytics </span>. You can also choose to select your reporting source per activity. </p> <p>Starting with this release, there are some important workflow considerations you should be aware of when you choose the reporting source in <span class="wintitle"> Preferences </span> or per activity.</p></td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* Improved the handling of audiences referenced in Target activities that have been deleted in Adobe Audience Manager (AAM). (TGT-23338)

    * If an audience was deleted in AAM, a warning icon in both the [!UICONTROL Audience] list and the audience picker displays. A tool-tip in the UI also indicates that the audience was deleted in AAM. 
    * If you attempt to combine multiple audiences with a deleted audience, or if you attempt to save an activity that references a deleted audience, a warning message displays.

  See [About audiences](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html). 

* Fixed an issue that prevented users in certain situations from being able to create an activity when Adobe Analytics was selected as the reporting source on the [!UICONTROL Administration] page. Users saw a "Please select a report suite" message even though they were not given the option of selecting the report suite. (TGT-31968)

### Platform (October 19, 2018) 

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js 1.6.2 </p> </td> 
   <td colname="col2"> <p>This is a maintenance release and addresses the following issue: </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Fixed an issue that on some customer sites lead to an infinite "async" loop. </p> </li> 
     </ul> </p> <p> <p>Important:  In addition, at.js Version 1.6.2 also contains all of the enhancements and fixes included in at.js Version 1.6.1 and 1.6.0. These versions are no longer available for download. We recommend that you upgrade to version 1.6.2 if using 1.6.1 or 1.6.0. </p> </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="html" scope="external"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.9.1 (September 26, 2018) {#section_95CF405C95E44DBEA3CB308FDD5071CD}

<!-- 

target/r_release-notes-2018.xml

 -->

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_7ABC8E7477194D4C8C9E82ECE60E3498"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Offers in Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_9C39ACD865CE4167BDBAA093EDFD3B68"> 
      <li id="li_19710BA5965E4F858B128E1E9FF89471"> <p>You can now use multiple offers from the same location in an exclusion group. For a large number of exclusions (order of 1,000s), you will also observe faster loading of the Manage Content dialog box and preview page while authoring an Automated Personalization (AP) activity. (TGT-31329) See <a href="/help/main/c-activities/t-automated-personalization/managing-exclusions.md#topic_30B4E4F89C914EB2B20B038C0299ED2E" format="dita" scope="local"> Manage Exclusions </a>. </p> </li> 
      <li id="li_542C66E2998541BC87D0A96F4672C665"> <p>You can now filter offers by reporting groups. (TGT-31643) See <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creating an Automated Personalization Activity </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>We have added an <span class="wintitle"> Insert Before </span> action to the (VEC). This is similar to the previously existing <span class="wintitle"> Insert After </span> option. When you select an element on the page, you can click <span class="wintitle"> Insert Before </span> and choose whether you want to insert an image, HTML, or text. The inserted element appears before the selected element. (TGT-30473) See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* We updated the look and feel of Criteria cards to be more intuitive and user-friendly. (TGT-30469) 
* Performance improvements in UI for faster loading of pages.

### Target Standard/Premium 18.8.1 (August 21, 2018) {#section_66A0030993D54565BE30E56AC9CAC1DA}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_4785030753B24AA1A973E1DF790B83DD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Personalization Insights reports </p> </td> 
   <td colname="col2"> <p>Access specialized reports for your Automated Personalization (AP) and Auto-Target (AT) activities: </p> <p> 
     <ul id="ul_54652C5AE0984657BB9A0E46673CB2F1"> 
      <li id="li_0807959BA7D94114BE47A43D3454CAB4"> <p><b>Automated Segments:</b> See how different automated segments defined by Target's personalization models respond to offers/experiences in your activity. </p> </li> 
      <li id="li_48210B1E4EB24288B96CDECAF1CEE34A"> <p><b>Model Attribute Ranking:</b> See the top attributes that influenced Target's personalization models and the relative importance of each attribute. </p> </li> 
     </ul> </p> <p> <p>Note:  This feature will be available soon. Stay tuned for an announcement of the exact date when this feature will be ready for you to use. </p> </p> <p>See <a href="/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> Personalization Insights Reports </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_406B95728467496CA6CC5892F88B69FE"> 
      <li id="li_6D717868FB204A3A95832E709773B424"> <p>You can dock the Modifications panel vertically along the side of the Target UI or horizontally at the bottom. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Modifications </a>. </p> </li> 
      <li id="li_27750AFBCB3E4CB8B0B53592B2447E59"> <p>We have grouped various VEC actions to make your job quicker and more efficient. (TGT-30472) </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </li> 
      <li id="li_27FEBEE245E64ADF9ADF561C6CBBDE8F"> <p>You can edit offers more efficiently, thanks to a larger edit window. (TGT-31052) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tips and Tricks </p> </td> 
   <td colname="col2"> <p>Get the most out of Adobe Target by learning more about various features and see why you should give them a try. The Tips and Tricks functionality displays on the Activities list page and provides links to videos, use-cases, blogs, documentation, and much more. Become a Target Power User! </p> <p>See <a href="/help/main/c-activities/activities.md#section_F77F30A246A14B538D9363B7F3639F97" format="dita" scope="local"> Tips and Tricks </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Basics Webinar Series </p> </td> 
   <td colname="col2"> <p>Participate in the new Target Basics Webinar Series, a Customer Success Webinar Series brought to you by the Community. </p> <p> The next webinar, Best Practices in Reporting &amp; Value Socialization, is scheduled for August 22, 2018 from 8 to 9 a.m. (PDT). </p> <p>See <a href="/help/main/cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Target Basics Webinar Series </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* We have added several improvements to make Target even more secure than it was before. (TGT-31090, TGT-31089, TGT-31143)

### Target Standard/Premium 18.7.1 (July 25, 2018) {#section_A4A9C20EB677455F84FF0BA389F645E5}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_7E3513EABA4948DC92EADCCE0234A9FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A/B and Experience Targeting (XT) activities </p> </td> 
   <td colname="col2"> <p>Edit and delete experiences right from the activity diagram. Now you can jump into the Visual Experience Composer (VEC) for a specific experience or delete an experience right from the diagram. </p> <p> <img src="assets/experience_edit.png" id="image_FA6E5F07B04A4B4BA02EA71EDB6908A7" /> </p> <p>See: </p> <p> 
     <ul id="ul_CB0C1146716F4C09BF924CF3DFA7DC1A"> 
      <li id="li_3767DD36F597481FB312CC577CD668F0"> <p>A/B activity: <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Add Experience </a> </p> </li> 
      <li id="li_E2990CA178C6446BA7206643A3164FEF"> <p>XT activity: <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Create Experience </a> </p> </li> 
     </ul> </p> <p>(TGT-30229) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>Compare one profile attribute to another profile attribute instead of to a static number. </p> <p>See <a href="/help/main/c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md#concept_4C2124B79A5B4556A6C1D10C0F5E40A0" format="dita" scope="local"> Creating a Profile Attribute Comparison Audience </a>. </p> <p> (TGT-28406) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom Code </p> </td> 
   <td colname="col2"> <p>"Custom Code" is now available from the "Add Modifications" panel instead of having its own tab. You can also add more than one custom code and optionally name each custom code. (TGT-28504) </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Modifications </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_371C18DFC6D24E94B3D4FFFD83FC8D3A"> 
      <li id="li_9D11939014E7479AB7FD8910852A5386"> <p>View a list of activities that reference a selected criteria on its Criteria card. The card lists active and inactive activities. (TGT-27672) </p> </li> 
      <li id="li_B97BF9305EB04F6D8B1F6178B2E0CB34"> <p>From the activity diagram, Criteria cards now show when results are ready to display. (TGT-27673) </p> <p>See <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Templates </p> </td> 
   <td colname="col2"> <p>Adobe Target Experience Templates are pre-coded offer samples with configurable inputs to be used in Target to execute some common marketer use cases. These experience templates are provided free to developers and marketers as a starting point to execute some common external use cases in Adobe Target - either via the Visual Experience Composer or Form-Based Experience Composer. Customization might be required to integrate successfully with your webpage or platform architecture. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652" format="dita" scope="local"> Experience Templates </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Basics Webinar Series </p> </td> 
   <td colname="col2"> <p>Participate in the new <a href="/help/main/cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Target Basics Webinar Series </a>, a Customer Success Webinar Series brought to you by the Community. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* Increased the Rich Text Editor modal's size for better usability. (TGT-24775) 
* The diagrams in the Target step (step 2 of the three-step guided workflow) for Automated Personalization (AP) and Multivariate Test (MVT) activities have been redesigned to be more consistent with the designs used for A/B, Experience Targeting (XT), and Recommendations activities. (TGT-30712) 
* The metric value for the Multivariate Test (MVT) Location Contribution report is now more consistent with the values for other metrics, which is rounded to two decimal places. (TGT-30921)

### at.js Version 1.5.0 (June 22, 2018) {#section_53C622F4978F4BC9ACD932D4B7194C12}

<table id="table_B332A93D4A6E4568BA3F7FA8EC0787F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js version 1.5.0 is now available. </p> <p> <p>Note:  The issue numbers in parentheses are for internal Adobe use. </p> </p> <p> 
     <ul id="ul_41FE0EED2D8B4ADE84FC4CA0FA0CE8A0"> 
      <li id="li_2DC17381CB7949AFA35B054B9CA723FA"> <p>The details of the <span class="codeph"> at-request-succeeded </span> event contain the redirect flag. This flag can be used to determine if the page will be redirected to a different URL. If you want to know the URL, subscribe to <span class="codeph"> at-content-rendering-redirect </span>. (TNT-29834) </p> </li> 
      <li id="li_2852878862724BB2BD475C8FC7BF20DA"> <p>Fixed an issue that caused <span class="codeph"> window.targetGlobalSettings.enabled </span> to fail with a runtime exception if it was set to false. (TNT-29829) </p> </li> 
      <li id="li_96E5E409B36444F1B0E3E2606DC03996"> <p>Fixed an issue that caused the page to fail while loading in the Visual Experience Composer (VEC) if using custom code to a fire global mbox request and using body hiding. (TNT-29795) </p> </li> 
      <li id="li_818AA4EDDAC04D8B9BB4BA708D6BEF99"> <p>Added support for <span class="codeph"> screenOrientation </span>, <span class="codeph"> devicePixelRatio </span>, and <span class="codeph"> webGLRenderer </span>. These new Target request parameters are used for iPhone X and other modern device detection. For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. (TNT-29781) </p> </li> 
      <li id="li_87E3FB8B423C472AB1EE0DF2D7C64885"> <p>Fixed an issue where the Adobe Audience Manager (AAM) location hint wasn't always sent. (TNT-29695) </p> </li> 
      <li id="li_E9E5A5035AC24F54ADEF5447E3F15D3B"> <p>For browsers that support it, at.js 1.5.0 switches to MutationObserver for selector polling. Versions prior to at.js 1.0.0 used a MutationObserver polyfill, which proved to be problematic. To avoid the polyfill issues, version1.5.0 uses the following pseudo code to decide which scheduling mechanism to use: </p> <p> 
        <code>
          if MutationObserver is supported scheduler = MutationObserver else if document is visible scheduler = requestAnimationFrame else scheduler = setTimeout 
        </code> </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.6.1 (June 20, 2018) {#section_B63C660815B245DA9922BE33E03734A1}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_5A60FFE5E86148F4BDC6A7031D03D6BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature / Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>When you click an action in the Modifications panel, the VEC automatically scrolls the web page and the corresponding element is highlighted. You no longer need to manually scroll down to find the HTML element that was affected by the modification. </p> <p> <img src="assets/modifications_panel.png" id="image_6E01280636E34ADDA9527AD18A34310B" /> </p> <p>(TGT-30441) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Supported browsers </p> </td> 
   <td colname="col2"> <p>Added Microsoft Edge support for the Target UI and for content delivery. </p> <p>For more information, see . <a href="https://experienceleague.adobe.com/docs/target-dev/developer/implementation/supported-browsers.html" format="dita" scope="local"> Supported Browsers </a> (TGT-14102) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p>The Recently Viewed Items criteria now returns results specific to a given <a href="/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> environment </a>. If two sites belong to different environments and a visitor switches between the two sites, each site shows only recently viewed items from the appropriate site. If two sites are in the same environment and a visitor switches between the two sites, the visitor will see the same recently viewed items for both sites. </p></td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* The Backup row of the Recommendations CSV download now has a leading "&#42;" (double quotes enclosing an asterisk) instead of &#42; (a single asterisk). 
* The Top Sold / Top Viewed row in the Recommendations CSV download no longer has a leading comma.

### Target Platform Changes (June 19, 2018) {#section_0638BD69F3C640479A2A258AD78C0884}

This release includes the following enhancement:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

* Updated the device list to include the latest phone models. Added the capability to deliver targeted content to specific iPhone models by using the Device Marketing Name or Device Model.

  Customers using the Mobile SDK do not need to do anything to leverage this functionality. Customers using at.js must upgrade to at.js version 1.5.0.

  For more information, see [Mobile](/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89). (TNT-26714 & TNT-28288)

### Target Download API (June 5, 2018) {#section_B8729DA10F18433C8D8E01B04F308ED2}

You can use the recommendations download API to download your recommendations in a .CSV file that can be viewed in a spreadsheet or text editor. For improved security, starting on **June 5, 2018**, Target will block HTTP requests and allow only HTTPS requests.

### Target Standard/Premium 18.5.1 (May 22, 2018) {#section_7C1427793C2A48DBAC39F8290717DC5B}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_1C51F61184684072BC69AD15BA68BEBB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_8D08FE4AC7D748EFB2BBFF87DBDC5CE5"> 
      <li id="li_B8929C19276D42168A28A3775CDEDFB3"> <p>You can save up to ten different presets of an individual activity's report after configuring it as desired (metrics, audiences, advanced settings, and so forth). All Target users can display, edit, and delete the various presets, regardless of who created them. (TGT-21268) </p> </li> 
      <li id="li_7ADA62F2ACA049C9B4A8986B09A9F4AA"> <p>You can configure an individual activity's report as desired and then save that configuration as your default/favorite preset. This is the view that displays whenever you view that activity's report going forward. (TGT-10082) </p> </li> 
      <li id="li_DC63C04F3A884BDDA55B5515E4643B7B"> <p>Alerts and messages inside reports let you know if one (or more) audience, metric, host group, or experience has been deleted from a previously configured preset report. The alert or message instructs you to choose another audience, metric, host group, or experience to make a preset again. (TGT-29424) </p> </li> 
     </ul> </p> <p>For more information, see the Target Preset section in <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Report Settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Profile scripts </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F382C8E7708846A08676E1534BC92878"> 
      <li id="li_70E89504525C4119B588C230DCE772E8"> <p>You can view profile script information pop-up cards similar to offer information cards. These profile script information cards let you view the list of activities that reference the selected profile script, along with other useful metadata. (TGT-28253) </p> <p>For more information, see the Viewing Profile Script Information Cards section in <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_DFEB778393024E3EBBC482F31A5B39BC"> 
      <li id="li_4049E334A38F4F94842FF1E35F177FE9"> <p>Custom Audience creation now allows using the mbox parameter directly without having to mandatorily specify the mbox name. The mbox name is now optional. This change lets you use parameters from multiple mboxes or reference a parameter that has not yet been recorded on the edge. Alternately, you can also filter on mbox parameter with the mbox name filter. </p> <p>This same improvement has also been extended to Recommendations Criteria, Recommendations Promotions, and Template Testing rules. </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Custom Parameters </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7765B69E679D4C94B1E863E340DFDE15"> 
      <li id="li_F2AF7E1AFBD6461990EF1D83D1989582"> <p>While selecting Recommendations criteria in the Form-Based Experience Composer, there is now a direct link to the selected Criteria card so you can quickly and easily edit the criteria. (TGT-28483) </p> <p>For more information, see <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </li> 
      <li id="li_517F0A174587416B8621D6F710C1AC48"> <p>Recommendations Criteria, Recommendations Promotions, and Template Testing rules creation now allow using the mbox parameter directly without having to mandatorily specify the mbox name. The mbox name is now optional. This change lets you use parameters from multiple mboxes or reference a parameter that has not yet been recorded on the edge. Alternately, you can also filter on mbox parameter with the mbox name filter. </p> <p>This same improvement has also been extended to Custom Audience creation. </p> <p>For more information, see <a href="/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Recommendations FAQ </a>. </p> </li> 
      <li id="li_AAB242830D1E47B78E58A980B717C736"> <p>Updated the UI for Recommendations Design cards. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* Updated the UI for Step 2 of the Target three-step guided workflow used to create or edit an A/B Test, Experience Targeting (XT), or Recommendations activity. (TGT-18911)

### Target Standard/Premium 18.4.1 (April 25, 2018) {#section_445DBC5402BA456BAF2D24AEA33A91C9}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_6D99C48B72D24728BF623608053931D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Experience Manager (AEM) Experience Fragments </p> </td> 
   <td colname="col2"> <p>Using experience fragments created in AEM in Target activities lets you combine the ease-of-use and power of AEM with powerful Automated Intelligence (AI) and Machine Learning (ML) capabilities in Target to test and personalize experiences at scale.&amp;nbsp;&amp;nbsp; </p> <p>AEM brings together all of your content and assets in a central location to fuel your personalization strategy. AEM lets you easily create content for desktops, tablets, and mobile devices in one location without writing code. There's no need to create pages for every device—AEM automatically adjusts each experience using your content. </p> <p> Target lets you deliver personalized experiences at scale based on a combination of rules-based and AI-driven machine learning approaches that incorporate behavioral, contextual, and offline variables.&amp;nbsp; With Target you can easily set up and run A/B and Multivariate activities to determine the best offers, content, and experiences. </p> <p>Experience fragments represent a huge step forward to link the content/experience creators and managers to the optimization and personalization professionals who are driving business outcomes using Target. </p> <p>For more information, see <a href="/help/main/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8" format="dita" scope="local"> AEM Experience Fragments </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> 
    <ul id="ul_EAB90C510EA04D6A8AEFF23A77DB2337"> 
     <li id="li_47DA6EB92CC84FFDBFDC9CC9386AF654"> <p>You can now refresh a report to update the report's table and graph view without refreshing the entire page, its configuration, or its date range. (TGT-28125) </p> <p>For more information, see <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Report Settings </a>. </p> </li> 
     <li id="li_AB2DE7A45D914FD7AEB0832187AF3844"> <p>The calendar in reports now contains pre-defined date ranges, such as Last 7 Days, Last 15 Days, and so forth. (TGT-29171) </p> <p>For more information, see <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Report Settings </a>. </p> </li> 
     <li id="li_46DF9037E0ED4935B3BCDB35E8BED065"> <p>The table view column width was modified to reduce horizontal scrolling when multiple metrics are applied. (TGT-26575) </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>UI localization </p> </td> 
   <td colname="col2"> <p>The Target UI is now available in the following languages: </p> <p> 
     <ul id="ul_DB6C771FCFDF43F498F8754920A70BCD"> 
      <li id="li_A65D07DF66844AC8BEEC1D413F214191"> <p>Chinese Simplified </p> </li> 
      <li id="li_5986DD06AF5B4F76B3A02CFBF2DC3644"> <p>Chinese Traditional </p> </li> 
      <li id="li_341FDC1CEC2B4C4BBD45CB2A0A54F2A3"> <p>Korean </p> </li> 
      <li id="li_A4C31539B98E42348D5F1A18C63EAB6C"> <p>Italian </p> </li> 
      <li id="li_97E3E0A916B64601BBF601AAED581174"> <p>Portuguese </p> </li> 
     </ul> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>When creating a custom audience based on an mbox parameter, <span class="codeph"> mboxParameter </span> no longer prompts you for <span class="codeph"> mboxName </span>. mbox name is now optional. This change lets you use parameters from multiple mboxes or reference a parameter that has not yet been recorded on the edge. (TGT-25807) </p> <p> <p>Note:  This feature is visible in the Target UI but is currently disabled. This feature will be enabled soon (date to be communicated). </p> </p> 
  </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* Transport Layer Security (TLS) is the most-widely deployed security protocol used today for web browsers and other applications that require data to be securely exchanged over a network. Adobe has security compliance standards that require the end-of-life of older protocols and is mandating the use of TLS 1.2 in order to have the most up-to-date and secure version in use. Starting with the Target 18.4.1 release (April 25, 2018), Adobe Target will take steps to move towards TLS 1.2 encryption and phase out support for TLS 1.0 encryption completely by September 12, 2018. It is important that you go through the specifics and plan out the changes for a smooth transition. For more information, see [TLS (Transport Layer Security) Encryption Changes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}. 
* UI for Recommendations Criteria Cards has been improved for better usability. (TGT-27829)

### at.js (April 3, 2018) {#section_932DF1004F4648668FE4984BFAF2EC49}

This release includes the following features and enhancements:

<table id="table_76576D9D931B4DA99900F2C03175938E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js version 1.3.0 is now available. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html" format="dita" scope="local"> Download at.js </a> and <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details </a>. </p> <p> 
     <ul id="ul_349BEB37B6C94FF0801F121042037803"> 
      <li id="li_4C2F82F4DD394ED5A0BFF978B15FEDDF"> <p>The following new events are available to help in tracing, debugging, and customizing interaction with at.js: </p> <p> 
        <ul id="ul_EFF7E2FCEA0D42298779DDE13B54503F"> 
         <li id="li_6A2B06A522004EDE96D9A552571A7C30"> <p>LIBRARY_LOADED </p> </li> 
         <li id="li_61AA203A21DF4B7EAE075374A09C8FF0"> <p>REQUEST_START </p> </li> 
         <li id="li_DAF9CC1E86834C62B93419429B43A2CB"> <p>CONTENT_RENDERING_START </p> </li> 
         <li id="li_A52DC337115248A1BE5AF5B358BE5A9A"> <p>CONTENT_RENDERING_NO_OFFERS </p> </li> 
         <li id="li_7D71E48016B1446995493EBBF7D32447"> <p>CONTENT_RENDERING_REDIRECT </p> </li> 
        </ul> </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html" format="dita" scope="local"> at.js custom events </a>. </p> </li> 
      <li id="li_E2704294F8BA47FFAABE7572F67FB5C0"> <p>You can augment an at.js request with additional parameters that come from data providers. Data providers should be added to <span class="codeph"> window.targetGlobalSettings </span> under the <span class="codeph"> dataProviders key </span>. </p> <p>For more information, see "Data Providers" in <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_02EAFE6DA0D44CF88980184FD14226A5"> <p>at.js requests now use GET, but it will switch to POST when the URL size exceeds 2048 characters. There is a new property named <span class="codeph"> urlSizeLimit </span> where you can increase the size limit if necessary. This change allows Target to align at.js to AppMeasurement, which uses the same technique. </p> </li> 
      <li id="li_43363A4F3A764394AA88D2595F93D8C0"> <p>Target now enforces that the <span class="codeph"> mbox </span> key in the <span class="codeph"> adobe.target.applyOffer(options) </span> function is used. This key has been required in the past, but Target now enforces its use to ensure that Target has proper validation and customers are using the function correctly. </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html" format="dita" scope="local"> adobe.target.applyOffer(options) </a> . </p> </li> 
      <li id="li_7336D8D48A894291A378E0BB212B7F9B"> <p>at.js has improved event and click tracking functionality. at.js uses <span class="codeph"> navigator.sendBeacon() </span> to send event tracking data and will fallback to synchronous XHR when <span class="codeph"> navigator.sendBeacon() </span> is not supported. This fallback mostly affects Internet Explorer 10 and 11 and some versions of Safari. Safari will add support for <span class="codeph"> navigator.sendBeacon() </span> in the iOS 11.3 release. </p> </li> 
      <li id="li_28D7324137B14C75BF6F1EA0B2487C9B"> <p>at.js can now render offers even when a page is opened in background tabs. Some Target Customers encountered an issue when <span class="codeph"> requestAnimationFrame() </span> was disabled because of the browser throttling behavior for background tabs. </p> </li> 
      <li id="li_3278979E1C6C41DEA7E8025AEB337985"> <p>This release adds many performance improvements, including shorter callstacks when inspecting a Chrome CPU profile. </p> </li> 
      <li id="li_AAA9C0DCC3354DFA8907968C8E6427F6"> <p>at.js 1.3.0 no longer supports content delivery on Microsoft Internet Explorer 9. For a list of supported browsers, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/implementation/supported-browsers.html" format="dita" scope="local"> Supported Browsers </a>. Going forward, all requests are executed via <span class="codeph"> XMLHttpRequest </span> with CORS support with no JSONP requests. This change greatly improves security. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.3.1 (March 20, 2018) {#section_880706BE15544A03A2C951F267F4AEC5}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_AE38682151A948AEA21E35A353F18D76"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Popularity by Entity Attribute </p> </td> 
   <td colname="col2"> <p><b>New: March 22, 2018</b> </p> <p>You can now choose the Popularity by Entity attribute in the existing flow when a Custom attribute is selected as the key. </p> <p>After selecting the desired key (in this case, a custom profile attribute), for "Recommendation Logic," you can choose two new options: </p> <p> 
     <ul id="ul_7A6F2398ADE846EF8A7A3110C2736BF7"> 
      <li id="li_66BFF016564749B298B88F6B9638B64E"> <p>Most Viewed </p> </li> 
      <li id="li_937FE5C40ED8471391B282D1ACE8C133"> <p>Top Sellers </p> </li> 
     </ul> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>While viewing an audience's definitions pop-up card (for example, from the Audience Library), you can now see other activities that reference that audience, if applicable. This way you can avoid accidental impact to activities while editing audiences. </p> <p>Previously, when you tried to delete an audience that was referenced by activities, a warning displayed informing you that the audience cannot be deleted with at maximum of 10 activities referencing the audience. </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> About Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> <p>Improved the lift and bounds information in reports to be more comprehensive and useful, including a tooltip that explains how bounds are calculated. (TGT-28729) </p> <p>For more information, see <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Average Lift, Lift Bounds, and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization (AP) and Auto-Target activities </p> </td> 
   <td colname="col2"> <p>Additional guidance is available in the UI and in Help to help you allocate traffic percentages more effectively in Automated Personalization (AP) and Auto-Target activities. </p> <p>For more information, see <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Determining Traffic Allocation </a> and <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creating an Automated Personalization Activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Inclusion rules, collections, and exclusions for Custom Criteria </p> </td> 
   <td colname="col2"> <p>You can now perform real-time filtering on top of your own custom criteria output. For example, you can limit your recommended items to only those from a visitor's favorite category or brand. This gives you the power to combine off-line calculations with real-time filtering. </p> <p>With the addition of inclusion rules on Custom Criteria, this turns otherwise static recommendations into dynamic recommendations based a visitor's interests. </p> <p> 
     <ul id="ul_BDD55AB34F4A43C691D2399C16AA3D6C"> 
      <li id="li_133C33E0D02E4861A4C855BD8A492E69"> <p>Custom Criteria are now configurable, like other criteria in recommendations. </p> </li> 
      <li id="li_AC201F0917BF465C985E8947635F762E"> <p>You can use collections, exclusions, and inclusions (including the special rules for Price and Inventory) in the same way as any other criteria. Collections and exclusions were already supported. This release adds inclusions. </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> <p>(TGT-28488) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Inclusion rules, collections, and exclusions for Recently Viewed Criteria </p> </td> 
   <td colname="col2"> <p>Recently Viewed items can now be filtered so that only items with a particular attribute are displayed. For example, a multi-national company with multiple businesses might have a visitor view items across multiple digital properties. In this case, you can limit the recently viewed items to display only for the respective property where it was viewed. This prevents Recently Viewed items from displaying on another digital property's site. </p> <p> 
     <ul id="ul_A2D260F01CA047EEA72EF56BD0EE88FA"> 
      <li id="li_DB107DD357B741CCB2B7A4FDAD16F9D6"> <p>Recently Viewed Criteria are now configurable, like other criteria in recommendations. </p> </li> 
      <li id="li_85452C03F0924D4C8D854509F1293021"> <p>You can use collections, exclusions, and inclusions (including the special rules for Price and Inventory) in the same way as any other criteria. Collections and exclusions were already supported. This release adds inclusions. </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> <p>(TGT-22843) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Target Extension for Adobe Launch </p> </td> 
   <td colname="col2"> <p>Launch is the next-generation of tag management capabilities from Adobe. Launch gives customers a simple way to deploy and manage all of the analytics, marketing, and advertising tags necessary to power relevant customer experiences. </p> <p>The Target extension lets you quickly and easily implement Target in your environment. </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html" format="dita" scope="local"> Implementing Target using Adobe Launch </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following enhancements, fixes, and changes:

* When creating or editing A/B and Experience Targeting (XT) activities, Target retains information about the last opened experience, page, or experience version (via multiple audiences feature) and opens the appropriate page the next time you open the Target UI. (TGT-28225) 
* Security fixes have been made for compliance purposes.

### Target Standard/Premium 18.2.1 (February 15, 2018) {#section_837CBBB7A89D45D99855A8C5F5E7BFFB}

This release includes the following features and enhancements:

<table id="table_1C7A462AE8D4492FA5555F060031F665"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>The Adobe Marketing Cloud has been re-branded and is now called the Adobe Experience Cloud. </p> </td> 
   <td colname="col2"> <p>The Experience Cloud is Adobe's integrated family of digital marketing solutions and services. It's also an intuitive interface that lets you quickly access your cloud solutions and core services. </p> <p>Re-branding and UI Changes: Adobe Marketing Cloud has been re-branded and is now called the Adobe Experience Cloud. In addition, you will see UI changes in the Target interface and in the Solution Switcher. </p></td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes some back-end enhancements, fixes, and changes.

### Target Platform (January 18, 2018) {#section_F6A0DC31636D403F92BDB9DCE7A3F6ED}

This release includes the following features and enhancements:

<table id="table_0F5BF9370E214302BDFE0AC2D66EC773"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js 1.2.3 adds support for JSON offers. JSON offers are supported only in activities created using the Form-based Experience Composer. Currently the only way to use JSON offers is via direct API calls. See <a href="/help/main/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> Create JSON Offer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Other changes </p> </td> 
   <td colname="col2"> <p>Exclusion rules, catalogs, algorithm inclusion rules, and run-time filtering are now case in-sensitive. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.1.1 (January 23, 2018) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

This release includes the following features and enhancements:

>[!NOTE]
>
>The issue numbers in parentheses are for internal Adobe use.

<table id="table_872FE2BE61CC4A5CA369D9A6C730686E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_42D7C86043C94A7BBA5ED405B2902E3A"> 
      <li id="li_50F2A7D05AB244E18D263A476BD906B3"> <p>You can now create Time Frame audiences without start or end dates. This lets you use the same audience in multiple activities (without making a copy of the audience) while controlling the start and end dates at the activity level. See <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. (TGT-25975) </p> </li> 
      <li id="li_6F08D63BC4F040859D51C47C3521C5E1"> <p>Copy and Edit functionality is available for activity-only audiences when you hover over an audience on the Choose Audience &gt; Activity Only Audience page. Previously, this functionality existed only for Library audiences. See <a href="/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Creating an Activity-Only Audience </a>. (TGT-27410) </p> </li> 
      <li id="li_A8CF45E6DC37401AA273F7D6CF617524"> <p>Activity-only audiences across activities can have the same name. Previously, duplicate names would result in the addition of time stamps—a duplicate audience named "Target on Weekday" would get saved as "Target on Weekday-1456732099201." </p> <p>Library audiences continue to require unique names. (TGT-17967) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reports </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C595EEF916494342AD99FF0FDF999927"> 
      <li id="li_8C74478D3480406591DC876F69C19329"> <p>You can now view confidence intervals for continuous variables. (TGT-22085) </p> </li> 
      <li id="li_21B31F91685C46CAA47688FDE5735312"> <p>Target now displays lift bounds when statistically significant in reports.(TGT-27301, TGT-27794, and TGT-26387) </p> </li> 
     </ul> </p> <p>See <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_BD0C5B260E7E4F139FBC1FBA286C0B81"> 
      <li id="li_FCDBABE6C5034A3596F5BBF024245FB9"> <p>Target now supports creation of JSON offers in the Offer Library for use in the Form-Based Experience Composer. See <a href="/help/main/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> Create JSON Offer </a>. (TGT-27064) </p> </li> 
      <li id="li_5500AE7DCF4146E88E4619382CE8E836"> <p>You can now view the activities that reference a code offer in each offer's definition pop-up card. This functionality does not apply to image offers. See <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. (TGT- 26277) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_63613AD2D744442AA12CD23F4DAC75B4"> 
      <li id="li_4DD5CF06D93A4083BCB34A4FFA293C89"> <p>The UI now displays the status of uploading custom algorithm data for recommendations. See <a href="/help/main/c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Uploading Custom Criteria </a>. (TGT-23891) </p> </li> 
      <li id="li_14FCFDD0A0E84B47AF1488DB4DDF197B">The Value is Present and Value is Not Present operators are now available while creating algorithm inclusion rules. See <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. (TGT-24110) </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Target Insider newsletter </p> </td> 
   <td colname="col2"> <p>The Adobe Target Insider is a monthly newsletter for members of the Adobe Target community. Learn about product updates and future plans, personalization and optimization tips and tricks, customer successes, upcoming events, information-filled white papers, popular blog posts, and more. Read the <a href="https://theblog.adobe.com/stay-optimized-adobe-target-insider-newsletter/" format="https" scope="external"> announcement letter </a> to learn more. </p> <p> <a href="https://www.adobe.com/subscription/adobe_target_newsletter.html" format="html" scope="external"> Subscribe to the newsletter </a> to help you deliver the exceptional customer experiences that drive business success. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following customer-facing enhancements, fixes, and changes:

* You can now scroll the page while rearranging experiences on Step 2 of the three-step guided workflow while creating activities. (TGT-27652) 
* You can right-click an activity from the Activity List to open the activity in a new tab. For example, in Firefox, right-click the desired activity > Open Link in New Tab. (TGT-27409) 
* Made performance improvements to the Designs page (Recommendations > Designs). The speed to display and search for designs has been improved. (TGT-21792) 
* at.js is now the default implementation option to download. (TGT-24676) 
* URL validation now allows the use of double hyphens in the URL. Previously, a URL with double hyphens could not be loaded into the Visual Experience Composer (VEC). (TGT-28176) 
* Multiple UI localization fixes for supported languages.

## Releases 2017 {#reference_59C7622A111C4147804A8AAC6D27BB8D}

### Target Platform (November 8, 2017) {#section_536B3C0F32ED441C8D82704B94F6AF7E}

This release includes the following features and enhancements:

<table id="table_793CDDF1BD9E48BDBABBF6CD979BE186"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js version 1.2.2 is now available. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html" format="dita" scope="local"> Download at.js </a>. </p> <p> 
     <ul id="ul_3C4C9385A0F3489AA2137A2C88AE93CF"> 
      <li id="li_E658799D930547E6901ACFBF7C541F1F"> <p>Fixed an issue that returned a JavaScript error when the Target library loaded on a page using QUIRKS mode. (TNT-28312) </p> </li> 
      <li id="li_050620115ED84CBDA736D94E9AAC6550"> <p>Fixed an issue that caused Target click tracking to break Analytics data collection calls. (TNT-28261) </p> </li> 
      <li id="li_97BC1B7295364ACDAD3FB07005ED592F"> <p>Fixed an issue that caused <span class="codeph"> getOffer() params </span> to fail when <span class="codeph"> targetPageParams() </span> returns an empty string. (TNT-28359) </p> </li> 
      <li id="li_B542D4A4E37141BA8BE79D416E1B58DB"> <p>Fixed an issue with session ID generation when using x-only. (TNT-28361) </p> </li> 
     </ul> </p> <p>The default timeout for at.js is changed from 15 seconds to 5 seconds. </p> <p>If your current setting was 15 seconds, it will be updated to the new default of 5 seconds. If you previously changed it to something different, your setting will not be affected. </p> </td> 
  </tr>  
 </tbody> 
</table>

### Target Standard/Premium 17.11.1 (November 8, 2017) {#section_324A9B1DA0B14F5999FEE41F15B13A44}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use):

<table id="table_6ADDF3552AD04666B76F2D3F457BB042"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Offers </p> </td> 
   <td colname="col2"> <p> If a user has the "Editor" permission, that user cannot edit an offer referenced to a live or scheduled activity. </p> <p> <p>Note:  For Target Premium customers using <a href="https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html" format="html" scope="external"> Enterprise User Permissions </a>, if a user selects the All Workspaces option, Target uses the highest permission of the user across workspaces. If the highest permission is "Editor," Target restricts editing as mentioned above </p>. </p> <p>These restrictions apply to all offers, not just offers created in Target. (TGT-27276) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Response tokens </p> </td> 
   <td colname="col2"> <p>Added the following built-in parameters: </p> <p> 
     <ul id="ul_17AD5B9788514E9DB14ED435A4224BFE"> 
      <li id="li_334F10A5B7934215B4D37278901BAF96"> <p>profile.tntId </p> </li> 
      <li id="li_AA9B4611035344549CC933FFC499289F"> <p>profile.marketingCloudVisitorId </p> </li> 
      <li id="li_DD751027371D4293BF9DB872278BD1B3"> <p>profile.thirdPartyId </p> </li> 
      <li id="li_B6D983A1B68D49AAA40CB401437676F1"> <p>profile.categoryAffinity </p> </li> 
      <li id="li_F5E86BFD14CA4C198F36F3F9987750F9"> <p>profile.categoryAffinities </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.10.1 (October 25, 2017) {#section_EF74751744024C209A02F45322642D37}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use):

<table id="table_307DF0CD143048BC9E419444C556B8FB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E91AEC68A6E45D8B2907C77E752FEC6"> 
      <li id="li_A5778B528358433DB31D700D8F9BCB79"> <p>You can create activity-only audiences from within the three-step guided workflow when creating an activity. This audience can be used in other places within the same activity, but is not stored in the Audiences Library for use in other activities. (TGT-25474) </p> <p> <img src="assets/adhoc_audience.png" id="image_32C7C8B72F51425595A2E266AEFA17E9" /> </p> <p>For more information, see <a href="/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Creating an Activity-Only Audience </a>. </p> </li> 
      <li id="li_691812682A5B42C0941324F2BC7D5740"> <p>For all activities, you can choose a success metric that qualifies the user for the audience. In the past, Target qualified users for an audience when they entered the activity, whereas now you can choose when to evaluate the audience by choosing a success metric. (TGT-15805) </p> <p> <img src="assets/success_metric.png" id="image_0CEC6015A2C4429790A063FE54CC1A35" /> </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-target/apply-reporting-audience-success-metric.md#concept_5F11149ACCA84FE79C7B9F766B6B0595" format="dita" scope="local"> Apply a Reporting Audience to a Success Metric </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Auto-Target </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6F89BD36373E47C4B3A6F8584D431D82"> 
      <li id="li_5F7B590AF8F24066ADD270E9F75CB12F"> <p>Auto-Target activities now support segment-level reporting. (TGT-22777) </p> <p>For more information, see <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </li> 
      <li id="li_35042E7D6BB04265B42F08A23A774E92"> <p>You can change the Control percentage for Auto-Target activities. (TGT-26467) </p> <p> <img src="assets/auto-target-control-small.png" id="image_81F6F61DB61240C289FB71362851AA53" /> </p> <p>For more information, see <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Offers </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_667DDEDDC5284C8393F8BCA5CD9EF12A"> 
      <li id="li_E00DB93297EC4100B46E42D867757DAA"> <p>You can now view offer definition details on a pop-up card in the Offers Library without opening the offer. (TGT-26377) </p> <p> <img src="assets/offer-card.png" id="image_1980AE8E9BED424085CC482C773C20EC" /> </p> <p>For more information, see <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. </p> </li> 
      <li id="li_F71AC4FDAC0E4BEE81D39490E82686C0"> <p>You can copy and edit offers and folders in the Offer selector while creating an activity. (TGT-26936) </p> <p> <img src="assets/offer-picker.png" id="image_1077A6C7A8DD40FB9370CB55BD7260E5" /> </p> <p>For more information, see <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Form-based Experience Composer </p> </td> 
   <td colname="col2"> <p>In the Form-based Experience Composer, Refinements have been replaced with full audience functionality. Refinements for existing activities have been migrated to activity-only audiences. (TGT-13646) </p> <p>For more information, see <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Response Tokens </p> </td> 
   <td colname="col2"> <p>You can now create response tokens from Target without waiting for them to be created in or imported to Target. Previously, in the Response Token UI, you could see only the tokens created via API. Changes to the feature also help you avoid response tokens duplicates. (TGT-26534) </p> <p>For more information, see <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following customer-facing enhancements, fixes, and changes:

* You can delete imported audiences (Target Classic, Experience Cloud, etc.) from the Audience Library. Target warns you if you try to delete an audience used for an active activity. (TGT-25171) 
* Audiences imported from Target Classic are now labeled as Adobe Target Classic in the Audience Library. In the past, the UI did not differentiate between Target Standard/Premium and Target Classic. (TGT-27093) 
* Collections now apply to all criteria (including recently viewed items). (TGT-26646) 
* You can filter by Workspace in the Audience Library and Offer Library (applies to Target Premium users with Enterprise User Permissions). (TGT-26813) 
* Made improvements in the Reports UI for better scrolling in tables and placements of filter drop-down lists. (TGT-23713 & TGT-26819)

### Target Platform Changes (October 13, 2017) {#section_6C298C5C3D01415CB4B658EB2166096C}

<table id="table_8457FAE3508F454F9DFDEF093FBD7E40"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>October 13, 2017</b> </p> <p> <span class="filepath"> at.js </span> version 1.2.1 is now available. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details </a>. </p> <p> 
     <ul id="ul_14D6BB3B51974789BBFC036A45B7A56B"> 
      <li id="li_AE9826C8FC4A4DF4BE61BB72C2946C93"> <p>Fixed an issue when click tracking on a link with target="_blank" prevented Target from opening the link in a new tab. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.9.1 (September 25, 2017 & October 12, 2017) {#section_ECC5DD8B6ED443788B46F53E25FC896E}

This release includes the following features and enhancements (issue numbers in parentheses are for internal Adobe use):

<table id="table_0A8817F64F434875A485FD671C6988AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Mobile Experience Preview </p> </td> 
   <td colname="col2"> <p><b>Updated: October 12, 2017</b> </p> <p> You can now select multiple mobile app activities from the UI and preview them on your device. This feature will allow you to enroll yourself into multiple experiences for previewing and QA without relying on special test builds and simulators. </p> <p>This feature requires that you download and install the appropriate 4.14 (or later) version of the Adobe Mobile SDK. </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html" format="dita" scope="local"> Target Mobile Preview </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mobile Batch and Prefetch Delivery </p> </td> 
   <td colname="col2"> <p><b>Updated: October 12, 2017</b> </p> <p> Content for multiple mboxes can be pre-fetched in a single call and cached locally on the device without worrying how, when, and if the end user will see the content. </p> <p>This feature requires that you download and install the appropriate 4.14 (or later) version of the Adobe Mobile SDK. </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/version-4/prefetch-offer-content.html" format="dita" scope="local"> Prefetch Offer Content </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activities </p> </td> 
   <td colname="col2"> <p>The following enhancements have been made in the activity-creation workflow: </p> <p> 
     <ul id="ul_2D251AC11FC54E86AE84DEFFB6FDF43C"> 
      <li id="li_AB8F12B3CF654120BD16EAE570517741"> <p>While editing an activity, you can make the desired changes on the currently displayed step, click the drop-down on the split button, then select <span class="wintitle"> Next </span> to advance to the next step, click <span class="wintitle"> Save and Close </span> to save your changes and display the activity's <span class="wintitle"> Overview </span> page, or click <span class="wintitle"> Save </span> to save your changes and remain on that step. </p> <p> <img src="assets/edit_split_button_2.png" id="image_ABC7EE42F5D341EC88AACC54CA98DA2F" /> </p> <p>For more information, see <a href="/help/main/c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Edit an Activity</a>. </p> </li> 
      <li id="li_4C71E2570ECF4BBAB08443D89230CE82"> <p>While editing an activity, you can open the desired workflow step, make your changes (for example experience percentages, audiences, and so forth), then save or close the activity without having to advance through the three-step guided workflow. </p> <p> <img src="assets/edit_activity.png" id="image_0B9A2EF729C34A1D9FA84B8B7B17A3C1" /> </p> <p>For more information, see <a href="/help/main/c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Edit an Activity</a>. </p> </li> 
      <li id="li_36EF9AD13B2D40ADB99343C9F758D5FD"> <p>You can now edit or copy an audience by hovering over the desired audience in the <span class="wintitle"> Choose Audience </span> dialog box while choosing targeting in step 2 of the three-step guided workflow. </p> <p> <img src="assets/audience_picker_hover.png" id="image_6DC33A0856A346948E517F0BA4C9039F" /> </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md#concept_A268236C1224451DB7844BF67F41A087" format="dita" scope="local"> Select Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting </p> </td> 
   <td colname="col2"> <p>The following new features and enhancements are available for reporting: </p> <p> 
     <ul id="ul_2D1AF91D1B4E478FBFFA0B83EE30075E"> 
      <li id="li_98E67A4DA8BF4CFF90C279FAC12F4C54"> <p>You can choose the counting methodology for graphs in reports. Note that this is not supported in Auto-Target and Automated Personalization (AP) activities. </p> <p>For more information, see the "Counting Methodology" row in <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a>. </p> </li> 
      <li id="li_5803CE90DB764C9E983702CB6C1AFEE3"> <p>You can view multiple metrics in a single report for Auto-Target A/B activities. (TGT-23464) </p> <p>For more information, see <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> View Multiple Metrics in a Report </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>You can now view the definitions of audiences imported from Target Classic or created via API. (TGT-22630) </p> <p> <img src="assets/imported_mobile_audience_rn.png" id="image_6ED9EA63FD7D440286DBAFDBD696BA64" /> </p> <p>For more information, see "Viewing Audience Definitions" in <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> About Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Code Editor </p> </td> 
   <td colname="col2"> <p>The Form-based Experience Composer and the HTML offers editor now use the same code editor that the Visual Experience Composer (VEC) uses in custom code. (TGT-25808) </p> <p>This enhancement gives you the following features when using the code editor in the Form-based Experience Composer and when creating HTML offers: </p> <p> 
     <ul id="ul_CBB17806FBF34774A8160A61204ED014"> 
      <li id="li_22665F583F1742E280D5BC7EC4203007"> <p>Line numbers are now visible for better usability. </p> </li> 
      <li id="li_B0D863CDAD2E46A4B133BB86886EB527"> <p>Syntax highlighting helps you avoid incorrect syntax for HTML offers. </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geo Targeting </p> </td> 
   <td colname="col2"> <p>You can now use latitude and longitude in geo-targeting. (TGT-12129) </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Node.JS SDK </p> </td> 
   <td colname="col2"> <p>You can install the node.js SDK from <a href="https://www.npmjs.com/package/@adobe/target-node-client" format="https" scope="external"> npm @adobe/target-node-client </a> to easily implement and run server-side tests on your node.js applications. The VisitorID service is enabled in the node SDK to connect all your Adobe data and you can use choose to use Adobe Analytics as your reporting source (A4T). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following customer-facing enhancements, fixes, and changes (issue numbers in parentheses are for internal Adobe use):

* Users with Approver permissions can now generate and enable profile API authentication tokens. (TGT-24074)

  For more information, see [Profile API Settings](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/profile-api-settings.html){target=_blank}. 

* When creating an activity in the Visual Experience Composer and the user reloads the page, the activity URL and associated properties are retained in the UI. The need to reload can occur if the activity uses mixed content (secure and insecure content) or there are permission issues. (TGT-28230) 
* Improved the messaging when an activity uses mixed content (secure and insecure content). The message provides information to help users perform the necessary steps needed to open an HTTP site or a site that has mixed calls (HTTPS and HTTP). (TGT-26271)

For more information, see [Enabling Mixed Content in Your Browser](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md#concept_46D022D50280468C9EF6D5DF6EFC911C). 

* Improved the workflow when a user's Target session times out while configuring options on the Administation, Audiences, and Recommendations pages. When the user clicks Save, the session-expired message displays, but after logging back in, a dialog informs the user of a successful login and the UI remains on the same page in Target with no data loss. (TGT-25557)

### Target Platform Changes (September 27, 2017) {#section_AC32516DFBA64AD2AC9A74171D452778}

<table id="table_701D8D53D1DF4F28ADAC6EC221B0208A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>September 27, 2017</b> </p> <p> <span class="filepath"> at.js </span> version 1.2.0 is now available as a maintenance release that contains mostly bug fixes. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details </a>. </p> <p> 
     <ul id="ul_D11024549C3643C7A756988087498D24"> 
      <li id="li_E1B3994125B64F6AB20B29FE8BCD8459"> <p>Fixed an issue that prevented default actions for click-tracking special cases. (TNT-28089) </p> </li> 
      <li id="li_53806C902AA04B31B59AA87A1E707348"> <p>Fixed an issue when click-tracking on a link with <span class="codeph"> target="_blank" </span> that prevented Target from opening the link in a new tab. (TNT-28072) </p> </li> 
      <li id="li_94F5794330D14C71BA07B3F17D0705FD"> <p> IP addresses can be used as the cookie domain. (TNT-28002) </p> </li> 
      <li id="li_7D2A11B17672419583F9632CDA00D28F"> <p>Fixed an issue that caused flicker in redirect offers with a global mbox or other regional mboxes. (TNT-27978) </p> </li> 
      <li id="li_BA27A749A7A242478080F3D8E04148FC"> <p> Fixed an issue in Experience Targeting activity setup failing within the VEC when switching between Browse and Compose. (TNT-27942) </p> </li> 
      <li id="li_FA11ABA5B9CD435080426805C5359A51"> <p> Fixed incorrect handling on flicker style classes for click-track elements. (TNT-27896) </p> </li> 
      <li id="li_E2DFBAE52FCA4996BA083868CBFCCD10"> <p>Fixed an issue that caused global mbox parameters to become mixed up with all mbox parameters. (TNT-27846) </p> </li> 
      <li id="li_B3153BBD66AA4D51AE81EF6C903CF78D"> <p>Made changes to ensure that Handlebars, Mustache, and other client-side templating libraries are properly handled by <span class="filepath"> at.js </span>. (TNT-27831) </p> </li> 
      <li id="li_B859939C1B5A4DF78CF8ADF236B88306"> <p>Made changes to ensure that <span class="codeph"> sdidParamExpiry </span> is properly initialized and passed to the Visitor API. This is a regression that has been added to <span class="codeph"> at.js 1.1.0 </span>. Previous <span class="filepath"> at.js </span> versions are not affected. This affects only clients using redirect offers and A4T. (TNT-27791) </p> </li> 
      <li id="li_24A748DFB7824AE6AC7331B7EA940BFF"> <p>Made changes to ensure that <span class="codeph"> SCRIPT </span> is executed regardless of the type attribute being used. (TNT-27865) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT) </p> </td> 
   <td colname="col2"> <p><b>September 21, 2017</b> </p> <p>With the release on September 21, Target will change the way users are placed into experiences in Experience Targeting (XT) activities (Landing Page campaigns in Target Classic). For all new and existing activities in both Target Standard/Premium and Target Classic, users must meet the experience targeting rules on every impression to continue to see the experience's content and to be counted in reports. Previously, if the user no longer qualified for any experience, the user would continue to see the content from, and be counted in reports for, the last experience they did qualify for. </p> <p>This change will happen automatically as part of the release for all existing activities and for any new activities created post-release. If the previous method (prior to September 21) is desired, you can create audiences using profile scripts so a user only must meet a condition once to continue to fall into that audience in the future. Then, use those audiences for each experience in the activity. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.8.1 (August 22, 2017) {#section_71A554D072F04B18B359C1626529E5D8}

<table id="table_AAC16F89060D4CC09762A370B86C0885"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Enterprise User Permissions for Target Premium </p> </td> 
   <td colname="col2"> <p>Create separate workspaces in Target and then assign users different roles and permissions for individual digital properties. </p> <p>For more information, see <a href="/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838" format="dita" scope="local"> Enterprise User Permissions </a>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>QA Mode </p> </td> 
   <td colname="col2"> <p>Perform easy activity QA with preview links that never change, optional audience targeting, and QA reporting that stays segmented from live activity data. </p> <p>For more information, see <a href="/help/main/c-activities/c-activity-qa/activity-qa.md" format="dita" scope="local"> Activity QA </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements, Fixes, and Changes**

This [!DNL Target] release includes the following customer-facing enhancements, fixes, and changes: (issue numbers in parentheses are for internal Adobe use):

* We've added more places where you can view audience definition details on a pop-up card in the Target UI without opening the audience. Note that this functionality applies only to audiences created in [!DNL Target Standard/Premium. (TGT-25772)] 
* You can now view definitions of adhoc audiences inside activity creation/overview. (TGT-25570) 
* The following variables are now available as [Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59) arrays: `entiites` and `entityN.categoriesList`.

### Target Platform Changes (August 3, 2017) {#section_FA5BF6808EA74F3A9E8E941530879208}

<table id="table_1B43199F1AE64E69AE65313B23741444"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>August 3, 2017</b> </p> <p> <span class="filepath"> at.js </span> version 1.1 is now available. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html" format="dita" scope="local"> Download at.js </a>. </p> <p>The following enhancements and fixes are included in <span class="filepath"> at.js </span> version 1.1: </p> <p> 
     <ul id="ul_B7408267413347888938E2E7D48ABDBD"> 
      <li id="li_4DDF6DCFE6014C6795B6A9C9DFB54C21"> <p>Added response token handling. For more information, see <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </li> 
      <li id="li_741CD22B7D074FBA90180B2E36FACE0D"> <p>Resolved issue so that <span class="codeph"> document.currentScript polyfill </span> doesn't interfere with Angular 1.X. </p> </li> 
      <li id="li_EF1B3D3DCC7F4D2490D2BFE660EC661C"> <p>Made changes to ensure that click tracking doesn't interfere with visibility property. Click tracking elements are marked with the <span class="codeph"> at-element-click-tracking </span> CSS class instead of <span class="codeph"> at-element-marker </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.3 (August 3, 2017) {#section_D90CB766679442C7A0642E5D79657674}

<table id="table_C81EA97B251547169BC9681E5DDB4B8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Response Tokens </p> </td> 
   <td colname="col2"> <p>Response tokens let you automatically output eligible variables (e.g., profile attributes) in the Target responses that deliver activities (i.e. display mboxes). Response tokens can be used for debugging purposes or for integration with 3rd-party providers (such as Clicktale). </p> <p>Response tokens are similar to <span class="keyword"> Adobe Target Classic </span> server plug-ins and provide feature parity between the two solutions. </p> <p> <p>Note:  Response tokens are available with <span class="filepath"> at.js </span> 1.1 or later.</span>. </p> </p> <p>For more information, see <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Response Tokens </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.2 (July 27, 2017) {#section_6980EC04D3CF4A00919953B9B10BC472}

<table id="table_DB51BD66756F4EBD875ED008B2C7C5D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Auto-Target </p> </td> 
   <td colname="col2"> <p>Auto-Target in now available to all Target Premium customers. </p> <p>Auto-Target uses advanced machine learning to identify multiple high performing marketer-defined experiences, and serves the most tailored experience to each visitor based on their individual customer profile and the behavior of previous visitors with similar profiles, in order to personalize content and drive conversions. </p> <p>While creating an A/B activity using the three-step guided workflow, you can choose to allocate traffic using the <span class="wintitle"> Auto-Target For Personalized Experiences </span> option: </p> <p> <img src="assets/auto-target-ui-small.png" id="image_DB7899CAD51D411EAB858CE132BECAA5" /> </p> <p>For more information, see <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.1 (July 20, 2017) {#section_BB75DE30174F4ADD963451909FB81D74}

<table id="table_BCE36E0D56804E7B8861858DCF2F380E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>You can now view audience definition details on a pop-up card in various places in the Target UI without opening the audience. Note that this functionality applies only to audiences created in <span class="keyword"> Target Standard/Premium. </span> </p> <p> <img src="assets/audience_details.png" id="image_AD0F411715DA43ACB4A913B1E54C13DC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Success metrics </p> </td> 
   <td colname="col2"> <p>Previously, Target allowed dependency on a single metric and that metric had to be reached before its count incremented. You can now provide dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increment. </p> <p>Multiple-metric dependency functionality is not supported for the following: </p> <p> 
     <ul id="ul_EC856F910B704D648065EA7DA13EE5B0"> 
      <li id="li_1A82414FE50B414CAA1A0A88E80BCC1B"> <p>Recommendations activities. This functionality is supported for all other activity types. </p> </li> 
      <li id="li_2D6CF42264D445FCB6C400ED321DE952"> <p>If you use Analytics as your reporting source (A4T). </p> </li> 
      <li id="li_E3A983A70BB04AE8B25A7CEC1F5FE1D9"> <p>The "Viewed a Page" metric type. </p> </li> 
      <li id="li_9AAF6BB275F7489BA691676E308172D5"> <p>The "Clicked an Element" metric type for Visual Experience Composer (VEC) activities. </p> </li> 
     </ul> </p> <p>For more information, see the following topics: </p> <p> 
     <ul id="ul_4B0EFFDD257C42579E19569DCBE15BE3"> 
      <li id="li_2402575F27F547968BD536C460BF81B5"> <p>A/B: <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </p> </li> 
      <li id="li_FB5E7CBC0154406C989F5A5C6CAA0C8F"> <p>Automated Personalization (AP): <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creating an Automated Personalization Activity </a> </p> </li> 
      <li id="li_57C36A7945A24A52BCBD62CA0F15B668"> <p>Experience Targeting (XT): <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </p> </li> 
      <li id="li_06674A3152A547268A1AE5EE818EF1A5"> <p>Multivariate (MVT): <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting (Auto-Allocate A/B Tests) </p> </td> 
   <td colname="col2"> <p>The ability to view multiple metrics is now available for Auto-Allocate A/B activities. </p> <p>For more information, see <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> View Multiple Metrics in a Report </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>Audience site page types and comparison operators now match types and comparison operators in Target Classic. </p> <p>You can now create site pages audiences using you own "user-defined query parameter" or "user-defined header." </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/site-pages.md#concept_6425D5304568490899E8340CC94798A9" format="dita" scope="local"> Site Pages </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activities </p> </td> 
   <td colname="col2"> <p>The Activity list now lets you filter on Auto Allocate and Auto Target activity types. </p> <p>For more information, see <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Criteria &amp; Promotions </p> </td> 
   <td colname="col2"> <p>You can now handle empty values when filtering by Entity Attribute Matching, Profile Attribute Matching, and Parameter Matching. </p> <p>For more information, see <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This [!DNL Target] release includes the following customer-facing enhancements and fixes: (issue numbers in parentheses are for internal Adobe use):

* Improved the workflow when a user's [!DNL Target] session times out while creating or editing an activity or offer. When the user clicks [!UICONTROL Save], the session-expired message displays, but after logging back in, a dialog informs the user of a successful login and the UI remains on the same page in [!DNL Target] with no data loss.

  If a user performs intermittent action on a [!DNL Target] page and experiences a session timeout, the user is directed to re-log in and is then directed to the last page worked on in the [!DNL Target] UI.  

* Fixed an issue that caused custom code changes to be lost if the user browses away (changes experiences, switches page, switches audience, clicks Next, etc.) and forgets to save changes. The user is now prompted to save the changes. (TGT-23766) 
* When an activity is archived, "Archived the activity" displays instead of "Updating the activity." (KB-1517) 
* The drop-down picker in the following locations within the Target UI has been replaced with auto-complete functionality to improve speed and performance: (TGT-22939)

    * Activity Page > *activity* > Step3 > Report Suite picker 
    * Audiences > Create Audience > Visitor Profile 
    * Recommendations > Feed Creation > When source type > Analytics > Report Suite picker

* Improved error messaging when a site has "X-Frame-options" set to SAMEORIGIN and the site cannot be loaded in the Visual Experience Composer (VEC). The message prompts the user to switch to the Enhanced Experience Composer in Administration > Visual Experience Composer. (TGT-17356) 
* Reports in Target Standard/Premium now display in your account's time zone rather than the Target server time zone (US EST). (TGT-24868) 
* If activities created in [!DNL Target] are updated from outside of [!DNL Target] (for example, via Adobe I/O), the following activity attributes are imported back into [!DNL Target]:

  `thirdpartyId`

  `startDate`

  `endDate`

  `status`

  `priority`

  `marketingCloudMetadata(remoteModifiedBy)`

  This import job will run when the activities page is opened, with a maximum delay of ten minutes. (KB-1526)

### Target Standard/Premium 17.6.2 (June 22, 2017) {#section_F0372B07B56E454CB048CE79FF56E9CD}

<table id="table_8C4DB1B83B874E4C85CE9FF352E7B857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F5BB1074DD4140C798CB55D68DEEF824"> 
      <li id="li_9596AABA14C64DEEB2E70E8ADED8AA74">Automated Personalization activities can be created using the form-based composer. </li> 
      <li id="li_315F5FF590404670A677FEA6E4E0DF5D">New confidence numbers for Automated Personalization </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Criteria and Promotions </p> </td> 
   <td colname="col2"> <p> You can now create dynamic criteria and promotions based on profile attribute matching and parameter matching. </p> <p> <img src="assets/inclusion_rules.png" id="image_D136F75A5C2B428390FE231559AEC2D3" /> </p> <p> <p>Note:  If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>VEC Code Editor improvements </p> </td> 
   <td colname="col2"> <p> If the page format changes and actions cannot be applied, an alert now appears next to each failing action. Previously, a general error notified the user that the page structure had changed. Now, the code editor highlights each failed action. </p> </td> 
  </tr> 
 </tbody> 
</table>

This [!DNL Target] release includes the following customer-facing enhancements and fixes:

* Improved performance on host groups and recommendations entity search pages. 
* More descriptive error messages throughout Target, especially when related to sync failures. 
* Fixed an issue that caused the count on activity diagram to sometimes be incorrect in UI when auto-dedupe is applied after creating exclusion groups. 
* Fixed an issue where the manual inclusions might not be correctly reflected in UI when an existing activity with Exclusion Group is edited.

### Target Standard/Premium 17.6.1 (June 8, 2017) {#section_1D05FE23CE3744DDB5D28E933341F575}

<table id="table_47117524922A472AA977C652B581B356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT) activities </p> </td> 
   <td colname="col2"> <p>Drag-and-drop functionality lets you arrange audiences and experiences in the desired order while creating or editing XT activities. Visitors will be evaluated for experiences in order, from top to bottom. </p> <p> <img src="assets/move_exp.jpg" id="image_0AA2EE2B5B00462C8E125A30F145E654" /> </p> <p>For more information, see <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Create Experience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting: A/B, XT, and Recommendations </p> </td> 
   <td colname="col2"> <p>Reports for A/B, XT, and Recommendations activities include visual representations that let you visually see the confidence interval and lift so that you can more accurately determine a winner. You can mouse over the representations to see the actual numbers. This feature is not available for activities that use Analytics as the reporting source (A4T). </p> <p> <img src="assets/whisker.JPG" id="image_DFD8EED61D52497280066D55AD473479" /> </p> <p>For more information, see <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Report Settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization (AP) activities </p> </td> 
   <td colname="col2"> <p>You can create Exclusion Groups in AP activities to ensure that experiences with the designated offers are automatically excluded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Criteria and Promotions </p> </td> 
   <td colname="col2"> <p><b>(Scheduled to be released June 22, 2017)</b> You can now create dynamic criteria and promotions based on profile attribute matching and parameter matching. </p> <p> <img src="assets/inclusion_rules.png" id="image_694305D969AF43F7822012F69614250C" /> </p> <p>For more information, see <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. </p> <p> <p>Note:  If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Naming activities </p> </td> 
   <td colname="col2"> <p>You are now prompted to name the activity before saving. You cannot save an activity without a name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New location for Target Forum </p> </td> 
   <td colname="col2"> <p> The Target Forum has moved to the new <a href="https://experienceleaguecommunities.adobe.com/t5/adobe-target/ct-p/adobe-target-community" format="https" scope="external"> Adobe Community Platform </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.4.1 (April 27, 2017) {#section_24E6889AF1E0405497F6F77A407A9A46}

This release includes the following features and enhancements:

<table id="table_9554D0094421417C88548BDC97B710F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Reporting </td> 
   <td colname="col2"> <p><b>View Multiple Goals/Metrics:</b> You can now view multiple metrics in A/B and Experience Targeting (XT) activities, with the exception of <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Auto-Allocate </a> and <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target </a> A/B activities. </p> <p>For more information, see <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> View Multiple Metrics in a Report </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This [!DNL Target] release focuses on back-end fixes and includes the following customer-facing enhancements and fixes: (issue numbers in parentheses are for internal Adobe use):

* Fixed an issue that caused the "Increment Count, Release User & Allow Reentry" setting in Advanced Settings for activities to not function correctly. (TNT-26556) 
* Fixed an issue that prevented Customer Attribute data from being removed from Target after being updated with NULL in the Experience Cloud user interface. (TNT-26462)

### Target Platform Changes (April 13, 2017) {#section_B59C26405EB7482AA80820D6D39B9C44}

<table id="table_6167ECB7B44F40DCADF299F46F1F795C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> at.js </span> version 0.9.6 is now available. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html" format="dita" scope="local"> Download at.js </a>. </p> <p>The following enhancements and fixes are included in <span class="filepath"> at.js </span> version 0.9.6: </p> <p> 
     <ul id="ul_108DF85393614C69988E299485D338FD"> 
      <li id="li_4117C900982240B5AFFCFE1B2716A443"> <p>Redirect offer support for A4T. After you download and install <span class="filepath"> at.js </span> version 0.9.6, you can use redirect offers in activities that use <span class="keyword"> Adobe Analytics </span> as the Reporting Source for <span class="keyword"> Target </span> (A4T). Besides <span class="filepath"> at.js </span> version 0.9.6, there are other minimum requirements your implementation must meet in order to use redirect offers and A4T. For more information and additional important information you should know, see <a href="/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Redirect Offers - A4T FAQ </a>. </p> </li> 
      <li id="li_DA5321D72E81496DB7C49D589E1A59C4"> <p>Prior to <span class="filepath"> at.js </span> 0.9.6, when the Visitor API was present on the page and the <span class="codeph"> visitorApiTimeout </span> setting was too aggressive, Target could run into a situation when no MCID data was sent in the <span class="keyword"> Target </span> request. This could lead to issues like unstitched hits in <span class="keyword"> Analytics </span> when using A4T. </p> <p>This behavior has been changed in <span class="filepath"> at.js </span> 0.9.6, even if the <span class="codeph"> visitorApiTimeout </span> is set to say 1 ms, Target will try to collect SDID, tracking servers, and customer IDs data and send those in the Target request. </p> </li> 
      <li id="li_B11CE11D9A594CB1ABB85BD0D93C4A15"> <p>Added the <span class="codeph"> selectorsPollingTimeout </span> setting. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_D6F862099A374FE394F4DA3520A1BBF0"> <p>The format of the response from <span class="codeph"> getOffer() </span> has been changed. For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html" format="dita" scope="local"> adobe.target.getOffer(options) </a>. </p> </li> 
      <li id="li_80166567ED8945ECB37FEEE2C5F06ACE"> <p>Console logging has been added for unsupported <span class="codeph"> &lt;!DOCTYPE&gt; </span> declarations. </p> </li> 
      <li id="li_02904EBAE8D3400092B762F0B28B0C86"> <p>Fixed an issue where <span class="keyword"> Target Classic </span> plugins weren't being applied correctly when multiple default offers were delivered to a single mbox. (TGT-22664)</p> </li> 
      <li id="li_7016022D9DDE4529B77984F195825AB7"> <p>Improved cookie-setting for two letter top-level-domains (TLDs) to ensure that the mbox cookie is set correctly for these domains (for example, <span class="filepath"> test.no </span>, <span class="filepath"> autodrives.ca </span>, and so forth). </p> </li> 
      <li id="li_3B1F618DEC744056B5BB172C4DBB359A"> <p>The algorithm for extracting the top-level domain that should be used when saving cookies has changed in <span class="codeph"> at.js </span> version 0.9.6. Because of this change, cookies cannot be saved to addresses that use IP. Most of the time, IP addresses are used for testing purposes, but as workarounds you can use DNS entries or adjust the hosts file on a local box. </p> </li> 
      <li id="li_A52181499E63402DB4E16E33E36A9400"> <p>Fixed move and rearrange actions handling when properties are string values instead of integers. </p> </li> 
     </ul> </p> <p>For information about this and previous versions of <span class="filepath"> at.js </span>, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.3.1 (March 30, 2017 - Updated April 13, 2017) {#section_5C13660A8AA34F35A9CBEFEEC88738D0}

This release includes the following features and enhancements:

<table id="table_4BA8DA701BC64427957355E144570EFE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Analytics for Target (A4T) </p> <p>Redirect Offers </p> </td> 
   <td colname="col2"> <p><b>Updated April 13, 2017.</b> </p> <p>You can now use redirect offers in activities that use <span class="keyword"> Analytics </span> as the reporting source. </p> <p>These libraries must be included on both the page with the redirect offer and the page to which the visitor is redirected. As a part of this change, new URL parameters will automatically be added to your redirect URLs if the Visitor Id service is implemented on your site, regardless of whether or not you are using Analytics as the reporting source for that activity. </p> <p>For more information, see <a href="/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Redirect Offers - A4T FAQ </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>The following enhancements have been made to audience targeting: </p> <p> 
     <ul id="ul_C920198404654C97A33190A29ACA6990"> 
      <li id="li_DB52EF909C9640649981940460CDF2B5"> <p><b>Week and Day Parting:</b> You can set <span class="wintitle"> Week and Day Parting </span> options to create recurring patterns for audience targeting. </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </li> 
      <li id="li_2541A6EF2D604CE098012A16909C237E"> <p><b> Exclusions in Combined Audiences:</b> You can now add exclusion rules and exclude audiences when combining multiple audiences. </p> <p>For more information, see <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p><b>Dynamic Promotions:</b> Target Recommendations now supports dynamic matches for promotions. </p> <p>For more information, see <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Use Dynamic and Static Inclusion Rules </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>The ability to view multiple metrics in a report, included in the Target 17.3.1 release (March 30, 2017) has been removed due to unexpected behavior. This feature will be available again in an upcoming release.

This [!DNL Target] release includes the following enhancements and fixes: :

* The [!DNL Target] user interface has been updated to support redirect offers in activities that use [!UICONTROL Analytics for Target] (A4T) as the reporting source. This functionality will require [!DNL at.js] 0.9.6, which will be available soon. 
* The [!DNL Target] user interface was updated in some places:

    * In reports and activities, some options ( [!UICONTROL Edit], [!UICONTROL Share to Feed], [!UICONTROL View Experience URLs], etc.) are now accessed by clicking the [!UICONTROL More Options] icon (  ![icon_more_options image](assets/icon_more_options.png)    
    
      ). 
    * In the [!UICONTROL Offers] library, offers now display in a list rather as cards. Other minor UI changes were made throughout the [!UICONTROL Offers] library UI.

* Significantly improved performance on the [!UICONTROL Activity] and [!UICONTROL Audience] lists. Also, load times for search results return significantly faster. 
* "Views" is now "Visits" in the [!UICONTROL Offer Level Report] for [!UICONTROL Automated Personalization] reports. 
* [!DNL Target] now supports switching of environments (host groups) for [!UICONTROL Automated Personalization] activities. 
* [!UICONTROL Automated Personalization] activities now support host groups.

### Target Standard/Premium 17.2.1 (February 21, 2017) {#section_FC6412353DE64E848FFD5E8EFF72C7C7}

>[!NOTE]
>
>[!DNL Adobe Experience Manager] 6.2 with FP-11577 (or later) now supports [!DNL at.js] implementations with its [!UICONTROL Adobe Target Cloud Services] integration. For more information, see [Feature Packs](https://experienceleague.adobe.com/docs/) and [Integrating with Adobe Target](https://experienceleague.adobe.com/docs/) in the *Adobe Experience Manager 6.2* documentation.

This [!DNL Target] release focuses on usability and performance improvements and includes the following enhancements and fixes (issue numbers in parentheses are for internal Adobe use):

* Added additional items to the Help menu that can be accessed from the top right corner of the [!DNL Target] user interface. New options include: "Blogs" and "Videos." The "Adobe Experience Cloud Status" option is now "Adobe Target Standard/Premium Status." (TGT-22629) 
* When deleting an audience, [!DNL Target] displays a list of activities that reference that audience. Users can click each activity in the list to display its [!UICONTROL Overview] page. (TGT-17997) 
* Improved `user.activeCampaigns` to return the campaign ID for all campaigns/activities that the user is in, even if he or she has not interacted with the campaign/activity in the current session. (TNT-26237) 
* The [!UICONTROL Create Activity] button on the [!UICONTROL Activities] page is now active before all activity names are loaded in the list. This improvement lets users create new activities faster, especially when the account has many configured activities. (TGT-21470) 
* Made enhancements to the Enhanced Experience Composer (EEC) to improve loading time for websites running HTTPS accessed via proxy. Target no longer fetches static resources via proxy. (TGT-21793) 
* Made performance improvements on the [!UICONTROL Goals & Settings] page, especially load time when many metrics are defined for an activity. (TGT-21654) 
* Added a tool tip on the [!UICONTROL Goals & Settings] page of all activities using [!UICONTROL Analytics for Target] (A4T) reporting informing users that a tracking server is not required if the activity's pages have at.js (version 0.9.1 or later) loaded. (TGT-22607) 
* Metric names now display on the [!UICONTROL Goals & Settings] page without users needing to expand each metric to view the entire metric name. This improvement lets users edit metrics quicker and more efficiently. (TGT-21276) 
* You can now apply [!DNL Recommendations] inclusion rules to custom criteria (uploaded via CSV), just like any other criteria. (TGT-21896) 
* Improved the user interface and usability of the [!UICONTROL Offers] page, especially when creating or managing folders and creating offers. (TGT-22509 and TGT-22187) 
* Improved the user experience in the [!UICONTROL Visual Experience Composer] (VEC) when selecting items to hide. 
  (TGT-22224) 
* Improved the user experience when creating activities using the [!UICONTROL Form-Based Experience Composer]. When choosing an mbox location, the validation border remains highlighted after clicking [!UICONTROL Next]. (TGT-22221) 
* Enhanced the downloaded reports to differentiate between active and deleted offers. (TGT-22449) 
* Fixed an issue that prevented older assets from displaying in the infinitely scrollable asset list in the Experience Cloud Assets core service user interface. (TGT-19733) 
* Fixed an issue where the extreme order setting was not honored in downloaded CSV reports. (TGT-21871) 
* Fixed an issue where extreme orders were not marked correctly in the downloaded [!UICONTROL Order Details]CSV report. (TGT-22500) 
* Fixed an issue that caused the incorrect order time to display in the downloaded [!UICONTROL Campaign Audit] CSV report, even though the report displayed the correct order date. (TNT-26469) 
* Fixed an issue that prevented the [!UICONTROL Disable JavaScript] option from working correctly on multi-page activities. (TGT-15130) 
* If you use the Form-Based Experience Composer with an mbox other than the auto-created global mbox ( `target-global-mbox`), and then choose an engagement metric as a success metric, the metric increments only on pages that have the mbox used in the activity. As an example, if your mbox is `homepage_mbox`, the [!UICONTROL Pages Per Visit] metric is the number of hits to the `homepage_mbox` during that visit.

  If this is not what you want, you can add another location to the activity and assign the global mbox to that location and give it default content. This workaround connects the global mbox to the activity and allows Target to count the metric for reporting.

### Target Platform Changes (January 18, 2017) {#section_EA41802B2B24426FBA88D25E17DBE360}

<table id="table_3A2CD47252894F119B0E60BF6A9285B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> version 0.9.4 </p> </td> 
   <td colname="col2"> <p>January 18, 2017 </p> <p> <span class="codeph"> at.js </span> version 0.9.4 contains the following changes: </p> <p> 
     <ul id="ul_8F149C28E2D946B9888B4D2F45167C3C"> 
      <li id="li_93E866BBFE374E93BCDB65BCFAC33B62"> <p> mbox names can now contain special characters, including ampersands ( &amp; ). (TNT-26144) </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html" format="dita" scope="local"> at.js Configurations </a>. </p> </li> 
      <li id="li_99309046030B4D93B59113C01A8789DA"> <p>Added <span class="codeph"> secureOnly </span> setting that indicates whether <span class="codeph"> at.js </span> should use HTTPS only or be allowed to switch between HTTP and HTTPS based on the page protocol. This is an advanced setting that defaults to False and can be overridden via <span class="codeph"> targetGlobalSettings </span>. (TNT-26183) </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-functions.html" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_D84D578C43A24D4896795999F841CEB8"> <p>The <span class="wintitle"> Legacy Browser Support </span> option is available in <span class="codeph"> at.js </span> version 0.9.3 and earlier. This option was removed in <span class="codeph"> at.js </span> version 0.9.4. </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html" format="dita" scope="local"> at.js Configurations </a>. </p> </li> 
     </ul> </p> <p>For detailed information about the changes in each version of <span class="codeph"> at.js </span>, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="html" scope="external"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.1.1 (January 19, 2017) {#section_88AFA2F54CF24DF7822CFEBB07DFABE2}

This release includes the following features and enhancements:

<table id="table_4F7D4A71F5DF4E8782C7DBEEEF24AD04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Content/Offers </p> </td> 
   <td colname="col2"> <p>The following enhancements are now available for offers: </p> <p> 
     <ul id="ul_7D8E81443E0F48B6A0C1D1DF6F27D292"> 
      <li id="li_EA529EF4EBC2416E9D3B9E7251E7AAAB"> <p>The Content page has been renamed to Offers. In addition, there are now two tabs along the right side to separate code offers from image offers. </p> <p>If you had code and images in the same folder before this release, Target will split them into two duplicate folders. </p> </li> 
      <li id="li_9574FA6BDCFB4BAB938273BF7F4B21C8"> <p>Offers created via Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services (AMS), and APIs are now visible in the Target Standard/Premium user interface. Offers created in Target Classic are editable in Target Standard/Premium. (TGT-15738) </p> <p> Offers updated in the last two years using these methods will be visible in Target Standard/Premium (i.e. January 2015 and beyond). </p> </li> 
      <li id="li_CAD67C9EBB564525ABD2269D918275F8"> <p>You can now filter offers by source and type. </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Offers </a>. </p> <p>The following enhancement has been made to geo-location targeting: </p> <p> 
     <ul id="ul_DD8B50F980B8447A8C37EA96530D8949"> 
      <li id="li_348E04AB29B14E6F83E3A7E7BF7D75B8"> <p>You can now use <span class="codeph"> profile.geolocation </span> values directly as tokens in offers, plugins, and so forth. (TNT-25967) </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reporting </p> <p> <p>Note:  These enhancements do not apply to Analytics for Target (A4T) reports. </p> </p> </td> 
   <td colname="col2"> <p>The following reporting enhancements are now available for Target reports. </p> <p> 
     <ul id="ul_ACFCA821B120419EA252EF5031309D52"> 
      <li id="li_0B634602BB044AEDB26DAF78189AB833"> <p>The user interface for reports has been redesigned. </p> </li> 
      <li id="li_309435D10AE84E8795C4CCC1F36747F7"> <p>Target reports now have an option to reset reporting data to remove old data. (TGT-5933) </p> </li> 
      <li id="li_9D30BFCC4CD6461B9DDCD5797A5E2B3A"> <p>The counting methodology options for reporting includes Visitors (the default), Visits, and Activity Impressions. (TGT-10002) </p> </li> 
     </ul> </p> <p>For more information, see <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Report Settings </a> and <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Counting Methodology </a>. </p> <p>The following reporting enhancements are now available for downloadable CSV reports: </p> <p> 
     <ul id="ul_18B0636A41B94F9F903ABFE3E13285DA"> 
      <li id="li_2422075AA0A34F868809C5D580FC5D4B"> <p>The offer-level CSV report now has additional details about each offer. (TGT-18995) </p> </li> 
      <li id="li_659D126E846348D4BE4544962F41539F"> <p>Downloaded offer-level CSV files now always include data from control and targeted segments for <span class="wintitle"> Automated Personalization </span> reports. (TGT-22000) </p> </li> 
     </ul> </p> <p>The following reporting enhancements are now available for Automated Personalization (AP) reports. </p> <p> 
     <ul id="ul_5743684487CD4905BA998C298FD423D7"> 
      <li id="li_EB48BA21E00C4878B4408D24DD23BA9C"> <p>Improved reporting load time for Automated Personalization activities. </p> </li> 
      <li id="li_B8ECCE250A674B83A66705AD5C45B9C3"> <p>The confidence interval for continuous variables (Revenue and Engagement metric types) is now displayed in Automated Personalization (AP) summary reports. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activities </p> </td> 
   <td colname="col2"> <p>The following enhancements are now available for Target activities: </p> <p> 
     <ul id="ul_436556860E6C4AEEB35411A02E78A199"> 
      <li id="li_5CC3B995D0AF4B658B3D6C3F6895AA41"> <p>Activities created in <span class="keyword"> Adobe Mobile Services </span> now display within the <span class="keyword"> Target Standard/Premium </span> user interface. (TGT-10806) </p> <p>For more information, see <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </li> 
      <li id="li_684F9FC5CF414F4A892E6495352B5939"> <p>When creating multivariate tests, you can now exclude more than 10 percent of experiences from the test, provided you acknowledge the warning that you must then use offline reporting for analysis. (TGT-21719) </p> <p>For more information, see <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> Preview Experiences for a Multivariate Test </a>. </p> </li> 
      <li id="li_B2FC7414C76848B39AD6EA20EE483F06"> <p>The Campaign ID is now visible on each activity's Overview page. This is useful for API and troubleshooting operations. (TGT-20928) </p> </li> 
      <li id="li_5A9880AFE5FB46168D92255AA088B854"> <p>The design for the Collisions and Change Log pages have been improved. </p> </li> 
      <li id="li_1489EA6C30C94B2AB394189E5FAFF6F6"> <p>The maximum allowed length of anonymous offer names in Automated Personalization (AP) activities has been increased from 30 to 250 characters. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiences </p> </td> 
   <td colname="col2"> <p>The following enhancements are now available for audiences: </p> <p> 
     <ul id="ul_F1D1F97266134D4ABE627CF2DCE2C6D4"> 
      <li id="li_99A611FCC1254D229D79B8FD075B952A"> <p> <span class="wintitle"> Device Marketing Name </span> is now available as a built-in option from the drop-down list when creating audiences targeting mobile devices. </p> <p>This change lets you easily pick a device model name rather than searching for the appropriate device model number. For example, the Galaxy S7's marketing device name is "Samsung Galaxy S7 Edge," while the device model is "SM-G9350." (TGT-18393) </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p>The following enhancements have been made to Recommendations: </p> <p> 
     <ul id="ul_9D3644890C0C472D8B485DE9A52898B3"> 
      <li id="li_1E5662348F6E4ABDB2B74FE3326F2FD3"> <p>The Backup Algorithm result line is now included in Top Viewed and Top Bought CSV downloads. The backup Recommendation starts with "*," </p> </li> 
      <li id="li_91DFD809378D4C20918F8F875747CE07"> <p>Additional statuses let you know the progress of your Recommendation feeds. </p> <p>For more information, see <a href="/help/main/c-recommendations/c-products/feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feeds </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhanced Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>Updated the IP addresses for the Enhanced Visual Experience Composer (VEC). </p> <p>If you allowlist IP addresses used for the VEC, add the new IP addresses. </p> <p>For more information, see <a href="/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4" format="dita" scope="local"> Troubleshooting the Visual Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Releases 2016 {#reference_607661929B504CCFAB3791B13C0DCDBE}

### Target Standard/Premium 16.10.2 (November 8, 2016) {#section_2FDEFB3D56CC4BD7BC04DBEECFF6E942}

**Fixes**

This release includes the following fixes:

* Fixed an issue in [!DNL Recommendations] where feeds could not be created for any non-default environments (host groups).  
* Made several improvements to reduce activity syncing errors. 
* You can no longer create redirect offers for activities using [!DNL Analytics for Target] (A4T).

### Target Standard/Premium 16.10.1 (October 25, 2016) {#section_F76F7329FCAC452FB88F8BE0BA727044}

This release includes the following features and enhancements:

<table id="table_F8C01B2A9F07443490DB3025AC3AAC2A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Auto-Allocate: Winner Badge </td> 
   <td colname="col2"> <p>We've now made it easier to determine a winner in an Auto-Allocate A/B activity. </p> <p>Many marketers make the mistake of prematurely declaring a winning experience before the results indicate the clear winner. </p> <p>When using the <span class="wintitle"> Automated Traffic Allocation </span> feature, <span class="keyword"> Target </span> displays a badge at the top of the activity's page indicating "No Winner Yet" until the activity reaches the minimum number of conversions with sufficient confidence. When a clear winner is declared, <span class="keyword"> Target </span> displays "Winner: Experience X." </p> <p>For more information, see <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a> and <a href="/help/main/c-activities/automated-traffic-allocation/determine-winner.md#concept_5741A89ED7224E1285A3BC34B2CCD0F9" format="dita" scope="local"> Determine a Winner </a>. </p> <p> <p>Note:  Auto-Allocate A/B activities are no longer supported in Analytics for Target (A4T) going forward. With this release, any active Auto-Allocate A/B activities with A4T enabled will be switched to <span class="wintitle"> Manual </span> mode (equal traffic allocation). </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target mobile devices by carrier </td> 
   <td colname="col2"> <p>Create an audience to target mobile devices based on mobile carrier (Verizon, Sprint, AT&amp;T, T-Mobile, etc.). The <span class="wintitle"> Mobile Carrier </span> option is under the <span class="wintitle"> Geo </span> settings. </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Generate mboxTrace authentication token from Target UI </td> 
   <td colname="col2"> <p>Enable advanced <span class="keyword"> Target </span> debugging tools by creating a temporary authentication token. </p> <p>Click <span class="uicontrol"> Generate Authentication Token </span> on the <span class="wintitle"> Implementation Details </span> page ( <span class="uicontrol"> Administration </span> &gt; <span class="uicontrol"> Implementation </span>). You can then add the resulting parameter to your web page URLs for troubleshooting purposes. </p> <p>For more information, see "Retrieve the Authorization Token to Use With Debugging Tools" in <a href="/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Troubleshooting Content Delivery </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Criteria set sequencing </td> 
   <td colname="col2"> <p>Use sets of up to five pre-created criteria in a single experience for greater control over the recommendations presented to visitors. </p> <p>For more information, see <a href="/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md"> Create Criteria Sequences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Insert external promotions </td> 
   <td colname="col2"> <p>Add promoted items and control their placement in your Recommendations designs. </p> <p>For more information, see <a href="/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Adding Promotions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="firstlook"> <p><b>First Look</b> </p> Auto-targeting in A/B activities </td> 
   <td colname="col2"> <p> <p>Note:  This "First Look" offering is enabled for a few customers in this release for testing and feedback. </p> </p> <p>Automatically target experiences in A/B tests to serve the right experience to the right visitor. </p> <p>For more information, see <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target For Personalized Experiences </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Platform Changes (October 10, 2016) {#section_0761AED70C3E44EA9D8546107B162CC1}

<table id="table_E3E52A4362724D05A8472DB5F51A2429"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> version 0.9.3 </p> </td> 
   <td colname="col2"> <p>October 10, 2016 </p> <p> <span class="codeph"> at.js </span> version 0.9.3 is available. </p> <p> 
     <ul id="ul_E4D300700390433E9EF8D5C9D3AA7669"> 
      <li id="li_E916EB3A77ED4CFF90CF6B4D30F188B1"> <p>Ensures mbox calls fire in Microsoft Internet Explorer 11 when legacy browsers are disabled in the <span class="codeph"> at.js </span> settings. </p> </li> 
      <li id="li_1130509832CE429DB6DE636404CC54E1"> <p>Ensures that default content is rendered if a dynamic remote offer fails (for example, if the URL is incorrect and returns a 404 error). </p> </li> 
      <li id="li_21B5225D894B43CB863A775C937F66F4"> <p>Ensures that elements are revealed quickly when VEC click-tracking selectors can't be found in the DOM. </p> </li> 
     </ul> </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (September 22, 2016) {#section_3CD20678B6254DE1A9BD41FDD2255DDD}

This release includes the following features and enhancements:

<table id="table_FED049F97C054CA895E0AEA3F2B180BF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Combine audiences </td> 
   <td colname="col2"> <p>Combine multiple audiences (including <span class="keyword"> Adobe Experience Cloud </span> audiences and <span class="keyword"> Target </span> audiences) on the fly during the activity-creation workflow. </p> <p>For example, you can target all loyalty customers by including a specific <span class="keyword"> Audience Manager </span> segment for loyalty status and combine it with a <span class="keyword"> Target </span> segment made up of people who signed up for your loyalty program during the current session, instead of creating a third, permanent audience. </p> <p>For more information, see <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target visitors during a specific time period </td> 
   <td colname="col2"> <p>Add start and end dates to target an audience. </p> <p>For example, using the new combined, ad-hoc audiences mentioned above, you can target low-spenders with specific content during the three days leading up to Black Friday and other content after Black Friday. </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Save smart collections </td> 
   <td colname="col2"> <p>Search functionality on the <span class="wintitle"> Content </span> page now includes saved folders, called smart collections, to save time when performing similar searches. </p> <p>For more information, see <a href="/help/main/c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Search Content and Create Smart Collections </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Add a link to an image. The link can be a click-through link, destination link, or a landing link. </p> <p>For more information, see <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements**

This release includes the following enhancements:

|  Enhancement  | Description  |
|---|---|
|  Visual Experience Composer (VEC)  | Improved error messaging.  |

**Known Issues**

* The [!UICONTROL Render Using JavaScript] option is currently not supported if it is used along with custom code in the Visual Experience Composer.

### Target Platform Changes (September 2016) {#section_1955146045A247D393DB824669A2A916}

<table id="table_8FDAEED5D84C4C718AB863BD6C383F20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> version 0.9.2 </p> </td> 
   <td colname="col2"> <p>September 21, 2016 </p> <p> <span class="codeph"> at.js </span> version 0.9.2 is available. </p> <p> 
     <ul id="ul_0778A9049C9D48A7B6CB4B79A95F0F4C"> 
      <li id="li_689FF306179F4EC3B391DEE3C53F4B1D"> <p>Added an <span class="codeph"> optoutEnabled </span> setting to enable or disable the Device Graph opt-out. If this setting is set to <span class="codeph"> true </span> and the visitor has opted out of tracking, the visitor's browser will not make any mbox calls. Device Graph is currently in Beta. This setting is set to <span class="codeph"> false </span> by default, but must be set to <span class="codeph"> true </span> if you are using Device Graph.</p> </li> 
      <li id="li_663462C0680049F89CA8FE1853F31807"> <p>Added <span class="codeph"> CustomEvent </span> support for the notification mechanism. Previously, the <span class="codeph"> at.js </span> event notification mechanism could not be used via standard DOM APIs, such as <span class="codeph"> document.addEventListener() </span>. Now you can use <span class="codeph"> document.addEventListener() </span> to subscribe to <span class="codeph"> at.js </span> events, such as request events and content rendering events. </p> </li> 
      <li id="li_3FB2914F8D2F4AFFAA9B4622E8CA1EFF"> <p>Fixed an issue related to offers created in the Visual Experience Composer (VEC). Prior to this release, Target hid the selectors and un-hid them only when all selectors matched. In <span class="codeph"> at.js </span> 0.9.2 Target un-hides the selectors as soon as they are matched. </p> </li> 
     </ul> </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (September 22, 2016) {#section_60ADF842E4A0424E8D2A81FB8B813A7A}

This release includes the following features and enhancements:

<table id="table_896218AECE4C4EC691B76E79CC7DC356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Combine audiences </td> 
   <td colname="col2"> <p>Combine multiple audiences (including <span class="keyword"> Adobe Experience Cloud </span> audiences and <span class="keyword"> Target </span> audiences) on the fly during the activity-creation workflow. </p> <p>For example, you can target all loyalty customers by including a specific <span class="keyword"> Audience Manager </span> segment for loyalty status and combine it with a <span class="keyword"> Target </span> segment made up of people who signed up for your loyalty program during the current session, instead of creating a third, permanent audience. </p> <p>For more information, see <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Combining Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target visitors during a specific time period </td> 
   <td colname="col2"> <p>Add start and end dates to target an audience. </p> <p>For example, using the new combined, ad-hoc audiences mentioned above, you can target low-spenders with specific content during the three days leading up to Black Friday and other content after Black Friday. </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Time Frame </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Save smart collections </td> 
   <td colname="col2"> <p>Search functionality on the <span class="wintitle"> Content </span> page now includes saved folders, called smart collections, to save time when performing similar searches. </p> <p>For more information, see <a href="/help/main/c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Search Content and Create Smart Collections </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Add a link to an image. The link can be a click-through link, destination link, or a landing link. </p> <p>For more information, see <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements**

This release includes the following enhancements:

|  Enhancement  | Description  |
|---|---|
|  Visual Experience Composer (VEC)  | Improved error messaging.  |

**Known Issues**

* The [!UICONTROL Render Using JavaScript] option is currently not supported if it is used along with custom code in the Visual Experience Composer.

### Adobe [!DNL Target] Standard/Premium 16.8.1 (August 23, 2016) {#section_A8854D4EDF014AEBB81F49EB104D4A20}

The Adobe Target Standard/Premium 16.8.1 (August 23, 2016) release includes the following features and enhancements:

<table id="table_AE048CB9EA1C4C7BBC2E9D90D26F7395"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Hosts and environment (host group) management </p> </td> 
   <td colname="col2"> <p>Organize your sites and pre-production environments for easy management and separated reporting. </p> <p>Hosts are bundled into environments for ease of management. The preset environments include Production, Staging, and Development. You can also add new environments. </p> <p>This feature achieves feature parity with <span class="keyword"> Target Classic </span>. </p> <p>For more information, see <a href="/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> Hosts </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Category Affinity </p> </td> 
   <td colname="col2"> <p>The category affinity feature automatically captures the categories a user visits and calculates the user's affinity for the category so it can be targeted and segmented on. This helps to ensure that content is targeted to visitors who are most likely to act on that information. </p> <p>This feature achieves feature parity with <span class="keyword"> Target Classic </span>. </p> <p>For more information, see <a href="/help/main/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> Category Affinity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enable/Disable Enhanced Experience Composer at the activity level </p> </td> 
   <td colname="col2"> <p>Enable/disable the <span class="wintitle"> Enhanced Experience Composer </span> at the account level (applies to all activities created in the account) or at the individual activity level. </p> <p>Previously, you could enable/disable the Enhanced Experience Composer only at the account level. </p> <p>For more information, see <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Offer performance report </p> </td> 
   <td colname="col2"> <p>Download an offer performance report with all Automated Personalization activity success metrics. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements**

This release includes the following enhancements:

<table id="table_E2E4BE72BD79413A821C6A6D1A3AB0F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Code Editor UI redesign </p> </td> 
   <td colname="col2"> <p>The code editor UI has been updated to be more intuitive and easier to use. </p> <p>For more information, see <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

The following known issues have been reported:

* Some of the UI text for the [!UICONTROL Category Affinity] feature displays in English only. Text in other languages will be available in the September [!DNL Target] release.

### Target Platform Changes (July 2016) {#section_09C18773707B4059852A41C764F817E4}

<table id="table_33B60910EAE24BAFA778F280F72FB683"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Change </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> version 0.9.1 </p> </td> 
   <td colname="col2"> <p>July 14, 2016 </p> <p> <span class="filepath"> at.js </span> version 0.9.1 is now available. </p> <p>For more information, see <a href="https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html" format="dita" scope="local"> at.js Version Details </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 16.7.1 (July 21, 2016) {#section_DB583EF9A30247A488EE319583911F22}

The Adobe Target Standard/Premium 16.7.1 (July 21, 2016) release includes the following features and enhancements:

<table id="table_EBA34BD2F5C745DD9EC5231AD79F6C00"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Priority settings for activities </td> 
   <td colname="col2"> <p>You can now set activity priority levels from 0-999 to allow for finer control over which activity displays if multiple activities are assigned to the same location with the same audience. </p> <p>This option must be enabled in <span class="wintitle"> Administration </span> &gt; <span class="wintitle"> Reporting </span> . </p> <p>The Fine-grained priorities option applies to A/B Test, Automated Personalization, Experience Targeting, and Multivariate Test activities. </p> <p>For more information, see the following topics: </p> <p> 
     <ul id="ul_FD92CD06CF25480887AC171274262E18"> 
      <li id="li_D321FAED82944D2685DA69EB310D80BE"><b>A/B Test: </b> <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_12ECDFD71DB94E22A85AB13B487E8503"><b>Automated Personalization: </b> <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a> </li> 
      <li id="li_84B893C214994246AB36E28E84C51460"><b>Experience Targeting: </b> <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_26533B659C0E49D6A6D3B3FEBE9CA930"><b>Multivariate Test: </b> <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Goals and Settings </a> </li> 
      <li id="li_FBACF2B73B2E491BBB85618153AC4568"><b>Activities: </b> <a href="/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02" format="dita" scope="local"> Activity Settings </a> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Multi-valued Recommendations attributes </td> 
   <td colname="col2"> <p>All custom <span class="keyword"> Recommendations </span> attributes can now contain multiple entity values. </p> <p>For more information, see <a href="/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local"> Custom Entity Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dynamic/remote offer support </td> 
   <td colname="col2"> <p>Dynamic content can be part of any form-based activity in <span class="keyword"> Target Standard/Premium </span>. Dynamic content is stored outside of <span class="keyword"> Target </span>. </p> <p>For more information, see <a href="/help/main/c-experiences/c-manage-content/about-remote-offers.md#concept_657016A0E6174C22B89036E9C8A0170F" format="dita" scope="local"> Create Remote Offers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Copy audiences and profile scripts </td> 
   <td colname="col2"> <p>You can now copy an existing audience that you can then edit to create a similar audience. </p> <p>For more information, see <a href="/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creating an Audience </a>. </p> <p>You can also copy existing profile scripts. </p> <p>For more information, see <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Use classes to determine element selectors </td> 
   <td colname="col2"> <p>Element selectors can now be based on classes or IDs in Automated Personalization and Multivariate Test activities. In previous versions, this option was only available for A/B Test activities. </p> <p>For more information, see <a href="/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local"> Element Selectors Used in the Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Content similarity </td> 
   <td colname="col2"> <p> Use Content Similarity rules to make recommendations based on item or media attributes. </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_699755B33F8F48ECABB6FC7E78289A79"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Enhancement </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Reporting improvements </p> </td> 
   <td colname="col2"> <p>Success metric report downloads now show metric and segment names instead of IDs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Evaluate mbox entry condition on each request in Automated Personalization activities </td> 
   <td colname="col2"> <p>In Automated Personalization activities, entry criteria (URL targeting, template rules, audience target) are evaluated for each request for more accurate offer delivery. </p> <p>For more information, see <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 16.6.1 (June 16, 2016) {#section_C1E9F43111BF4160AF31482CD53E00BD}

There is no customer-facing release planned for June.

**Fixes**

This release includes the following fixes:

* Fixed an issue where some customers saw a white screen when trying to edit their page inside the Visual Experience Composer.

**Known Issues**

The following known issues have been reported:

* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages. 
* Issue with experience preview URLs for experiences with a redirect. As a workaround, in the Experience Composer, click **[!UICONTROL Configure]**, choose **[!UICONTROL Multiple Audiences]**, and add **[!UICONTROL All visitors]** as the only audience. Continue to save your activity. This does not change the delivery of your activity, but allows preview to work. This will be fixed in the July release of Adobe Target. 

* The documentation shows the expected behavior for the Redirect URL checkbox. However, due to a bug, the check box does not show as selected by default. This defect will be fixed soon.

  To check this option in an existing activity with a redirect offer, use the following workaround:

    1. Open the Redirect to URL popup. 
    1. Change the URL to a dummy URL and save. 
    1. Change the dummy URL again to your campaign's expected redirect URL. 
    1. Check the "Include Current Query Parameters" option, and save.

  If you check the option while creating a new redirect offer, you can expect your query parameters to be included in the redirection.

  For older activities, if this option is checked in the experience composer of your activity, it means your redirection will include the query parameters. If it is not checked, current query parameters will not be included in redirection.

### Adobe [!DNL Target] Standard/Premium 16.5.1 (May 19, 2016) {#section_406CE09317994F55A26C2FDB77C77FEA}

The Adobe Target Standard/Premium 16.5.1 (May 19, 2016) release includes the following features and enhancements:

<table id="table_DDC5356FD6B8443EAA6EB81C03ADF73A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Experience Versions </td> 
   <td colname="col2"> <p>Versions targeted to different audiences can now be set up within experiences in A/B activities. </p> <p>See <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md#task_0138112E283A4A5B9F8AB9AAF2FBC2FF" format="dita" scope="local"> Target an Experience to Multiple Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations custom algorithms </td> 
   <td colname="col2"> <p>Custom algorithm mappings can be uploaded in a CSV file. It is no longer required to use the XML-based API. </p> <p>See <a href="/help/main/c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Uploading Custom Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analytics for Target: Analytics tracking server </td> 
   <td colname="col2"> <p>To ensure proper reporting tracking, you must specify a tracking server when you create or edit activities that use Analytics for Target (A4T). Existing activities will continue to run using current settings. </p> <p>See <a href="/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local"> Using an Analytics Tracking Server </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Instructional Videos </td> 
   <td colname="col2"> <p>The following instructional videos have been added to help: </p> <p> 
     <ul id="ul_47BAE946E764404497B7D81EE4C5D076"> 
      <li id="li_E16E50F94D3748E2985FB78F75140626">Using DTM to pass parameters to the global mbox </li> 
      <li id="li_A8CCDE3EFF25430580E6C372000CF964">Using DTM to deploy Target </li> 
      <li id="li_8897F7B5930B448D87274CEDFCC75AE4">Setting up a multivariate test </li> 
      <li id="li_2573DF52CE974ED0AF9EA433C97BC4C0">Creating an A/B activity </li> 
      <li id="li_52F28040D54D43E787B763E6AA998614">Understanding activity types </li> 
      <li id="li_577C8DDEB4CE429CA3C14BE5655F6E11">Configuring activity settings </li> 
      <li id="li_2F7FCA657FD04E02ADD6E6964A8EA1F0">Targeting an activity </li> 
      <li id="li_A08B8AFF48764D1B9EA706977F72AA66">Creating audiences </li> 
      <li id="li_493CDC3BEA5F4EA0821B971579177E03">Using audiences </li> 
      <li id="li_19045C86E1524649B56F82416934EF13">Using the Content Library </li> 
      <li id="li_8E89F3691A6F4400A2DFDFE5186DFA83">Using profile scripts </li> 
      <li id="li_2EBB2B61BFA24F5FB858C0551AB20F70">Setting account preferences </li> 
      <li id="li_E1886818C7BF4F36B07EC293F1A45911">Understanding Visual Experience Composer modes </li>  
      <li id="li_A87B876298344B2987BDC5FFD5580EC0">Creating and managing Target users </li> 
      <li id="li_F90E1083444E4DBAA8C406AC293C0FD6">Setting success metrics </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> User Interface improvements </td> 
   <td colname="col2"> <p>User interface improvements have been made to the Visual Experience Composer and Recommendations search. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations CSV download </td> 
   <td colname="col2"> <p>CSV downloads now have a line for all environments, including those that do not have entity recommendations (for example: 
     <code>
       # environment: 1724 
     </code>). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Enhancements**

Improvement made to improve the A4T provisioning process.

**Known Issues**

The following known issues have been reported:

* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages. 
* Issue with experience preview URLs for experiences with a redirect. As a workaround, in the Experience Composer, click **[!UICONTROL Configure]**, choose **[!UICONTROL Multiple Audiences]**, and add **[!UICONTROL All visitors]** as the only audience. Continue to save your activity. This does not change the delivery of your activity, but allows preview to work. This will be fixed in the July release of Adobe Target.

### New [!DNL Target] Implementation Library, at.js 0.8.0 (May 5, 2016) {#section_6A44C277E82D409AB6DCD0901F43794A}

at.js is a new implementation library for Target designed for both typical Web implementations and single-page applications.

Among other benefits, at.js improves page load times for Web implementations, improves security, and provides better implementation options for single-page applications.

at.js contains the components that were included in target.js, so there is no longer a call to target.js.

When implementing at.js, be aware of the following:

* Visual Experience Composer redirects do not work. 
* Internet Explorer versions earlier than 8 are not supported. 
* Asynchronous implementation means legacy integrations like the Test&Target to SiteCatalyst plugin may not work.  
* All calls to Target are made via XMLHTTPRequest and content is returned via JSON.

### Adobe [!DNL Target] Standard/Premium 16.4.1 Fix (May 5, 2016) {#section_70552F61E83140C7B4D2A245198B630E}

* at.js v 0.8.0 is now available for download from the Target interface. 
* Target APIs changed. `applyOffer` now requires `mbox param [0]`.

  ```
  adobe.target.applyOffer({ 
      "mbox": "target-global-mbox", 
   "params": {"test": "true"}, 
      "selector": ".banner-text", 
      "offer": offer 
  });
  ```

### Adobe [!DNL Target] Standard/Premium 16.4.1 (April 21, 2016) {#section_C968860FAB81485BA12BD588F4ECA401}

This release includes the following features and enhancements:

<table id="table_162CC5A0DB324B38A8A4252A18976686"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> User Interface Improvements </td> 
   <td colname="col2"> <p>The user interface has been changed significantly in this release. Among the most noticeable changes are: </p> <p> 
     <ul id="ul_28F382C60ADE43F5A3A4BD0CD5A5CE52"> 
      <li id="li_C47240826E5844D6843314F453F042FC">Navigation has moved from the left to the top </li> 
      <li id="li_3BB03504E98C40CC85583DCD9A4CEA06">Improved dialog boxes </li> 
      <li id="li_AE71506DF1E748A788C40E1F09951732">Improved activity creation flow </li> 
     </ul> </p> <p>The way Experience Cloud solutions, including Target, are selected has also changed. To access Experience Cloud solutions and services, click the menu icon: </p> <p> <img src="assets/menu-shell-400.png" id="image_6E9323E0EBEA41B1A7319D6BCC43E769" width="400" height="140" /> </p> <p>For more information about accessing Target and making Target your default page after logging in to the Experience Cloud, see <a href="/help/main/c-intro/target-access-from-mac.md#task_5467C72DAFCB4BB583762CAAFC00A5CF" format="dita" scope="local"> Access Target from the Adobe Experience Cloud </a>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Inclusion rules can be disabled for backup recommendations </td> 
   <td colname="col2"> <p>When backup recommendations are enabled, you can choose not to apply inclusion rules to your backup recommendations. . </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: New debugging capabilities in text area via <span class="codeph"> mboxTrace </span> </td> 
   <td colname="col2"> <p>Adding <span class="codeph"> &amp;mboxTrace </span> to a URL replaces recommendations on that page with debugging details, including information about served recommendations, criteria, design, exclusions, inclusions, backup recommendations served, and more. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations API: Upload a CSV for the Custom Criteria </td> 
   <td colname="col2"> <p>You can upload a CSV for the Custom Criteria via API. </p> <p>This ability will be added to the Target Premium user interface in an upcoming release. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations API: New Design APIs </td> 
   <td colname="col2"> <p>New Design APIs make it possible to manage your Recommendations designs via API. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Dependent Success Metrics </td> 
   <td colname="col2"> Automated Personalization now supports the ability to limit a success metric to only count if a previous success metric has already been met. <p>For more information, see <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Reports Summary View Download </td> 
   <td colname="col2"> The download option now allows users to download summary view (i.e. comparing Control and Automated traffic) as broken down by all available success metrics. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Customer attributes can be used as tokens in offers </td> 
   <td colname="col2"> <p>Previously, customer attributes could be referenced in profile scripts, formatted as <span class="codeph"> crs.get('&lt; <span class="varname"> Datasource Name </span>&gt;.&lt; <span class="varname"> Attribute name </span>&gt;') </span>. </p> <p>Now, the attributes are available as tokens in profile scripts and directly in offers without first requiring a profile script. The token should be in the form: <span class="codeph"> $crs. <span class="varname"> datasourceName </span>. <span class="varname"> attributeName </span> </span>. </p> <p>See <a href="/help/main/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_62B4821EB6564FF4A14159A837AD4EDB" format="dita" scope="local"> CRS Tokens </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Custom Code enhancement </td> 
   <td colname="col2"> Custom code can now execute the JavaScript code in the <span class="codeph"> &lt;head&gt; </span> tag. Execution of code no longer waits for the <span class="codeph"> &lt;body&gt; </span> tag to be present in DOM. Earlier, the selector was only the first element in the <span class="codeph"> &lt;body&gt; </span> tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Instructional Videos </td> 
   <td colname="col2"> Instructional videos have been added to help. Currently, you can view videos about the <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Visual Experience Composer and Form-Based Experience Composer </a>. More videos will be added in the coming weeks. </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* The issue introduced by Chrome version 48 that caused the Visual Experience Composer to function incorrectly in Chrome has been fixed. To benefit from this fix, update to Chrome version 50.

**Known Issues**

The following known issues have been reported:

* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages.

### Adobe [!DNL Target] Standard/Premium 16.3.1 (March 15, 2016) {#section_A5A9B03A5CCD4213AD656BE722B5FF67}

This release includes the following features and enhancements:

<table id="table_F2A89DF1EAB443B4B4C7E0BC6118384B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>First Look: </p> <p>New Target implementation library, at.js </p> </td> 
   <td colname="col2"> <p> <p>Note:  This "First Look" offering is available via API download. It will be available via the Target interface in an upcoming release. In the meantime, you can download the at.js library, test it in your environment, and deploy it in your production Target implementation. </p> </p> <p> at.js is a new implementation library for Target designed for both typical Web implementations and single-page applications. </p></p> <p>Among other benefits, at.js improves page load times for Web implementations, improves security, and provides better implementation options for single-page applications. </p> <p>at.js contains the components that were included in target.js, so there is no longer a call to target.js. </p> <p>When implementing at.js, be aware of the following: </p> <p> 
     <ul id="ul_8C50C669AA7B4464A5FDECFCFD8662ED"> 
      <li id="li_6065B208480D46178055B40A2654E0C6">Visual Experience Composer redirects do not work. </li> 
      <li id="li_A2FABD3C21994511A45DED84283E526E">Internet Explorer versions earlier than 8 are not supported. </li> 
      <li id="li_04499B391F784B89B09A1D6329B1C790">Asynchronous implementation means legacy integrations like the Test&amp;Target to SiteCatalyst plugin may not work. </li>  
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dependent Success Metrics </td> 
   <td colname="col2"> <p>This features provides the option per success metric to count someone as reaching the success metric only if they've previously reached a different success metric. </p> <p> For example, a test might change the hero image on the homepage. The marketer might only want to count conversions for people who clicked the hero image. So, the marketer can set a success metric for "clicked on homepage hero" and then another metric for purchasing. Then, the marketer can add a rule on the "purchasing" metric to ensure visitors have first reached the "clicked on homepage hero" success metric. </p> <p> <p>Note:  If audience targeting on a location in a success metric is set, this feature is not supported for that metric. </p> </p> <p> Dependent Success Metrics are only supported in AB, XT, and MVT activities. Automated Personalization and Recommendations support will be available later. </p> <p>For more information, see <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Auto-Allocate usability improvements </td> 
   <td colname="col2"> <p>After the model for an Auto-Allocate activity is ready, the following operations from the UI are not allowed: </p> <p> 
     <ul id="ul_52B790B2B0D746769A3471E09CE1A122"> 
      <li id="li_B9F0FFF019CE4CB697F5D0B60061DC27">Switching the "Traffic Allocation" mode to "Manual" </li> 
      <li id="li_C271B0BE4C5C4B06BB21703239E7B061">Changing the reporting source from "Adobe Target" to "Analytics" and vice-versa </li> 
      <li id="li_E023DDA7ED9142B58D54F42904ADC994">Changing the goal metric type </li> 
      <li id="li_619F4765CEEC48E0A45E1821C282A082">Changing options in the "Advanced Settings" panel </li> 
     </ul> </p> <p>Refer to <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a> for documentation about Auto-Allocate. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Known Issues**

The following known issues have been reported:

* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages. 
* Some interface issues might occur in Internet Explorer 10, including screen flicker and possible slowness. 
* The Chrome version 48 update introduced an issue that causes the Visual Experience Composer to function incorrectly in Chrome. Google is working on a solution. For information, refer to [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). To work around this issue:

    * Use Firefox or Internet Explorer. 
    * Enable the Enhanced Experience Composer, which can be configured from within the **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab.

### Adobe [!DNL Target] Standard/Premium 16.2.1 (February 18, 2016) {#section_47E5CEE2EED24CB3B71D7457673F3200}

This release includes the following features and enhancements:

|  Feature  | Description  |
|---|---|
|  Activity entry targeting by percentage.  | You can now limit entries into [A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) and [multivariate](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710) activities to a percentage of visitors or audience members. For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.  |
|  Support for Revenue, Orders, and Engagement in Auto-Allocate  | You can now choose Revenue (RPV), Orders, and Engagement metrics as goals for A/B activities with Auto-Allocation selected. Previously, only conversion metrics were supported. See [Automated Traffic Allocation](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).  |
|  Filter by source  | You can now filter the Activities list by the source where the activity was created. Choice are Adobe Target and Adobe Experience Manager. See [Activities](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).  |
|  Automated Personalization performance enhancements  | Automated Personalization has been redesigned to perform better with a large number of offer/location combinations.  |

**Known Issues**

The following known issues have been reported:

* When "Disable JavaScript" is selected for page A in a multipage activity, JavaScript is disabled everywhere, even though "Disable JavaScript" isn't selected on other pages. 
* Some interface issues might occur in Internet Explorer 10, including screen flicker and possible slowness. 
* The Chrome version 48 update introduced an issue that causes the Visual Experience Composer to function incorrectly in Chrome. Google is working on a solution. For information, refer to [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). To work around this issue:

    * Use Firefox or Internet Explorer. 
    * Enable the Enhanced Experience Composer, which can be configured from within the **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab.

### Adobe [!DNL Target] Standard/Premium 16.1.1 (January 28, 2016) {#section_8BF7705B452C449F961AEFC568A0778C}

This release includes the following features and enhancements:

<table id="table_8525ECC9B6D0435ABEF8C27F747B7A0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> User interface improvements. </td> 
   <td colname="col2"> <p>The Activities list and Audience list design have been improved, as has the search/sort functionality. Additional user interface changes will be included in upcoming releases. </p> <p>See <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> "Super" audiences </td> 
   <td colname="col2"> <p>Use nested AND/OR logic when configuring audiences. </p> <p>See <a href="/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creating an Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Select host groups in reports </td> 
   <td colname="col2"> <p>Host groups are available in reports. </p> <p> <p>Note:  This option is not available for Automated Personalization. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Support for Internet Explorer 11 </td> 
   <td colname="col2"> <p>Internet Explorer 11 is now supported in the Target interface. </p> <p>See <a href="https://experienceleague.adobe.com/docs/target-dev/developer/implementation/supported-browsers.html" format="dita" scope="local"> Supported Browsers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> View Confidence Interval in Target reports for continuous variables </td> 
   <td colname="col2"> <p>Display the Confidence Interval Range for the revenue metric type (RPV, AOV, Sales, Orders), and for engagement metrics. </p> <p>For example, if RPV = 200.00 and CI Range = 50.00 , then this should be displayed for RPV: 200.00 +/- 50.00 </p> <p>This change applies to A/B, Experience Targeting, and Multivariate tests. </p> <p>See <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Confidence Level and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Visual Experience Composer URL rules enhancement </td> 
   <td colname="col2"> <p>Previously, the URL template rules in the Visual Experience Composer formed an OR condition with the Page URL. Now you can choose AND or OR when specifying multiple URLs. OR is the default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: </p> <p>Change in global mbox delivery coding </p> </td> 
   <td colname="col2"> <p>When creating a design, it is now the default to wrap an HTML design in a <span class="codeph"> &lt;div&gt; </span> element. </p> <p>For information about creating a design, see <a href="/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Create a Design </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Life Time Value (LTV) machine learning reinforcement technique </p> </td> 
   <td colname="col2"> <p>This new algorithm focuses on long-term conversion across many sessions instead of focusing on improving conversion just in this session. This technique is suitable for sites with many returning visitors because it optimizes on overall revenue for the entire interaction with the visitor. </p> <p>See <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhancement: Allow targeting on hash (#) fragments </p> </td> 
   <td colname="col2"> <p>You can now target on the part of a URL that follows a hash (#). </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Include the Same Experience on Similar Pages </a> and other relevant topics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Download success metrics report </p> </td> 
   <td colname="col2"> <p> Download a single csv file with all success metric listed, instead of a report that only had the final activity goal. </p> <p>See <a href="/help/main/c-reports/reports.md" format="dita" scope="local"> Reports </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Fixed an issue that caused all AEM-based activities as Experience Targeting (XT) activities. AEM now uses the correct activity types for A/B and XT activities. 
* Removed an option to use non-conversion metrics as a goal in new Auto Allocated activities. This restriction will be lifted in an upcoming release. 
* Fixed an issue that prevented deletion of a profile script created in Target Classic from Target Standard. 
* Fixed an issue that wrapped a non-HTML Recommendations template in a `<div>` element when used in a form-based workflow. 
* Fixed an issue that caused collision calculations to time out with a large number of activities. 
* Fixed an issue that resulted in the CSV download showing the Summary report rather than the Success Metrics report. 
* Removed "Unique ID" pop-up message that sometimes appeared when editing elements.

**Known Issues**

The following known issues have been reported:

* When "Disable JavaScript" is enabled for pageA in a multipage activity, JavaScript remains enabled for all pages but the functionality remains disabled. 
* Some interface issues might occur in Internet Explorer 10, including screen flicker and possible slowness. 
* The Chrome version 48 update introduced an issue that causes the Visual Experience Composer to function incorrectly in Chrome. Google is working on a solution. For information, refer to [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). To work around this issue:

    * Use Firefox or Internet Explorer. 
    * Enable the Enhanced Experience Composer, which can be configured from within the **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab.

## Releases 2015 {#reference_8E940F500A374F9FBCD68CDE9E7E1A00}

### Adobe [!DNL Target] Standard/Premium 15.10.1 (November 2, 2015) {#section_B5135D75FA0D42A1A3C2711CA3A1B812}

<!-- 

target/r_release-notes-2015.xml

 -->

This release includes the following features and enhancements:

<table id="table_EE13D9B959DA4FB0AD6BC03FBF78AEF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Auto-Allocate in A/B Tests </p> </td> 
   <td colname="col2"> <p> You now have the option to automatically allocate traffic to increase overall campaign lift and discover winning experiences faster. This algorithm increases the overall campaign performance while maintaining the integrity of an A/B test. </p> <p>The algorithm relies on measured performance (e.g. conversion rate) and confidence intervals to produce a traffic distribution that is changed up to twice per hour. </p> <p>Key Benefits </p> <p> 
     <ul id="ul_A41C74C0C7C844F3A923CD6EA5D5D952"> 
      <li id="li_86D3C6A4993F4DC0907BF42986E6CCD1">Preserves the integrity of an A/B test by ensuring that visitors remain in the same experience, like they do in a manual A/B test </li> 
      <li id="li_B849EB2709F84831A1B7A4F312EAFA7E">Finds a statistically significant winner faster than a manual A/B test </li> 
      <li id="li_3F258C6DEB7245E2924115C5628BC3C6">Provides higher average campaign lift than a manual A/B test </li> 
      <li id="li_C9E82388B93E4A298000984B69CBAEDE">Allows you to toggle to a manual test at any time </li> 
     </ul> </p> <p>See <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automated Traffic Allocation </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Customer Attributes </p> </td> 
   <td colname="col2"> <p> Upload 1st party data, called Customer Attributes, using the Experience Cloud core service and choose attributes to share to Target. This functionality launched in March for Analytics and now integrates directly with Target. </p> <p> For example, you might use customer data such as membership status (gold, silver, etc.), purchase history, favorite destination, local store, and so on in your CRM or eCommerce/POS system. Now you can upload that data to Experience Cloud. After the user authenticates on your site, Target can match that data to their web behavior. </p> <p>See <a href="https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html" format="https" scope="external"> Customer Attributes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Multiple companies are available when selecting Analytics as the reporting source for Target. </p> </td> 
   <td colname="col2"> <p>When selecting Analytics as the reporting source for Target, you select an Analytics report suite to receive Target activity data. To do this, first choose from any of the Analytics companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to Adobe Target will be available for selection. If you don't see the report suite(s) you expect, first try logging out and logging back in to the Adobe Experience Cloud to try again. If the report suite is still missing from the list, please contact Customer Care. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New Built-in Options for Audience Creation </p> </td> 
   <td colname="col2"> <p>There are new built-in audience options: </p> <p> 
     <ul id="ul_16E7B53E324B4FB79E1B1E97A1CE65AC"> 
      <li id="li_60B55A81119E48FE83639B9740A2FD21">Target visitors based on which language they use on their browser. This is more accurate than geo-based language targeting. </li> 
      <li id="li_84CAAE7E02CA48FA9C7C00C0415046B6">Target visitors based on browser version, not just which browser is being used. </li> 
      <li id="li_AAF8170CAF4C45BB965D1A9A4E9204D5">You can now Target multiple browsers rather than only one. </li> 
     </ul> </p> <p>See <a href="/help/main/c-target/c-audiences/c-target-rules/browser.md#concept_221D8EEF53CC45AEACEB17CF336A3658" format="dita" scope="local"> Browser Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Exclude Past Purchases </p> </td> 
   <td colname="col2"> <p>Target now automatically excludes previously purchased items from a visitor's recommendations. This option can be disabled for any criteria. </p> <p>All out-of-the-box criteria now have this option enabled, including those used in activities that were running prior to this release. If you do not want to exclude past purchases, you should edit those activities. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Attribute Weighing </p> </td> 
   <td colname="col2"> <p> Recommendations ranking rules have changed for criteria. This change affects existing Recommendations. </p> <p> Use attribute weighting to "nudge" the algorithm. Marketers can influence the algorithm based on important description or metadata about the content catalog. Apply a higher weighting to these on-sale items so they show more often in the recommendation. Non-sale items are not completely excluded, but they display less often. Multiple weightings can be applied to the same algorithm, and the weightings can be tested on split traffic in the recommendation. </p> <p>These new weights have automatically been applied to all activities. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Set the Time for Feed Processing </p> </td> 
   <td colname="col2"> <p>Specify the time when you want a feed to update. </p> <p>See <a href="/help/main/c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Create Feed </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Use the Feed List to Set a Feed to Never Run </p> </td> 
   <td colname="col2"> <p>From the feed list, set a feed to never run if you do not want to update that feed. </p> <p>See <a href="/help/main/c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Create Feed </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Set a New Criteria Type Based on Content Similarity </p> </td> 
   <td colname="col2"> <p>An item-based criteria that can be used for the following: </p> <p> 
     <ul id="ul_86BDF2DE0FCE4665A2985D0C56E50A53"> 
      <li id="li_D83669F9019B431891E072C973B317D7">Current items with similar attributes </li> 
      <li id="li_4E45848423F2450999C699C64E0EE9E2">Last purchased item with similar attributes </li> 
      <li id="li_901D4AAF7BE244FCB9277DC7EDD91E32">Custom attributes that match a specified entity.id and use items with similar attributes </li> 
      <li id="li_49D52B0182F346E982C11A0C2DA50B4F">Last viewed item with similar attributes </li> 
      <li id="li_2DBAF32476AC435EB57D08D96CB55683">Most viewed item with similar attributes </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New Activity List Filters </td> 
   <td colname="col2"> <p>Several filters have been added to help you show the activities you are most interested in seeing in the Activities list. </p> <p>See <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Enhancement: Industry-Relevant Criteria Configuration </p> </td> 
   <td colname="col2"> <p>Irrelevant options during setup have been eliminated. In the past, some setup options for some industry verticals, such as Media, were not always relevant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>New Out-of-the-Box Criteria </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_47E67312A04E414EB797F9AE2A1F7599"> 
      <li id="li_5EDF9006145B4498B2EAD95D642057C5">More Videos Like This </li> 
      <li id="li_6A8DAACE7CD741D0BB766EBCB52BCD88">More Articles Like This </li> 
      <li id="li_1B44AB35B045416B8D8B72C428750822">More Content Like This </li> 
      <li id="li_FEC84CCF3DF3444DAB39F4764DE897B0">More Slideshows Like This </li> 
      <li id="li_5E874ACB5B004CACBDB4F8FF217BC593">More Products Like This </li> 
     </ul> </p> <p>See <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Improved reporting details shown when using Analytics as your reporting source. </td> 
   <td colname="col2"> <p>The details shown by default in an Analytics report when using A4T now match the details shown in the Target report. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Fixed an issue in the Global Experience Composer that prevented dragging a corner to resize a custom viewport.

**Known Issues**

The following known issues have been reported:

* When "Disable javascript" is enabled for pageA in a multipage activity, JavaScript remains enabled for all pages but the functionality remains disabled.

### Adobe [!DNL Target] Standard/Premium 15.9.1 (September 30, 2015) {#section_A54204291A99476688E8C0BD8255F93C}

This release includes the following features and enhancements:

<table id="table_907A952F54084C2A9C61F10E2B7A7BFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Mobile Web Experience Composer </td> 
   <td colname="col2"> <p> View your site as it looks on various mobile devices and different screen sizes. Set responsive site breakpoints once and use them across your activities to make sure your optimization activities look great on all the devices your visitors use. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5" format="dita" scope="local"> Mobile Viewports for Responsive Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Location targeting on form-based activity creation </td> 
   <td colname="col2"> <p> Apply targeting to your mbox locations to limit where your activity displays. </p> <p>See <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Background color selection in Visual Experience Composer for MVT and Automated Personalization activities </td> 
   <td colname="col2"> <p>A color picker enables you to set background colors when editing Automated Personalization and Multivariate Test activities. </p> <p>This feature was previously only available for A/B and Experience Targeting activities. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rich Text and HTML editing in Visual Experience Composer for MVT and Automated Personalization activities </td> 
   <td colname="col2"> <p> Text and HTML formatting in a word processor-like window when editing Automated Personalization and Multivariate Test activities. </p> <p> This feature was previously only available for A/B and Experience Targeting activities. </p> <p>These actions provide rich-text editing capabilities by adding HTML tags or applying styles. These modifications by the rich-text editor for any action can be seen in its source view. Users can press the HTML button in the rich-text editor to see the source view. The styles added by the rich-text editor can interfere with customer websites' styles. In this case, users can go to the source view and edit the modifications to align them with their websites' styles. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Form-based recommendations </p> </td> 
   <td colname="col2"> <p> Create recommendations activities for non-site locations including emails, consoles, kiosks, etc. </p> <p>See <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Display information about the key in the design </p> </td> 
   <td colname="col2"> <p>Show the key item in your Recommendations design. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Automated Personalization </p> <p>Conversion-based report </p> </td> 
   <td colname="col2"> <p> If the optimization goal is a conversion metric, then the Offer Detail report now shows the impact of the top predictive variables in lift and incremental conversions. This report was only revenue-based before, so this ability ensures that activities with no revenue data still produce relevant and actionable insights. </p> <p>See <a href="/help/main/c-reports/personalization-reports/reports-ap.md" format="dita" scope="local"> Automated Personalization Reports </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adobe Campaign e-mail integration with Target Standard </td> 
   <td colname="col2"> <p> Previously, it was required to use Target Classic to set up a targeted e-mail campaign using Adobe Campaign. With the release of two new features in Target Standard (form-based activity creation and redirect offers) it is now possible to use Target Standard to set up a targeted e-mail campaign with Adobe Campaign.</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Redirect Offers in Form-Based activity creation </td> 
   <td colname="col2"> <p> Support for the redirect offers functionality of Target Classic added in Target Standard form-based activity creation flow. </p> <p>See <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Experience URLs in activities no longer use on-site cookie </td> 
   <td colname="col2"> <p> The preview experience URLs available per activity are now more reliable. Easily copy the URLs and share with other team members, even if they don't use Adobe Target. </p> <p> <p>Note:  Updated experience URLs only work on activities created after July 30, 2015. Older activities continue to use the cookie-based preview functionality. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Reporting enhancement for Analytics as the reporting source for Target </p> </td> 
   <td colname="col2"> <p> Click to view the full Analytics report directly from the activity report page. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Activity List performance improvements </td> 
   <td colname="col2"> <p>Greatly improved the load time for activities in the list. Searching and filtering are much faster, particularly when there are a lot of activities in the list. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Fixed an issue that prevented Target report suites from showing up in the Target report suite selector, after being enabled for Analytics for Target. 
* Fixed an issue that prevented searching for activities by URL.

**Known Issues**

The following known issues have been reported:

* When "Disable javascript" is enabled for pageA in a multipage activity, JavaScript remains enabled for all pages but the functionality remains disabled.

### Adobe [!DNL Target] Standard/Premium 15.8.1 (August 20, 2015) {#section_1C26CB72316A404DB655EBE655F5B8C1}

The goal of this release is to provide feature parity with Target Classic. The most commonly used features of Target Classic are now available in Target Standard.

This release includes the following features and enhancements:

<table id="table_DF5B434D639345B4ACE2467B8966A908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Create and edit profile scripts </td> 
   <td colname="col2"> <p>Profile scripts run profile attribute "catchers" on each mbox request. When an mbox request is received, Target runs any relevant profile scripts, determines which activity should run, and displays content that is appropriate to that activity and that experience, then tracks the success of the activity. This enables you to track information about the visit, such as the visitor's location, time of day, number of times that visitor has been to the site, if they've purchased before and so on. This information is then added to the visitor's profile so you can better track that visitor's activity on your site. </p> <p>See <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profile Attributes </a>. 
     <!--(Copy help from Classic)--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Confidence interval for binary metrics </td> 
   <td colname="col2"> <p>Updated reports using Target-based data show the confidence interval of the lift, compared to the control. </p> <p>See <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Confidence Level and Confidence Interval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Download export activity report data </td> 
   <td colname="col2"> <p>Download data in a .csv format for quick import into Excel or other data analysis programs. This feature works for A/B, Experience Targeting, and Multivariate activities. </p> <p>See <a href="/help/main/c-reports/reports.md#section_3099BC87DCAE46A2B075E1FF5B6552A6" format="dita" scope="local"> Downloading Reports </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rich text and HTML editing in Visual Experience Composer </td> 
   <td colname="col2"> <p>Text formatting options are available when editing text and HTML for A/B and Experience Targeting activities in the Visual Experience Composer. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Background color selection in Visual Experience Composer </td> 
   <td colname="col2"> <p>A color picker enables you to set background colors when editing A/B and Experience Targeting activities in the Visual Experience Composer. This option is not available if a background image is set. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Archive activity </td> 
   <td colname="col2"> <p>Send an activity to the archive. You can approve an archived activity to make it active again. Activities in the archive do not display by default in the Activities list. </p> <p>See <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization </p> <p>Offer-level targeting </p> </td> 
   <td colname="col2"> <p>Allows marketers to apply targeting rules to offers in Automated Personalization. Makes it possible to exclude specific offers from being shown to a specified group of people. </p> <p>See <a href="/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E" format="dita" scope="local"> Target AP Offers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Show number of activities using design </p> </td> 
   <td colname="col2"> <p>The design library shows how many live and inactive activities are using each design. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Customized dynamic title displays in design </p> </td> 
   <td colname="col2"> <p>Choose a title to display when using a particular design. This title does not have to match the title displayed to visitors on the page. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>API Token </p> </td> 
   <td colname="col2"> <p>You can set your Client API token from Recommendations Premium. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Frequently used URLs </td> 
   <td colname="col2"> When entering a URL for an activity or a new page within an activity, a menu shows the most recent and most frequently used URLs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New mobile device targeting options </td> 
   <td colname="col2"> <p>You can now target multiple mobile devices without requiring a profile script. </p> <p>See <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobile </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 15.7.1 (July 30, 2015) {#section_9C888BFD04A94DD58616D3F67D209CCC}

This release includes the following features and enhancements:

<table id="table_46FF5AF77D824ADC941B1E472234F05C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity change log </td> 
   <td colname="col2"> <p>The change log lists changes made to an activity. The action and the user are listed with a timestamp for each change. </p> <p>See <a href="/help/main/c-activities/change-log.md#task_D6F224E8CE8346699187D21CD9A2B4AB" format="dita" scope="local"> Activity Change Log </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multipage activity </td> 
   <td colname="col2"> <p>A multipage activity enables you to create a story over multiple pages, with a design that is specific to each page. </p> <p>For example, you might want to test an offer for free shipping with purchases above a certain amount. You might want that offer to appear on your landing page, a category page, and certain product pages, but you want it to be a different size and in a different location on each page type. You could display a prominent offer on your home page, then reinforce that offer with smaller offers on other relevant pages. </p> <p>You can also use a multipage activity to define different layouts for your desktop and non-responsive mobile sites. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48" format="dita" scope="local"> Multipage Activity </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based activity creation </td> 
   <td colname="col2"> <p>Create an activity without using the Visual Experience Composer. Instead, choose locations and offers through a form. With this, Target Standard activities can be delivered in emails, mobile apps, kiosks, and other places that don't work with a Visual Experience Composer. </p> <p>See <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Form-Based Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Configurable success metrics </td> 
   <td colname="col2"> <p> Fine-grained options let you determine how to count success metrics. Options include counting the metric per impression or once per visitor, and choosing whether to keep the user in the activity or removing them. This is equivalent to the "advanced options" for success metrics available in Target Classic. </p> <p>See <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Success Metrics </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Enhancement: Experience Targeting experience limit removed. </td> 
   <td colname="col2"> The previous limit of ten experiences in Experience Targeting has been removed. </td> 
  </tr>  
  <tr> 
   <td colname="col1"> Real-time profile syncing for 3rdPartyId data </td> 
   <td colname="col2"> When a site visitor logs in mid-session and gets a 3rdpartyId, all previously-loaded profile attributes tied to the 3rdPartyId are now immediately available. See <a href="/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Visitor Profile </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations Premium: Facet Name Search </td> 
   <td colname="col2"> You can now search for a facet name. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Automated Personalization: Post-goal metric tracking </td> 
   <td colname="col2"> <p> Previously, Target restarted an experience when the visitor hit the modeling goal. Now, users can be kept in the activity for tracking purposes after reaching the modeling goal. </p> <p> For example, often an Automated Personalization activity is used to improve click-rates, and that is set as the modeling goal. However, it's important to see how increased click-rates lead to final conversion, so tracking through the final conversion is essential. </p> See <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Analytics as the reporting source for Target is now supported for XT activities. 
* Fixed an issue that caused the control experience displayed in Analytics to change once the activity became live.  
* Fixed an issue where values after a # in a URL were considered part of the path during audience/segment creation.

**Known Issues**

The following known issues have been reported:

* When "Disable javascript" is enabled for pageA in a multipage activity, JavaScript remains enabled for all pages but the functionality remains disabled.

### Adobe [!DNL Target] Standard/Premium 15.6.1 (June 25, 2015) {#section_43FEA310830E4E8E853FAB56B12B1301}

This release includes the following features and enhancements:

<table id="table_C0B37E1730014ADA8C36310093F5C43A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer compatibility improvements </p> </td> 
   <td colname="col2"> <p> A new account-wide setting to make it easier for Target to generate the right CSS selectors. For example, it can be specified if Target should use classes or IDs. This improves compatibility with AEM. This setting can be overridden per activity </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting support for Analytics as a reporting source </p> </td> 
   <td colname="col2"> <p>You can now use Analytics as a reporting source for Experience Targeting activities. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: Visual indication of model status </p> </td> 
   <td colname="col2"> <p> Once a predictive model passes the required quality criteria and is deemed valid, it is considered ready and is used to calculate a personalized score for offer decisioning. A clock icon changes to a check mark when the model is ready and Target is able to begin delivering personalized content. Since lift is expected only after the models are ready, the visual indication allows you to set the right expectation. Use the traffic estimator in the Visual Experience Composer to get a guideline of when the models will be ready. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Browse and Navigate in the Visual Experience Composer </p> </td> 
   <td colname="col2"> <p> Allows you to open the visual experience composer on one page, and then follow links and form submissions to reach other pages on your site, such as a shopping cart. Once on the page you want to test, flip the Visual Experience Composer back to "Compose" mode and create your experiences. For example, you can change a message on the Shipping page, then test it against the default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Faceted Catalog Search </p> </td> 
   <td colname="col2"> <p> Provides a more robust way to search your catalog. Also makes it easier to narrow down the search results to very specific set of products. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Show external campaigns in the Target Standard Activities list </p> </td> 
   <td colname="col2"> <p> You will now see Target Classic campaigns within the Target Standard Activities list. If you want to filter out Target Classic campaigns and only view Target Standard you can use the "Source" search filter option. For example, to view only Adobe Target Standard activities select the source filter and type "Adobe Target" as the source. The ability to view activities created in Recommendations Classic or Adobe Mobile Services will be added in a future release. </p> <p>You can activate and deactivate activities created in other solutions using the Target user interface. For all other changes you will be need to edit the activities in the source solution. </p> <p> For activities created in other solutions, audience information is not visible on the Overview page. View the audience information in the solution where the activity was created. </p> <p>See <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Added message to indicate that an activity that cannot be viewed is available for viewing in Target Classic. 
* Fixed an issue that caused URLs to redirect slowly. 
* Fixed an issue that broke click-tracking success metrics if other success metrics in the activity were deleted. 
* Fixed an issue where the image uploaded to the Recommendations design did not display correctly in the Visual Experience Composer. 
* Fixed an issue with the traffic estimator in Automated Personalization activities where the number of combinations was used instead of the sum of offers across locations. 
* Fixed an issue where mbox parameters would not always display on the audience creation screens. 
* Fixed an issue that blocked updates on the thumbnail for Recommendations designs.

### Adobe [!DNL Target] Standard/Premium 15.5.1_Hotfix (May 28, 2015) {#section_D751F55A3812417FAA72BD6872AE3C2A}

This hotfix release includes the following fixes:

* Fixed an issue where the Estimated Lift in revenue checkbox was not visible. 
* Fixed an issue that prevented the Create Activity button from displaying properly for some users. 
* Fixed an issue that caused the Activity Name text box to disappear in the Visual Experience Composer while editing A/B and Experience Targeting activities.

### Adobe [!DNL Target] Standard/Premium 15.5.1 (May 21, 2015) {#section_FF0F959908784AF0906EFB9E8324F207}

This release includes the following features and enhancements:

<table id="table_3985F758176F4884A94AFDFB78B24209"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Custom code entry and editing in Visual Experience Composer </p> </td> 
   <td colname="col2"> <p>Enables you to see, edit, and add new actions using a code editor within the Visual Experience Composer. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Add JavaScript and CSS to the top of your page </p> </td> 
   <td colname="col2"> <p> Add JavaScript code to your page(s) right below the <span class="codeph"> &lt;body&gt; </span> tag, without requiring the selection of an element on your page. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>New Audience Creation Options </p> </td> 
   <td colname="col2"> <p>You can now target by the following (located in the Geo section when creating an audience): </p> <p> 
     <ul id="ul_FE1E3605FB8042E9B5E80C0DB0C6C2AD"> 
      <li id="li_6D112A4DB2344B4E9F1B84E943A43DD8">ISP </li> 
      <li id="li_5C95F3F55D194D81905F8138FB546288">Network domain </li> 
      <li id="li_63E3606516BC4FFC8C91E49297542464">Connection speed (options are: broadband, dialup, mobile, t1, t3, satellite) </li> 
     </ul> </p> <p>See <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium New Features </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6DC206CB52E34498BC762FCCF77807AA"> 
      <li id="li_B26568D642974F17B4B2D6E42CFDC5B9"> <p>New Preview mode to view designs with JavaScript </p></li> 
      <li id="li_B8D1ADE874D244F198CBD3387ED3E310"> <p>Catalog Search now supports free search for English language </p> </li> 
      <li id="li_EB8D595EA8A84B37A3262F76543E1B05"> <p>Account-level support for inputting a static, base url to prepend to all relative <span class="codeph"> entity.thumbnailUrl </span> values </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Recommendations Premium Enhancements </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1CF5F2D0CDE84DDC9C445B5CD878EEAA"> 
      <li id="li_EB225752776449C6B21C2B2514B508C5"> <p>Improvements to design preview in VEC </p> </li> 
      <li id="li_2CD8267EF166421DBB6EFBF704625848"> <p>Layout improvements on out-of-the-box designs </p> </li> 
      <li id="li_D737754C200844638B536A3BE02E9C5F"> Collection shown in targeting diagram</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Recommendations Classic functionality now supported in Recommendations Premium </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E0D6A9C12B514DE3B3EA753BB4D56662"> 
      <li id="li_2A728C8938834162A0C0C1C926AC5DD9"> Partial template rendering <p>See <a href="/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content" format="dita" scope="local"> Content Settings </a>. </p> </li> 
      <li id="li_B1DFC829D19B4570AB5A7F937C7EF2CC"> Specify backup rules per criteria </li> 
      <li id="li_F8C9690CEC974E37B72A85C2FACFAA6D"> Support FTPS for product feeds</li> 
      <li id="li_3C0FA493C87345E4BE994936DF0D0162"> Custom algorithms now appear automatically as criteria</li> 
      <li id="li_5B074C9FB3CB46EBA6EB4D8B1098480E"> Hourly automatic reindexing of product catalogs for customers without feeds </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: QA links added </p> </td> 
   <td colname="col2"> <p> You can now preview how your experiences will look when delivered. View and share links to your AP experiences on your site to get a "true preview" of the experiences outside of Target's Visual Experience Composer. </p> <p>See <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics-powered MVT: Preview experience from Performance report </p> </td> 
   <td colname="col2"> <p>When using Analytics as the reporting source for multivariate tests, you can preview your MVT activities from the Performance report. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> A/B tests and Experience Targeting: three-step activity creation flow </p> </td> 
   <td colname="col2"> <p> <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md" format="dita" scope="local"> Create A/B </a>and <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Experience Targeting </a> activity in three steps instead of four. This change makes the process of creating these activities more like the workflow of other activities types, such as Automated Personalization and Multivariate Tests. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analytics as a reporting source is available with most activity types. </p> </td> 
   <td colname="col2"> <p> The A/B with Analytics activity type no longer exists. The option of using Analytics as your reporting source is now available on the Goal &amp; Settings page for all activity types except Automated Personalization and Experience Targeting. As a result, there is no longer a separate activity type called A/B Test with Analytics Data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Show external campaigns in the Target Standard Activities list </p> </td> 
   <td colname="col2"> <p> You will now see Target Classic campaigns within the Target Standard Activities list. If you want to filter out Target Classic campaigns and only view Target Standard you can use the "Source" search filter option. For example, to view only Adobe Target Standard activities select the source filter and type "Adobe Target" as the source. The ability to view activities created in Recommendations Classic or Adobe Mobile Services will be added in a future release. </p> <p>See <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activities </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Export Order Audit Report </p> </td> 
   <td colname="col2"> <p> Ability to export/download Order Audit Report added to Target reports. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beta: A4T lift and confidence </p> </td> 
   <td colname="col2"> <p> Lift and confidence now available for Analytics' standard metrics and custom events. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Fixed an issue in audience creation where changing operators deleted attribute values. 
* Made improvements so custom-coded regional mboxes are selectable in the Visual Experience Composer. 
* Fixed an issue in Recommendations where attributes with double-byte characters (for multilingual cases) bypassed inclusion filtering rules. 
* All activity types now support activity names up to 200 characters in length.

### Adobe [!DNL Target] Standard/Premium15.3.1 (March 26, 2015) {#section_591371851693496C820175753F588E73}

This release includes the following features and enhancements:

<table id="table_5A2F2058ACFB455E9F69484CA0C8D3DE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer improvements </p> </td> 
   <td colname="col2"> <p>Content that only appears on hover, such as flyout menus and mini-carts, is now selectable for editing in the Visual Experience Composer. </p> <p>See <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Traffic Estimator </p> </td> 
   <td colname="col2"> <p>The Traffic Estimator, formerly available only in the Multivariate Test activity type, is now available for Automated Personalization activities. </p> <p>See <a href="/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714" format="dita" scope="local"> Estimate the Traffic Required for Success </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Visual Preview </p> </td> 
   <td colname="col2"> <p>Visually preview every content combination inside the Visual Experience Composer. </p> <p>See <a href="/help/main/c-activities/t-automated-personalization/ap-preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> Preview Experiences for an Automated Personalization Test </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Improved content viewing </p> </td> 
   <td colname="col2"> <p>You can now see every item that qualifies for a collection or exclusion when viewing or editing the collection. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Improved search results </p> </td> 
   <td colname="col2"> <p>The total number of items that meet each search string is displayed. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Upload Customer Attributes in Adobe Analytics </p> </td> 
   <td colname="col2"> <p>Analytics users who capture enterprise customer data in a customer relationship management (CRM) database can upload that data into the Experience Cloud. </p> <p>Once the data is in the Experience Cloud, you can, for example, create an audience segment in Analytics that includes customer attributes in the segment definition, and then share that audience with Target. </p> <p> <p>Note:  Target is not yet able to consume raw customer attributes directly. </p> </p></td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* For Analytics for Target based activities, the Lift and Confidence columns are now hidden for Analytics metrics where the calculations cannot be performed. 
* Fixed an issue where the short format of the `charset` metatag was not recognized in the Enhanced Experience Composer

**Known Issues**

* Target-based conversion events for multivariate testing in Target Standard/Premium are not being reported when Analytics is being used as the reporting source for Target. This issue is expected to be fixed soon. 

### Adobe [!DNL Target] 15.2.1 (February 19, 2015) {#section_9AA19B060D814E08A673FB752E21D0C3}

This release includes the following features and enhancements:

<table id="table_1558E5A5BAB64CC281C193F5A49E2ECE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p class="premium">New activity type: Recommendations </p> </td> 
   <td colname="col2"> <p>Recommendations activities automatically display products or content that might interest your customers based on previous user activity. Recommendations help direct customers to relevant items they might otherwise not know about. </p> <p>Recommendations is available as part of the Target Premium solution. It is not included with Target Standard without a Target Premium license. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Fixed an error that caused a redirect offer not to work when revisiting a page.

### Adobe [!DNL Target] 15.1.1 (January 22, 2015) {#section_059F9B41804B4FA58D05C4485EDF926D}

This release includes the following features and enhancements:

<table id="table_5D4C3C5695BA4A88BC65E2721CFB073A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> New activity type: Multivariate test </td> 
   <td colname="col2"> <p> A full-factorial multivariate test compares all possible combinations of offers in your content areas to help you determine the best possible combination of content. Multivariate tests also show which content in which areas most contributes to activity success. A common use of multivariate tests is to optimize an entire page after you've used an A/B test to determine an optimal layout. With the multivariate test, you can optimize the individual assets on the page (such as the main image, headlines, or promotional content). </p> <p>For an introductory video, see <a href="https://my.adobeconnect.com/p2k6u8iiu6l/" format="https" scope="external"> https://my.adobeconnect.com/p2k6u8iiu6l/ </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browse to pages and in-page elements in the Visual Experience Composer </td> 
   <td colname="col2"> <p> Allows you to open the visual experience composer on one page, and then follow links and form submissions to reach other pages on your site, such as a shopping cart. Once on the page you want to test, flip the Visual Experience Composer back to "Compose" mode and create your experiences. For example, you can change a message on the Shipping page, then test it against the default. </p> <p> The Browse mode also lets you interact with a page to get to the right state, such as going through an image carousel, open a mini-cart, or close a pop-up. Once the page is in the state you need, flip to "Compose" mode and create your test. </p> <p> Currently works with A/B tests, experience targeting, and A/B tests with Analytics. </p> <p>See <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Experiences </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobile device targeting </td> 
   <td colname="col2"> You can select mobile device options when creating an audience. <p>See <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a> for more information. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Click tracking (Automated Personalization) </td> 
   <td colname="col2"> <p>You can now track clicks in Automated Personalization. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mboxTrace debugging utility </td> 
   <td colname="col2"> <p> Examine details about your Target page implementation and activity/experience delivery status for improved troubleshooting. </p> <p>See <a href="/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Troubleshooting Content Delivery </a> for more information. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

This release includes the following fixes:

* Fixed an issue where scrolling did not work properly in IE10.

## Releases 2014 {#reference_A841709C803C4ECEB236F62E6513EB0F}

### Adobe [!DNL Target] 14.10.2 (November 6, 2014) {#section_E7036B45DF974FB7B81E67261357A01B}

<!-- 

target/r_release-notes-2014.xml

 -->

This minor release is focused mainly on server stability. There are no new features as part of this patch.

### Adobe [!DNL Target] 14.10.1 (October 30, 2014) {#section_D557CB331A004155B91CFE5B197076F3}

This release includes the following features and enhancements:

|  Feature  | Description  |
|---|---|
|  Redirect offers  | Redirect an experience to a different URL so you can test one page against another page. See [Create a Redirect Offer](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).  |
|  Apply targeting on success metrics  | Choose a saved audience to apply on a success metric. With this feature you can limit what actions count for a particular success event. An example might be limiting conversions to when the order is more than $0, or only counting success when a user views a particular page in the same session as entering the activity.  |
|  Automated Personalization: Select and report against RPV/AOV metrics  | You can now select the RPV and AOV metrics in the Automated Personalization experience creation flow. For more information about creating n Automated Personalization activity, see [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).  |
|  Improved permission controls  | Only users with sufficient permissions can edit audiences.  |

This release includes the following enhancements:

* Overview page shows the activity goal. 
* A warning displays when JavaScript is entered in the HTML editing box.

### Adobe [!DNL Target] 14.9.1 (September 19, 2014) {#section_681F27FBFDFF46FE8A1A8E24A50A26F4}

This release includes the following features and enhancements: 

|  Feature/Enhancement  | Description  |
|---|---|
|  Allow insertion and editing of JavaScript  | Added the ability to edit and inject custom JavaScript in the experience editor when you choose **[!UICONTROL Edit HTML]** from the actions menu.  |
|  Automatic audience import  | Audiences are automatically imported in the background when a user opens the audience list and the imported audiences are more than 10 minutes old.  |
|  Increased size of HTML offers than can be synced to [!DNL Target Classic]  | Increased the former 64KB limit to 256KB.  |

This release includes the following fixes:

* Fixed an issue where video offers were not delivered correctly on Firefox. 
* Fixed an issue that prevented an undo on Edit Link from showing as undone in the Visual Experience Composer. 
* Fixed an issue in the Automated Personalization experience editor that caused a changed video offer to not appear as changed. 
* Fixed an error that caused an activity's Collision page from displaying in Google Chrome as a blank page.

### Adobe [!DNL Target] 14.8.1 (August 21, 2014) {#section_02D0DFA7A8D145B2B3FEFF83591243E1}

This release includes the following new features and enhancements: 

|  Feature/Enhancement  | Description  |
|---|---|
|  Enhanced syncing of HTML offers with [!DNL Target Classic] by increasing the character limit  | Raised the character limit of an HTML offer created under Content to align with the 256 KB limit of HTML offers synced to [!DNL Target Classic].  |
|  Improved user experience when an error is created in the Experience Editor.  | The Experience Editor displays a message when DOM structure changes on the page breaks the selectors.  |

**Fixes**

* Fixed an issue where the Reporting graph was not generated while navigating between activities. 
* Fixed a problem where selected links were not marked as selected when users clicked **[!UICONTROL Select Link]** on the [!UICONTROL Goals and Settings] page. 

* Fixed an error that prevented a new activity from appearing in the [!UICONTROL Activity List] after being activated on the [!UICONTROL Overview] page. 

* Fixed a problem that prevented users from selecting a link for click tracking. 
* Fixed an issue that caused duplicate offers to appear in an offer-level report. 
* Fixed an issue that prevented mbox elements from being inserted. 
* Fixed an error that caused link click conversions not to work. 
* Fixed a click-track conversion error that negated `target="_blank" functions.` 
* Fixed a problem where click tracking was navigating off the page.

### Adobe [!DNL Target] 14.6.1 (June 25, 2014) {#section_A520F01EEE0A4C2CBB3F2A37E6DD6F83}

This release includes the following new features:

>[!NOTE]
>
>Some features in this release are available only as part of the [!DNL Target Premium] solution.

<table id="table_A2A978B157D54E17BD7366ADC04C8FC9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="keyword"> Automated Personalization (Target Premium) </span> </td> 
   <td colname="col2"> <p> <span class="keyword"> Automated Personalization </span> provides advanced machine learning algorithms to drive personalized experiences and improved conversion rates for digital experiences. </p> <p> <p>Note:  <span class="keyword"> Automated Personalization </span> is available as part of the <span class="keyword"> Target Premium </span> solution. It is not included with <span class="keyword"> Target Standard </span> without a <span class="keyword"> Target Premium </span> license. If you have a <span class="keyword"> Target Standard </span> or <span class="keyword"> Target Premium </span> license, use the <span class="keyword"> Target </span> card in the Adobe Experience Cloud. </p> </p> <p>Implement one file on your site and to enable the ability to point and click on any content and then visually create and select additional content options for that area. Then, the modeling system automatically determines which piece of content to deliver to each individual based on all behavioral data the system has about the visitor. This ability provides a personalized experience for each visitor. The marketer does not need to run a test, then analyze the results, then deliver a winner before realizing the lift found from optimization. </p> <p> <span class="keyword"> Automated Personalization </span> provides: </p> 
    <ul id="ul_9EF654B10FFA46169EE2E033683BA82E"> 
     <li id="li_8D201BF8F37B4B2489D039A0340E065E">Two machine-learning algorithms: 
      <ul id="ul_E1DF69071C9047EEA692B5EF01176E4B"> 
       <li id="li_1F4ED87AB6D044C1BE04D0360F42D56F"> <span class="keyword"> Random Forest </span> </li> 
       <li id="li_BE6388BA88684501B741713CECF5AE91"> <span class="keyword"> Residual Variance Model </span> </li> 
      </ul> </li> 
     <li id="li_36E18493A95B4C96BFA3133CDFD8826A">Single line of code implementation with WYSIWYG content editing </li> 
     <li id="li_79B1878FA64A40E88A973C57C39FC5FF">Primary goal for the activity currently uses the Conversion metric. Revenue and engagement are available as additional metrics. </li> 
     <li id="li_FE94A79767EF4534BD02B2AFD7E27E1B">Connection to the <span class="keyword"> Master Marketing Profile </span> for seamless collection of advance visitor behavioral data </li> 
    </ul> <p>See <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multiple activities on one page </td> 
   <td colname="col2"> <p>Content from multiple Target Standard activities can be delivered on one page from one <span class="keyword"> Target </span> server call. </p> <p> <p>Note:  This does not affect the Target Classic priorities evaluation. </p> </p><p>For information about how Target determines which experience to show when multiple activities target the same location on a page, see <a href="/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F" format="dita" scope="local"> Priority </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fixes**

* Fixed an issue where some shared audiences that have been deleted still show in the [!UICONTROL Audiences] list. 
* Fixed an error where an unexpected [!UICONTROL Save] dialog box appeared in Internet Explorer 10. 
* Fixed a synchronization error when saving a campaign. 
* Fixed an issue where the audience for an experience was not shown on reports. 
* Fixed an issue that prevented the metrics lists in [!DNL Target] and [!DNL Analytics] from matching. 

* Fixed an issue that allowed users to specify their global mbox to be an mbox that is used to deliver HTML content by [!DNL Target Standard]. Using the global mbox in that way negatively affects content delivery and [!DNL Target Classic]'s ability to deliver multiple campaigns to a single page in a single request. 

* Fixed an error that resulted in removed items continuing to be displayed.

### Adobe [!DNL Target] Standard 14.5 (May 28, 2014) {#section_530EAB9376414D4989CA0740361DDCC2}

This release includes the following bug fixes:

* Fixed an issue where previewing an experience did not work as expected.

### Adobe [!DNL Target] Standard 1.7 (April 28, 2014) {#section_2C2B9B6299ED4F48A3B983AB015F381A}

[Target Standard 1.7 Release Webinar](https://my.adobeconnect.com/p1oabaz3cxi/)

This release includes the following new features: 

<table id="table_11CD9EE0C9534FF19C9154784C4BFCF0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Adobe Analytics-enhanced reporting for Adobe Target </td> 
   <td colname="col2"> Adobe Analytics customers can select Analytics as the default reporting source during the <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/create-a4t.md#task_FE48F7B077C44A5BA015B087428412EF" format="dita" scope="local"> test set-up process </a>. Selecting all success metrics or audiences you want to use to filter your results is no longer required. Within reporting, you can select any success metric or audience segment defined in Analytics and retroactively apply it to your reporting for extensive filtering and drill-down analysis of your optimization results. <p> <p>Note:  To request access to this feature, visit <a href="https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y" format="http" scope="external"> https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Master marketing profile real-time audiences </td> 
   <td colname="col2"> Leverage the master marketing profile that unifies visitor IDs and data into a single, actionable profile for use across solutions. A checkbox during the segment creation process in Adobe Analytics allows the segment to be available within the Adobe Target's custom audience library. A segment created in Analytics or Audience Manager can be used to target visitors in Target. <p> <p>Note:  To request access to this feature, visit <a href="https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y" format="http" scope="external"> https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Experience targeting activity type </td> 
   <td colname="col2"> <a href="/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4" format="dita" scope="local"> Target different experiences to different audiences in one activity </a>. <p> <p>Note:  This provides similar functionality to the Landing Page campaign in Target Advanced. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Multi-page testing </td> 
   <td colname="col2"> <p> <a href="/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Choose to run a test or targeted activity across a set of webpages </a>. You can now deliver tests to every product page, or modify your global nav on every page of the site. Use a simple rule builder to specify what the group of pages should be. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Bug Fixes**

This release includes the following bug fixes:

* Fixed an issue that prevented `target.js` from being compressed by Edge. 
* Fixed an issue in reports that prevented the conversion count in the Activity row from displaying for A/B activities. 
* Fixed an issue where a report no longer displayed after an experience with data was deleted. 
* Created a workaround to automatically bypass a Chrome version 34 defect that prevented pages with mixed content from displaying. All versions of Chrome can now be used.

**Known Issues**

This release includes the following known issues. This issue will be fixed in an upcoming update.

* Click tracking does not work on elements that have been rearranged using the Visual Experience Composer. Avoid setting up click tracking on rearranged elements until this is bug is fixed. 
* A synchronization error occurs if Geo audiences are created in Target Standard when geolocation is disabled in Target Advanced. 
* Unable to swap an image when the image is referenced in CSS. 
* If you swap an image, and then resize it, the experiences in the Experience Editor do not display correctly.

### Adobe [!DNL Target] Standard 1.6 (March 17, 2014) {#section_DB1319CDD8944F6FB749E525EB551017}

This release includes the following new features: 

|  Feature  | Description  |
|---|---|
|  Localized versions available  | Target Standard has been localized in French, German, Japanese, and Spanish  |
|  Simplified implementation  | Target Standard has been improved to make it easier to implement for existing Target Advanced users. The new implementation uses your existing global mboxes to run Adobe Standard activities.  |

**Bug Fixes**

This release includes the following bug fixes:

* Fixed an issue that caused Remove Item and Edit HTML to not work in certain cases.

**Known Issues**

This release includes the following known issues. This issue will be fixed in an upcoming update.

* Winner works based on Goal only and does not change based on metrics selected. 
* Click tracking does not work on elements that have been rearranged using the Visual Experience Composer. Avoid setting up click tracking on rearranged elements until this is bug is fixed. 
* A synchronization error occurs if Geo audiences are created in Target Standard when geolocation is disabled in Target Advanced. 
* Unable to swap an image when the image is referenced in CSS. 
* The new viztarget mbox type does not work with the Target Advanced/Adobe Analytics integration v4, the current version. 
* In reports, the number format and currency shown on the graph does not match the table if the locale is set to something other than dollar. 
* Audiences search box does not support non-ASCII characters. 
* For users of the Spanish and Japanese versions, saving an activity after setting the start and end dates results in an error. It is recommended that you save without setting start and end dates, and then activate and stop your activity from the Activity Overview or Activity List page when required.

### Adobe [!DNL Target] Standard 1.5 (February 25, 2014) {#section_5E9E3DDBCB82494AA62A21AC9282063F}

This release includes the following new features: 

<table id="table_67115780726F48859DC8E46E34567DC3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity collisions </td> 
   <td colname="col2"> <p> Target Standard now provides a list of activity collisions. An activity collision occurs when multiple activities are set up to deliver content to the same page. If an activity collision occurs, you may not see the expected content on your page because you've entered a different activity. </p> <p> All activities on the same URL are listed, regardless of any audience targeting in each activity. </p> <p> If your activity contains collisions, a <span class="wintitle"> Collisions </span> tab is available the on the activity overview page. Open this tab for a list of activities that are colliding. Click an activity in the list to view the overview page for that activity. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md#concept_0BC6B929592744DFA7DA01FF4F91052E" format="dita" scope="local"> Activity Collisions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> New targeting options: Profile, User </td> 
   <td colname="col2"> You can now target profile and user parameters. See <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Audiences </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Insert elements </td> 
   <td colname="col2"> <p>You can now add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following known issues. This issue will be fixed in an upcoming update.

* Winner works based on Goal only and does not change based on metrics selected. 
* Click tracking does not work on elements that have been rearranged using the Visual Experience Composer. Avoid setting up click tracking on rearranged elements until this is bug is fixed. 
* A synchronization error occurs if Geo audiences are created in Target Standard when geolocation is disabled in Target Advanced. 
* Unable to swap an image when the image is referenced in CSS.

### Adobe [!DNL Target] Standard 1.4 (January 20, 2014) {#section_CD27AEE32B4F40BDAB422711B96739A5}

This release includes the following new features and enhancements: 

<table id="table_9E303FF0CD954795A29369A6D4166DB5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feature </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Estimate revenue lift </td> 
   <td colname="col2"> <p>Target can estimate the revenue lift you would attain if all users view the winning experience. </p> <p>This estimate calculates the amount of lift achieved by the winning experience and your total number of visitors over the life of the test, and shows the lift you might achieve if every visitor sees the winning experience, if the trends continue as they have during the test. </p> <p> The accuracy of the estimate depends on a number of factors, including projected figures if current trends continue. These values are estimates based on past performance and should not be used for financial guidance. Future results may vary. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Undo/Redo </td> 
   <td colname="col2"> <p>You can undo changes you make to your activities during an editing session. You can also redo undone changes. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Move element </td> 
   <td colname="col2"> <p>You can move elements on your page. Unlike Rearrange Elements, Move does not shift other elements to make room for the element being moved. Use your arrow keys to fine tune the move. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Resize element </td> 
   <td colname="col2"> <p>You can resize an element on your page. When you select Resize, a handle appears in a corner of the element that lets you drag that corner to resize. </p> <p>See <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer Options </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Target a location when setting up an audience </td> 
   <td colname="col2"> <p>When creating an audience, you can select a location (mbox) and specify parameters for that location. </p> <p>See <a href="/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1" format="dita" scope="local"> Creating a New Audience </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Preview links (Enhancement) </td> 
   <td colname="col2"> <p>Preview links work as expected. </p> </td> 
  </tr> 
 </tbody> 
</table>

This release includes the following fixes:

* Fixed issues that prevented preview links from displaying as expected.

This release includes the following known issues. These issues will be fixed in an upcoming update.

* If Estimated Lift is enabled in Target Standard, and Target Advanced is set to a different time zone than the user's browser, the predicted revenue value might not appear on the Activities list or in the Reports status bar for up to one full day. Because Report View uses date but not time, the data appears in Report View but not for projected lift. 
* Click tracking does not work on elements that have been rearranged using the Visual Experience Composer. Avoid setting up click tracking on rearranged elements until this is bug is fixed. 
* A synchronization error occurs if Geo audiences are created in Target Standard when geolocation is disabled in Target Advanced. 
* Unable to swap an image when the image is referenced in CSS.

## Releases 2013

### Adobe [!DNL Target] Standard 1.3 (November 19, 2013) {#section_D633ACA56FA941648219EB3748D814EC}

This release includes the following new features and enhancements: 

|  Feature  | Description  |
|---|---|
|  Geo-targeting  | Target on Country, State, City, Zip code, or DMA.  |
|  Use the Visual Experience Composer to rearrange elements.  | You can rearrange child elements inside their parent element using the Visual Experience Composer.  |
|  Preview experiences directly on your site.  | Once you save an activity, you can preview it directly on your site, even if the activity is not live. This allows you to see how it will appear, without serving it through an iFrame. You can copy links to each test experience to view those experiences in your browser or to send them to your team members for them to view. People who view these pages will not be counted in the reports.  |

This release includes the following fixes:

* Fixed an issue where the click tracking metric was not deleted from an activity if the experience URL was reset. 
* Fixed an issue in the experience composer that caused the default experience to flash quickly before new content displays when navigating through experiences.

This release includes the following known issues. These issues will be fixed in an upcoming update.

* A synchronization error occurs if Geo audiences are created in Target Standard when geolocation is disabled in Target Advanced. 
* Unable to swap an image when the image is referenced in CSS. 
* Click tracking does not work on elements that have been rearranged using the Visual Experience Composer. Avoid setting up click tracking on rearranged elements until this is bug is fixed. 
* Users cannot select the **[!UICONTROL Remove]** action for content that is wrapped in an mbox.

### Adobe [!DNL Target] Standard 1.2 (Oct. 31, 2013) {#section_420B5E910D7341AA8DB059C8E1071D53}

There are four known issues with this release. These issues will be fixed in an upcoming update.

* On some clusters, editing a reusable offer may not be reflected on customer's site for activities that use that offer outside of an mbox. 
* Swapped images in area of a page that is not controlled by an mbox might result in a 404 error. 
* When you create a new audience, or edit and save an existing audience, it does not show in the Audiences list until you refresh the screen or search for the audience. 
* When you delete an HTML offer from Target Standard, it is not deleted from Target Advanced.

This release includes the following fixes and enhancements:

* Fixed multiple issues that caused some activities and experiences to fail to sync properly with Target Advanced. 
* Fixed an issue where [!DNL target.js] moves other scripts out of the `<head>` section of a page. 

* Fixed an issue that caused some referenced assets to copy when an activity is copied. 
* Fixed an issue that caused an updated image offer content to fail to update in both Scene7 and Target Advanced. 
* Fixed an issue where applying a search filter clears the audiences selected in "Audiences for Reporting." 
* Enhanced graphs to default to hourly results when a test has been live for less than two days. 
* Fixed an issue that caused copying a non-synced activity to fail. 
* Added keyboard input functionality to drop down menus for location.
* Improved the error message that displays when deleting an offer used in an activity.

### Adobe [!DNL Target] Standard 1.1 (Oct. 18, 2013) {#section_79FA6A61D2284D41A34F00014A342F07}

This release includes the following fixes and enhancements:

* Fixed an issue that caused the activity sync to fail in the first sync attempt after adding valid experiences to a partial activity. 
* Fixed an issue that resulted in a 500 error on the Summary report after deleting and adding an experience. 
* Fixed an issue that caused inaccurate visitor data when a visitor views multiple experiences. 
* Activity start and end times now sync correctly between Standard and Advanced. 
* Improved the display of mixed content. 
* Fixed an issue that caused the Visual Experience Composer to malfunction if JavaScript in the HTML code overrides the browser definition of the JSON object. 
* Fixed an issue where the displayed number of activities was incorrect when sorting according to status. 
* Fixed an issue where white space in the Goal field did not validate correctly. 
* Fixed an issue that caused the creation of multiple offers for a single in Advanced when the image was swapped. 
* Fixed an issue that caused search not to work on images in the content picker. 
* Fixed a defect that inverted activity list sorting when sorting by Name or State. 
* Fixed an issue where anonymous offers were not being deleted when no longer used in an activity. 
* Fixed a defect that caused an incorrect experience name to display on a shared card when editing an activity. 
* Fixed a defect where an updated image offer did not correctly update the content in both Scene7 and Target Advanced. 
* Fixed an issue where copying an image asset also copied Scene7-related properties that should not have been copied.
