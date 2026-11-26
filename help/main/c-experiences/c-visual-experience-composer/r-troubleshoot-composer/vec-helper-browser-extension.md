---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Discover why some websites might not open reliably in the [!UICONTROL Visual Experience Composer] (VEC). The VEC Helper browser extension lets you load websites reliably within the VEC.
title: How Do I Use the [!UICONTROL Visual Experience Composer] (VEC) Helper Extension?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
TQID: 'https://experienceleague.adobe.com/lqZGGWG1NVtKDzNGPq5k2bDPzxDfNWqPtJ-bYfLCr3Q'
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
# [!UICONTROL Visual Experience Composer] helper extension {#vec-helper-extension}

>[!BEGINSHADEBOX]

**On this page:** Learn how the legacy VEC Helper browser extension loads websites in the **[!UICONTROL Visual Experience Composer]** (VEC), and how to install and use it.

>[!ENDSHADEBOX]

The [!DNL Adobe Target] **[!UICONTROL Visual Experience Composer]** (VEC) Helper browser extension for [!DNL Google Chrome] loads websites reliably in the VEC, which makes it faster to author and check web experiences. The extension is not necessary in [!DNL Mozilla Firefox].

>[!IMPORTANT]
>
>* The legacy [!DNL Target] VEC Helper extension documented in this article was created with Manifest V2. [!DNL Google] announced that it would stop allowing extensions created with Manifest V2 starting in June 2024. For more information, see the [Manifest V2 support timeline announcement](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} from [!DNL Google] on the *Chrome for Developers* site.
>
>* Starting in June 2024, [!DNL Google] disables extensions created with Manifest V2, including the extension documented in this article. [!DNL Adobe] recommends moving to the newer [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) as soon as feasible.

## Why some websites do not open reliably in the VEC

A website might not open reliably in the VEC for the following reasons:

* The website has strict security policies.
* The website is in an iframe.
* The at.js library is not yet implemented on the website.
* The QA or staging site of the customer is internal and not available outside the network.
* The website uses [Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank} (SW), which the VEC currently supports only with limitations. See the following section.
* The website is opened in [!DNL Chrome] 80 or later, which enforces the SameSite cookie policies. For more information, see [Google Chrome SameSite cookie policies](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

The VEC Helper browser extension for [!DNL Chrome] solves the site-loading issues for which customers otherwise rely on the [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) or on third-party extensions such as Requestly.

### Service workers

A service worker (SW) is a web technology that a web page installs to intercept the requests for its domain. The SW survives the page visit and activates itself on subsequent visits. It decides which requests go through and which are intercepted and served from a cache.

A SW can cache the web page itself, static resources such as JS, CSS, IMG, and AJAX requests, their contents, and their response headers. These headers include the ones that the [Target VEC Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) tries to remove, such as `X-Frame-Options: SAMEORIGIN`, CSP (`Content-Security-Policy`), and `Set-Cookie`.

The [!DNL Chrome] extension APIs that intercept web requests do not receive the requests that a SW has intercepted and handled. When a SW serves the web page request from a cache, the extension therefore cannot fix the headers and the cookies, and the page does not load inside the VEC because of the cached `X-Frame-Options` or CSP headers.

As a potential workaround, disable the Service Workers in the [!DNL Chrome] Developer Tools > **Application** tab, then enable the "Bypass for network" check box in the Service Workers section.

## Benefits of the VEC Helper extension

* **Iframe-busting headers removed:** the extension removes headers such as `X-Frame-Options` and `Content-Security-Policy` from the website implicitly, so no complicated Requestly rules are needed.
* **at.js injection:** when a web page does not yet contain the [!DNL Target] at.js JavaScript library, the extension can inject it. Experiences can then be authored for the website, and the activities can be created and checked with preview links. With the Enhanced Experience Composer (EEC), the extension does not inject at.js, but the SameSite cookie functionality remains. To inject at.js on the web page, turn off the EEC.
* **Mobile viewports:** [mobile viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) are supported even without the **[!UICONTROL Enhanced Experience Composer]** (EEC).
* **New [!DNL Target] customers:** the extension makes it possible to experiment with [!DNL Target] even when the IT developers have not yet implemented [!DNL Target] on the website.
* **Partners:** partners who service the websites and [!DNL Target] accounts of multiple customers get one mechanism to support VEC loading, in place of multiple rules in third-party tools.

## Obtain and install the VEC Helper browser extension

Installing the extension in [!DNL Chrome] makes it possible to load websites reliably in the VEC, including websites that block iframes or that do not yet have at.js implemented.

1. Go to the [Adobe Target VEC Helper browser extension in the Chrome Web Store](https://chromewebstore.google.com/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca).
1. Click **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.
1. Open the VEC in [!DNL Target].
1. While in the VEC or [QA Mode](/help/main/c-activities/c-activity-qa/activity-qa.md), click the VEC Helper browser extension icon ( ![VEC Helper icon](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png) ) in the toolbar of [!DNL Chrome].
1. (Conditional) If the web page does not yet contain the [!DNL Target] at.js JavaScript library, switch the **[!UICONTROL Inject Target Libraries]** toggle on.

   The following illustration shows the VEC Helper with the **[!UICONTROL Inject Target Libraries]** setting enabled:

   ![VEC Helper extension panel with the Inject Target Libraries toggle on and the Cookies toggle off, showing that the Cookies setting sets the SameSite=None and Secure flags on all cookies for requests inside the VEC](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   The VEC Helper then asks whether it should inject the [!DNL Target] libraries in the page to enable authoring:

   ![Inject Target Libraries prompt saying that the Target VEC Helper extension wants to inject Target libraries in the page to enable authoring, with the Cancel and Allow buttons](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Conditional) Switch the **[!UICONTROL Cookies]** toggle on to add the `SameSite=None` attribute browser fix automatically.

   ![VEC Helper extension panel with the Cookies toggle switched on and highlighted, over the Visual Experience Composer showing a sample page](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   For more information on the `SameSite=None` attribute browser fix, see [Google Chrome SameSite cookie policies](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Usage notes

* The **[!UICONTROL Inject Target Libraries]** flag in the extension is off by default. Turn it on to use the VEC on a site on which [!DNL Target] is not yet implemented.

  The flag is a global setting, so it is enabled or disabled for all websites opened in the VEC. For example, with the flag on, opening a website that already has at.js implemented displays a message that at.js is already loaded. [!DNL Adobe] expects that most customers already have at.js implemented on their pages and use the default setting of off.

* The extension loads the latest version of at.js that is available in the [!DNL Target] UI under **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
* To use the extension to inject at.js in [QA Mode](/help/main/c-activities/c-activity-qa/activity-qa.md), another Chrome tab must be open. This tab must be authenticated to the same [!DNL Adobe Experience Cloud] organization in which the activity was created.
* The VEC displays messages in the following cases:

  * A website fails to load in the VEC. The message suggests installing the VEC Helper browser extension.
  * at.js is not yet implemented on the website. The message suggests installing the extension.
  * The extension is enabled and powers the loading. The messages display when the extension injects the at.js library, if necessary, or helps open the website reliably in the VEC. 
