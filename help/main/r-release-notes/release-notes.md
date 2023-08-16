---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates 
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

## [!DNL Adobe Target] Edge planned infrastructure upgrade {#edge}

The planned edge infrastructure upgrade requires additional IP or domains to be allow-listed. Review and allow-list the NAT and IP/domains for edge deployments 41-48. Infrastructure upgrades begin August 9, 2023.

For more information, see [Allowlist Target edge nodes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank} in the *Adobe Target Developer Guide*.

## [!DNL Target] Standard/Premium 23.8.1 (August 9, 2023)

This release contains the following enhancements and fixes:

* Fixed an issue that sometimes prevented activities from syncing properly, as shown in the "[!UICONTROL Status]" column on the [!UICONTROL Activity] list page. (TGT-46010 & TGT-44831)
* Fixed an issue that sometimes prevented the "[!UICONTROL View in Analytics]" link from displaying on the [!UICONTROL Reports] page of activities that use [!UICONTROL Analytics for Target] (A4T) as the reporting source. (TGT-45808)
* Adjusted the presentation of values in tables to display as percentages instead of numbers with decimals. For example, 8% instead of .08. (TGT-45548)
* Fixed an issue that prevented customers from using keyboard focus to move to the next element in the [!UICONTROL Goals & Settings] page for [!UICONTROL Experience Targeting] (XT) activities. (TGT-44526)
* Fixed an issue that caused keyboard loss of focus after opening the "[!UICONTROL Add audiences]" dialog while creating an activity. (TGT-44525)

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|
     
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
