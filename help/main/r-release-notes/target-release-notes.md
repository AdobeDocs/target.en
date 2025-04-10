---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: April 10, 2025**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target permissions update (April 22, 2025)

This future update enhances organizational control over [!DNL Target] instance configurations, preventing accidental updates that could affect activity delivery across various testing and personalization teams.

Effective April 22, 2025, only [!UICONTROL Product] and [!UICONTROL Solutions] admins will be able to update settings in the [!UICONTROL Administration] sections, regardless of their roles in [!DNL Target] workspaces. Users without this permission will have read-only access to the [!UICONTROL Administration] sections.

For more information, see [Administer Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.4 (April 15, 2025)

This release includes the following fixes and updates:

* Added an error message to guide users on resolving duplicate options in an activity. (TGT-51927)
* Fixed an issue where ClickTrack selectors were not removed when deleting pages or experiences with redirect offers. (TGT-51952)
* Fixed an issue where [!DNL Target] failed to correctly detect a "#" character in the activity URL. (TGT-52093)
* Fixed an issue where audience definitions were not visible when editing offer-level targeting in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52148)
* Fixed an issue where audience refinements and activity targeting audiences were reversed in the UI. (TGT-52158)

## [!DNL Target Standard/Premium] 25.4.3 (April 10, 2025)

This release includes the following fixes and updates:

* Fixed an error that prevented customers from opening the audience information pop-up for certain [!UICONTROL Experience Targeting] (XT) activities. (TGT-52049)
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

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
