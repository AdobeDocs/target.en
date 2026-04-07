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

<!--
## [!DNL Target Standard/Premium] 26.4.2 (April 7, 2026)

**Activities**

+++See details

* **Custom code preserved when applied to additional views.** Fixed an issue where custom code applied to one **[!UICONTROL View]** could be removed when adding or saving custom code for another **[!UICONTROL View]** in the same **[!UICONTROL Activity]**. (TGT-53933)

* **Reporting metrics column order.** The updated [!DNL Target] interface allows reporting metrics to be reordered without clearing the full selection and re-adding metrics in sequence. Previously, users were required to unselect all metrics and select them again in the desired order, which was time-consuming when many metrics were enabled and when adjusting column placement to limit horizontal scrolling. (TGT-53044)

+++

-->

## [!DNL Target Standard/Premium] 26.4.1 (April 2, 2026)

**Activities**

+++See details

* **Audience attributes visible in the Activities view.** Fixed an issue where audience rule details viewed from an **[!UICONTROL Activity]** did not display certain attributes that appeared when opening the same audience from the **[!UICONTROL Audiences]** section. (TGT-54742)

* **Export CSV on Activities and Audiences list pages.** Added an **[!UICONTROL Export CSV]** action so you can export activity lists from the user interface, including when filters are applied, without relying solely on APIs for routine exports. (TGT-51466)

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
