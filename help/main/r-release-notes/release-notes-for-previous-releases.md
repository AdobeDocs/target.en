---
keywords: Release notes;prerelease notes;future enhancements;future fixes;future features;upcoming release
description: View a list of features, enhancements, and fixes included in previous releases of Adobe Target.
title: What Features Are Included in Previous Releases?
feature: Release Notes
exl-id: e4d261a1-d3aa-46ea-b1ce-efa76a90dc71
TQID: 'https://experienceleague.adobe.com/cjheajZKokzwCNspfQckh6PHh5ecetdj7vZrrq9IqXw'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
    internal-label: Integrations
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: df62f171-ac37-440f-8f0f-f41a72ebdd34
    internal-label: Analytics integration
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: c5abb976-5170-45d6-bcac-66d15d10a4d4
    internal-label: Release notes
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
    internal-label: Experimentation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
    internal-label: Mobile experience
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: e6ff21d3-dec6-4298-8590-7c749fffaf78
    internal-label: Content and assets
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
    internal-label: Web experience
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
---
# Release notes for previous releases

Release notes for previous [!DNL Adobe Target] releases, including release notes for [!DNL Target Standard/Premium], the [!DNL Target] platform, and the [!DNL Target] Javascript library (at.js). 

Release notes are listed in descending order by month and year of release. 

>[!NOTE]
>
>See [Target release notes (current)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) for information about the current month's Target releases (platform and Target Standard/Premium).

## Release notes - 2026

## [!DNL Target Standard/Premium] 26.9.8 (September 30, 2026)

### Features

<table>
<thead>
<tr>
<th><strong>Sample size calculator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Sample Size Calculator helps you plan experiments before launch by estimating required traffic, test duration, the number of experiences, or the minimum effect you can reliably detect. Available from the Activities menu, it uses your inputs to help you determine the resources and runtime needed for your test.</p>
<p>The Sample size calculator feature is currently available as a beta feature.</p>
<p>For more information, refer to the <a href="../c-activities/sample-size-calculator.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Insights</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI insights provides AI-generated experiment learnings and optimization opportunities for A/B Test activities with Manual traffic allocation. Once an experiment reaches statistical significance, insights highlight attributes of the winning experience that likely contributed to its performance. Suggested opportunities include new experience ideas, hypotheses, and implementation guidance to help improve conversion rates.</p>
<p>The AI insights feature is currently available as a beta feature.</p>
<p>For more information, refer to the <a href="../c-activities/ai-insights.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Improvements

**[!UICONTROL Administration]**

+++ See details

* **Unable to grant AI permissions to users**. Users with Product Admin and System Admin access could not grant AI permissions to other users. Attempting to enable the AI permission resulted in an `Unauthorized` error, even when AI was enabled for the organization. (TGT-56261)

+++

## [!DNL Target Standard/Premium] 26.9.7 (September 28, 2026)


**[!UICONTROL Recommendations]**

+++ See details

* **"Invalid user input" error in the Visual Experience Composer**. When editing a Recommendations activity in the Visual Experience Composer, an "Invalid user input" error appeared when attempting to save and close the activity.

+++


## [!DNL Target Standard/Premium] 26.9.6 (September 24, 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Endless redirection loop when accessing an SSO-authenticated page through the Visual Experience Composer**. When a page URL loaded in the Visual Experience Composer went through an SSO/login redirection flow, the Visual Experience Composer entered an endless redirect loop and never reached the intended page. (TGT-56233)

+++

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

## [!DNL Target Standard/Premium] 26.8.5 (August 18, 2026)

**Recommendations**

+++See details

* **Null-value filter for exclusions and collections.** You can now use the **Value is present** and **Value is not present** operators when defining exclusion rules and collection filters in [!DNL Recommendations]. (TGT-55790)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click metrics elements not showing in the VEC editor after saving the activity.** Fixed an issue where previously configured click metrics were not displayed when you edited the goals and metrics for an activity in the [!UICONTROL Visual Experience Composer], even though the metrics continued to be tracked correctly in activity reports. (TGT-55826)

* **Intermittent "No Modifications" message in the VEC.** Fixed an issue where the **[!UICONTROL Modifications]** panel intermittently displayed "No Modifications" for existing modifications in active Experience Targeting activities. (TGT-55842)

+++

## [!DNL Target Standard/Premium] 26.8.3 (August 13, 2026)

**Activities, offers, and audiences**

+++See details

