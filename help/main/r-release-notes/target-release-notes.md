---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: April 2, 2025**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target permissions update (April 22, 2025)

This future update enhances organizational control over [!DNL Target] instance configurations, preventing accidental updates that could affect activity delivery across various testing and personalization teams.

Effective April 22, 2025, only [!UICONTROL Product] and [!UICONTROL Solutions] admins will be able to update settings in the [!UICONTROL Administration] sections, regardless of their roles in [!DNL Target] workspaces. Users without this permission will have read-only access to the [!UICONTROL Administration] sections.

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
