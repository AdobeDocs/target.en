---
keywords: vec;visual experience composer; vec;iframe;extension;browser;faq
description: Discover why some websites might not open reliably in the [!UICONTROL Visual Experience Composer] (VEC). The [!UICONTROL Visual Editing Helper] browser extension lets you load websites reliably within the VEC.
title: How Do I Use the [!UICONTROL Visual Editing Helper] Extension?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
TQID: 'https://experienceleague.adobe.com/wUWUT-FvVIAo52PDaBMfmT7vxv8VOR71hSGhxFvylus'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
    internal-label: Web experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Visual Editing Helper] extension {#visual-editing-helper}

>[!BEGINSHADEBOX]

**On this page:** Learn how the **[!UICONTROL Visual Editing Helper]** browser extension loads websites reliably in the **[!UICONTROL Visual Experience Composer]** (VEC), and how to install and use it.

>[!ENDSHADEBOX]

The [!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper]** browser extension for [!DNL Google Chrome] loads websites reliably in the [!DNL Adobe Target] **[!UICONTROL Visual Experience Composer]** (VEC), which makes it faster to author and check web experiences.

>[!IMPORTANT]
>
>This extension replaces the previous [Target VEC Helper browser extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), as described in the Important note at the top of that article. Manifest V3 introduces security enhancements, so [!DNL Adobe] requires downloading this new extension to continue authoring websites visually in [!DNL Target].

## Why some websites do not open reliably in the VEC

A website might not open reliably in the VEC for the following reasons:

* The website has strict security policies.
* The website is in an iframe.
* The QA or staging site of the customer is internal and not available outside the network.

The extension solves these site-loading issues, for which customers otherwise rely on the [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) or on third-party extensions such as Requestly.

## Benefits of the extension

* **Iframe-busting headers removed:** the extension removes headers such as `X-Frame-Options` and `Content-Security-Policy` from the website implicitly, so no complicated Requestly rules are needed.
* **at.js injection:** when a web page does not yet contain the [!DNL Target] at.js library, the extension can inject it. Experiences can then be authored for the website, and the activities can be created and checked with preview links. With the [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) (EEC), the extension does not inject at.js, but the SameSite cookie functionality remains. To inject at.js on the web page, turn off the EEC.
* **Mobile viewports:** [mobile viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) are supported even without the **[!UICONTROL Enhanced Experience Composer]** (EEC).
* **New [!DNL Target] customers:** the extension makes it possible to experiment with [!DNL Target] even when the IT developers have not yet implemented [!DNL Target] on the website.
* **Partners:** partners who service the websites and [!DNL Target] accounts of multiple customers get one mechanism to support VEC loading, in place of multiple rules in third-party tools.

## Obtain and install the extension

Installing the extension in [!DNL Chrome] makes it possible to load websites reliably in the VEC, including websites that block iframes or that do not yet have at.js implemented.

1. Go to the [[!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper]** browser extension in the Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Click **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.
1. Open the VEC in [!DNL Target].
1. While in the VEC or QA Mode, click the **[!UICONTROL Visual Editing Helper]** browser extension icon ( ![Visual Editing Helper icon](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) in the toolbar of [!DNL Chrome].

   The extension is enabled automatically when a website is opened in the [!DNL Target] VEC to power authoring. It has no conditional settings, and it handles all settings automatically, including the SameSite cookie settings. For more information on the `SameSite=None` attribute browser fix, see [Google Chrome SameSite cookie policies](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Usage notes

* The extension loads the latest version of at.js that is available in the [!DNL Target] UI under **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**, and at.js downloads the authoring libraries.
* To use the extension to inject at.js in [QA Mode](/help/main/c-activities/c-activity-qa/activity-qa.md), another Chrome tab must be open. This tab must be authenticated to the same [!DNL Adobe Experience Cloud] organization in which the activity was created.
* The VEC displays messages that suggest installing the extension in the following cases:

  * A website fails to load in the VEC.
  * at.js or alloy.js is not yet implemented on the website.

* If the new extension was tried and the [old extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) is used again, but [!DNL Target] fails to load the website, clear all browser data and disable the new extension.

## Latest changes to the extension (January 17, 2026)

The extension adds a startup cookie cleanup experimental feature to the VEC Helper. The feature cleans unpartitioned cookies once per tab when authoring begins, instead of continuously, which improves performance and reliability. It tracks the history of each tab to prevent redundant cleanup and clears that history when the tab is closed, so cleanup behaves correctly when the tab is reopened. Unit tests ensure consistent behavior.

![Options of the VEC Helper extension, including the cookie processing modes, the advanced logging option, and the experimental features Delay webpage loading, Cookie cleaning, and Startup cookie cleanup](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper.png)

## Frequently asked questions

+++ Does the extension do anything when it is used outside of [!DNL Adobe Target] or [!UICONTROL Adobe Journey Optimizer] (AJO)?

The extension activates only when the website is loaded inside an iFrame in [!DNL Adobe] products ([!DNL Target], [!DNL AJO]). Outside of this flow, the extension does not try to add, remove, or modify any headers, and it does not try to inject any code inside the website.

+++

+++ What does the extension do when it is active in the [!DNL Adobe Target] VEC?

When a website is loaded inside an iFrame in [!DNL Adobe] products ([!DNL Target], [!DNL AJO]), the extension injects code that is bundled with the extension into the website and downloads helper files from the [!DNL Adobe] CDN to enable visual authoring.

+++
