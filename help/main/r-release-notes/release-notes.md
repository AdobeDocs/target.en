---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates;current updates
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
---
# [!DNL Target] release notes (current)

Explore the latest features, enhancements, and fixes in [!DNL Adobe Target]. These release notes also cover updates to [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform components when applicable. 

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## Time-sensitive updates you need to know {#time-sensitive}

[!BADGE Important]{type=Informative}

For time-sensitive updates related to [!DNL Adobe Target] and your implementation, [!DNL Adobe] provides detailed release notes and documentation through [!UICONTROL Experience League]. Here are some keys highlights relevant to your implementation:

### [!DNL Target] UI version toggle deprecation

For more information, see [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.5.1 (May 7, 2026)

**Integrations**

+++See details

* **[!DNL Adobe Target] management in Experimentation Accelerator.** Added support for assigning [!DNL Target] workspaces to Experimentation Accelerator sandboxes so teams can view experiments from [!DNL Adobe Target] in Experimentation Accelerator in one place. [Learn more](../c-integrating-target-with-mac/experimentation-accelerator.md)

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

<!--
* **Blank page or CORS errors with Enhanced Experience Composer.** Fixed an issue where the [!UICONTROL Visual Experience Composer] could fail to load when Enhanced Experience Composer (EEC) was enabled. (TGT-54576)




**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Click tracking for Experience B.** Fixed an issue where click tracking was not saved for **[!UICONTROL Experience B]** in the [!UICONTROL Visual Experience Composer]. (TGT-54843)

+++
-->

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
