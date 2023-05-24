---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease 
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: May 24, 2023**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target] Standard/Premium 23.5.2 (May 31, 2023)

This release contains the following enhancements and fixes:

* Fixed an issue that caused a blank page to display while generating a Profile API authorization token. (TGT-45387)
* Fixed an issue that prevented an image from displaying in the [!UICONTROL Create Design] panel if the image name contains GB 18030 characters. (TGT-44614)
* Fixed an issue that caused reports for [!UICONTROL Auto Personalization] activities to freeze during analysis. (TGT-44820)
* Fixed an issue that caused no activities to display in the Target UI for the Default workspace for certain customers. (TGT-45286)
* Updated the behavior of the "Disallow Duplicates" flag. Excluded repeating offers flags are updated to allow repeating offers if they are the default content offer (for APIs v3, v4) and allow duplicate options if the options reference the default content offer and have no templates defined. (TNT-46617)
* Fixed an issue in which a query parameter was added to a URL that prevented the page from loading in the Visual Experience Composer (VEC). (TGT-44873)
* Fixed an issue in which some characters were incorrectly escaped in Text/HTML in experiences. (TGT-44600)

## [!DNL Target] Standard/Premium 23.5.3 (Date to be determined)

This release contains the following enhancements:

|Feature|Details|
|--- |--- |
|[!UICONTROL QA mode] for [!UICONTROL Automated Personalization] activities|[!DNL Adobe Target] [!UICONTROL QA mode] is now available for [!UICONTROL Automated Personalization] activities, replacing [!UICONTROL Preview links] functionality.<P>For more information, see [Activity QA](/help/main/c-activities/c-activity-qa/activity-qa.md).|
|Real-Time CDP Profile Attributes shared with [!DNL Target]|[!UICONTROL Real-Time CDP Profile Attributes] can be shared with [!DNL Target] for use in HTML and JSON offers.<P>For more information, see [Share Real-Time CDP Profile Attributes with [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes).|

* Performance enhancements to disallow duplicates functionality (including reduction in load time) while [managing exclusions](/help/main/c-activities/t-automated-personalization/managing-exclusions.md#concept_4EF78013F80E48EFA024AE0274C9F037) in [!UICONTROL Automated Personalization] activities.

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
