---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: August 27, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice. Information in this article is updated frequently, especially before releases.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.8.4 (August 28, 2025)

This release contains the following updates and fixes:

**[!UICONTROL Activities]**

+++See details
* **Fixed an issue where scheduled activities incorrectly displayed a "[!UICONTROL Live]" status in the updated UI during the activity-create process**: Activities with future activation dates now correctly show a "[!UICONTROL Scheduled]" status. (TGT-53187)
* **Scheduled activities incorrectly displayed a [!UICONTROL Live] status until the page was refreshed**: Customers reported that when scheduling an activity to go Live at a future date and time, the status initially appeared as [!UICONTROL Live] instead of [!UICONTROL Scheduled]. This caused confusion despite the confirmation message indicating the correct scheduling behavior. The activity status now accurately reflects [!UICONTROL Scheduled] immediately after saving, without requiring a page refresh. (TGT-52937)
* **Changes to duplicated experiences unintentionally affected the original experience**: Customers reported that when duplicating an experience within an activity and assigning a new audience, any changes made to the duplicated experience—such as design or criteria—were also reflected in the original experience. This prevented the creation of independent variations and impacted production workflows. Duplicated experiences can now be edited independently without affecting the original version. (TGT-53361)
* **Fixed an issue that prevented customers from saving an activity due to an `InvalidProperty.Json` error**: Previously, customers encountered an "Invalid user input" error when attempting to save an activity without making changes. The error was caused by an unrecognized property name 'content' in the JSON payload. This issue has been resolved, and activities can now be saved successfully in the updated UI, even when no modifications are made. (TGT-53513)

+++

**Analytics for Target (A4T)**

+++See details
* **Cannot type report suite names when creating A4T activities**: Customers were unable to type into the [!UICONTROL Report Suite] drop-down when selecting [!UICONTROL Analytics] as the reporting source in the updated UI.  This issue made it difficult to locate specific report suites, especially for organizations with large lists. The drop-down now supports typing and searching by name, improving efficiency during the activity-create process. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++See details
* **Expired "Time Frame" audiences blocked activity saving even after removal**: Previously, customers were unable to save an activity if it had previously included an expired "Time Frame" audience—even after that audience was removed. This issue was caused by lingering validation on the activity-only audience, which continued to trigger errors. Activities can now be saved as expected once expired audiences are removed. (TGT-53517)
* **Additional pages and multiple audiences disappeared after saving an activity**: Previously, customers creating an [!UICONTROL A/B Test] activity in the activity-create process experienced a loss of configured additional pages and multiple audiences after saving. This behavior was unexpected and caused confusion during setup. These configurations now persist correctly after saving the activity. (TGT-52357)

+++

**Decision offers**

+++See details
* **Unable to edit decision offers or select specific page elements in the updated VEC**: Customers encountered multiple issues in the updated UI that blocked their ability to update existing activities or create new ones:

  * Decision offers were incorrectly displayed as HTML offers, preventing edits.
  * Specific page elements could not be selected in the VEC.
  *  Changes made during editing were not saved.
  * Certain regional URLs failed to load properly in the VEC, requiring manual cookie adjustments.

  Customers can now edit decision offers, select page elements accurately, and save changes as expected. Regional pages also load correctly in the VEC. (TGT-53425)

* **Offer Decision selectors could not be modified and changed unexpectedly after saving**: Customers reported that when applying Offer Decisions in the updated UI, the selector could not be changed from its default value. Attempts to modify the selector (for example, to `#tf-cq-hr or body`) were ignored, and after saving the activity, the selector was replaced with a generic value like `#cdq_element_0`. This issue caused the offer to disappear from the Visual Experience Composer (VEC) and blocked further edits. Customers can now modify Offer Decision selectors as intended, and saved selectors persist correctly without unexpected changes. (TGT-53433)
* **Offer Decisions disappeared from activities after saving**: Customers reported that Offer Decisions applied to page elements in the updated UI were no longer visible after saving the activity. In some cases, the selector was changed unexpectedly, and the offer failed to render in the VEC upon re-editing. Offer Decisions now persist correctly after saving, and selectors remain stable, ensuring offers are visible and editable as expected. (TGT-53434)

