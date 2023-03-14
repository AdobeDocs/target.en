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

>[!NOTE]
>
>Due to issues that have since been fixed, the "Optimized A4T metrics for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]" feature that was released on March 8 & 9 has been temporarily removed. After further internal testing, the feature will be released again in the next few weeks.

This release contains the following fixes:

* Updates for custom web components authoring with the [!UICONTROL Visual Experience Composer] (VEC):

  * Fixed Shadow DOM elements selection in the VEC by improving the authoring process so there is no dependency on the [!DNL Target] implementation type when authoring the shadow root. Now, selecting Shadow DOM elements in the VEC should work for any website.
  * Fixed an issue that prevented loading HTML elements using #Shadow DOM in the VEC. (TGT-35801)
  * Fixed VEC issues with SPA websites using ShadowDOM. (TGT-43169)
  * Fixed an issue with the Optimization Goal: "clicked an element" that did not properly identify the CSS selector in ShadowDOM.

>[!NOTE]
>
>To ensure delivery of the changes authored in the VEC, ensure that you are using a [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js)) with a version greater than 2.8.

**Known issue**: Click-tracking on a shadow root element when using [!DNL Adobe Experience Platform Web SDK] is not working correctly. (TNT-47012)

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
