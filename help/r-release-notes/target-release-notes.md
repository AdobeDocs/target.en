---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease
description: Learn about the new features, enhancements, and fixes included in the upcoming release of Adobe Target, including SDKs, APIs, and JavaScript libraries.
title: What New Features Are Included in the Upcoming Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# Target release notes (prerelease)

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: June 24, 2021**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages could be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: As of March 31, 2021, [!DNL Adobe Target] no longer supports the mbox.js library. Post March 31, 2021, all calls made from mbox.js gracefully fail and impact your pages that have [!DNL Target] activities running by serving default content.
>
>To avoid any potential issues with your sites, migrate to the most recent version of the new [!DNL Adobe Experience Platform Web SDK] or the at.js JavaScript library. For more information, see [Overview: implement Target for client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.6.1 (June 30, 2021)

This release contains the following new features and enhancements. The issue numbers in parentheses are for internal [!DNL Adobe] use.

|Feature|Details|
| --- | --- |
|[!UICONTROL Analytics for Target] (A4T)|Clicking the "[!UICONTROL View in Analytics]" link on the [!UICONTROL Reports] page from an activity that uses [!DNL Analytics] as the reporting source (A4T), [!DNL Analysis Workspace] now opens. Previously, the link opened [!DNL Analytics] reporting. (TGT-36959)|
|![Premium](/help/assets/premium.png) [!DNL Recommendations]|The following enhancements apply to [!DNL Recommendations] popularity algorithms:<ul><li>A new six-hour "lookback window" (data range) option is available for all popularity (Most Viewed/Top Sellers) algorithms when [!DNL Target] is the behavioral data source. (This lookback window is *not* available when [!DNL Adobe Analytics] is the behavioral data source.)</li><li>When selected, the following algorithms run approximately every three hours (instead of every 12 hours).<ul><li>Most viewed</li><li>Most purchased</li><li>Most viewed by category</li><li>Most purchased by category</li><li>Most viewed by custom attribute (using groupBy feature)</li><li>Most purchased by custom attribute (using groupBy feature)</li></ul></ul>Release date to be announced. (TOP-1086)|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