* **Edit enabled for API/MCP-created activities, offers, and audiences.** Activities, offers, and audiences created via the [!DNL Adobe Target] Admin API and [!DNL Target] MCP can now be edited in the [!DNL Target] UI. After an API-created activity is edited in the UI, it is treated as UI-modified. Previously restricted actions, including [!UICONTROL Copy] and [!UICONTROL Delete], become available, subject to your permissions and the activity status. (TGT-55116)

+++

## [!DNL Target Standard/Premium] 26.8.2 (August 11, 2026)

**Audiences**

+++See details

* **Unable to copy and save a custom code modification in an activity using an activity-only audience.** Fixed an issue where copying an activity that used an activity-only audience failed to save with an "Invalid audience ids" error after you added a custom code modification. (TGT-55785)

+++

**Localization**

+++See details

* **Corrupted multi-byte characters in activity URL.** Fixed an issue where multi-byte characters in the activity URL appeared corrupted in the [!UICONTROL Visual Experience Composer] and on the **[!UICONTROL Collisions]** tab. (TGT-55708)

* **Unlocalized error message when opening a deleted design.** Fixed an issue where the **[!UICONTROL Requested resource was not found]** error message was not localized when you tried to open a design that had been deleted by another user. (TGT-50902)

+++

## [!DNL Target Standard/Premium] 26.8.1 (August 4, 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Truncated icons in [!UICONTROL Experience Audiences] panel.** Fixed an issue where the **[!UICONTROL Add]** and expand/collapse icons were hidden or truncated in the **[!UICONTROL Experience Audiences]** panel during activity creation. (TGT-55372)

+++

## [!DNL Target Standard/Premium] 26.7.5 (July 30, 2026)

**Activities**

+++See details

* **Bayesian statistics for [!DNL A/B Test (Manual)] activities** [!DNL A/B Test (Manual)] activities now support Bayesian statistics as an alternative to Welch's t-test. Choose the statistical methodology in [!UICONTROL Goals & Settings]: a Bayesian activity's report shows probability-based decision metrics, such as [!UICONTROL Chance to Beat Control], and credible intervals instead of the frequentist confidence interval.

* **[!DNL Customer Journey Analytics] reporting for [!DNL Auto-Allocate] activities.** [!DNL Auto-Allocate] activities can now use [!DNL Customer Journey Analytics] as their reporting source, in addition to [!DNL Target] and [!DNL Adobe Analytics] (A4T).

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Unable to select or modify HTML offers in activity.** Fixed an issue where adding certain HTML or Experience Fragment offers to an activity caused the [!UICONTROL Visual Experience Composer] to crash, preventing offers from being selected or modified. (TGT-55732)

+++

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

## [!DNL Target Standard/Premium] 26.6.8 (June 24, 2026)

**Activities**

+++See details

* **Source filter for API and MCP created resources.** Fixed an issue where filtering by [!UICONTROL Adobe Target API] or [!UICONTROL Adobe Target MCP] did not work on the activities, audiences, and offers listing pages. (TGT-55236)

* **Activity source filter values.** Fixed an issue where the [!UICONTROL Adobe Target API] or [!UICONTROL Adobe Target MCP] source filter did not display newly API-created audiences. (TGT-55237)

+++

**Localization**

+++See details

* **Unlocalized strings in the [!UICONTROL Create JSON Offer] modal.** Fixed an issue where strings in the [!UICONTROL Create JSON Offer] modal, including [!UICONTROL Name] and [!UICONTROL Workspace], were not localized during activity creation. (TGT-50084)

* **Unlocalized toast message in a [!UICONTROL Recommendations] activity.** Fixed an issue where an unlocalized toast message appeared when adding recommendations in a form-based [!UICONTROL Recommendations] activity. (TGT-50463)

* **Unlocalized string in the [!UICONTROL Collections] and [!UICONTROL Exclusions] dialogs.** Fixed an issue where the "Item Payload" string was not localized in the [!UICONTROL Collections] and [!UICONTROL Exclusions] dialogs in [!UICONTROL Recommendations]. (TGT-51542)

* **Unlocalized "Approver" string in the [!UICONTROL Audiences] tab.** Fixed an issue where the "Approver" string was not localized in the [!UICONTROL Workspace] column on the [!UICONTROL Audience Library] page. (TGT-51751)

+++

## [!DNL Target Standard/Premium] 26.6.5 (June 17, 2026)

**Activities**

+++See details

