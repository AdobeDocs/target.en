---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates 
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
---
# [!DNL Target] release notes (current)

These release notes provide information about features, enhancements, and fixes for each [!DNL Adobe Target Standard] and [!DNL Target Premium] release. In addition, release notes for [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform changes are also included, when applicable.

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## [!DNL Target] Standard/Premium 23.3.1 (March 28-30, 2023)

This release is available according to the following staggered schedule:

* **March 28**: Europe, Middle East, and Africa (EMEA) region
* **March 29**: Asia-Pacific (APAC) region
* **March 30**: Americas region

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

## at.js version 2.10.2 (March 7, 2023)

* Fixed an issue that caused the `trackEvent` function to always return an error.

For information about all at.js releases, see [at.js version details](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} in the [Adobe Target Developer Guide](https://experienceleague.corp.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|
     
## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|[Documentation Changes](/help/main/r-release-notes/doc-change.md)|View detailed information about updates to this guide that are not included in these release notes.|
|[Release notes for previous releases](/help/main/r-release-notes/release-notes-for-previous-releases.md).|View information about new features and enhancements in previous releases of Target Standard and Target Premium.|
|[Adobe Experience Cloud Release Notes](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank}|View the latest release notes for the Adobe Experience Cloud solutions.|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|[Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank}|Receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions.|
|[Target Release Notes - Prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank}|Information about the current month's Target releases, including prerelease information.|
