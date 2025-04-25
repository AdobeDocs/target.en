---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: April 24, 2025**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.4.5 (April 25, 2025)

This release includes the following fixes and updates:

* Fixed an issue that caused discrepancies in audience listings between the [!UICONTROL Activity] settings page and the [!UICONTROL Reporting] overview page. (TGT-52203)
* Fixed an issue that prevented adding a new page to an activity due to an invalid user input error. (TGT-52263)
* Fixed an issue where recommendations did not display on the customer's website after activating the [!DNL Recommendations] activity. (TGT-52164)
* Fixed an issue that caused `OptionLocalIDs` to incorrectly increment when the option remains unchanged. (TGT-52187)
* Fixed an issue so that downloaded reporting files correctly show data present in the reporting UI. (TGT-52068)
* Fixed an issue so that batch operations no longer fail after adding page-delivery rules. (TGT-52097)
* Fixed an issue that caused [!DNL Target] to trim all query parameters from the website's URL. (TGT-52100)
* Resolved a console error that prevented customers from creating activities in both the legacy and updated Target UI. (TGT-52181)
* Fixed an issue that blocked customers from adding new pages, causing an invalid user input error. (TGT-52258)
* Fixed an issue that caused modifications to disappear after adding additional pages then navigating back to the [!UICONTROL Experiences] tab. (TGT-52264)
* Fixed an issue that blocked customers from changing the audience in an [!UICONTROL Experience Targeting] (XT) activity. (TGT-52191)
* Fixed an error that prevented editing of an XT activity due to an unsupported UI rule. (TGT-52273)
* Fixed an issue where activity modifications were not displayed in the [!DNL Target] UI, despite being successfully delivered to the web page. (TGT-52192)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) where breadcrumbs were not always displayed at the bottom of the editor, causing difficulties in precisely selecting elements. (TGT-51169)
* Fixed an issue where the [!UICONTROL Audience] drop-down list failed to display all audiences due to pagination. (TGT-52204)
* Fixed an issue that caused an invalid user input message when adding new offers in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52210)
* Fixed an issue where [!UICONTROL Analytics for Target] (A4T) was incorrectly selected as the reporting source, even though the customer did not have access to A4T. (TGT-52226)
* Fixed an issue that prevented saving an activity with the [!UICONTROL View a Page] URL metric. (TGT-52260)
* Fixed an issue that blocked customers from selecting workspaces while creating offers within an activity. (TGT-52289)
* Fixed an issue where modifications from one experience were incorrectly displayed when switching to another experience. (TGT-52184)
* Fixed an issue where the default offer was incorrectly displayed in the [!DNL Target] UI when opening the activity. (TGT-52198)

## [!DNL Target Standard/Premium] 25.4.5 (April 25, 2025)

This release includes the following fixes and updates:

* Fixed an issue that prevented [!DNL Target] from recognizing the "#" character in a website's URL. (TGT-52093)
* Fixed an issue that prevented clearing audiences and editing combined audiences in the updated UI for [!UICONTROL Automated Personalization] (AP) activities. (TGT-52149)
* Fixed an issue that caused audience refinements and activity audiences to be reversed in the updated UI. (TGT-52158)

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
