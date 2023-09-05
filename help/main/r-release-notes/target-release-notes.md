---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease 
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: September 4, 2023**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target] Standard/Premium 23.9.1 (September 6-11, 2023)

This release is available according to the following staggered schedule:

* **September 6**: Americas region
* **September 7**: Europe, Middle East, and Africa (EMEA) region
* **September 11**: Asia-Pacific (APAC) region

This release contains the following enhancements and fixes:

* Fixed an issue that caused inconsistent reporting data in the [!DNL Target] UI and the [!DNL Adobe Analytics] UI for [!UICONTROL Auto-Allocate] activities that use [!UICONTROL Analytics for Target] (A4T) as the reporting source. (TGT-46112)
* Increased the timeout for PUT calls to the Target Delivery API to 15 seconds to avoid timeout errors. (TGT-46091)
* Fixed an issue that displayed the incorrect report name when switching between the [!UICONTROL Table View] and the [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes] reports. (TGT-46040)
* Enhanced the [!UICONTROL Visual Experience Composer] (VEC) to support Lightning DOM (Web Components). (TGT-45422)
* Fixed an issue that caused VEC actions to be applied in the incorrect order. In some cases, the VEC applied some modifications asynchronously and adding extra modifications to an element caused errors if that element displays after an [!UICONTROL Insert] action. (TGT-45983)
* Fixed an issue when opening a Single Page Application (SPA) page in the VEC and then going to Browse mode caused the Back and Forward arrows to not function correctly. (TGT-45956)
* Fixed an issue that prevented the URL from consistently updating when browsing through a Single Page Application (SPA) website. (TGT-45417)

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
