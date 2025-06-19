---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: June 19, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.6.3 (June 20, 2025)

This release includes the following fixes and updates:

* Added the [!UICONTROL Rearrange] option to the updated [!UICONTROL Visual Experience Composer] (VEC) UI to align with functionality available in the legacy VEC. (TGT-46957)
* Fixed an issue where copying an activity from one workspace to another workspace triggered errors such as "must not be null" or "Something went wrong." (TGT-52474)
* Fixed an issue where [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes] reports were not generated for certain activities. (TNT-52904)
* Fixed an issue in the updated VEC where default content handling in [!UICONTROL Automated Personalization] (AP) activities did not match the legacy UI. The system now automatically adds a default `optionGroup` named "Default Content" with `optionGroupLocalId = 0` when no group is explicitly added. This group includes the default option (for example, `optionLocalId: 0`). If the default content is removed, the corresponding option group is also removed. (TGT-52651)
* Fixed an issue in [!UICONTROL Multivariate Test] (MVT) activities where reusing an `experienceLocalId` from previously removed experiences was incorrectly disallowed. (TNT-52672)
* Fixed an issue where URLs in activity locations failed to display query parameters due to invalid characters, such as slashes (/). (TNT52845)
* Improved the validation error message for [!DNL A/B Test] activity updates via the backend API. When duplicate location names are present, the message now clearly states: "Duplicate names are not allowed" for `locations.selectors`. (TGT-52589)
* Fixed an error that occurred when updating a live [!UICONTROL Recommendations] activity due to an unrecognized property in the request payload. The system now properly handles the "Invalid JSON. Unrecognized property name" error. (TNT52723)
* Fixed a backend validation error that caused a "400 Bad Request" error when saving a [!UICONTROL Recommendations] activity. (TNT-52716)
* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] where hovering over an mbox with special characters in the [!UICONTROL Location] drop-down caused the editor to go blank and triggered a "Failed to execute 'querySelector' on 'Element'." error. (TGT-52717)
* Improved feed-status accuracy with a new "PARTIALLY_IMPORTED" indicator. Previously, feeds were marked as "success" even when not all rows in a file were imported, which was misleading. 
* Fixed an error where, after migrating to AP V2, certain API calls to `/admin/rest/ui/v1/campaigns` returned client-side errors (HTTP 4xx). (TGT-52721)

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
