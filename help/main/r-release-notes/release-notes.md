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

## [!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics] (May 8, 2024)

The integration between [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} and [!DNL Target] provides powerful analysis and timesaving tools for your optimization program.

The primary benefits of using [!DNL Customer Journey Analytics] as the reporting source for [!DNL Target] are:

* Marketers can dynamically apply [!DNL Customer Journey Analytics] success metrics to [!DNL Target] activity reports at any time. It is not required to specify everything before running the activity. 
* Marketers can take advantage of [!DNL Customer Journey Analytics] features, such as the [Experimentation Panel](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, to further analyze their website personalization. 
* Marketers can have a single source of reporting for [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/reporting/cja-ajo){target=_blank} and [!DNL Target]. Both personalization products can be connected to [!DNL Customer Journey Analytics] for a more holistic view of your web personalization. 

For more information, see [Target reporting in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

## [!UICONTROL Visual Experience Composer] helper extension (April 23, 2024)

The legacy [!DNL Target] Visual Experience Composer helper extension was created using Manifest V2. [!DNL Google] announced that it will no longer allow extensions created using Manifest V2 starting in June 2024. For more information, see [[!UICONTROL Visual Experience Composer] helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] recommends that customers move to the newer [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) as soon as feasible.

## Updates for `Browser:iPad` and `Browser:iPhone` in [!UICONTROL Browser] audience attributes (April 30, 2024)

|Updates|Details|
|--- |--- |
|[!UICONTROL Browser:iPad] and [!UICONTROL Browser:iPhone] updated in [Browser attributes](/help/main/c-target/c-audiences/c-target-rules/browser.md) used when creating audiences.|[!DNL Adobe Target] lets you [target on any of several category attributes](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), including visitors who use a specific [browser or browser options](/help/main/c-target/c-audiences/c-target-rules/browser.md) when they visit your page.<P>Starting with the [!DNL Target] Standard/Premium 24.3.1 (March 4-6, 2024), built-in audiences created using the Target UI, such as `Browser:iPad` and `Browser:iPhone` will be updated to perform proper targeting for [!DNL iPad] and [!DNL iPhone] using `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` and `profile.mobile.isTablet`.<P>This update requires no action on the customers' side.<p><B>Important</b>: For customers to perform proper targeting for [!DNL iPad] and [!DNL iPhone] in profile scripts (and JavaScript segments), manual changes must be made by the customer by **April 30, 2024**. For examples of alternate settings that must be manually changed, see [Updates for [!DNL iPad] and [!DNL iPhone] in [!UICONTROL Browser] audience attributes](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates).|

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|
     
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
