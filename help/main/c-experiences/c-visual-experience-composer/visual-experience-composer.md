---
keywords: visual experience composer;vec;wysiwyg
description: Learn the basics of using the Visual Experience Composer (VEC) in Adobe Target. The VEC is a WYSIWYG editor that lets you easily create personalized experiences.
title: How Do I Use the Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
TQID: 'https://experienceleague.adobe.com/X4nfYuOtD3TVusnVIIEZhXwUdCZ-dMvbZeJlrkmI9Hs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Visual Experience Composer] (VEC)

The [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] is a WYSIWYG editor for creating and testing personalized experiences directly on websites and mobile web pages without editing code.

Create experiences and offers for [!DNL Target] activities by dragging and dropping elements, swapping content, and changing page layouts. The composer also provides options for editing HTML and JavaScript.

## Browser requirements {#browser-requirements}

[!DNL Safari] is supported for the [!DNL Adobe Target] interface, but not for the VEC. If you open the VEC in [!DNL Safari], an overlay prompts you to switch to [!DNL Google Chrome] to edit experiences.

Browsers such as [!DNL Firefox] might block pages that contain mixed content, such as a non-secure page within a secure site, from displaying in the VEC. If a page does not display, click the icon next to the URL in the browser address bar, then click **[!UICONTROL Disable protection on this page]**. This issue does not affect how pages display to site visitors.

## Open the VEC {#open-the-vec}

To set the page that opens by default in the VEC, enter a default [!UICONTROL Visual Experience Composer] URL on the [!DNL Target] **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab.

If you do not set a default URL, the VEC opens with a blank page where you can specify a URL.

![VEC highlighted](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Edit experiences {#edit-experiences}

### View and name experiences {#view-and-name-experiences}

Use the tabs in the [!UICONTROL Experiences] rail to view how your page appears to different audiences or with different experiences. Give each experience a descriptive name to make it easier to identify in the list.

For example, when testing the position of the Home link in your navigation bar, name the experience in which it appears first "Home link first."

![Rename an experience in the Experiences rail](/help/main/c-experiences/c-visual-experience-composer/assets/rename_exp.png)

### Select and modify elements {#select-and-modify-elements}

Move your cursor over the page to highlight individual elements with a context-sensitive box.

Click a highlighted element to display the editing options for that element type. For example, select an image and click **[!UICONTROL Change Image source]** to replace it, or select a button to change its text color.

![Editing options for a selected element](/help/main/c-experiences/c-visual-experience-composer/assets/properties-exp.png)

You cannot edit content inside an iframe embedded in the page. To edit that content, ensure that the iframe document is [!DNL Target]-enabled, then load the iframe URL directly in the VEC.

Changes to the page structure outside the VEC can affect locations used by an activity. If those locations change, [!DNL Target] might not be able to find the elements you modified, which can cause issues when editing experiences.

### Browse and design {#browse-and-design}

Click **[!UICONTROL Browse]** to navigate to a page accessible from the current page, such as a shipping page or shopping cart, and test changes there.

![Browse mode in the VEC](/help/main/c-experiences/c-visual-experience-composer/assets/browse_exp.png)

In Browse mode, you can also access elements that appear on hover, such as flyout menus and mini-carts. When you reach the page or element you want to edit, click **[!UICONTROL Design]** to edit the experience.

If a hover state depends on JavaScript, ensure that **[!UICONTROL Disable JavaScript]** is not selected. JavaScript must be enabled to edit elements that depend on it.

For details about the available editing options, see [Visual Experience Composer Options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

## Manage page loading {#manage-page-loading}

Some editing options remain available while a page loads or after it fails to load. You can also cancel page loading to access these options without waiting.

### Edit a page while the page is loading or after the page fails to load {#loading}

You can make some changes before a page finishes loading in the VEC or after it fails to load, for example, because custom code no longer works.

Use the available editing options to:

* Make simple changes, such as adding custom code or renaming an experience
* Copy existing custom code from a page that is no longer accessible
* Make simple edits to a page that cannot load in the VEC

The [!UICONTROL Experiences] rail, [!UICONTROL Components] rail, and [!UICONTROL Configure] options remain accessible while the page loads or after it fails to load.

### Cancel loading of a page within the VEC {#cancel-loading}

Cancel page loading in the VEC to edit the activity without waiting for the page to finish loading.

Canceling page loading is useful when you need to:

* Make minor edits to existing modifications
* Delete one or more existing modifications
* Insert or edit custom code
* Correct an incorrectly entered page URL
* Enable or disable JavaScript before loading the page in the VEC
* Add template testing rules to the [!UICONTROL Page Delivery] criteria
* Override the global [!UICONTROL Enhanced Experience Composer] (EEC) toggle when loading a page through the EEC or in iframe-only mode

After canceling page loading, you can switch between experiences in the activity without waiting for the page to load. Click **[!UICONTROL Reload]** to display the page in the VEC again.

>[!IMPORTANT]
>
>If you edit custom code or make other modifications after canceling page loading, perform quality assurance (QA) testing to verify that your changes are delivered as expected.

To stop page loading, click **[!UICONTROL Cancel Loading]** while the page is loading. The page remains unloaded for this activity during the current editing session unless you reload it.

Click **[!UICONTROL Reload]** to resume managing experiences in the current activity or add new modifications.