+++

**Experience Fragments**

+++See details
* **Customers received an error when inserting [!UICONTROL Experience Fragments] using [!UICONTROL Insert Before] or [!UICONTROL Insert After]**:  Customers encountered an error when attempting to insert [!UICONTROL Experience Fragments] into an activity using the [!UICONTROL Insert Before] or [!UICONTROL Insert After] options in the updated UI. The error message displayed was:

  "Offer content must contain exactly one HTML element."

  This issue was specific to the updated UI and did not occur in the previous version. It has now been resolved, and customers can successfully insert [!UICONTROL Experience Fragments] without encountering this error. (TGT-53432)

* **Error message when adding an [!UICONTROL Experience Fragment] to an activity**: Previously, customers attempting to insert an [!UICONTROL Experience Fragment] using the [!UICONTROL Insert Before] or [!UICONTROL Insert After] option encountered the error: "Offer content must contain exactly one HTML element." This error appeared despite the fragment being valid and accepted in the legacy UI, which included a toggle to support this configuration. The issue has been resolved in the updated VEC. (TGT-53442)

+++

**Localization**

+++See details
* **Toast messages in the [!UICONTROL Goals & Settings] step were not localized**: Previously, customers encountered an unlocalized toast message when entering unsupported characters—such as emojis—in the [!UICONTROL Objective] field during the activity-create process. Toast messages are now properly localized across all supported languages, ensuring a consistent and accessible experience for global customers. (TGT-52251)
* **A string in the [!UICONTROL Create Audience] dialog was not localized**: Previously, the message "Choose at least a start or end date for 'does not repeat'" appeared unlocalized in the [!UICONTROL Create Audience] modal when configuring time-frame attributes. The string is now properly localized across all supported languages, ensuring a consistent experience for global customers in the [!UICONTROL Audiences] workflow. (TGT-52253)
* **The tooltip in the [!UICONTROL Create Audience] dialog was not localized**: Previously, when customers hovered over the error tooltip after entering unsupported characters—such as emojis—in the audience name field, the tooltip appeared unlocalized. The tooltip now displays properly localized messaging across all supported languages, ensuring a consistent and accessible experience in the [!UICONTROL Audiences] workflow. (TGT-52254)

+++

**[!DNL Recommendations]**

