---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
---
# [!DNL Target] release notes (current)

These release notes provide information about features, enhancements, and fixes for each [!DNL Adobe Target Standard] and [!DNL Target Premium] release. In addition, release notes for [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform changes are also included, when applicable.

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## [!DNL Target] Standard/Premium 22.13.3 (January 25, 2023)

This release contains the following new features, enhancements, and fixes:

|Feature|Details|
| --- | --- |
|Automated Personalization (AP)|Added support for JSON offers in [!UICONTROL Automated Personalization] (AP) activities using the Form-Based Experience Composer.<br>For more information, see [Create JSON offers](/help/main/c-experiences/c-manage-content/create-json-offer.md). (TGT-41460)|
|Recommendations|Friendly names in [!UICONTROL Analytics for Target] A4T reporting is now available. Previously, [!DNL Target] listed experience IDs only. This enhancement aligns reporting between [!DNL Adobe Analytics] and [!DNL Target] and helps customers streamline building reports in A4T. (TGT-41853)|
|Activity QA|Implemented [QA mode](/help/main/c-activities/c-activity-qa/activity-qa.md) for AP activities for select customers. This functionality will be available to all customers after an initial testing phase. (TGT-44341)|

* Fixed an issue that caused a "500 error" in [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] (XT) activities that contain recommendations. This issue was caused when [!DNL Target] failed to properly delete criteria objects from the [!DNL Target] UI and [!DNL Recommendations] backend that are no longer in use. (TGT-44383)
* Removed the location from the displayed offer name in the [!UICONTROL Offer Level] report for [!UICONTROL Automated Personalization] activities. This change makes the report more readable. (TGT-44294)
* Renamed the "[!UICONTROL Experience Fragment]" option in the [!UICONTROL Visual Experience Composer] (VEC) workflow. The option is now "[!UICONTROL HTML XF]." (TGT-44132)
* Removed the 45-day and 90-day calendar options from the AP and [!UICONTROL Auto-Target] [!UICONTROL Personalization Insights] and [!UICONTROL Important Attributes] reports in the [!DNL Target] UI. Because of usage patterns and to improve performance, these date ranges have been deprecated. The UI has been updated to reflect the currently allowed ranges: 15, 30, and 60 days. (TGT-39357)
* Disallowed the ability to change the [!UICONTROL Same as Optimization Goal] setting on the [!UICONTROL Goals & Settings] page after the activity is live. (TGT-43923)
* Fixed an issue that caused issues with the default workplace in the [!DNL Target] backend when upgrading from [!DNL Target Standard] to [!DNL Target Premium]. (TGT-44081 & TGT-44306)
* Changed the link on the [!UICONTROL Implementation] page ([!UICONTROL Administration] > [!UICONTROL Implementation]) for "Implementation Methods with On-Device Decisioning" to point to the page that explains how to use on-device decisioning for all supported SDKs: Node.js, Java, .NET, and Python. For more information, see [Getting Started with Target SDKs](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Fixed an issue that caused file-upload issues when using [!DNL Scene7] and [!DNL Target].
* Enhanced the accessibility of the [!DNL Target] UI for persons with disabilities by using results from an internal usability audit. These accessibility enhancements include access to features that were previously not accessible via the keyboard, alt text enhancements, the ability to zoom parts of the UI to be more usable, improved keyboard focus, and more.   (TGT-42759) 
* Made various localization fixes throughout the [!DNL Target] UI.

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|Documentation changes|View detailed information about updates to this guide that are not included in these release notes.<br>For more information, see [Documentation Changes](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C).|
|Release notes for previous releases|View information about new features and enhancements in previous releases of Target Standard and Target Premium.<br>For more information, see [Release notes for previous releases](/help/main/r-release-notes/release-notes-for-previous-releases.md).|
|Adobe Experience Cloud release notes|View the latest release notes for the Adobe Experience Cloud solutions.<br>For more information, see [Experience Cloud Release Notes](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html).|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|Adobe Priority Product Update|To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)|
|Upcoming release notes|For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/main/r-release-notes/target-release-notes.md) page.|
