---
keywords: mixed content;secure;insecure;chrome;troubleshooting;vec;visual experience composer;unsecure;http;https;firefox;internet explorer
description: Learn how to enable mixed content in [!DNL Chrome], [!DNL Firefox], and [!DNL Edge].
title: How to Enable Mixed Content in my Browser
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
---
# Enabling mixed content in your browser

Mixed content occurs if the initial request is secure over HTTPS, but HTTPS *and* HTTP content is loaded to display the web page. HTTPS content is secure. HTTP content is insecure.

Modern browsers might block the display of a page or display warning messages if secure content is mixed with insecure content.

A warning message displays if the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] tries to open a page containing mixed content. This message informs you how to disable blocking in your browser. Disabling blocking lets you open an HTTP site or a site that has mixed content (HTTPS and HTTP).

![Mixed content warning](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Previously, when mixed content was not allowed, you could still perform some actions in Step 1 of the three-step guided workflow when creating activities. [!DNL Target] now blocks actions in Step 1. When this message displays, you must enable mixed content before continuing creating the activity.

Your browser's security settings might block mixed content or insecure (HTTP) content being loaded into a secure (HTTPS) page or frame (such as the VEC). If you don't want to disable your browser's security settings, you must have an HTTPS website.

If your website is running on an insecure (HTTP) domain, you are required to allow the VEC to load active mixed content.

>[!IMPORTANT]
>
>Allowing mixed content affects the VEC only and not your live website.

For more information, see [Mixed Content](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) on the *Mozilla Developer Network* (MDN) website.

## Enabling mixed content in [!DNL Google Chrome] {#task_FF297A08F66E47A588C14FD67C037B3A}

If you're visiting a site via a secure connection, [!DNL Chrome] verifies that the content on the web page has been transmitted safely.

See "[Manage warnings about unsafe sites](https://support.google.com/chrome/answer/99020?hl=en)" in Google Chrome Help.

If you are using the VEC with the latest version of [!DNL Chrome] (version 79.0.3945.117 or later), you must update your site settings. Visitors to your site do not need to complete these steps.

1. Click the lock (caution) icon, then click **[!UICONTROL Site settings]**. 

   ![Site Settings](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scroll to **[!UICONTROL Insecure content]**, then use the drop-down list to change "Block (default)" to "Allow."

   ![Insecure content](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Reload the VEC page.

## Enabling mixed content in [!DNL Mozilla Firefox] {#task_5448763B8DC941FD80F84041AEF0A14D}

By default, [!DNL Firebox] blocks pages that mix secure and insecure content. You should permanently change this setting to use [!DNL Target]. Visitors to your site do not need to complete these steps.

1. In Firefox, enter `about:config` in the address bar.
1. Acknowledge the warning message displayed by [!DNL Firefox].

   ![Firefox warning](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. In the search bar, type `block_active`.

   ![Firefox block_active setting](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Double-click ` **[!UICONTROL security.mixed_content.block_active_content]**` .

   The value changes from "True" to "False." When the value shows "False," you are finished. 

   ![Firefox security](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. Restart your computer after changing this setting.

## Enabling mixed content in [!DNL Microsoft Edge]

If you're visiting a site via a secure connection, [!DNL Edge] verifies that the content on the web page has been transmitted safely.

If you are using the VEC with the latest version of [!DNL Edge], you must update your site settings. Visitors to your site do not need to complete these steps.

1. In [!DNL Edge], click **[!DNL Microsoft Edge]** in the menu bar, **[!UICONTROL Settings]**, then click **Cookies and Site Permissions**. 

1. Scroll to **[!UICONTROL Insecure content]**.

1. Click **[!UICONTROL Insecure content]**, then click **[!UICONTROL Add]** next to **[!UICONTROL Allow]**, add the site on which to allow insecure content, then click **[!UICONTROL Add]**.

1. Reload the VEC page.
