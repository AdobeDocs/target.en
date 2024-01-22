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

## Deprecation of iPad and iPhone from Browser audience attribute (April 30, 2024)

|Deprecation|Details|
|--- |--- |
|[!DNL iPad] and [!DNL iPhone] to be deprecated from the [Browser attribute](/help/main/c-target/c-audiences/c-target-rules/browser.md) used when creating audiences.<p>Deprecation date:<P>April 30, 2024|[!DNL Adobe Target] lets you [target on any of several category attributes](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), including users who use a specific [browser or browser options](/help/main/c-target/c-audiences/c-target-rules/browser.md) when they visit your page.<P><B>Starting April 30, 2024, iPad and iPhone will be removed from the available [!UICONTROL Browser] type drop-down list when creating categories for audiences.</b><P>If you have audiences that target iPads or iPhones using the [!UICONTROL Browser] attribute, you must change these settings before April 30, 2024 to ensure that these audiences continue to function as expected.<p>For examples of alternate settings, see [Deprecation of iPad and iPhone from Browser audience attribute (April 30, 2024)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation).|

## [!DNL Target] Standard/Premium 24.1.1 (January 22, 23, & 25, 2024)

This release is scheduled for the following days:

* **January 22**: Europe, Middle East, and Africa (EMEA) region
* **January 23**: Asia-Pacific (APAC) region
* **January 25**: Americas region

This release contains the following enhancements and fixes:

* [!UICONTROL Analytics for Target] (A4T) activities with revenue goal metrics did not display "Revenue" as the column name and the revenue metric did not display in ($) format in reporting. This was a cosmetic issue that has been remedied. (TGT-46995)
* Fixed an issue that caused reporting date intervals to not work correctly. (TGT-47396)
* Fixed an issue that caused the incorrect status to display on the [!UICONTROL All Activities] page after customers activated or deactivated an activity using the [!UICONTROL More Actions] icon. (TGT-47367)
* Fixed an issue that caused the [!UICONTROL Important Attributes] report to not display for a single customer. (TGT-47272)
* Fixed an issue that caused an "Invalid payload" message to display when a single customer tried to enable "Require Authentication." (TGT-47195)
* Updated numerous localized strings in the [!DNL Target] UI.

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