* **Error when an activity uses audiences deleted at source.** Fixed an issue where you could see an error indicating that an activity uses one or more audiences that were deleted at the source. (TGT-55272)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details

* **A4T reports not visible.** Fixed an issue where [!UICONTROL Analytics for Target] (A4T) reports did not display. (TGT-55432)

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

## [!DNL Target Standard/Premium] 26.6.3 (June 11, 2026)

**Localization**
 
+++See details

* **Unlocalized first day of the week in Audience calendar modals during activity creation.** Fixed an issue where the first day of the week was not localized in the calendar in the **[!UICONTROL Create]**, **[!UICONTROL Edit]**, and **[!UICONTROL Duplicate Audience]** modals during Activity creation. (TGT-50510)

* **Unlocalized percent format in Activity overview reports.** Fixed an issue where the percent format was not localized in a table on the **[!UICONTROL Reports]** tab on the **[!UICONTROL Activity Overview]** page. (TGT-50094)

* **Unlocalized number format in the [!UICONTROL Create Criteria] dialog.** Fixed an issue where the number format was not localized in the **[!UICONTROL Create Criteria]** dialog in **[!UICONTROL Recommendations]**. (TGT-52250)

+++

## [!DNL Target Standard/Premium] 26.6.1 (June 4, 2026)

**Activities**

+++See details

* **Incomplete activity URL on [!UICONTROL Activity Overview].** Fixed an issue where the [!UICONTROL Activity Overview] did not display the complete URL for an activity. (TGT-54029)

* **Unlocalized date format in Activity reports.** Fixed an issue where the date format was not localized on the **[!UICONTROL Reports]** tab when you chose a **Last X days** option from the **[!UICONTROL Preset Date Range]** drop-down list. (TGT-51637)

* **Unable to save Form-based Activity with certain GB18030 characters in [!UICONTROL Location].** Fixed an issue where you could not save a form-based activity when the **[!UICONTROL Location]** field contained specific GB18030 characters. (TGT-46980)

+++

**[!UICONTROL Audiences]**

+++See details

* **Unlocalized Calendar in Create Audience flow for Simplified and Traditional Chinese.** Fixed an issue where the calendar in the **[!UICONTROL Start]** and **[!UICONTROL End]** fields of **[!UICONTROL Time frame]** attributes was not localized in Simplified Chinese (CHS) and Traditional Chinese (CHT) locales during the Create Audience flow. (TGT-50619)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Unlocalized tooltips in the updated Activity builder.** Fixed localization issues where **[!UICONTROL Refinements]** and **[!UICONTROL Content]** information tooltips were not localized in the updated [!UICONTROL Visual Experience Composer] activity builder. (TGT-53721)

* **Unlocalized [!UICONTROL All Visitors] in [!UICONTROL Experience Audiences].** Fixed an issue where the **[!UICONTROL All Visitors]** string in **[!UICONTROL Experience Audiences]** in the left rail was not localized in the [!UICONTROL Visual Experience Composer]. (TGT-50086)

+++

**[!UICONTROL Reports]**

+++See details

* **Unlocalized date format in the [!UICONTROL Create Preset] window.** Fixed an issue where the date format in the **[!UICONTROL Date range]** field of the **[!UICONTROL Create Preset]** window was not localized. (TGT-49239)

+++

**Localization**

+++See details

* **GB18030 character display in multiple areas.** Fixed issues where some Private Use Area characters displayed incorrectly as letters in the **[!UICONTROL Audience]** UI, **[!UICONTROL Administration]** > **[!UICONTROL Properties]**, mobile viewport configuration, and toast notifications. (TGT-49622, TGT-49623, TGT-49624, & TGT-49625)

+++

## [!DNL Target Standard/Premium] 26.5.2 (May 14, 2026)

**Administration**

+++See details

* **Regex validation for Allowed URLs.** Fixed an issue where invalid regular expressions could be entered in the **[!UICONTROL Allowed URLs]** field without proper validation. (TGT-55095)

+++

**Audiences**

+++See details

* **Buttons in [!UICONTROL Edit Audience] dialog.** Fixed an issue where buttons within the **[!UICONTROL Edit Audience]** dialog no longer rendered correctly. (TGT-54638)

+++

**[!DNL Adobe Target] MCP server (Public Beta)** 

+++See details

