---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates;current updates
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!DNL Target] release notes (current)
 
Explore the latest features, enhancements, and fixes in [!DNL Adobe Target]. These release notes also cover updates to [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform components when applicable. 

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## [!DNL Target Standard/Premium] 26.7.4 (July 23, 2026)

**Reporting**

+++See details

* **Conversion rate graph not available for specific mobile audience.** Fixed an issue where the [!UICONTROL Conversion Rate] graph did not render for certain mobile audiences. (TGT-55611)

* **"Viewed an mbox" conversion goal not working when selected from dropdown.** Fixed an issue where selecting an mbox from the dropdown in [!UICONTROL Goals & Settings] for a "Viewed an mbox" conversion goal saved the mbox name incorrectly, preventing conversions from being recorded. (TGT-55588)

+++

**Audiences**

+++See details

* **Layout issue on the Audience Library page.** Fixed a layout issue that occurred when filters were enabled on the [!UICONTROL Audience Library] page while the side navigation was collapsed. (TGT-55502)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Mobile version does not load correctly.** Fixed an issue where the [!UICONTROL Visual Experience Composer] did not offer a way to refresh, preventing the mobile view from loading correctly. (TGT-54408)

* **Edit or delete modification actions not working.** Fixed an issue where editing or deleting a modification from the [!UICONTROL Edit Experience] view did not work. (TGT-55250)

* **Browse mode unresponsive after activity loads.** Fixed an issue where [!UICONTROL Browse] mode became unresponsive for experiences containing a modification, preventing further navigation and authoring. (TGT-55306)

* **Unable to select elements inside Salesforce LWC (Shadow DOM).** Fixed an issue where the [!UICONTROL Visual Experience Composer] could not select elements nested inside Salesforce Lightning Web Components using Shadow DOM, resulting in a "selector not found" error. (TGT-54956)

* **Duplicate offers appeared in the [!UICONTROL Visual Experience Composer].** Fixed an issue where modifications and offers intermittently appeared duplicated in the activity authoring UI. (TGT-55685)

+++

**Administration**

+++See details

* **Renamed the content generation assistant to [!UICONTROL Generate content].** Renamed the "AI Assistant" content-generation capability to [!UICONTROL Generate content] across [!DNL Target] UI surfaces. (TGT-55689)

+++

**Recommendations**

+++See details

* **Popularity-based recommendations using profile attributes.** [!DNL Target] now supports grouping popularity recommendations, Most Viewed and Top Sellers, dynamically by visitor profile attributes such as country, preferred language, or membership level. (TAPER-7614)

* **Recommendation collection mismatch between [!UICONTROL Collections] and activity configuration.** Fixed an issue where a [!UICONTROL Recommendations] collection returned additional, non-qualifying entities when viewed from activity configuration compared to the [!UICONTROL Recommendations] > [!UICONTROL Collections] view. (TGT-55554)

+++

## [!DNL Target Standard/Premium] 26.7.2 (July 16, 2026)

**Activities**

+++See details

* **Incorrect goal information on the [!UICONTROL Activity Overview] page.** Fixed an issue where the [!UICONTROL Activity Overview] page for [!DNL Automated Personalization] activities showed additional goals instead of the optimization goal. (TGT-55553)

* **Unresponsive screen when navigating pages in [!UICONTROL Browse] mode.** Fixed an issue where the screen became unresponsive when navigating between pages in [!UICONTROL Browse] mode. (TGT-55565)

+++

**Homepage**

+++See details

* **UI change for [!UICONTROL Top performers] and [!UICONTROL Saves].** Updated the UI for the top performers and saves experience. (TGT-54975)

+++

**Audiences**

+++See details

* **Unlocalized strings in [!UICONTROL Create Profile Script] dialog.** Fixed an issue where strings in the [!UICONTROL Create Profile Script] dialog were not localized. (TGT-51527)

+++

## [!DNL Target Standard/Premium] 26.7.1 (July 9, 2026)

**Activities**

+++See details

* **Inconsistent source display across [!UICONTROL Activities], [!UICONTROL Audiences], and [!UICONTROL Offers] pages.** Fixed an issue where the source displayed inconsistently across the [!UICONTROL Activities], [!UICONTROL Audiences], and [!UICONTROL Offers] pages. (TGT-55247)

* **Activity source changes when editing via UI.** Fixed an issue where editing an activity through the UI changed the original activity source. (TGT-55248)

+++

**Audiences**

+++See details

* **Incorrect default workspace when editing an audience.** Fixed an issue where the default workspace was incorrect after you edited an audience. (TGT-55510)

+++

**Reporting**

+++See details

* **CSV download failure for May reports.** Fixed an issue where downloading a CSV report for May failed. (TGT-55524)

+++

## Time-sensitive updates you need to know {#time-sensitive}

[!BADGE Important]{type=Informative}

For time-sensitive updates related to [!DNL Adobe Target] and your implementation, [!DNL Adobe] provides detailed release notes and documentation through [!UICONTROL Experience League]. Here are some keys highlights relevant to your implementation:

### [!DNL Target] UI version toggle deprecation

For more information, see [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md).

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
