---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: March 11, 2025**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.3.5 (March 11, 2025)

This release includes the following fixes and updates:

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

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