[!DNL Adobe Target] now provides an MCP (Model Context Protocol) server that surfaces experimentation, personalization, and reporting operations directly inside any MCP-compatible application. With this integration, marketing and technical personas can inspect A/B tests, analyze performance reports, and explore audiences and offers — all using natural-language prompts instead of navigating multiple UI screens or writing queries against the [!DNL Adobe Target] REST API. This capability is currently available in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor**, and **ChatGPT**.

This capability is available to all customers in Public Beta.

For more information, see [[!DNL Adobe Target] MCP server](../c-integrating-target-with-mac/mcp/target-mcp.md).

+++

## [!DNL Target Standard/Premium] 26.5.3 (May 21, 2026)

**[!UICONTROL What's new] page**

+++See details

* **New [!UICONTROL What's new] page.** Added a new **[!UICONTROL What's new]** page in the [!DNL Adobe Target] UI to help you discover the latest features, enhancements, and updates without leaving the product. (TGT-55137)

+++

**Activities**

+++See details

* **Wrong experience selected when editing Targeting in [!UICONTROL Automated Personalization] activities.** Fixed an issue where the wrong experience could be selected while editing the **[!UICONTROL Targeting]** step in an [!UICONTROL Automated Personalization] (AP) activity. (TGT-55176)

* **Earlier date when closing a scheduled activity.** Fixed an issue that prevented you from selecting an earlier date to close a scheduled activity. (TGT-55163)

+++

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

## [!DNL Target Standard/Premium] 26.5.1 (May 7, 2026)

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

## [!DNL Target Standard/Premium] 26.4.4 (April 28, 2026)

**Activities**

+++See details

* **Error with Audience filter in Reports.** Fixed an issue where changing the audience filter within **[!UICONTROL Goals & Settings]** caused an error in the Reporting section of the [!DNL Target] user interface. (TGT-55006)

* **Sort activities by priority.** Added sorting by priority on the activities list using the **[!UICONTROL Priority]** column header, with ascending and descending order consistent with other sortable columns. (TGT-54948)

* **Additional activity properties not retained after save.** Fixed an issue where certain **[!UICONTROL Properties]** selections did not persist after saving and reopening an activity. (TGT-53889)

+++

**Localization**

+++See details

* **Japanese labels for [!UICONTROL Page Delivery] rule operators.** Fixed unreadable or corrupted strings for page delivery rule operator labels in the Japanese UI. (TGT-53097)

+++

**APIs**

+++See details

* **Reporting [!DNL GraphQL] API support for `segmentId`.** Added `segmentId` to the reporting [!DNL GraphQL] API. (TGT-55021)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Modifications shown on the wrong experience in the editor.** Fixed an issue where a delete or other modification could appear on the wrong experience after switching between experiences in the [!UICONTROL Visual Experience Composer]. (TGT-54955)

* **Modifications removed when deleting insert HTML.** Fixed an issue where deleting the extra **[!UICONTROL HTML]** block added with **[!UICONTROL Insert before]** or **[!UICONTROL Insert after]** also removed a linked modification that had no CSS selector. (TGT-54530)

+++

## [!DNL Target Standard/Premium] 26.4.3 (April 9, 2026)

**Activities**

+++See details

* **Location missing from some activities.** Fixed an issue where **[!UICONTROL Location]** was missing from some activities. (TGT-54951)

* **Reporting metrics column order.** The updated [!DNL Target] interface allows reporting metrics to be reordered without clearing the full selection and re-adding metrics in sequence. Previously, users were required to unselect all metrics and select them again in the desired order, which was time-consuming when many metrics were enabled and when adjusting column placement to limit horizontal scrolling. (TGT-53044)

+++

<!--
**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

## [!DNL Target Standard/Premium] 26.4.2 (April 7, 2026)

**Activities**

+++See details

* **Custom code preserved when applied to additional views.** Fixed an issue where custom code applied to one **[!UICONTROL View]** could be removed when adding or saving custom code for another **[!UICONTROL View]** in the same **[!UICONTROL Activity]**. (TGT-53933)
+++

## [!DNL Target Standard/Premium] 26.4.1 (April 2, 2026)

**Activities**

+++See details

* **Audience attributes visible in the Activities view.** Fixed an issue where audience rule details viewed from an **[!UICONTROL Activity]** did not display certain attributes that appeared when opening the same audience from the **[!UICONTROL Audiences]** section. (TGT-54742)

* **Export CSV on Activities list page.** Added an **[!UICONTROL Export CSV]** action so you can export activity lists from the user interface, including when filters are applied, without relying solely on APIs for routine exports. (TGT-51466)

* **Experience modifications flagged when selectors are not found.** Experience modifications now run a selector-existence check; when a selector is not found on the page, the modification is flagged as invalid. (TGT-54815)

* **[!UICONTROL Automated personalization] activities.** Fixed interface and activity-loading issues that prevented users from reliably creating, editing, or managing Automated personalization activities, which blocked campaign setup and delayed personalization use cases. (TGT-54421)

+++

**Audiences**

+++See details

* **Audience name and description visible when creating audiences from an activity.** Fixed an issue where the audience **[!UICONTROL Name]** and **[!UICONTROL Description]** fields did not stand out clearly when creating or editing an audience from the activity flow, compared to creating the audience directly under **[!UICONTROL Audiences]**. (TGT-54837)

+++

**Insights**

+++See details

* **[!UICONTROL Live Activities] count on Insights.** Fixed an issue where the **[!UICONTROL Live Activities]** metric on the Insights dashboard could report a higher total than the number of activities that appeared as live in **[!UICONTROL All Activities]**. (TGT-54788)

+++

**Recommendations**

+++See details

* **Long ID lists in [!UICONTROL Global Exclusions].** Fixed an issue where pasting or entering a long list of IDs in **[!UICONTROL Global Exclusions]** could be truncated in the updated interface compared with the legacy, causing an incomplete exclusion list. (TGT-54422)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Enhanced Experience Composer (EEC) status indicator in the [!UICONTROL Visual Experience Composer].** The EEC indicator denotes whether Enhanced Experience Composer is enabled. Its presentation has been revised so that it no longer resembles an interactive toggle since it serves only as a non-interactive status display. (TGT-54828)

* **Collapsible left rail in the [!UICONTROL Visual Experience Composer].** The left rail can now be collapsed while an activity is open for editing. This improves access to **[!UICONTROL Components]** and **[!UICONTROL Properties]** for activities that include multiple audiences and pages, including on smaller displays. (TGT-54269)

+++

## [!DNL Target Standard/Premium] 26.3.7 (March 26, 2026)

**Audiences**

+++See details

* **Audience source label accuracy in the Audiences interface.** Fixed an issue where audiences coming from the Adobe Target v2 destination in Adobe Experience Platform could appear with **Adobe Experience Cloud** as the source instead of **Adobe Experience Platform**. This update improves source-label consistency when filtering and reviewing audiences. (TGT-54802)

+++

## [!DNL Target Standard/Premium] 26.3.6 (March 23, 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Intermittent grey screen after authentication in the new Visual Experience Composer UI.** Fixed an issue where users could intermittently see a grey screen after signing in to the new Visual Experience Composer, which prevented further editing. This update improves post-authentication loading reliability. (TGT-54626)

+++

## [!DNL Target Standard/Premium] 26.3.4 (March 19, 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Design/Browse mode selection visible in the Visual Experience Composer web editor.** This fix resolves an issue where switching between Design, Browse, and Preview modes worked correctly, but the active mode was not clearly indicated in the interface. The selected mode is now visibly highlighted so you can see which mode you are in. (TGT-54790)

* **Private network URLs in the Visual Experience Composer (Chrome).** Chrome can block pages on a private network unless local network access is allowed. The **[!UICONTROL Visual Experience Composer]** now requests that permission in the framing Experience Cloud uses, so Chrome can show an allow prompt instead of failing silently. After you allow access, internal URLs can load in the VEC when your environment supports it. (TGT-54346)

+++

## [!DNL Target Standard/Premium] 26.3.2 (March 10, 2026)

**Activities**

+++See details

* **Direct offer changes in experience are not saved.** This fix resolves an issue where modifications made to direct offers within an activity experience were not being saved. Previously, when users opened a direct offer, made changes, and saved it, the changes appeared reflected initially but were lost when reopening the offer. The fix ensures that changes to direct offers are properly saved and persist when the offer is reopened. (TGT-54653)

+++

**Implementation**

+++See details

* **Add flicker management toggle on the Implementation screen.** A new toggle has been added to the [!UICONTROL Implementation] screen to control the enablement of the flicker management setting. This toggle allows administrators to configure flicker management directly from the Implementation screen. (TGT-52247)

+++

**Overview**

+++See details

* **Show full name of audience and experience in Overview page.** This enhancement updates the [!UICONTROL Overview] page to display the full name of audiences and experiences. Previously, long names were truncated and not fully visible, requiring users to triple-click to select all text to see the complete name. The update ensures that full audience and experience names are visible, making it easier for users to identify and review activity configurations. (TGT-53323)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **VEC changes not reflected on sites using Shadow DOM (Salesforce Lightning Web Components).** This fix addresses an issue where changes made in Adobe Target (such as CTA color changes) were not being saved or reflected on the live site for Salesforce-based sites using Lightning Web Components (LWC). The CMS was not accepting updates from Target activities, and this issue occurred consistently across A/B tests and other activity types. (TGT-54059)

+++

### [!DNL Target Standard/Premium] 26.3.1 (March 3, 2026)

**Activities**

+++See details

* **Custom code lost when applied to additional views.** This fix resolves an issue where custom code applied to one view was lost when adding and applying custom code to an additional view. Previously, when users applied custom code to multiple views in an activity, the previously applied custom code would disappear. The fix ensures that custom code is properly preserved across all views when applying modifications to additional views. (TGT-54230)

+++

**Criteria**

+++See details

* **Profile Parameter 'In Between' rule not saving in criteria.** This fix resolves an issue where criteria rules using the **In Between** operator for profile parameters were not being saved correctly. Previously, when users configured a rule with the **In Between** operator and entered range values, the criteria appeared to save successfully, but the rule would disappear when reopening or editing the criteria. The fix ensures that **In Between** rules are properly saved and persist when criteria are reopened. (TGT-54498)

+++

**Insights**

+++See details

* **Change Insights page position after all activities.** The **Insights page** position has been updated to appear after the **All Activities** page in the navigation. The All Activities page is now the default page of the Target application. (TGT-54672)

+++

**Navigation**

+++See details

* **Make the left navigation collapsible.** The left navigation is now collapsible and expandable for all tabs. When collapsed, icons are displayed with tooltips. When expanded, both icons and text are shown. This enhancement provides users with more screen space when needed while maintaining quick access to navigation options. (TGT-54608)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Default experienceEditorType to "visual" when backend returns null.** This fix addresses an issue where the `experienceEditorType` value was being returned as null in some scenarios, causing unintended behavior in the UI where the editor type was not properly initialized. (TGT-54690)

+++

### [!DNL Target Standard/Premium] 26.2.2 (February 16, 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Unable to add images to activities - Unknown error.** This fix resolves an issue where users encountered an "Unknown error" when attempting to add or replace images in activities. The issue was related to Scene7 URL synchronization and authentication failures. The fix ensures that images can be added and replaced correctly in the Visual Experience Composer. (TGT-54137)

+++

### [!DNL Target Standard/Premium] 26.2.1 (February 8, 2026)

**Properties**

+++See details

* **Property token not automatically re-added after removal.** This fix addresses an issue where property tokens that users had deselected were automatically re-added when editing an activity. Previously, when users removed an auto-detected property and navigated between steps, the system would reintroduce the removed property without any alert or prompt, resulting in activities being enabled on unexpected properties. The update ensures that once a property token is removed, it remains removed during all subsequent edits and navigation. (TGT-54040)

+++

### [!DNL Target Standard/Premium] 26.1.2 (January 30, 2026)

**Adobe Target Insights Dashboard**

+++See details

Adobe Target now includes a new insights dashboard that provides a high-level view of how your organization is using Target for experimentation and personalization. The dashboard surfaces key metrics such as live activities, activities live and modified, completed activities, published activities, and A/B testing activity. Use the time range selector to explore trends over different periods, including a recap view for 2025. This dashboard remains available as an ongoing way to track adoption and activity over time.

See [Adobe Target Insights Dashboard](/help/main/c-activities/insights-dashboard.md) 
+++

**Administration**

+++See details

* **Allowlisted URLs management feature.** A new "Allowlisted URLs" management feature has been added to the [!UICONTROL Administration] section to manage allowed remote offer URL patterns. This feature includes the ability to display allowlisted URLs in a table, search and filter URLs, add new URLs via modal dialog, and delete URLs with confirmation. The feature helps customers control which URLs can be used for remote offers, improving security and compliance. (TGT-54486)

+++

**Insights**

+++See details

* **Support for filtering by createdAt and modifiedAt in GraphQL.** Support for filtering activities by `createdAt` and `modifiedAt` date fields has been added to the GraphQL API. This enhancement enables accurate filtering in the Target UI, reduces client-side data processing, and eliminates the need for multiple API calls to retrieve filtered activity data. (TGT-54499)

+++


### [!DNL Target Standard/Premium] 26.1.1 (January 18, 2026)

**Activities**

+++See details

* **Unable to copy activity - invalid user input.** The issue causing users to see an unhelpful "invalid user input" error when copying an activity has been fixed. Previously, when an activity was duplicated, its workspace‑specific property assignments were not preserved, causing the backend to reject the save request because ABActivity requires at least one property belonging to a non‑default workspace. This mismatch triggered a generic error in the UI, leaving users without guidance. The fix ensures that workspace assignments are correctly retained during copy operations, allowing users to save the copied activity without modification and preventing misleading validation errors. (TGT-54282) 
* **Enable workspace column the web editor offer.** This update addresses customer confusion caused by offers from the [!UICONTROL Default Workspace] appearing in other workspaces within the Web Editor. Although this behavior is working as designed, [!UICONTROL Default Workspace] offers are intentionally visible across all workspaces, customers reported that the UI did not make workspace origin clear, especially when creating activities in a non‑default workspace such as "Approvers." To improve clarity, the [!UICONTROL Workspace] column has now been enabled in the Web Editor's offer list, allowing users to easily distinguish which workspace each offer belongs to and preventing misinterpretation of the additional offers displayed. (TGT-54138)
* **Links with target="_blank" open in a new tab.** This fix resolves an issue where authored websites containing links with ~target="_blank"~ would open in a new browser tab when clicked in [!UICONTROL Browse] mode, disrupting the in‑editor preview experience. The behavior occurred because the authored page's native link attributes were not being intercepted by the extension's injected JavaScript, unlike in the legacy UI where anchor elements were transformed and their targets overridden to keep navigation inside the editor. The update ensures that links using ~target="_blank"~ are now properly handled within the Web Editor so they no longer open external tabs during authoring. (TGT-54134)
* **Deselect Property warning.** This update introduces a visual warning to clearly inform users when they deselect an auto‑detected property in the Activity Editor. Previously, removing an auto‑detected property provided no indication that the property would be permanently deleted, which c0uld lead to accidental loss of targeting configuration. The fix adds a warning icon, consistent with the behavior in the legacy UI, to notify users that deselecting the property removes it from the activity. (TGT-54121)
* **[!UICONTROL Workspaces] dropdown is limited to 20 in the [!UICONTROL Users] section.** This fix resolves an issue where the [!UICONTROL Workspaces] dropdown in the [!UICONTROL Administration] > [!UICONTROL Users] section displayed only 20 workspaces, even when a user had access to many more. The underlying GraphQL call for `licenseGroups` was also limited to 20 results, causing the UI to show an incomplete list despite the user having access to more workspaces in the organization. The update removes this hard limit so the full set of available workspaces is now returned and displayed correctly. (TGT-53820)
* **Fixed an issue where the offers modal did not show the workspace column.** Fixed an issue where the offers modal did not display the workspace column in the updated UI. This caused confusion for customers because offers from the [!UICONTROL Default Workspace] appeared alongside offers from the selected workspace without any indication of their origin. The workspace column is now enabled so customers can clearly identify which workspace each offer belongs to. (TGT-52320)

+++

**Properties**

+++See details

* **Activity edit should not add auto‑detected property if already removed.** This fix addresses an issue where editing an activity would automatically reintroduce an auto‑detected property that the user had previously removed. When reopening an activity for editing, the system incorrectly restored the removed property, leading to inconsistent behavior and confusion in the [!UICONTROL Properties List]. The update ensures that once an auto‑detected property is removed, it remains removed during all subsequent edits and does not reappear unless the user explicitly adds it back. (TGT-54182)
* **Do not add auto‑detected properties if already removed.** This fix ensures that once a user manually removes an auto‑detected property from an activity, the system no longer reintroduces it during subsequent navigation within the activity editor. Previously, if a user deselected an auto‑detected property, moved to the [!UICONTROL Targeting] step, and then returned to [!UICONTROL Experiences], the editor would repopulate the removed property based on the auto‑detected list stored in the Activity Editor state slice. The updated logic now compares the auto‑detected properties against the current properties in the ~ActivityState~ slice and prevents re‑adding any auto‑detected property that the user has already removed. This results in consistent behavior across steps and respects user intent. (TGT-54181)
* **Add Auto‑detected text into the properties list.** This enhancement updates the [!UICONTROL Properties List] to clearly label any property that was automatically detected by the system. When an auto‑detected property is also present in the user‑visible [!UICONTROL Properties List], it now displays the "(Auto‑Detected)" text next to its name, using the value stored in the ~ActivityEditorSlice~ state. This mirrors the behavior of the legacy UI and helps users easily distinguish between manually selected properties and those properties identified automatically. (TGT-54120)
* **Add Auto-detected [!UICONTROL Properties] into the state.** This update ensures that the ~ActivityEditorSlice.ExperienceEditor~ state consistently maintains an up‑to‑date list of all auto‑detected property IDs passed from the Web Editor into the Activity [!UICONTROL Experiences] tab. Each time the user navigates into the [!UICONTROL Experiences] tab, the state is refreshed with any newly detected properties while preventing duplicates, ensuring accurate tracking and reliable downstream behavior. (TGT-54119)

+++

**Recommendations**

+++See details

* **[!UICONTROL Environment] drop‑down shows only 100 results.** This fix addresses a limitation where customers with more than 100 environments could only see the first 100 entries in the [!UICONTROL Environment] drop‑down within [!UICONTROL Recommendations]. The underlying GraphQL query (~getEnvironmentsV2~) was paginated with a hard‑coded page size of 100, causing the UI to display only a partial list even when additional pages were available. For customers who have more than 100 environments, this issue resulted in missing options and an incomplete selection experience. The update increases the limit so that all environments are returned and displayed, ensuring full visibility regardless of environment count. (TGT-53903)

+++

**Reports**

+++See details

* **Fixed an issue where the [!UICONTROL Reports] arrow did not clearly indicate expandable columns.** Fixed an issue where the reporting table did not clearly show that additional columns could be expanded in the updated UI. A disappearing tooltip has been added to the [!UICONTROL Reports] arrow near the column headers to help customers understand that more columns are available. (TGT-53479)

+++

**Views**

+++See details

* **Unable to delete modifications applied to views.** This fix resolves an issue where users were unable to delete modifications within an activity unless the modification had first been reapplied to additional views. When editing an activity (for example, activity ID 302467), attempts to delete any modification had no effect, preventing users from removing unwanted changes. However, once a modification was re‑applied using "Apply to more views" and assigned to a `Page Load` event, deletion suddenly worked as expected. (TGT-54088) 

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **[!UICONTROL Experience Fragment] name was truncated in the new VEC UI** (TGT-54312)
* **Unable to use [!UICONTROL Advanced Settings] for [!UICONTROL Revenue] metric.** This fix resolves an issue where users encountered a 403 "Access denied" error when configuring [!UICONTROL Advanced Settings] for the [!UICONTROL Revenue] metric in [!UICONTROL Goals & Settings]. The problem occurred when adding a dependency condition tied to the primary goal; the backend incorrectly required the editor privilege even for users who already had sufficient permissions to create and edit activities. As a result, saving the activity failed despite valid configuration. The update corrects the permission check so that users with appropriate access can successfully add Revenue metric dependencies without triggering a forbidden‑resource error. (TGT-54092)
* **Fixed an issue where the Add button did not apply to selected images.** Fixed an issue that prevented customers from adding certain images when selecting or updating an image in the activity‑create process. When customers searched for specific assets, for example, images returned when searching for "ipp," clicking the [!UICONTROL Add] button did not apply the selected image and no modification was created. Selecting other images, such as `Homepage-banner-1-moz.jpg`, continued to work as expected. This update ensures that all valid images can be applied consistently in the updated UI. (TGT-53610)
* **Fixed an issue where deleting a URL condition reset the goal metric configuration.** Fixed an issue where removing a single URL condition in the [!UICONTROL Goal] metric caused the entire configuration to reset in the updated UI. When customers attempted to delete a saved URL condition under [!UICONTROL Conversion] > [!UICONTROL Viewed a Page], the goal type unexpectedly switched to [!UICONTROL Viewed an Mbox], and all previously configured settings were removed. This update ensures that only the selected URL condition is deleted, and all remaining goal settings stay intact. (TGT-53271)
* **Fixed an issue where search did not look through subfolders.** Fixed an issue where searching for offers did not return results from subfolders in the updated UI. Customers could only find an offer if they manually navigated to the folder where it was stored, making search behavior inconsistent with API capabilities. Search now supports recursively looking through folders so customers can locate offers without needing to open each folder individually. (TGT-51954)

+++
