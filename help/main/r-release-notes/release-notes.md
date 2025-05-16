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

## [!DNL Adobe Target] [!DNL AI Assistant] release (May 16, 2025)

We are thrilled to announce the launch of the [!DNL AI Assistant] in [!DNL Adobe Target]! This powerful user interface feature is designed to help you navigate and understand [!DNL Target] concepts with ease. Available across multiple products in [!DNL Adobe Experience Cloud], including [!DNL Target], [!DNL AI Assistant] is here to revolutionize your experience.

[!DNL AI Assistant] in [!UICONTROL Target] is a conversational tool that you can use to accelerate your workflows with [!DNL Experience Platform] applications and services. Use [!DNL AI Assistant] to boost your overall productivity and amplify your understanding of product knowledge

In [!DNL Target], the first phase of [!DNL AI Assistant] provides invaluable product knowledge grounded in [!DNL Experience League] documentation. Whether you're setting up a profile script, troubleshooting errors, or considering an upgrade to the AEP Web SDK, [!DNL AI Assistant] has you covered.

For more information, see [Adobe Experience Platform AI Assistant overview](/help/main/c-intro/ai-assistant.md).

## [!DNL Target Standard/Premium] 25.5.2 (May 8, 2025)

This release includes the following fixes and updates:

* [!DNL Target] users with [!UICONTROL Product Administrator] and [!UICONTROL System Administrator] rights can now edit all settings on the [!UICONTROL Administration] pages, regardless of their role in [!DNL Target]. Users without these permissions have read-only access to these settings. This update ensures stricter access control over [Administration settings](/help/main/administrating-target/administrating-target.md). (TGT-48179)
* Fixed a caching issue that prevented saving activity [Site Preferences](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings). (TGT-52213) 
* Fixed an issue where customers couldn't enable selection by ID and class in the [!UICONTROL Site Preferences] section after loading the site in the VEC. The [!UICONTROL Site Preferences] setting automatically reverted to disabled even after being enabled. (TGT-52207)
* Fixed an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to display the correct page when [page delivery](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) URLs ended with a forward slash (/). (TGT-52237)
* Fixed an issue that prevented the removal of custom code modifications when changing experiences. (TGT-52240)
* Fixed an issue where HTML modifications in the VEC overlaid existing page elements. (TGT-52265)
* Fixed an issue that prevented editing custom code in the updated VEC due to the existing custom code not being visible in the editor. (TGT-52272)
* Fixed an issue that caused a "Duplicate names are not allowed" error message when saving a Recommendations activity. (TGT-52318)
* Fixed an issue in the updated VEC that prevented customers from editing text elements or removing container objects. (TGT-52348)
* Fixed an issue that blocked [!DNL Customer Journey Analytics] from displaying correctly on an activity [!UICONTROL Overview] page. (TGT-52359)
* Fixed an issue that prevented reporting groups from persisting in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52368)
* Fixed an issue that prevented saving activities that include offer decisioning. (TGT-52390)
* Fixed an issue where the default offer was selected, but other offer content displayed in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Multivariate Test] (MVT) activities. (TGT-52372)
* Fixed GET permissions logic to check with OR between full org access and specific org + user access. (TGT-52374)
* Fixed an issue where audience names did not display after selecting an audience for [!UICONTROL Managed Content] and [!UICONTROL Reporting Audiences], even though [!UICONTROL Show Only Selected] was enabled. (TGT-52393)

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
