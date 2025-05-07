---
keywords: visual experience composer;vec;wysiwyg
description: Learn the basics of using the Visual Experience Composer (VEC) in Adobe Target. The VEC is a WYSIWYG editor that lets you easily create personalized experiences.
title: How Do I Use the Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
---
# [!UICONTROL Visual Experience Composer] (VEC)

The [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] is a WYSIWYG editor that allows customers to create and test personalized experiences directly on their websites or mobile web pages without needing to edit code.

>[!NOTE]
>
>The [!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release included an updated version of the VEC. For information about how the updated VEC differs from the previous version, see [Visual Experience Composer changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md). For an overview of the various options in the updated VEC, see [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

The VEC lets you easily create and test personalized experiences and offers in the site context. You can create experiences and offers for [!DNL Target] activities by dragging and dropping, swapping, and modifying the layout and content of a web page (or offer) or mobile web page.

The VEC is one of the main features of [!DNL Target]. The VEC lets marketers and designers create and change content using a visual interface. Many design choices can be made without requiring direct editing of the code. Editing HTML and JavaScript is also possible using the editing options available in the composer.

On the [!DNL Target] **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab, you can enter the default [!UICONTROL Visual Experience Composer] URL.

This URL determines where you start when you open the VEC. If you do not enter a default URL, you start with a blank page when you open the editor, and then you can specify a URL.

![VEC highlighted](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

>[!NOTE]
>
>Certain browsers, such as [!DNL Firefox], might block a page from displaying in the VEC if the page contains mixed content (for example, a non-secure page in a secure site). If your page does not display, click the icon next to the URL in the browser address bar and click **[!UICONTROL Disable protection on this page]**. This issue does not affect the display of your pages to site visitors.

Content inside an iframe on the page can't be modified in the VEC. To edit content within an iframe, ensure that the iframe document is [!DNL Target]-enabled, then load that iframe URL in the VEC.

You can use the tabs in the [!UICONTROL Experiences] rail to view your page as it would appear to different audiences or with different experiences. You can provide a name for each experience. For example, if you are testing the location of the Home link in your nav bar, you might name an experience where the Home link appears first. For example, "Home link" to make it easier to identify the experiences in the list.

>[!NOTE]
>
>Changes to the structure of a page that affect the locations used in an activity created on that page can cause issues with experience editing. If a location has been changed outside the VEC, [!DNL Target] might not be able to find the location where the content was changed.

As you move your mouse around the page, a context-sensitive box follows the cursor, highlighting the elements on the page.

<!--Click the **[!UICONTROL Overlays]** icon to change the way the highlight displays. For example, you can choose to highlight only images, links, regional mboxes, modifications, or JavaScript. You can change the color of the highlight. You can also specify a highlight color and type of fill used to highlight different element types.

![Change Overlay settings](/help/main/c-experiences/c-visual-experience-composer/assets/change-overlay.png)-->

Click a highlighted element for a menu of options available for that element type. For example, you can click an image and select **[!UICONTROL Change Image]** to change the image to another image. Or click a button and change the text color.

You can also click **[!UICONTROL Browse]**, then navigate to a page that is available from the primary page, such as a shipping page or shopping cart, and test changes on that page. You can also access page elements that are available when you hover, such as flyout menus and mini-carts. When you are finished browsing to the page, click **[!UICONTROL Design]** to edit the experience. For example, you might want to change the design of a shopping cart drop-down or a carousel of images.

>[!NOTE]
>
>If a hover state depends on JavaScript, make sure **[!UICONTROL Disable JavaScript]** is not selected. JavaScript must be enabled to edit JavaScript elements.

For information about the options available in the VEC, see [Visual Experience Composer Options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

You can perform some modifications on a page while the page is loading (or after the page fails to load), or you can cancel page loading in the VEC. For more information, see:

* [Edit a page while the page is loading or after the page fails to load](#loading)
* [Cancel loading of a page within the VEC](#cancel-loading)

## Edit a page while the page is loading or after the page fails to load {#loading}

You can perform many actions before the page loads in the VEC, or even if the page fails to load altogether (for example, custom code is no longer operational).

Some reasons why you might want to access or make edits to a page while it is loading within the VEC or after it fails to load:

* You want to make a simple modification to a page, such as to add custom code or change an experience's name
* You want to copy existing custom code from a page that is no longer accessible
* You know that a page will not load within the VEC, but you want to make simple edits anyway

While the page loads (or after it fails to load), the [!UICONTROL Experiences] rail, [!UICONTROL Components] rail, and [!UICONTROL Configure] options are accessible.

## Cancel loading of a page within the VEC {#cancel-loading}

You can cancel the loading of a page within the VEC to unlock editing of the activity without waiting for the page to load. This feature saves time and helps you make simple edits or insert custom code more efficiently without waiting for the page to load within the VEC.

Some reasons why you might want to cancel page loading within the VEC include:

* You want to make minor edits to existing modifications
* You want to delete one or more existing modifications
* You want to insert or edit custom code
* You mistakenly entered the wrong URL for the page
* You want to enable or disable JavaScript before loading the page in the VEC
* You want to add more template testing rules to the [!UICONTROL Page Delivery] criteria
* You want to override the global [!UICONTROL Enhanced Experience Composer] (EEC) toggle when loading a page via the EEC or iframe-only

If you cancel page loading in the VEC you can switch between experiences in the activity without waiting for the page to load. To see the page within the VEC again, you must click the **[!UICONTROL Reload]** button.

>[!IMPORTANT]
>
>Be aware that when custom code or any modifications are made, by choosing to cancel loading within the VEC, you must ensure that your coding or changes are done properly. Ensure that you perform proper QA to ensure that your custom code and any other modifications are delivered as expected.

To cancel loading of a page within the VEC, click the **[!UICONTROL Cancel Loading]** button while the page is loading. The page will not load in the VEC for this activity during the current editing session.

To continue managing experiences in the current activity or to add new modifications, you must click the **[!UICONTROL Reload]** button.
