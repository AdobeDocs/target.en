---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: June 27, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.6.4 (June 26, 2025)

This release includes the following fixes and updates:

* Added the [!UICONTROL Rearrange] option to the updated [!UICONTROL Visual Experience Composer] (VEC) UI to align with functionality available in the legacy VEC. (TGT-46957 & TGT-52876)
* Fixed an issue where modifications made to variant experiences (for example, Experience B) in an [!UICONTROL A/B Test] activity were not being retained. After switching between experiences, the changes to the variant would disappear. This issue did not affect the Control experience. (TGT-52664)
* Fixed an issue where certain customers were unable to create or save activities, while others could perform the same actions without issue. The problem was inconsistent across accounts.(TGT-52842)
* Fixed an issue where in the updated VEC, users were unable to move modifications to the [!UICONTROL Page Load event], a capability that existed in the legacy UI. (TGT-52617)
* Fixed an issue in the updated UI where [!UICONTROL page load] events were not visible in [!DNL Target] when creating changes; updates only applied to views. (TGT-52604)
* Fixed an issue that prevented some activity modifications from displaying properly in the updated VEC. (TGT-52818)
* Fixed a null pointer exception that occurred when fetching reporting data for [!UICONTROL Automated Personalization] (AP) activities. (TGT-52362)
* Fixed an issue that prevented offer-level details from appearing in the .CSV file for [!UICONTROL Automated Personalization] (AP) activities. (TGT-52675)
* Fixed an issue when applying modifications in the updated VEC, changes initially appear correctly, including the expected [!UICONTROL Experience Fragment]. However, upon switching experiences or making additional edits, some modifications fail to apply due to selector issues. (TGT-52679)
* Fixed an issue where when a new activity was created by cloning an existing one, the QA links in the cloned activity incorrectly retained the page URLs from the original activity. (TGT-52775)
* Fixed an issue that unintentionally prevented [!UICONTROL On-device Decisioning] from being available in the updated VEC. (TGT-52371)
* Fixed an issue that prevented editing a product [!DNL Recommendations] activity. When attempting to access the VEC via the Target UI, an error appeared on the [!UICONTROL Overview] page, preventing any edits. (TGT-52823)
* Fixed an issue that prevented saving a [!DNL Recommendations] activity when experience names exceeded 50 characters. (TGT-52619)
* Fixed an issue where customers were unable to save a Recommendations activity after modifying the criteria in the new UI. The issue appears to be permission-related and does not affect all users with similar roles. (TGT-52816)
* Fixed an issue where users with the [!UICONTROL Editor] role were unable to edit a [!DNL Recommendations] activity. Attempting to change the design and save the activity resulted in a 403 Forbidden error, stating that the "[editor]" privilege was required, even though the user already had that role in the relevant workspace. (TGT-52836)

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
