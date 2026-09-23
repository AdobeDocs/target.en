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

## [!DNL Target Standard/Premium] 26.9.5 (September 21, 2026)

### Feature

<table>
<thead>
<tr>
<th><strong>Content pre-hiding</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content pre-hiding helps reduce page flicker by hiding only the sections that Adobe Target personalization is about to change, providing a smoother experience while content loads. This approach avoids hiding the entire page and helps minimize implementation effort when new activities are launched.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>For more information, refer to the <a href="../administrating-target/content-pre-hiding.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Improvements

**[!UICONTROL Analytics for Target]**

+++See details

* **A4T report link not generated in [!DNL Target] UI**. For [!DNL A4T] activities, the report link was not generated in the **[!UICONTROL Reports]** section, even though the underlying report data was visible in both the [!DNL Target] UI and the [!DNL Adobe Analytics] UI. (TGT-56247)

+++

## [!DNL Target Standard/Premium] 26.9.4 (September 17, 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **[!UICONTROL Insert Before] control inaccessible for [!DNL Experience Fragments] on the top-most page element**. In the Visual Experience Composer, selecting the top-most element on a page scrolled the page upward, causing the **[!UICONTROL Insert Before]** control to render above the visible viewport where it coul not be selected. (TGT-55829)

+++

## [!DNL Target Standard/Premium] 26.9.3 (September 16, 2026)

**[!UICONTROL Reporting]**

+++See details

* **Missing [!UICONTROL Lift] and [!UICONTROL Confidence] values in some [!DNL A4T Auto-Target] reports**. For [!DNL A4T Auto-Target] activities using the **[!UICONTROL Maximize Visit Conversion Rate]** optimization goal, the default **[!UICONTROL My Primary Metric]** report metric did not resolve correctly, leaving **[!UICONTROL Lift]** and **[!UICONTROL Confidence]** blank. (TGT-56137)

+++

**[!UICONTROL Analytics for Target]**

+++See details

* **[!UICONTROL Reporting Source] field is now read-only for live activities without [!DNL Analytics] access**. Previously, when a live activity's owner did not have access to [!DNL Adobe Analytics], the **[!UICONTROL Reporting Source]** field and its related field remained editable. (TGT-56089)

+++

## [!DNL Target Standard/Premium] 26.9.2 (September 8, 2026)


**[!UICONTROL Recommendations]**

+++See details

* **[!DNL New] user interface encodes feed URLs incorrectly**. When creating a recommendations feed from a URL in the new [!DNL Target] interface, the feed URL was encoded incorrectly, causing feed creation to fail with an unknown error. (TGT-56084)

+++

**[!UICONTROL Reporting]**

+++See details

* **Automated Segments report does not consistently display attribute values**. The Automated Segments report inconsistently displayed attribute values and ranges for [!DNL Automated Personalization] and [!DNL Auto-Target] activities. Some automated segments showed only the attribute name instead of the associated value or range. (TGT-55855)

+++

## [!DNL Target Standard/Premium] 26.9.1 (September 1, 2026)

**[!UICONTROL Audience]**

+++See details

* **Copying an Activity with an activity-only audience fails to save**. When an A/B activity uses an activity-only (locally-scoped) audience rule and a Custom Code modification, copying it and saving the copy fails with an "Invalid audience ids" error. (TGT-55785)

+++

**[!DNL Adobe Target] MCP server — Recommendations tools (Public Beta)**

+++See details

The [!DNL Adobe Target] MCP server now exposes Recommendations tools, letting you list, inspect, create, and update criteria, collections, designs, promotions, and exclusions, and search the product catalog directly from your AI assistant.

This capability requires a Recommendations-enabled tenant with **Target Premium**; it is not available on non-Premium accounts.

For more information, see [MCP server tools reference](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md).

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
