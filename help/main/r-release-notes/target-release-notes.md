---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease
description: Learn about the new features, enhancements, and fixes included in the upcoming release of Adobe Target, including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# Target release notes (prerelease)

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: March 14, 2023**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages could be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target] Standard/Premium 22.15.1 (March 8 & 9, 2023)

This release will be available according to the following staggered schedule:

* **March 8**: Americas region
* **March 9**: Europe, Middle East, and Africa (EMEA) region
* **March 9**: Asia-Pacific (APAC) region

This release contains the following new features, enhancements, and fixes:

|Feature|Details|
| --- | --- |
|Optimized A4T metrics for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]|[!DNL Target] lets you choose metrics based on binomial events or metrics based on continuous events when using [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities.<P>Be aware of the following change in supported metrics:<ul><li>[!DNL Target] preserved the previous behavior for existing activities until (DATE TO BE DETERMINED). After this date, activities using non-supported metrics will be discontinued to force existing activity migration to the new behavior.</li></ul>For more information, see [Supported goal metrics](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported) in *A4T support for Auto-Allocate and Auto-Target activities*.|
|[!UICONTROL Auto-Allocate] using [!UICONTROL Analytics for Target] (A4T)|New tutorial:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul>|
|[!UICONTROL Auto-Target] using [!UICONTROL Analytics for Target] (A4T)|New tutorial:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Target] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul>|

This release contains the following fixes:

* Updates for custom web components authoring with the [!UICONTROL Visual Experience Composer] (VEC):

  * Fixed Shadow DOM elements selection in the VEC by improving the authoring process so there is no dependency on the [!DNL Target] implementation type when authoring the shadow root. Now, selecting Shadow DOM elements in the VEC should work for any website.

  **NOTE**: To ensure delivery of the changes authored in the VEC, ensure that you are using a Target SDK (at.js or [!DNL Adobe Experience Platform Web SDK]) with a version greater than 2.8.

* Fixed an issue that prevented loading HTML elements using #Shadow DOM in the VEC. (TGT-35801)
* Fixed VEC issues with SPA websites using ShadowDOM. (TGT-43169)
* Fixed an issue with the Optimization Goal: "clicked an element" that did not properly identify the CSS selector in ShadowDOM.
 
**Known issue**: Click-tracking on a shadow root element when using alloy.js is not working correctly. (TNT-47012)

## at.js version 2.10.2 (March 7, 2023)

* Fixed an issue that caused the `trackEvent` function to always return an error.

For information about all at.js releases, see [at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|


## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
