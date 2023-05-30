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

## [!DNL Target] Standard/Premium 23.5.2 (May 31, 2023)

This release contains the following enhancements and fixes:

|Feature|Details|
|--- |--- |
|Real-Time CDP Profile Attributes shared with [!DNL Target]|[!UICONTROL Real-Time CDP Profile Attributes] can be shared with [!DNL Target] for use in HTML and JSON offers.<P>For more information, see [Share Real-Time CDP Profile Attributes with [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes).|

* Fixed an issue that caused a blank page to display while generating a Profile API authorization token. (TGT-45387 & TGT-45423)
* Fixed an issue that prevented an image from displaying in the [!UICONTROL Create Design] panel if the image name contains GB 18030 characters. (TGT-44614)
* Fixed an issue in which some GB 18030 symbol characters were incorrectly escaped in Text/HTML in experiences. (TGT-44600)
* Fixed an issue that caused reports for [!UICONTROL Auto Personalization] activities to freeze during analysis. (TGT-44820)
* Fixed an issue that prevented searching for an activity on the [!UICONTROL Activity] page if the activity name contains a square bracket ( [ or ] ). (TGT-44777)
* Fixed an issue that prevented an activity from syncing if the activity's objective contains special characters. (TGT-44982)
* Fixed an issue that caused no activities to display in the [!DNL Target] UI for the Default workspace for certain customers. (TGT-45286)
* Updated the behavior of the "Disallow Duplicates" flag. Excluded repeating offers flags are updated to allow repeating offers if they are the default content offer (for APIs v3, v4) and allow duplicate options if the options reference the default content offer and have no templates defined. (TNT-46617)
* Fixed an issue in which a query parameter was added to a URL that prevented the page from loading in the [!UICONTROL Visual Experience Composer] (VEC). (TGT-44873)
* Made various localization fixes throughout the [!DNL Target] UI.

## [!DNL Target] Standard/Premium 23.5.1 (May 23-25, 2023)

This release will be available according to the following staggered schedule:

May 23: Europe, Middle East, and Africa (EMEA) region
May 24: Asia-Pacific (APAC) region
May 25: Americas region

This release contains the following new enhancements and fixes:

* Fixed an issue that prevented certain customers from creating audiences with visitor profiles using "greater than" or "less than" operators. (TGT-45271)
* Made various localization fixes throughout the [!DNL Target] UI.
* Updated the Target UI in various places for an upcoming UI refresh (changes are behind a feature flag until the updates are released). 

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
