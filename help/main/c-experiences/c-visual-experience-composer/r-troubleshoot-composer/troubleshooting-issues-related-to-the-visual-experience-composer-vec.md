---
keywords: Targeting;visual experience composer;vec;troubleshoot visual experience composer;troubleshooting;tls;tls 1.2
description: Learn how to troubleshoot problems in the [!UICONTROL Visual Experience Composer] (VEC).
title: How Do I Troubleshoot Issues Related to the [!UICONTROL Visual Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
---
# Troubleshooting issues related to the [!UICONTROL Visual Experience Composer]

Display problems sometimes occur in the [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) under certain conditions.

## When I open my website in the [!UICONTROL Visual Experience Composer], the [!DNL Target] libraries do not load. (VEC only) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

+++Details
[!DNL Target] adds two parameters (`mboxEdit=1` and `mboxDisable=1`) while opening the website in the [!UICONTROL Visual Experience Composer].

If your website (specially Single Page Apps), trims parameters or actually removes them while navigating from one page to another (without a page reload) the [!DNL Target] functionality breaks and the [!DNL Target] libraries do not load.

To avoid this problem, ensure that you do not trim or remove these two parameters.

+++

## My page won't open in the EEC, or loads slowly. Activities or experiences load slowly in the VEC. (VEC only) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

+++Details
Several issues can affect page performance in the [!UICONTROL Target] experience composers. Some common issues include:

* You do not have an mbox on the page. 
* Your site uses proxy blocking, which does not allow the page to be opened in either experience composer. 
* Your site doesn't allow itself to be opened in an iFrame.

If issues occur in the [!UICONTROL Enhanced Experience Composer], try turning off the [!UICONTROL Enhanced Experience Composer] and use the [!UICONTROL Visual Experience Composer] instead.

To disable the [!UICONTROL Enhanced Experience Composer], go to **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** and turn off the **[!UICONTROL Enable Enhanced Experience Composer]** option.

Some users see the following error message in the console:

![Console error message](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

If neither the [!UICONTROL Visual Experience Composer] nor the [!UICONTROL Enhanced Experience Composer] works, use a browser extension like [!DNL Requestly] ([!DNL Chrome] or [!DNL Firefox]) or Modify Response Headers (Firefox) that can overwrite the X-Frames header options for your site and allow them to be loaded in iFrames, enabling the VEC. If you are unable to use browser extensions, use the [Form-based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>In addition to the following information, you can use the [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) for [!DNL Google Chrome].

>[!NOTE]
>
>These plugins should be used only in the context of VEC editing.
>
>For the [!DNL Requestly] extension, whenever there is a need to remove headers, you should do either of following:
>
>* Add URL rules for the URL that you want to open in the VEC so that headers are removed for those URLs only.
>
>* Enable the rule when you are editing in the VEC and disable the rule when you are not using the VEC.
>
>For the [!UICONTROL Modify Response Header] extension ([!DNL Firefox]), because you can't add a URL rule, you must do the following:
>
>* Enable the rule when you are editing in the VEC and disable the rule when you are not using the VEC.

**To use the [!DNL Requestly] extension on [!DNL Chrome] or [!DNL Firefox]:**

1. Turn off the [!UICONTROL Enhanced Experienced Composer]. 
1. Install the [!DNL Requestly] browser extension on [!DNL Chrome] or [!DNL Firefox]. 
1. Open the extension and configure it using the following: 
1. Select **[!UICONTROL Modify headers]**. 
1. Enter the following:

    * Rule name 
    * Modification rules

        * Toggle **[!UICONTROL Add]** to **[!UICONTROL Remove]**. 
        * Toggle **[!UICONTROL Request]** to **[!UICONTROL Response]**. 
        * Enter "X-Frame-Options" as the header name. 
        * Repeat previous steps and enter "x-frame-options" as the header name.

          >[!NOTE]
          >
          >Headers that are manipulated via [!DNL Requestly] are case sensitive.

        * Change **[!UICONTROL Equals]** to **[!UICONTROL Contains]** as the condition for the source URL and enter the URL of the activity that you are trying to load in the VEC.

      ![chrome_extension image](assets/chrome_extension.png)

1. Click **[!UICONTROL Save]**.

   ![requestly image](assets/requestly.png)

   You should now be able to load the page quickly with the [!UICONTROL Visual Experience Composer].

**To use the [!DNL Modify Response Headers] extension on [!UICONTROL Firefox]:**

1. Install the [!UICONTROL Modify Response Headers] on [!DNL Firefox] and restart the browser. 
1. From your [!DNL Firefox] extensions, select the Modify Response Headers extension. 
1. Click **[!UICONTROL Preferences]**. 
1. Select **[!UICONTROL Filter]** from the [!UICONTROL Action] drop down. 
1. In the [!UICONTROL Header Name] field, enter: **[!UICONTROL X-Frame-Options]**. 
1. Repeat Steps 4 and 5 to add a filter with **[!UICONTROL x-frame-options]**. 
1. Click **[!UICONTROL Add]**. 
1. Click **[!UICONTROL Start]**.

![Firefox extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

After setting up an extension, open [!DNL Target]. Your pages should now load in the [!UICONTROL Visual Experience Composer], even if the [!UICONTROL Enhanced Experience Composer] is disabled.

+++

## My page does not display in the VEC (VEC only) {#does-not-load}

+++Details
* Best compatibility with VEC is ensured by the newest version of the extension: [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). 

  To verify whether you are using the latest version, go to [!UICONTROL Extensions] > [!UICONTROL Manage Extensions] then click [!UICONTROL Details].

* The [!UICONTROL Visual Experience Composer] requires authoring libraries in order to perform modifications on the web page. These libraries are embedded in the at.js library and are downloaded by the extension from [!DNL Adobe] servers each time VEC is used. 

  The extension downloads the at.js library regardless of whether at.js or the [!DNL Adobe Experience Platform Web SDK] are already included in the page. 
  
  Ensure there are no invalid changes added to the at.js headers configured in the [!UICONTROL Administration] > [!UICONTROL Implementation] section.

* Ensure that the web page is not blocking requests mandatory for loading when embedded within an iFrame. This includes the use of frame-ancestors CSP directives or custom JS code embedded in the customer website, meta HTML tags, or the x-frame-options header.

* Ensure that the web page's Javascript does not interfere with the authoring libraries. Do not use or include files using the following reserved names:

  * `target-vec-helper.js`
  * `target-vec.js`
  * `target.js`
  * `admin.css`
  * `sizzle.js`
  * `mixContentCheck.html`

    Additionally, accidental overriding of variables or events defined within these files could lead to issues with VEC.

* The browser is blocking a non-secure page on a secure site.

  Click the icon to the left of the URL in the browser address bar and click **[!UICONTROL Disable protection on this page]** 

* You entered an invalid URL. 
* If your website fails to load in the VEC, or behaves unexpectedly, a potential fix is to accept cookies on your website in the browser before trying to load the website in [!DNL Target].

+++

## The VEC appears broken when I use [!UICONTROL Browse] mode. (VEC only) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

+++Details
While using [!UICONTROL Browse] mode, if you access a URL that does not have [!DNL Target] libraries implemented ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}) or contains a frame-buster header, the VEC appears broken. Due to browser security concerns, [!DNL Target] cannot properly access the URL you navigated to or the VEC URL does not update consistently if the page loads.

This issue occurs because VEC loads the web page in an `<iframe>`. The current security mechanisms of browsers prevent the [!DNL Target] UI from accessing the elements of the given frame because of the same-origin policy. Browsers block scripts trying to access a frame with a different origin and that includes information such as the `location.href`.

You must use the new [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) to inject the [!DNL Target] library into the pages in order to browse them optimally.

+++

## Issues caused by CSS conflicts in the [!UICONTROL Visual Experience Composer]

+++Details
Verify whether there are any CSS files that might impact the visibility while loading the web page in the editor. For example using the `overflow: hidden` property on the page body could lead to scrolling issues or trigger click events that could interfere with the menu for authoring.

+++
