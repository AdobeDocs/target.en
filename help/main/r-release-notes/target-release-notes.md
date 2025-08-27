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

## [!DNL Target Standard/Premium] 25.8.4 (September 1, 2025)

This release contains the following updates and fixes:

**[!UICONTROL Activities]**

+++See details
* **Customers could not copy activity or document names from the [!UICONTROL Activity Overview]**: Previously, customers were unable to copy the name of an activity or the associated offer/document directly from the [!UICONTROL Activity Overview] in the updated activity-create process. This limitation impacted usability, especially on smaller screens. Customers can now easily copy both activity and document names without workarounds. (TGT-51850)
* **Fixed an issue that prevented proactive ingestion of curated [!DNL Target] customer data during activity creation**: Improved the activity-create process by enabling the proactive collection of reports, content, and screenshots from [!DNL Target] customers. This enhancement addresses data gaps identified in existing use cases and helps ensure more accurate insights during activity and experiment setup. (TGT-52415)

+++

**[!UICONTROL Recommendations]**

+++See details
* **Product list was not visible in the [!UICONTROL View Collection] dialog:** Previously, customers were unable to see the product list when viewing a collection in the [!UICONTROL Recommendations] tab. The [!UICONTROL View Collection] dialog now correctly displays the associated products, improving transparency and usability in the updated Recommendations UI. (TGT-50531)
* **Fixed an issue that caused case-sensitive filtering in [!UICONTROL Product Catalog Search] advanced search**: The advanced search filtering in the [!UICONTROL Product Catalog Search] page now correctly ignores case sensitivity, aligning with the behavior of both the backend and GraphQL services. This update ensures consistent and accurate suggestion results for customers regardless of text casing. (TGT-53585)

+++

**[!UICONTROL Reports]**

+++See details
* **Reports failed to load for the Desktop audience due to an invalid audience name error**: Customers encountered a GraphQL error when attempting to view reports for the one audience in the activity-create process. The system returned an "Invalid audience name: XXXXX" message, preventing access to reporting data. Reports now load correctly for the Desktop audience. (TGT-53371)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* **Clicking "Accept Cookies" using the [!UICONTROL Enhanced Experience Composer] (EEC) failed due to a missing function**: Customers reported that attempting to accept cookies via the EEC resulted in a console error: `handleclickAcceptAllButton is not defined`. The cookie acceptance functionality now works as expected, ensuring a smoother experience during activity creation in the updated UI. (TGT-52794)
* **The new EEC UI failed to load certain pages that were previously supported in the legacy UI**: Customers reported that the new EEC could not load some pages, which were accessible in the legacy UI despite iframe-busting code present on the site. The updated activity-create process now supports loading these pages, restoring compatibility for activity creation workflows. (TGT-53061)
* **The VEC displayed a blank white screen when editing experiences**: Customers from a certain tenant reported that the VEC screen went blank when attempting to edit experiences in the updated VEC. This issue affected both newly created and older activities, preventing workflow continuity. The VEC now loads correctly, allowing customers to edit experiences without interruption. (TGT-53547)
* **The VEC crashed and displayed a blank screen when loading certain activities**: Customers from a certain tenant reported that the VEC failed to load specific activities. The experience editor remained stuck on "Applying initial modifications" before crashing and showing a blank screen. Console errors indicated a failure to read undefined properties. The editor now loads affected activities without errors in the updated VEC. (TGT-53548)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
