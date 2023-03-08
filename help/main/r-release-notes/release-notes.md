---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
---
# [!DNL Target] release notes (current)

These release notes provide information about features, enhancements, and fixes for each [!DNL Adobe Target Standard] and [!DNL Target Premium] release. In addition, release notes for [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform changes are also included, when applicable.

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## [!DNL Target] Standard/Premium 22.15.1 (March 8 & 9, 2023)

This release will be available according to the following staggered schedule:

* **March 8**: Americas region
* **March 9**: Europe, Middle East, and Africa (EMEA) region
* **March 9**: Asia-Pacific (APAC) region

This release contains the following new features and enhancements:

|Feature|Details|
| --- | --- |
|Optimized A4T metrics for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]|[!DNL Target] lets you choose metrics based on binomial events or metrics based on continuous events when using [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities.<P>Be aware of the following time-sensitive change in supported metrics:<ul><li>[!DNL Target] preserved the previous behavior for existing activities until September 9, 2023. After this date, activities using non-supported metrics will be discontinued to force existing activity migration to the new behavior.</li></ul>For more information, see [Supported goal metrics](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported) in *A4T support for Auto-Allocate and Auto-Target activities*.|
|[!UICONTROL Auto-Allocate] using [!UICONTROL Analytics for Target] (A4T)|New tutorial:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul>|
|[!UICONTROL Auto-Target] using [!UICONTROL Analytics for Target] (A4T)|New tutorial:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Target] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul>|

## at.js version 2.10.2 (March 7, 2023)

* Fixed an issue that caused the `trackEvent` function to always return an error.

For information about all at.js releases, see [at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|Documentation changes|View detailed information about updates to this guide that are not included in these release notes.<br>For more information, see [Documentation Changes](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C).|
|Release notes for previous releases|View information about new features and enhancements in previous releases of Target Standard and Target Premium.<br>For more information, see [Release notes for previous releases](/help/main/r-release-notes/release-notes-for-previous-releases.md).|
|Adobe Experience Cloud release notes|View the latest release notes for the Adobe Experience Cloud solutions.<br>For more information, see [Experience Cloud Release Notes](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html).|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|Adobe Priority Product Update|To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)|
|Upcoming release notes|For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/main/r-release-notes/target-release-notes.md) page.|