+++See details
* **Unable to disable [!UICONTROL Front Promotion] in live activity**: Fixed an issue where customers were unable to disable [!UICONTROL Front Promotion] in live activities using the updated UI. Changes made in the promotion section during the activity-create process now persist as expected, ensuring accurate configuration of live activities in [!UICONTROL Product Catalog Search]. (TGT-53231)
* **Editing a duplicated experience's recommendation impacted the original experience**: Customers reported that when duplicating an experience within an activity and modifying the recommendation design or criteria in the duplicate, those changes were unintentionally applied to the original experience.  This issue prevented the creation of independent variations and disrupted expected behavior in the updated activity-create process. Duplicated experiences can now be edited independently without affecting the original version. (TGT-53369)
* **Cannot view the product list when editing a collection or exclusion in the [!UICONTROL Recommendations] tab** Previously, the product list filtered by applied rules was not visible in the edit modal, making it difficult for customers to confirm which products were included or excluded. The product list now displays correctly and updates in real time as rules are modified, improving visibility and usability in the updated [!DNL Recommendations] UI. (TGT-53481)
* **Updated the layout of the [!UICONTROL View Details] dialog in the [!UICONTROL Recommendations] tab**: Previously, the [!UICONTROL View Details] dialog lacked a clear structure, making it difficult for customers to access item-specific and inventory-related information. The layout has been updated to include two tabs: one tab displays details for the selected item, and the second tab shows the inventory filtered by the current rules of the collection or exclusion. This improvement enhances clarity and usability in the updated [!DNL Recommendations] UI. (TGT-53503)
* **Customers could not search report suites in the [!UICONTROL Goals & Settings] drop-down**: Previously, the report suites drop-down in the [!UICONTROL Goals & Settings] section of the activity-create process did not support text input for searching, making it difficult for customers with large numbers of report suites to locate the correct one. This functionality, available in the legacy UI, has been restored. Customers can now type to search and select report suites more efficiently. (TGT-53514)
* **Customers are unable to download the custom criteria CSV in the [!DNL Recommendations] UI**: Previously, clicking the download link for custom criteria CSVs in the [!UICONTROL Recommendations] tab returned a 404 error and failed to open in a new tab. The download link now opens in a new tab and correctly serves the CSV file, improving accessibility and usability for customers managing custom criteria. (TGT-51966)
* **Enabling a [!UICONTROL Recommendations] promotion without input data triggered a generic error message**: Previously, customers enabling a front or back promotion in a Recommend[!UICONTROL ]ations activity without specifying required fields encountered a vague "Invalid input error" with the code `error.restapi.missingFields`. The system now provides a clear and actionable error message indicating which fields are missing, improving usability and reducing confusion during the activity-create process. (TGT-52616)
* **Product thumbnails and images were not loading consistently in [!UICONTROL Catalog Search]**: Customers reported that product thumbnails and full-size images in [!UICONTROL Catalog Search] were intermittently missing or broken, especially after navigating or modifying column visibility. Thumbnails and images now load reliably, regardless of column settings or navigation behavior, improving the overall experience in the [!UICONTROL Recommendations] workflow. (TGT-52778)
* **Unable to create [!UICONTROL Designs] and [!UICONTROL Criteria] in the [!UICONTROL Stage] environment**: Customers encountered an "Invalid User input" error when attempting to create [!UICONTROL Designs] or [!UICONTROL Criteria] in the [!UICONTROL Recommendations] tab on the [!UICONTROL Stage] environment. Customers can now successfully create [!UICONTROL Designs] and [!UICONTROL Criteria] without errors in the [!UICONTROL Stage] environment. (TGT-53205)
* **[!UICONTROL Promotions] were not removed from [!UICONTROL Recommendations] activities after saving**: Customers reported that promotions added to [!DNL Recommendation] activities continued to appear even after being removed and saved. This issue affected both staging and production environments and persisted across multiple save attempts. Promotions now correctly reflect changes made during activity editing in the updated activity-create process. (TGT-53490)

+++

**[!UICONTROL Reports]**

+++See details
* **[!UICONTROL Automated Segments] displayed a null audience in activity reports**: Customers observed that when viewing [!UICONTROL Automated Segments] in the [!UICONTROL Reports] section of an activity, the audience field appeared as null, even though valid segment data was expected. This issue affected visibility into audience targeting and reporting accuracy. [!UICONTROL Automated Segments] now correctly display the associated audience information in activity reports. (TGT-52793)
* **Activity reports failed to download in CSV format**: Customers attempting to export activity reports from the [!UICONTROL Reports] tab encountered a failure when selecting the CSV download option. This issue affected both standard reports and order-details exports. Reports now download correctly in CSV format. (TGT-53464)

+++

**Single Page Applications (SPAs)**

+++See details
* **Switching between [!UICONTROL Browse] and [!UICONTROL Design] modes reset single-page application (SPA) states in the web editor**: Customers reported that switching between [!UICONTROL Browse] and [!UICONTROL Design] modes in the VEC caused the web editor to reload, resetting the SPA state and disrupting the activity-create process. The editor now preserves the SPA navigation state when switching modes, ensuring a smoother and more consistent editing experience. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer (VEC)]**

