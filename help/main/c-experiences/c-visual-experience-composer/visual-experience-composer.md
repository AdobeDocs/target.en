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
# Get started with the [!UICONTROL Visual Experience Composer] {#vec-overview}

>[!BEGINSHADEBOX]

**On this page:** Learn how to open the [!UICONTROL Visual Experience Composer] (VEC), edit experiences, and manage page loading.

>[!ENDSHADEBOX]

The [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] is a WYSIWYG editor for creating and testing personalized experiences directly on websites and mobile web pages, without editing code.

Experiences and offers for [!DNL Target] activities are created by dragging and dropping elements, swapping content, and changing page layouts. The composer also provides options for editing HTML and JavaScript.

## Browser requirements {#browser-requirements}

[!DNL Safari] is supported for the [!DNL Adobe Target] interface. Form-based activities can be created in [!DNL Safari] with all functionality, except the VEC and the [!UICONTROL Enhanced Experience Composer] (EEC). If the VEC is opened in [!DNL Safari], an overlay prompts the user to switch to [!DNL Google Chrome] to edit experiences.

Browsers such as [!DNL Firefox] might block pages that contain mixed content, such as a non-secure page within a secure site, from displaying in the VEC. If a page does not display, click the icon next to the URL in the browser address bar, then click **[!UICONTROL Disable protection on this page]**. This issue does not affect how pages display to site visitors.

## Open the VEC {#open-the-vec}

To set the page that opens by default in the VEC, enter a default [!UICONTROL Visual Experience Composer] URL on the [!DNL Target] **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab. If no default URL is set, the VEC opens with a blank page where a URL can be specified.

![Administration page with the Visual experience composer tab highlighted, showing the Default URL, Enhanced Experience Composer, and Load Mixed Content settings](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Edit experiences {#edit-experiences}

### View and name experiences {#view-and-name-experiences}

The tabs in the **[!UICONTROL Experiences]** rail show how the page appears to different audiences or with different experiences. A descriptive name for each experience makes it easier to identify in the list. For example, when testing the position of the Home link in a navigation bar, the experience in which it appears first can be named "Home link first."

![Rename Experience dialog with the name Home link first, opened from the rename icon of Experience B](/help/main/c-experiences/c-visual-experience-composer/assets/rename_exp.png)

### Select and modify elements {#select-and-modify-elements}

Moving the cursor over the page highlights individual elements with a context-sensitive box. Clicking a highlighted element displays the editing options for that element type. For example, selecting an image and clicking **[!UICONTROL Change Image Offer]** replaces it, and selecting a button allows changing its text color.

![Editing options displayed above a selected image](/help/main/c-experiences/c-visual-experience-composer/assets/properties-exp.png)

Content inside an iframe embedded in the page cannot be edited. To edit that content, ensure that the iframe document is [!DNL Target]-enabled, then load the iframe URL directly in the VEC.

Changes to the page structure outside the VEC can affect the locations used by an activity. If those locations change, [!DNL Target] might not be able to find the elements that were modified, which can cause issues when editing experiences.

### Browse and design {#browse-and-design}

Click **[!UICONTROL Browse]** to navigate to a page accessible from the current page, such as a shipping page or shopping cart, and test changes there.

![Browse mode in the VEC, with the URL field and the back and forward arrows](/help/main/c-experiences/c-visual-experience-composer/assets/browse_exp.png)

In Browse mode, elements that appear on hover, such as flyout menus and mini-carts, can also be accessed. When the page or element to edit is reached, click **[!UICONTROL Design]** to edit the experience.

If a hover state depends on JavaScript, ensure that **[!UICONTROL Disable JavaScript]** is not selected. JavaScript must be enabled to edit elements that depend on it.

For details about the available editing options, see [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

## Manage page loading {#manage-page-loading}

Some editing options remain available while a page loads or after it fails to load. Page loading can also be canceled to access these options without waiting.

### Edit a page while the page is loading or after the page fails to load {#loading}

Some changes can be made before a page finishes loading in the VEC, or after it fails to load, for example because custom code no longer works.

The available editing options allow the following:

* Make simple changes, such as adding custom code or renaming an experience
* Copy existing custom code from a page that is no longer accessible
* Make simple edits to a page that cannot load in the VEC

The **[!UICONTROL Experiences]** rail, **[!UICONTROL Components]** rail, and **[!UICONTROL Configure]** options remain accessible while the page loads or after it fails to load.

### Cancel loading of a page within the VEC {#cancel-loading}

Canceling page loading in the VEC allows editing the activity without waiting for the page to finish loading. This is useful to:

* Make minor edits to existing modifications
* Delete one or more existing modifications
* Insert or edit custom code
* Correct an incorrectly entered page URL
* Enable or disable JavaScript before loading the page in the VEC
* Add template testing rules to the **[!UICONTROL Page Delivery]** criteria
* Override the global [!UICONTROL Enhanced Experience Composer] (EEC) toggle when loading a page through the EEC or in iframe-only mode

After page loading is canceled, it is possible to switch between experiences in the activity without waiting for the page to load. Click **[!UICONTROL Reload]** to display the page in the VEC again.

>[!IMPORTANT]
>
>If custom code is edited or other modifications are made after page loading is canceled, perform quality assurance (QA) testing to verify that the changes are delivered as expected.

To stop page loading, click **[!UICONTROL Cancel Loading]** while the page is loading. The page remains unloaded for this activity during the current editing session, unless it is reloaded.

Click **[!UICONTROL Reload]** to resume managing experiences in the current activity or add new modifications. 
