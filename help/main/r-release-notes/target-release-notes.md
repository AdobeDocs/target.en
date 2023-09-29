---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease 
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: September 29, 2023**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target] Standard/Premium 23.9.4 (October 2-4, 2023)

This release is available according to the following staggered schedule:

* **October 2**: Europe, Middle East, and Africa (EMEA) region
* **October 3**: Americas region
* **October 4**: Asia-Pacific (APAC) region

This release contains the following enhancements and fixes:

|Feature|Details|
| --- | --- |
|[!UICONTROL Activities] UI refresh<P>and<P>[!UICONTROL Feeds] UI refresh|As part of the [!DNL Adobe Target] team's ongoing effort to improve the user-experience for [!DNL Target] users, this release refreshes the [!UICONTROL Activities] and [!DNL Recommendations] [!UICONTROL Feeds] pages in the [!DNL Target] UI. This update unifies and standardizes design patterns that were previously inconsistent, while adding new enhancements.<P>For more information see [Activities](/help/main/c-activities/activities.md) and [Feeds](/help/main/c-recommendations/c-products/feeds.md).|
|[!DNL Recommendations] implementation pattern|The *Recommendations implementation pattern using at.js* pattern helps you understand and create your [!DNL Adobe Target Recommendations] implementation when using the at.js JavaScript library.<P>For general information about Target patterns, see [Implementation patterns overview](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/pattern-overview.html){target=_blank} in the *Adobe Target Developer Guide*.<P>The new Recommendations implementation pattern is comprised of the following articles:<ul><li>[Recommendations implementation pattern using at.js overview](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html){target=_blank}</li><ul><li>[Initialize SDKs](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/initialize-sdk.html){target=_blank}</li><li>[Configure data collection](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/data-collection.html){target=_blank}</li><li>[Render experiences](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/render-experiences.html?lang=en){target=_blank}</li><li>[Notify [!DNL Target]](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/notify-target.html?lang=en){target=_blank}</li></ul></ul>|

* Added [!UICONTROL Visual Experience Composer] (VEC) enhancements for dynamic frameworks. (TGT-44064)
* Fixed an issue that caused the selected date in the `getViewInAnalyticsId` request to not update properly. This fix helps recompute the [!DNL Analytics] link in reporting when the date range and metrics report settings are changed. (TGT-46246)

## [!DNL Target] Standard/Premium 23.9.3 (September 18, 2023)

This release contains the following enhancements and fixes:

* Enhanced the [!UICONTROL Visual Experience Composer] (VEC) to support Lightning Web Components (Light DOM). (TGT-45422)
* Fixed an issue that caused VEC actions to be applied in the incorrect order. In some cases, the VEC applied some modifications asynchronously and adding extra modifications to an element caused errors if that element displays after an [!UICONTROL Insert] action. Also fixes the VEC URL that now updates when clicking anchor links. (TGT-45983)
* Fixed an issue with the VEC [!UICONTROL Overlay] feature, which now supports elements in Shadow DOMs. (TGT-45202 & TGT-45262)
* Fixed an issue when opening a Single Page Application (SPA) page in the VEC and then going to [!UICONTROL Browse] mode caused the Back and Forward arrows to not function correctly. (TGT-45956)
* Fixed an issue that prevented some web pages from loading in the VEC. (TGT-45983)

## [!DNL Target] Standard/Premium 23.9.2 (September 12-14, 2023)

This release is available according to the following staggered schedule:

* **September 12**: Americas region
* **September 13**: Asia-Pacific (APAC) region
* **September 14**: Europe, Middle East, and Africa (EMEA) region

This release contains the following enhancements and fixes:

* Changed the [!DNL Analytics] API to the new [!DNL Analytics] API version 2.0. (TGT-45345)
* Fixed issues that impacted [!UICONTROL Automated Personalization] (AP) activities for some customers, including timely syncing the activity on the [!DNL Target] backend and delivering the expected experience in preview links. (TGT-46202)

## [!DNL Target] Standard/Premium 23.9.1 (September 6-11, 2023)

This release is available according to the following staggered schedule:

* **September 6**: Americas region
* **September 7**: Europe, Middle East, and Africa (EMEA) region
* **September 11**: Asia-Pacific (APAC) region

This release contains the following enhancements and fixes:

* Fixed an issue that caused inconsistent reporting data in the [!DNL Target] UI and the [!DNL Adobe Analytics] UI for [!UICONTROL Auto-Allocate] activities that use [!UICONTROL Analytics for Target] (A4T) as the reporting source. (TGT-46112)
* Increased the timeout for PUT calls to the Target Delivery API to 15 seconds to avoid timeout errors. (TGT-46091)
* Fixed an issue that prevented the URL from consistently updating when browsing through a Single Page Application (SPA) website. (TGT-45417)

## [!DNL Target] Standard/Premium 23.5.2 (Date to be determined)

This release contains the following enhancements and fixes:

* Enabled optimization criteria selection for [!DNL Adobe Analytics] metrics.
* Enabled sync of external audiences using sling jobs.
* Fixed an issue where SC report suites containing a dot character in the name were not supported.
* Enabled functionality to let customers delete and edit built-in audiences.

## [!DNL Target] Standard/Premium 23.5.3 (Date to be determined)

This release contains the following enhancements:

|Feature|Details|
|--- |--- |
|[!UICONTROL QA mode] for [!UICONTROL Automated Personalization] activities|[!DNL Adobe Target] [!UICONTROL QA mode] is now available for [!UICONTROL Automated Personalization] activities, replacing [!UICONTROL Preview links] functionality.<P>For more information, see [Activity QA](/help/main/c-activities/c-activity-qa/activity-qa.md).|

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
