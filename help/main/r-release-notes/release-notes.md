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

## Target permissions update (April 22, 2025)

This future update enhances organizational control over [!DNL Target] instance configurations, preventing accidental updates that could affect activity delivery across various testing and personalization teams.

Effective April 22, 2025, only Product and Solutions Admins will be able to update settings in the [!UICONTROL Administration] sections, regardless of their roles in [!DNL Target] workspaces. Users without this permission will have read-only access to the [!UICONTROL Administration] sections.

For more information, see [Administer Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.1 (April 2, 2025)

This release includes the following fixes and updates:

* Fixed an issue that caused experience audiences to disappear from activities. (TGT-52003)
* Fixed an issue that caused unexpected elements during delivery. (TGT-52011)
* Fixed an issue that blocked customers from viewing the audience in the targeting graph on the Ove[!UICONTROL r]view page and during activity editing. (TGT-52050)
* Fixed an issue that prevented customers from reordering experiences in order of priority in [!UICONTROL Experience Targeting] (XT) activities. (TGT-52054)
* Fixed an issue that caused incorrect rendering when undoing text style changes. (TGT-51876)
* Fixed an issue that when modifying a redirect offer, [!DNL Target] also removes any [!UICONTROL ClickTrack] selectors associated with that offer. (TGT-51936)
* Fixed an issue that caused [!DNL Target] to incorrectly save the selector when cancelling [!UICONTROL ClickTrack]. (TGT-51937)
* Fixed an issue that triggered an invalid name error after opening and closing the mbox picker on the [!UICONTROL Goals & Settings] page without making any changes. (TGT-51983)
* Fixed an issue that blocked editing ad hoc offers created in the legacy [!DNL Target] UI. (TGT-51984)
* Fixed an issue that blocked editing activities that have ad-hoc offers that contain custom code. (TGT-51995)
* Fixed an issue that caused exclusion rules to display as inclusion rules when editing combined audience definitions. (TGT-51999)
* Fixed an issue that prevented custom code from displaying correctly during experience editing. (TGT-52005)
* Fixed an issue that made the [!UICONTROL Insert Before] option unavailable for inserting content before the navigation bar. (TGT-52031)
* Fixed an issue that prevented correct highlighting of the default experience in reporting. (TGT-51716)
* Fixed an issue that triggered a `default message [Invalid optionLocalIds: xx]]` message when creating an activity. (TGT-52038)

## at.js version version 2.11.8 (March 31, 2025)

* Resolved CodeQL-identified vulnerability in string suffix validation to prevent edge cases during resize and move operations. (TNT-51516)

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
