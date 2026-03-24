---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates;current updates
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
hold: true
---
# [!DNL Target] release notes (current)

Explore the latest features, enhancements, and fixes in [!DNL Adobe Target]. These release notes also cover updates to [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform components when applicable. 

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## Time-sensitive updates you need to know {#time-sensitive}

[!BADGE Important]{type=Informative}

For time-sensitive updates related to [!DNL Adobe Target] and your implementation, [!DNL Adobe] provides detailed release notes and documentation through [!UICONTROL Experience League]. Here are some keys highlights relevant to your implementation:

### [!DNL Target] UI version toggle deprecation

For more information, see [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.3.4 (March 19, 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Design/Browse mode selection visible in the Visual Experience Composer web editor.** This fix resolves an issue where switching between Design, Browse, and Preview modes worked correctly, but the active mode was not clearly indicated in the interface. The selected mode is now visibly highlighted so you can see which mode you are in. (TGT-54790)

* **Private network URLs in the Visual Experience Composer (Chrome).** Chrome can block pages on a private network unless local network access is allowed. The **[!UICONTROL Visual Experience Composer]** now requests that permission in the framing Experience Cloud uses, so Chrome can show an allow prompt instead of failing silently. After you allow access, internal URLs can load in the VEC when your environment supports it. (TGT-54346)

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