+++See details
* **Renaming a location in an [!UICONTROL Automated Personalization] (AP) or [!UICONTROL Multivariate Test] (MVT) activity did not persist after navigating to the [!UICONTROL Targeting] step and returning.** Customers can now successfully edit and save location names, and the changes remain visible throughout the activity-create process. (TGT-52367)
* **The legacy VEC UI displayed on tenants in the [!UICONTROL Stage] environment**: Fixed an issue when accessing certain tenants in the [!UICONTROL Stage] environment were incorrectly shown the legacy UI instead of the updated VEC. This issue was reproducible across multiple login paths and affected the [!UICONTROL Activities] section. The updated UI now displays correctly for both tenants in the [!UICONTROL Stage] environment. (TGT-52261)
* **Selecting a background color caused the page to crash in the updated VEC**: 
Fixed an issue where selecting a background color from the [!UICONTROL Style] panel in the updated VEC caused the page to crash and go blank. Console errors indicated a failure to read properties from an undefined element, specifically related to `querySelector`. Customers can now safely select background colors without triggering a crash. (TGT-53561)
* **Activities could not be saved due to an invalid user input error**: Fixed an error when attempting to save existing activities in the updated VEC. The error appeared only during edits, not when creating new activities with the same property. The error message included:

  `Invalid Json. Unrecognized property name 'content'. Location: line - 1, column - 432.`

  Activities using the affected property can now be saved successfully after editing. (TGT-53507)

* **Transparent images no longer included the "fmt=png-alpha" parameter in the updated VEC**: Customers reported that when replacing images in the updated UI, transparent backgrounds were no longer preserved. The image URLs generated by the updated VEC omitted the `fmt=png-alpha` parameter, which previously ensured transparency in the old UI. The updated UI now correctly appends the `fmt=png-alpha` parameter for transparent images, restoring expected rendering behavior. (TGT-52615)
* **Customers could not proceed to the targeting section in AP activities without adding two locations**: Customers creating [!UICONTROL Automated Personalization] (AP) activities in the updated UI were unable to proceed to the targeting section unless two locations were added. This behavior differed from the previous UI, where a single location was sufficient. The issue blocked activity creation and saving for customers who preferred to use only one location. Customers can now proceed to targeting and save AP activities with a single location, restoring expected functionality. (TGT-53426)
* **HTML Offers duplicated in the workspace when switching experiences**: Previously, customers inserting HTML offers in experienced duplicated content in the workspace after switching between experiences. This issue also caused the workspace to become non-scrollable, impacting usability. HTML Offers no longer duplicate, and the workspace remains scrollable when switching experiences in the updated VEC. (TGT-53487)
* **Manually updating a CSS selector caused the VEC screen to go blank**: Customers reported that while editing an offer in the VEC, manually updating the CSS selector triggered a blank screen, even when the selector was valid and present on the page. The VEC screen now remains stable when selectors are manually updated during the activity-create process. (TGT-53553)
* **Truncation issue in the Start date field when selecting 'specified date and time' in [!UICONTROL Goals & Settings]**: Customers experienced a truncation issue in the [!DNL Start date] field when choosing the specified date and time option in the duration section of the [!UICONTROL Goals & Settings] page during activity creation. The full date and time now display correctly across supported locales. (TGT-47843)
* **Filter icon disappeared when minimizing the browser in the [!UICONTROL Manage Content] rail**: Customers reported that the filter icon in the [!UICONTROL Manage Content] rail of the [!UICONTROL Automated Personalization] activity-create flow disappeared when the browser window was resized or minimized. The filter icon now remains visible and accessible regardless of browser size, improving usability across screen resolutions. (TGT-51449)

+++

**[!UICONTROL Workspaces]**

+++See details
* **Customers restricted to a single workspace could view activities from other workspaces**: Customers with access limited to a specific workspace were still able to select [!UICONTROL All Workspaces] in the updated UI and view activities from other workspaces. This behavior posed a risk of unintended changes to live activities outside their assigned scope. Workspace restrictions are now enforced correctly, and customers can view activities only within their assigned workspace. (TGT-53101)
* **Customers could view activities from the [!UICONTROL Default Workspace] without access**: Customers were able to see activities from the [!UICONTROL Default Workspace] despite not having access to it. Workspace permissions are now correctly enforced in the updated UI, ensuring customers only see activities associated with their assigned workspace. (TGT-53297)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
