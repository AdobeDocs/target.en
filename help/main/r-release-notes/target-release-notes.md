---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: April 17, 2025**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

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

## Target permissions update (April 22, 2025)

This future update enhances organizational control over [!DNL Target] instance configurations, preventing accidental updates that could affect activity delivery across various testing and personalization teams.

Effective April 22, 2025, only [!UICONTROL Product] and [!UICONTROL Solutions] admins will be able to update settings in the [!UICONTROL Administration] sections, regardless of their roles in [!DNL Target] workspaces. Users without this permission will have read-only access to the [!UICONTROL Administration] sections.

For more information, see [Administer Target](/help/main/administrating-target/start-target.md).

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
