---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates,current updates
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

## [!DNL Target Standard/Premium] 25.5.1 (May 5, 2025)

This release includes the following fixes and updates:

* Fixed an issue preventing audience refinements from displaying for certain activities in the updated UI. (TGT-52057)
* Fixed an issue that prevented the use of combined audiences in activities. (TGT-52346)
* Fixed an issue that prevented the creation of a new activity in a non-default workspace using an activity-only audience from the same workspace. (TGE-52349)
* Fixed an issue that caused activity-only audiences to disappear from the updated UI after creating and selecting a new audience. (TGT=52091)
* Fixed an issue that prevented the use of duplicate audiences in activities. (TGT-51200 & TGT-52057)
* Fixed an issue that caused audience refinements and activity audiences to be reversed in the updated UI. (TGT-52158)
* Fixed an issue that prevented the creation of a new activity due to the user input error: "non-default workspace not allowed for this user." (TGT-52267)
* Fixed an issue that prevented offers from displaying in the updated UI for both default and non-default workspaces. [!DNL Target] now displays offers from both workspaces. (TGT-52339)
* Fixed an issue where [!DNL Target] did not warn customers when editing an activity and changing a modified website element. (TGT-52100)
* Fixed an issue where editing an offer with ad-hoc offers created a new offer instead of updating the existing one. (TGT-52135)
* Fixed Fixed an issue that caused an invalid payload error when moving offers to folders. (TGT-52325)
* Fixed Fixed an issue that caused an user input error when moving offers to folders. (TGT-52296)
* Added an `audienceMetadata` field for each activity, and ensured it is read and updated when editing the activity. (TGT-51004)

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
