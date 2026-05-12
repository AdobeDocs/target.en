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


## Latest updates - May 12, 2026

**[!DNL Adobe Target] MCP server (Public Beta)** 

[!DNL Adobe Target] now provides an MCP (Model Context Protocol) server that surfaces experimentation, personalization, and reporting operations directly inside any MCP-compatible application. With this integration, marketing and technical personas can inspect A/B tests, analyze performance reports, and explore audiences and offers — all using natural-language prompts instead of navigating multiple UI screens or writing queries against the [!DNL Adobe Target] REST API. This capability is currently available in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor**, and **ChatGPT**.

This capability is available to all customers in Public Beta.

For more information, see [[!DNL Adobe Target] MCP server](../c-integrating-target-with-mac/mcp/target-mcp.md).


## [!DNL Target Standard/Premium] 26.5.1 (May 7, 2026)

**Integrations**

+++See details

* **[!DNL Adobe Target] management in Experimentation Accelerator.** Added support for assigning [!DNL Target] workspaces to Experimentation Accelerator sandboxes so teams can view experiments from [!DNL Adobe Target] in Experimentation Accelerator in one place. [Learn more](../c-integrating-target-with-mac/experimentation-accelerator.md)

+++

**Activities**

+++See details

* **[!UICONTROL Graph View] out of sync with table and download.** Fixed an issue where activity reports could show missing or zero metrics in **[!UICONTROL Graph View]** for some date ranges even though **[!UICONTROL Table View]** and the downloaded report still showed the correct values. (TGT-54998)

+++

**[!UICONTROL Audiences]**

+++See details

* **Audience usage list not fully rendered.** Fixed an issue in which the **[!UICONTROL Usage]** section in audience details could display only a subset of mapped activities even when additional activities were associated with that audience. (TGT-55094)

+++

**[!UICONTROL Administration]**

+++See details

* **Clearer confirmation for last-octet IP obfuscation.** When you change **[!UICONTROL Obfuscate Visitor IP addresses]** to **[!UICONTROL Last octet]** on **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**, the confirmation dialog now explains that [!DNL Target] hides the last octet of the visitor IP address. (TGT-44821)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Blank or incomplete page with Enhanced Experience Composer (EEC).** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load the site in the editor when **[!UICONTROL Enhanced Experience Composer]** was enabled. (TGT-54576)

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
