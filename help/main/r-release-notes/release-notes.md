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

# [!DNL Target Standard/Premium] 25.3.5 (March 11, 2025)

This release includes the following fixes and updates:

* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) where breadcrumbs were not always displayed at the bottom of the editor, causing difficulties in precisely selecting elements. (TGT-51844)
* Resolved an issue that prevented users from changing offers in the [!UICONTROL Modifications] panel. (TGT-51800)
* Resolved an issue where actions were incorrectly displayed in the left panel for experiences and audiences, including in [!UICONTROL ClickTrack] mode. (TGT-51895)
* Resolved an issue where [!UICONTROL ClickTrack] selectors were not applied to the correct audience page. (TGT-51871)

## [!DNL Target Standard/Premium] 25.3.4 (March 7, 2025)

This release includes the following fixes and updates:

* Resolved an issue where activity-only audiences were not visible in the [!UICONTROL Audiences] panel, preventing their editing or reuse. (TGT-51860)
* Fixed an issue that blocked [!DNL Target Standard] customers from creating activities using [!UICONTROL Analytics for Target] (A4T) reporting. (TGT-51854)
* Fixed an issue that excluded local ID counters from the payload during batch create and edit operations. (TGT-51867)

## [!DNL Target Standard/Premium] 25.3.2 (March 6, 2025)

This release includes the following fixes and updates:

* Fixed an issue where copying an activity with an activity-only audience failed to create a new activity, mistakenly using the original activity's audience instead. (TGT-51855)
* Fixed an issue that prevented editing of [!UICONTROL Experience Targeting] (XT) activities with activity-only audiences. (TGT-51846)
* Fixed an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to apply modifications to an experience correctly on the first edit. (TGT-51843)
* Fixed an issue that triggered an 'ID' error when clicking on certain elements within the VEC. (TGT-51814)
* Updated error handling in the VEC during activity creation. (TGT-51759)
* Fixed an issue where a missing view in the [!UICONTROL Modifications] panel caused an 'invalid user input' error when saving the activity. (TGT-51827)
* Fixed an issue that prevented the creation of recommendations criteria. (TGT-51834)
* Added a confirmation message before redirecting to a different URL. (TGT-51703)
* Fixed issues with GraphQL integration tests within offers and folders. (TGT-51839)

## [!DNL Target Standard/Premium] 25.3.1 (March 3, 2025)

This release includes the following fixes and updates:

* A combined audience can include subgroups, each containing multiple audiences. This release fixed an issue that prevented subgroup audiences from displaying in the [!UICONTROL Rules] dialog box. (TGT-51813)
* Resolved an issue where some experience audiences were replaced with [!UICONTROL All Visitors] when opening older activities. (TGT-51812)
* Resolved an issue that prevented editing activities with activity-only audiences. (TGT-51807)
* Resolved an issue that prevented editing page head modifications in the updated [!DNL Target] UI. (TGT-51797)
* Resolved a null error that occurred when duplicating an experience, deleting another experience, and then trying to save the activity. (TGT-51796)
* Resolved an issue that prevented audience exclusion rules from displaying in the audience's info panel during the [!UICONTROL Targeting] step of creating activities. (TGT-51579)
* Updated error messages localized in Korean. (TGT-51701 & TGT-51699)

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
