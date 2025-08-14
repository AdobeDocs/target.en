---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: July 24, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.8.2 (August 13, 2025)

This release includes the following fixes and updates:

**[!UICONTROL Activities]**

+++See details
* Fixed an issue in the updated [!DNL Target] UI where certain activities failed to load when attempting to edit. This issue caused customers leaving users in an indefinite loading screen. This issue impacted multiple activities and was reported to occur inconsistently across customers. With this fix, affected activities now load properly, allowing seamless editing and reducing disruption to activity workflows. (TGT-53209)
* Fixed an issue in the activity-create process that prevented customers from saving changes due to a backend validation error: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` This issue occurred when modifying specific elements within an activity, resulting in a failed save operation. The fix ensures that `optionLocalId` references are now correctly validated, allowing customers to save activities without encountering this error. (TGT-53293)
* Fixed an issue in the activity-create process that caused the UI to crash after switching pages three times during editing. The crash was triggered by invalid option references, resulting in console errors such as "Option with localId '7' not found." With this update, customers can now switch between pages and apply modifications without encountering system failures or interruptions. (TGT-53295)
* Fixed an issue in the activity-create process where customers were unable to save changes to an activity due to an invalid user input error. The error occurred when modifying experiences in the updated UI, preventing updates from being committed. The activity can now be saved successfully, allowing customers to edit and publish without interruption. (TGT-53267)
* Fixed an issue in the activity-create process where customers were unable to edit activities in the updated UI due to a continuous loading screen. Customers can now open and modify activities without encountering loading failures. (TGT-53415)

+++

**Experience Fragments (XFs)**

+++See details
* Fixed an issue in the activity-create process that allowed customers to edit the HTML of [!DNL Experience Fragments] (XFs) exported from [!DNL Adobe Experience Manager] (AEM) within [!DNL Target]. This behavior was unintended, as XFs should remain locked for editing once published from AEM. The fix ensures that the "Edit HTML" option is no longer available for AEM-exported fragments, preserving content integrity and expected governance. (TGT-53286)

+++

**QA mode**

+++See details
* Fixed an issue in the activity-create process where leading spaces in the activity URL were not trimmed properly when saving. This caused invalid QA links and incorrect formatting in the back-end. After the update, URLs are now saved cleanly, preventing broken links and improving the reliability of QA workflows for customers. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++See details
*  Fixed an issue in the new [!UICONTROL Catalog Search] UI where the [!UICONTROL Advanced Search] feature failed to provide suggestions. Users were required to input exact values with precise spelling, making the search experience cumbersome and error-prone. With this fix, the [!UICONTROL Advanced Search] now offers relevant suggestions as users type, improving usability and reducing friction in locating products. (TGT-52008)
* Resolved several issues, including poor responsiveness of criteria details on small-screen devices, lack of results when selecting "All host groups" in the [!UICONTROL Environment] filter, and inability to interact with entities that have no name. These fixes improve usability across screen sizes, ensure accurate filtering, and allow full interaction with all product entities, enhancing the overall experience for users. (TGT-52992)
* Fixed an issue in the [!DNL Recommendations] activity-create process where product IDs were missing from the product detail screen, making it difficult for customers to copy or reference product IDs during workflows. Product IDs now appear clearly in the detail view, improving visibility and supporting more efficient product management for customers. (TGT-51964)
* Fixed an issue in the activity-create process where the [!UICONTROL Message] column in the [!DNL Recommendations] view did not display product data, even though messages were present. Customers had to manually remove and re-add the column to temporarily reveal the content, which would often disappear again when scrolling or searching. This update restores consistent visibility of product messages, improving catalog navigation and review workflows. (TGT-52777)
* Fixed an issue in the activity-create process where selecting the "All host groups" environment in the [!DNL Recommendations] view returned no results. Customers can now view product data across all host groups as expected, improving visibility and filtering accuracy during activity setup. (TGT-53006)
* Fixed an issue in the activity-create process where disabling the front promotion toggle in activity settings did not persist after saving. Customers attempting to remove the front promotion found the toggle re-enabled upon revisiting the activity, preventing proper customization. This update allows changes to be saved reliably, giving customers full control over promotion settings. (TGT-53215)

+++

**Visual Experience Composer (VEC)**

+++See details
* Fixed an issue in the activity-create process where certain activities failed to load, leaving customers unable to access modifications. Additionally, the [!UICONTROL Cancel] button was unresponsive, preventing customers from stopping the loading process or exiting the edit view. This fix ensures that activities now load reliably and the [!UICONTROL Cancel] button functions as expected, improving overall stability and user experience in the Visual Experience Composer (VEC)(TGT-53218)
* Fixed an issue in the updated VEC UI where modifications failed to load when switching between experiences in an Experience Targeting (XT) activity. Customers were unable to edit experiences beyond the one they initially entered, and the [!UICONTROL Cancel] button was either missing or unresponsive. This fix ensures that modifications now load correctly across all experiences and that the [!UICONTROL Cancel] button functions reliably, even without the Helper extension, improving editing workflows and reducing frustration. (TGT-53256)
* Fixed an issue where switching between multiple experiences caused a white screen. Also fixed an issue in the activity-create process where customers encountered a white screen when attempting to modify multiple experiences within an activity. This issue occurred after applying changes to two experiences and then selecting a third experience, preventing further edits. The update ensures smooth transitions between experiences, allowing customers to make modifications without interruption. (TGT-53266)
* Fixed an issue where custom code modifications made in the Visual Experience Composer (VEC) were not reliably saved in a single attempt. Customers reported that changes, such as styling updates or HTML edit, were intermittently missing from the website and QA URLs, even after using both the [!UICONTROL Edit Content] and final [!UICONTROL Save] buttons. This regression has been resolved, ensuring that all custom code changes persist as expected across editing sessions. (TGT-53418)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
