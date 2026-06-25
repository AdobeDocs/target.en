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

## [!DNL Target Standard/Premium] 26.6.5 (June 17, 2026)

**Activities**

+++See details

* **Error when an activity uses audiences deleted at source.** Fixed an issue where you could see an error indicating that an activity uses one or more audiences that were deleted at the source. (TGT-55272)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details

* **A4T reports not visible.** Fixed an issue where [!UICONTROL Analytics for Target] (A4T) reports did not display. (TGT-55432)

+++

**[!DNL Adobe Target] MCP server**

+++See details

* **Consolidated activity tools.** The [!DNL Adobe Target] MCP server activity tools have been consolidated to reduce tool-selection overhead and extend read and report coverage to all activity types. Six per-type tools have been replaced with four unified tools:

  * `get_activity` replaces `get_ab_activity`, `get_xt_activity`, and `get_abt_activity`. Retrieves full activity details for all types: A/B Test, Experience Targeting, Automated Personalization, Auto-Allocate, Multivariate Test (MVT), and Recommendations. The activity type is auto-detected from the ID.
  * `update_activity` replaces `update_ab_activity`, `update_xt_activity`, and `update_abt_activity`. Supports A/B Test, Experience Targeting, and Automated Personalization activities; Auto-Allocate, MVT, and Recommendations activities are read-only.
  * `get_activity_performance_report` replaces `get_ab_performance_report` and `get_xt_performance_report`. Retrieves conversion, lift, and confidence metrics for all activity types.
  * `get_activity_orders_report` replaces `get_ab_orders_report` and `get_xt_orders_report`. Retrieves order and revenue metrics for all activity types.

  For more information, see [[!DNL Adobe Target] MCP server tools reference](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md).

+++

## [!DNL Target Standard/Premium] 26.6.4 (June 16, 2026)

**Activities**

+++See details

* **[!UICONTROL Save & Close] in the updated [!DNL Target] UI.** Restored the **[!UICONTROL Save & Close]** option in the updated [!DNL Target] UI. (TGT-55152)

* **QA URLs in the updated [!DNL Target] UI.** Fixed an issue where QA URLs did not work correctly in the updated [!DNL Target] UI. ([TGT-55110](https://jira.corp.adobe.com/browse/TGT-55110))

+++

**Localization**

+++See details

* **Unlocalized percent format in Activity overview graph reports.** Fixed an issue where the percent format was not localized in the chart in **[!UICONTROL Graph view]** on the **[!UICONTROL Reports]** tab on the **[!UICONTROL Activity Overview]** page. (TGT-50100)

* **Japanese characters in the activity URL.** Fixed an issue where Japanese characters in the activity URL appeared corrupted on the **[!UICONTROL Activity Overview]** page and in the activity list after you saved an activity. (TGT-53459)

* **Unlocalized timestamp in the default activity name.** Fixed an issue where the timestamp was not localized in the activity title when you retained the default activity name during activity creation. (TGT-53273)

+++

**[!UICONTROL Recommendations]**

+++See details

* **Multi-byte characters in the URL after creating feeds.** Fixed an issue where multi-byte characters appeared corrupted in the URL after you created feeds. (TGT-54793)

+++

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

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
