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

## [!DNL Target Standard/Premium] 25.4.4 (April 17, 2025)

This release includes the following fixes and updates:

* Added an error message to guide users on resolving duplicate options in an activity. (TGT-51927)
* Fixed an issue where `ClickTrack` selectors were not removed when deleting pages or experiences with redirect offers. (TGT-51952)
* Fixed an issue caused by allowing empty `ClickTrack` selectors. [!DNL Target] now requires that the selector field must not be blank. (TGT-52107)
* Fixed an issue that incorrectly allowed metrics with duplicate names. Metrics now require unique names. (TGT-52201)
* Fixed an issue where audience definitions were not visible when editing offer-level targeting in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52148)
* Fixed an issue that prevented customers with [!UICONTROL Editor] rights from saving activities. (TGT-52227)
* `OptionLocalIDs` no longer increment incorrectly when the option remains unchanged. (TGT-52139)
* Fixed an issue that caused an "Invalid `optionLocalIds`" message when trying to create an activity. (TGT-52154)
* Discrepancies between `OptionLocalIDs` defined for an activity and those used to define experiences have been fixed. (TGT-52215)
* Fixed an issue that caused a validation failure that occurred when trying to create an A/B activity. (TGT-51923)

## [!DNL Target Standard/Premium] 25.4.3 (April 11, 2025)

This release includes the following fixes and updates:

* Fixed an error that prevented customers from opening the audience information pop-up for certain [!UICONTROL Experience Targeting] (XT) activities. (TGT-52049)
* Fixed an issue where the audience setting reverted to "[!UICONTROL All Visitors]" following changes made in the [!UICONTROL Visual Experience Composer] (VEC). (TGT-52132)
* Fixed an issue where audience refinements were not displayed for specific activities (TGT-52057) 
* Fixed an issue that prevented customers from inserting an [!UICONTROL Experience Fragment] in the default workspace. (TGT-52073)
* Fixed an issue where an offer showed as "Content not found" and did not display on the [!UICONTROL Offers] page for an [!UICONTROL Automated Personalization] (AP) activity. (TGT-52150)
* Added the ability to allow duplicate audiences within an activity. (TGT-51200)
* Fixed an issue where the wrong mbox name displayed on the [!UICONTROL Goals & Settings] page for an XT activity after editing. (TGT-52026)
* Fixed an issue where `defaultContent` displayed in options despite not being in `experiences/optionLocations`. (TGT-52036)
* Fixed an issue to ensure that empty strings are not converted to null values. (TGT-52037)
* Fixed an issue requiring customers to reconfigure the [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] on the [!UICONTROL Goals & Settings] page after edits. (TGT-52071)
* Fixed an issue where an activity with no page-delivery rules displayed multiple rules on the [!UICONTROL Overview] page. (TGT-52084)
* Added an error message for users attempting to save an offer with characters outside the basic multilingual plane, such as emojis. (TGT-52105)
* Fixed an issue where opening an activity triggered the error message: "This Activity is using one or more audiences deleted at source." (TGT-52120)
* Fixed an issue where ClickTrack metrics were not displayed in the updated [!UICONTROL Visual Experience Composer] (VEC) during editing. (TGT-52152)
* Fixed an issue where a URL with a query parameter as the activity location did not display the query parameter on the activity's [!UICONTROL Overview] page. (TGT-51635)
* Fixed an issue that prevented the entire experience URL from displaying in [!UICONTROL Browse mode] within the [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* Fixed an issue where editing an activity caused page delivery to add a "/" to the end of the URL, rendering it invalid. (TGT-52114)
* Fixed an issue where the [!UICONTROL Activity QA] link in the [!UICONTROL Form-Based Experience Composer] incorrectly redirected to the [!DNL Adobe Experience Cloud] homepage. (TGT-52055)
* Fixed an issue where additional pages added to the [!UICONTROL A/B Test] activity were not retained after saving and reopening. (TGT-51994)
* Fixed an issue that prevented customers from deleting styles in the inline style section. (TGT-52070)
* Restored access to [audience definition cards](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) in the [!UICONTROL Activity QA] dialog box, similar to the legacy UI. (TGT-52056)
* The updated UI did not save pages or audiences without modifications. If customers added new pages or audiences to an activity but make no changes to them, [!DNL Target] discarded the unmodified audiences upon saving. Notifications have added in relevant places to inform users of this behavior. (TGT-52104)

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
