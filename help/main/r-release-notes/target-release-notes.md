---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease
description: Learn about the new features, enhancements, and fixes included in the upcoming release of Adobe Target, including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# Target release notes (prerelease)

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: March 27, 2023**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages could be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target] Standard/Premium 23.3.1 (March 28-30, 2023)

This release will be available according to the following staggered schedule:

* **March 28**: Europe, Middle East, and Africa (EMEA) region
* **March 29**: Asia-Pacific (APAC) region
* **March 30**: Americas region

This release contains the following new features, enhancements, and fixes:

|Feature|Details|
|--- |--- |
|AEM content fragments for headless personalization and experimentation|Use [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Content Fragments] in [!DNL Target] activities. Combine the ease-of-use and power of AEM with powerful Artificial Intelligence (AI) and Machine Learning (ML) capabilities in [!DNL Target] to test and personalize experiences at scale.|
|Optimized A4T metrics for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]<p>(Release date March 30, 2023)|[!DNL Target] lets you choose metrics based on binomial events or metrics based on continuous events when using [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities.<P>Be aware of the following change in supported metrics:<ul><li>[!DNL Target] preserved the previous behavior for existing activities until September 9, 2023. After this date, activities using non-supported metrics will be discontinued to force existing activity migration to the new behavior.</li></ul>|
|[!UICONTROL Auto-Allocate] using [!UICONTROL Analytics for Target] (A4T)|Updated tutorial:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul>|
|[!UICONTROL Auto-Target] using [!UICONTROL Analytics for Target] (A4T)|Updated tutorial:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Target] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul>|

* Enhanced audience and activity synchronization so that items created in [!DNL Adobe Experience Platform] and [!DNL Adobe Audience Manager] are available in the [!DNL Target] UI quicker. (TGT-44568)
* Made change to allow users to remove the [!UICONTROL Default URL] under [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer] > [!UICONTROL Default URL]. This change lets customers change the default URL back to an empty string, which was previously not possible after initial configuration. (TGT-44577)
* Removed restrictions that prevented customers from editing or deleting out-of-the box audiences (audiences with reserved names). (TGT-44655)
* Disabled the "[!UICONTROL Done]" option while loading spinners were visible in the [!DNL Target] UI when creating [combined audiences](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* Fixed the [!UICONTROL Language] link at the bottom of the [!UICONTROL Audiences] page so that it correctly links to the "[!UICONTROL Account communication preferences]" page. (TGT-43562)
* Resolved an issue that sometimes prevented customers from creating [!UICONTROL A/B Test] activities after selecting the [!UICONTROL Adobe Analytics] option under [!UICONTROL Administration] > [!UICONTROL Reporting] > [!UICONTROL Reporting Experience Cloud Solution]. (TGT-44844)
* Fixed an issue that prevented customers from viewing the last experience in a [!UICONTROL Multivariate Test] activity with many experiences from within the [!UICONTROL Visual Experience Composer] (VEC). The [DOM path](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) at the bottom of the VEC sometimes prevented customers from seeing the last experience. (TGT-44578)
* Fixed an issue that caused the Browse URL in the VEC to not reflect the current page that is visible in a normal browser session if the page requires authorization or invokes redirects. (TGT-44350)
* Fixed an issue that prevented customers from changing the [!UICONTROL Filter Incompatible Criteria] setting in [!UICONTROL Recommendations] > [!UICONTROL Settings]. (TGT-44398)
* Fixed an issue that caused POST requests to create new [!DNL Recommendations] feeds to fail when using [!UICONTROL Analytics Classifications] with report suites with dots in their names. (TGT-44598)
* Updated links in the [!DNL Target] UI to point to the new [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* Enhanced security to prevent Server-Side Request Forgery (SSRF) attempts in [!DNL Recommendations] feeds. (TGT-43769)
* Fixed an issue that prevented customers from viewing preview images in [!DNL Recommendations] designs if the image name contains [GB18030 characters](https://en.wikipedia.org/wiki/GB_18030){target=_blank}. (TGT-44614)
* Fixed an issue that caused some [GB18030 characters](https://en.wikipedia.org/wiki/GB_18030){target=_blank} to be escaped in the [!UICONTROL Modifications] panel while editing [!UICONTROL Text/HTML] on an activity's [!UICONTROL Experiences] page. (TGT-44600)
* Made various localization fixes throughout the [!DNL Target] UI.


## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|


## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
