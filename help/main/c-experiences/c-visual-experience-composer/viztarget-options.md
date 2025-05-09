---
keywords: visual experience composer options;experience composer options;experience options;edit text;edit html;edit text/html;edit background color;background color;insert element;edit link;link;visual experience composer link;edit css class;css class;swap offer;offer swap;swap image;image swap;remove item;item remove;hide item;item hide;rearrange;move element;element move;resize element;element resize;element;expand selection;navigate to this link;navigate link;link navigate;navigate;link;undo;redo;undo/redo;custom events;web components;offer decision;offer decisioning
description: Explore the options available in the [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).
title: How Do I Use the [!UICONTROL Visual Experience Composer] (VEC) Options?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
---
# Visual Experience Composer options

The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2015) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the updated UI and its options.

>[!TIP]
>
>To to learn how the updated VEC differs from the legacy VEC, see [Visual Experience Composer changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md).

>[!IMPORTANT]
>
>The updated [!UICONTROL Visual Editing Composer] requires the [!DNL Adobe Experience Cloud] [[!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) available on the [!DNL Chrome Web Store].

The VEC displays when you create or edit an existing activity.

![Visual Experience Composer (VEC)](/help/main/c-experiences/c-visual-experience-composer/assets/new-vec.png)

## VEC UI overview

The following sections explain the options available in the updated VEC for an [!UICONTROL A/B Test] activity. The options vary, depending on the activity type.

### [!UICONTROL Experiences] rail

The [!UICONTROL Experiences] rail displays in the left rail of the VEC.

![Experiences rail](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

You can view, create, rename, or remove experiences using the [!UICONTROL Experiences] rail. 

The following options are available in the [!UICONTROL Experiences] rail: 

* **View an experience**: To view an experience, click the desired experience to display it in the [!UICONTROL Design] canvas.
* **Add an experience**: Click the **[!UICONTROL Add]** icon ( ![Add icon](/help/main/assets/icons/Add.svg) ) to add a new experience. Configure the new experience as desired.
* **Rename an experience**: Click the **[!UICONTROL Rename]** icon ( ![Rename icon](/help/main/assets/icons/Rename.svg) ) to display the [!UICONTROL Rename Experience] dialog box. Specify the new name, then click **[!UICONTROL Save]**.
* **Duplicate, delete, or redirect an experience**: Click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ), then choose **[!UICONTROL Duplicate]**, **[!UICONTROL Delete]**, or **[!UICONTROL Redirect to URL]**.

### Activity settings/configuration {#settings}

Click the [!UICONTROL Configure] icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ) displayed on top of the [!UICONTROL Design] canvas to display the activity properties menu.

![Activity configurations options](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

The following options are available:

* **[!UICONTROL Properties]**: Assign properties to the activity or remove properties from the activity. [!UICONTROL Properties] is a ([[!DNL Target Premium]](/help/main/c-intro/intro.md#premium) feature. For more information, see [Enterprise user permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).
* **[!UICONTROL Page Delivery]**: Include the same experience on similar pages on your site. Use a page template to provide structure to your pages, or if your pages contain similar elements, to test variations in similarly structured page elements or across your entire domain. For more information, see [Include the same experience on similar pages](/help/main/c-experiences/c-visual-experience-composer/temtest.md).
* **[!UICONTROL Site Preferences]**: Configure your site preferences to specify how [!DNL Target] generates CSS selectors. For more information, see _CSS selectors_ in [Configure the [!UICONTROL Visual Experience Composer]](/help/main/administrating-target/visual-experience-composer-set-up.md).
* **Add Additional Pages**: Add additional pages to the activity to create a multipage activity that lets you create a story over multiple pages, with a design that is specific to each page. For more information, see [Multipage activity](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md).
* **Single Audience**: Use a single audience for the activity.
* **Multiple Audiences**: Assign multiple audiences to the activity. Click the Add Audiences icon ( ![Add icon](/help/main/assets/icons/Add.svg) ), then select one or more audiences from the list. You can also [combine audiences](/help/main/c-target/combining-multiple-audiences.md) or [create a new audience](/help/main/c-target/c-audiences/create-audience.md) from the [!UICONTROL Add Audiences] dialog box.

### [!UICONTROL Design]/[!UICONTROL Browse] modes

Use the [!UICONTROL Design]/[!UICONTROL Browse] toggles displayed on top of the design canvas to switch between design and browse mode.

![Design and browse toggles](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

Use the [!UICONTROL Browse] mode to navigate your site and to pick the view or page you want to update. Switch back to [!UICONTROL Design] mode to add or edit your changes.

### [!UICONTROL Undo]/[!UICONTROL Redo]

You can undo changes made by clicking the [!UICONTROL Undo] icon ( ![Undo icon](/help/main/assets/icons/Undo.svg) ). 

![Undo icon in VEC](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

To redo an action, expand the [!UICONTROL ]Undo/[!UICONTROL Redo] button group and choose [!UICONTROL Redo].

### [!UICONTROL Components] rail

You can add a number of components to your web page and edit them as needed by using the new [!UICONTROL Components] rail.

![Components rail](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

>[!NOTE]
>
>If you see the [!UICONTROL Modifications] rail in this area instead of the [!UICONTROL Components] rail, click the **[!UICONTROL Show Components]** icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ). The [!UICONTROL Show Components] icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ) and the [!UICONTROL Show Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) act as toggles to show the appropriate options.

To add a new component to an experience: 

1. Click the desired component that you want to add to highlight it.

   The available components are grouped into logic containers:

    * [!UICONTROL Basic]
      * [!UICONTROL Divider]
      * [!UICONTROL HTML]
      * [!UICONTROL Image]
    * [!UICONTROL Text]
      * [!UICONTROL Heading]
      * [!UICONTROL Paragraph]
      * [!UICONTROL Link]
    * [!UICONTROL Dynamic]
      * [[!UICONTROL Recommendation]](/help/main/c-recommendations/recommendations-as-an-offer.md)
      * [[!UICONTROL Experience Fragment]](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md)
      * [[!UICONTROL HTML Offer]](/help/main/c-experiences/c-manage-content/manage-content.md)
    
1. Drag the component over an existing page element in the [!UICONTROL Design] canvas. 
1. Choose to insert the component before of after the selected element. 

   As compared to the previous VEC version, you cannot replace a selected element with a component.

### [!UICONTROL Modifications] rail

To open the [!UICONTROL Modifications] rail, click the [!UICONTROL Show Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) in the [!UICONTROL Components] rail.

![Modifications rail](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

>[!NOTE]
>
>The [!UICONTROL Show Components] icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ) and the [!UICONTROL Show Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) act as toggles to show the appropriate options.

The [!UICONTROL Modifications] rail shows all changes that have been made to your page in the [!UICONTROL Visual Experience Composer] (VEC) and lets you make additional changes (such as CSS Selector, Mbox, and Custom Code).

Click the **[!UICONTROL More Options]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) in the rail header to add a modification, delete all modifications, or delete all invalid modifications. Click [!UICONTROL Select] to perform bulk operations: [!UICONTROL Apply to All Pages] or [!UICONTROL Delete].

Click the **[!UICONTROL More Options]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) next to each modification to view its information, delete the modification, or to apply the modification to more views.

### [!UICONTROL Design] canvas

The [!UICONTROL Design] canvas lets you select viewports, including fit-to screen, [!UICONTROL Desktop], [!UICONTROL Tablet], [!UICONTROL Mobile Landscape], and [!UICONTROL Mobile Portrait]. By default, the canvas fits the page to the screen along with the viewports defined in the [Administration](/help/main/administrating-target/visual-experience-composer-set-up.md) section.

![Viewport options](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png) 

You can also zoom in or zoom out by clicking the appropriate icon ( ![Zoom In icon](/help/main/assets/icons/ZoomIn.svg) or ![Zoom Out icon](/help/main/assets/icons/ZoomOut.svg) ).

When you click a page element in the [!UICONTROL Design] canvas, a menu shows the options that are available for that element type. In addition, a DOM path displays at the bottom of the page that lets you easily navigate through the page structure.

The various [!UICONTROL Visual Experience Composer] (VEC) actions are grouped in appropriate menu options to make your job quicker and more efficient:

![VEC options menu](/help/main/c-experiences/c-visual-experience-composer/assets/vec-options.png)

>[!NOTE]
>
>The available options depend on the activity type and element that you are creating or editing. For more information about editing images and offers in an [!UICONTROL A/B Test] activity, see [Edit elements using the [!UICONTROL Design] canvas](#design) below.

### [!UICONTROL Properties] rail

The [!UICONTROL Properties] rail lets you change properties of selected elements on the page, whether these elements are HTML elements or objects specific to [!DNL Target], such as recommendations or offers.

![Properties rail](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

Click the icons on top of the rail to edit HTML code or delete, duplicate, or hide elements. Changes appear in the [!UICONTROL Modifications] rail.

The [!UICONTROL Properties] rail is collapsible in the right rail. Click the [!UICONTROL Show/Hide Properties] icon ( ![Properties icon](/help/main/assets/icons/Propertie.svg) ) to the right of the rail to collapse or display the [!UICONTROL Properties] rail.

## Edit elements using the [!UICONTROL Design] canvas {#design}

The following sections show you how to edit images and text in the [!UICONTROL Design] canvas. The Design canvas, along with the Components, Modifications, and Properties rails provide you with powerful tools to let you easily create experiences for your activities.

### Image options

If you click an image in an [!UICONTROL A/B Test] activity, the VEC looks like similar to the following illustration:

![VEC with image selected](/help/main/c-experiences/c-visual-experience-composer/assets/vec-image.png)

Select components from the [!UICONTROL Components] frame on the left side to insert the following elements:

* Basic (divider, HTML, image).
* Text (heading, paragraph, link).
* Dynamic ([Recommendation](/help/main/c-recommendations/recommendations-as-an-offer.md), [Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), HTML offer).

The menu at the top of the image lets you do the following:

* Insert a link ( ![Insert Link icon](/help/main/assets/icons/Link.svg) ).
* Change the image ( ![Choose Image icon](/help/main/assets/icons/Images.svg) ).
* Add personalization ( ![Add Personalization icon](/help/main/assets/icons/PersonalizationField.svg) ).
* Delete the image ( ![Delete icon](/help/main/assets/icons/Delete.svg) ).

The [!UICONTROL Properties] pane on the right side lets further configure the image's properties.

The icons at the top of the frame let you do the following:

* Edit the HTML ( ![Insert HTML icon](/help/main/assets/icons/Code.svg) ). See [Edit HTML](#html) below for more information.
* Duplicate the image ( ![Duplicate icon](/help/main/assets/icons/Code.svg) ).
* Delete the image ( ![Delete icon](/help/main/assets/icons/Delete.svg) ).
* Hide the image ( ![Hide icon](/help/main/assets/icons/VisibilityOff.svg) ). 

The options in the right frame let you do the following:

* Edit the CSS class.
* Configure the image's properties (source, title, alt text).
* Edit the link URL.
* Configure the image's size (height and width). Click [!UICONTROL Show Advanced Options] to configure the image's minimum and maximum size, width, height, overflow, and object fit.
* Configure the image's position on your page (absolute, fixed, relative, static, or sticky.)
* Configure the element's spacing, including margin and padding.
* Configure the element's effects (opacity). Click [!UICONTROL Show Advanced Options] to configure the image's sepia, grayscale, contrast, brightness, and blur values. You can also invert or rotate the image.
* Configure the image's inline styles.

### Text options

If you click text in an [!UICONTROL A/B Test] activity, the VEC looks like similar to the following illustration:

![VEC with text selected](/help/main/c-experiences/c-visual-experience-composer/assets/vec-text.png)

Select components from the [!UICONTROL Components] frame on the left side to insert the following elements:

* Basic (divider, HTML, image).
* Text (heading, paragraph, link).
* Dynamic ([Recommendation](/help/main/c-recommendations/recommendations-as-an-offer.md), [Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), HTML offer).

Click the [!UICONTROL Show Modifications] icon ( ![Show Modifications icon](/help/main/assets/icons/History.svg) ) to display the modifications to the experience.

The menu at the top of the text element lets you do the following:

* Configure the text's properties (heading level, paragraph, block quote, or monospace)
* Select the text's color ( ![Text Color icon](/help/main/assets/icons/TextColor.svg) )
* Configure the text's attributes (bold, italic, underline, or strike through) ( ![Choose text Attributes icon](/help/main/assets/icons/Text.svg) ).
* Configure the text's alignment (left, center, right, justify) ( ![Text Alignment icon](/help/main/assets/icons/TextAlignCenter.svg) ).
* Insert a link ( ![Insert Link icon](/help/main/assets/icons/Link.svg) ).
* Replace the content with an HTML offer, [Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), or [Recommendation](/help/main/c-recommendations/recommendations-as-an-offer.md).
* Edit the HTML ( ![Insert HTML icon](/help/main/assets/icons/Code.svg) ).
* Add personalization ( ![Add Personalization icon](/help/main/assets/icons/PersonalizationField.svg) ).
* Delete the image ( ![Delete icon](/help/main/assets/icons/Delete.svg) ).

The [!UICONTROL Properties] rail on the right side lets further configure the text's properties.

The icons at the top of the frame let you do the following:

* Edit the HTML ( ![Insert HTML icon](/help/main/assets/icons/Code.svg) ). See [Edit HTML](#html) below for more information.
* Duplicate the text ( ![Duplicate icon](/help/main/assets/icons/Code.svg) ).
* Delete the text ( ![Delete icon](/help/main/assets/icons/Delete.svg) ).
* Hide the text ( ![Hide icon](/help/main/assets/icons/VisibilityOff.svg) ).

The options in the right frame let you do the following:

* Edit the CSS class.
* Configure the text's background color and image.
* Configure the text's typography (heading style, font size, font weight, line height, alignment, text color, text style (bold, italic, underlined, or strike through)).
* Configure lists, including bulleted, numbered, or A,B,C.
* Choose the border color.
* Configure the text box's size (height and width). Click [!UICONTROL Show Advanced Options] to configure the text box's minimum and maximum size, width, height, overflow, and object fit.
* Configure the text box's position on your page (absolute, fixed, relative, static, or sticky) and set the number of pixels from the top, right, bottom, and left.
* Configure the element's spacing, including margin and padding.
* Configure the element's effects (opacity). Click [!UICONTROL Show Advanced Options] to configure the image's sepia, grayscale, contrast, brightness, and blur values. You can also invert or rotate the text.
* Configure the inline styles.

## Edit HTML

In addition to HTML code, you can edit and inject custom JavaScript.

Several rich text formatting options are available when editing text and HTML for [!UICONTROL A/B] and [!UICONTROL Experience Targeting] activities. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and the rich-editing view of the HTML.

The following HTML5 tags can be nested:

|Tag|Allowed Nested Tags|
| --- | --- |
|`<a>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>`|
|`<ins>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`|
|`<del>`|`<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>`|
|`<label>`|`<p>`|

## Navigate elements using the DOM path {#dom-path}

When you click an element on the page, the VEC options menu displays. In addition, when you click an element, the corresponding DOM path displays at the bottom of the page.

![DOM path](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path-refresh.png)

If you do not see the DOM path, click the [!UICONTROL Show DOM] icon ( ![Show DOM icon](/help/main/assets/icons/LayersBringToFront.svg) ).

You can use the DOM path to quickly see information about the selected element (type, ID, and class) and move up or down the DOM path to select the desired element.

<!--When you hover over the DOM path, a blue box highlights the corresponding element in the VEC. When you click the element, an orange box highlights the element and the VEC options menu displays, as explained above.-->

You can easily navigate to any parent, sibling, or child element within the VEC using the DOM path.

The DOM path feature is also available when setting up [click tracking](/help/main/c-activities/r-success-metrics/click-tracking.md).

<!--## [!UICONTROL Edit]

The following options are available:

### [!UICONTROL Text/HTML] {#edit-text-html}

Change the HTML code for the element, such as the text for a text area, button, or link.

In addition to HTML code, you can edit and inject custom JavaScript.

Several rich text formatting options are available when editing text and HTML for [!UICONTROL A/B] and [!UICONTROL Experience Targeting] activities. You can choose a font, select a font style, change text alignment, and other standard text formatting options. When modifying HTML, you can toggle between the code view and rich-editing view of the HTML.

The following HTML5 tags can be nested:

|Tag|Allowed Nested Tags|
| --- | --- |
|`<a>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>`|
|`<ins>`|`<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`|
|`<del>`|`<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>`|
|`<label>`|`<p>`|

### [!UICONTROL Background Color]

Use the color picker to select or configure a background color. You can select a color swatch, and adjust it using RGB values or color hex codes. The red x in the color picker makes the background transparent.

**Note:** This option is not available for an element where a background image is set. 

### [!UICONTROL Styles] {#styles}

Use the [!UICONTROL Styles] panel to view or edit the value of existing styles for the selected element. You can also add additional styling.

To access the [!UICONTROL Styles] panel, click a page element from within the VEC, then click **[!UICONTROL Edit]** > **[!UICONTROL Styles]**.

The [!UICONTROL Styles] panel displays on the right side of the VEC. The panel contains a list of styles that lets you edit or add to the selected element. A real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.

![Styles panel](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

As you apply different styles, you can always revert your changes by clicking the [!UICONTROL Revert] icon that displays at the top-right corner of the [!UICONTROL Styles] panel after you change any section. Clicking the [!UICONTROL Revert] icon reverts all changes on the current section's panel.

Expand each section to edit or add styles, as explained below. To save your changes, click the [!UICONTROL Back] icon at the top of the panel to return to the panel's main display, then click **[!UICONTROL Save]**. 

Blue dots on the main panel and next to each option on the various section panels indicate that you have changed the corresponding styles. This visual indicator makes it easy for you to review your changes before clicking [!UICONTROL Save].

>[!NOTE]
>
>Quick actions for layout changes, background color, resizing, and move are also available as separate actions in the VEC menu. These options can be used as separate actions or you can use the Styles menu, as explained here.

* **[!UICONTROL Background]**

  Change the background color and image.

  * Color (specify the color code or use the color picker)
  * Image (select an image from the image picker)
  * Image source (specify an external URL)
  * Attachment
    * Click the top drop-down list to select scroll, fixed, or local
    * Click the bottom drop-down list to select repeat, repeat-x, repeat-y, no-repeat, space, or round
  * Clip
    * Click the top drop-down list to select border-box, padding-box, content-box, or text
    * Click the bottom drop-down list to select auto audio or audio

* **[!UICONTROL Typography]**

  Change the typography of an element. Typography edits are quick and easy. 

  Although the rich text editor (Edit Text/HTML) is available for fine tuning, quick actions to change the entire element is available via this option. If you want to apply typography changes to only a part of the text (not to the full text), use the [rich text editor](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md). 

  You can edit the following typography styles:

  * [!UICONTROL Font size]
  * [!UICONTROL Font weight]
  * [!UICONTROL Font style]
  * [!UICONTROL Color] (specify the color code or use the color picker)
  * [!UICONTROL Word spacing]
  * [!UICONTROL Line height]
  * [!UICONTROL Text alignment]

* **[!UICONTROL Margin]**

  Change the margin for the selected element. You can change the left, right, bottom, and top margins.

  Click the drop-down icon for each margin to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to set the margin or specify the number of pixels for each margin)

  Margin supports positive and negative values.

  Target also supports other size units, such as rem, pc, em. For more information about these units, see [Web Style Sheets CSS Tips and Tricks](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Padding]**

  Change the padding for the selected element. You can change the left, right, bottom, and top padding.

  Drag the slider to set the padding or specify the number of pixels for padding.

  Padding supports width scales from 0 onwards.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Border]**

  Click the border icons at the top of the panel to change the selected element's border.

  You can edit the following styles for each border (top, right, bottom, and left):

  * [!UICONTROL Border style] (none, hidden, dotted, dashed, solid, or double)
  * [!UICONTROL Border color] (specify the color code or use the color picker)
  * [!UICONTROL Border width] (drag the slider to select a border width or specify the width in pixels)

  Border supports width scales from 0 onwards.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Position]**

  Move the selected element from its current position. You can change the element's top, bottom, left, right, and [Z-index](https://www.w3schools.com/cssref/pr_pos_z-index.asp) position.

  Click the [!UICONTROL Static] drop-down list to choose from the following position options:

  * [!UICONTROL Static]
  * [!UICONTROL Relative]
  * [!UICONTROL Absolute]
  * [!UICONTROL Sticky]
  * [!UICONTROL Fixed]

  Click the drop-down icon for each position to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to position the element or specify the number of pixels you want to move the element)

  Position supports positive and negative values.

  Target also supports [other size units](https://www.w3.org/Style/Examples/007/units.en.html), such as rem, pc, em.

* **[!UICONTROL Size]**

  Change the selected element's width and height.

  Click the drop-down icon next to [!UICONTROL Width] and [!UICONTROL Height] to choose from the following options:

  * [!UICONTROL Auto] 
  * [!UICONTROL Value] (drag the slider to size the element or specify the number of pixels for each dimension)

* **[!UICONTROL Filter]**

  Drag the slider for each filter option or specify the desired percentage:

  * [!UICONTROL Sepia]
  * [!UICONTROL Contrast]
  * [!UICONTROL Brightness]
  * [!UICONTROL GrayScale]
  * [!UICONTROL Blur]
  * [!UICONTROL Opacity]
  * [!UICONTROL Invert]
  *[!UICONTROL  Hue-rotate]
  * [!UICONTROL Saturate]

* **[!UICONTROL CSS Editor]**

  The real-time CSS Editor lets you view changes and add styles if you are comfortable using Cascading Style Sheets (CSS) or if you receive code from your developer.

  The CSS Editor displays any changes that you make in the Styles panel. As shown in the illustration below, the font size, top border, and image size have been changed:

  ![CSS editor with changes](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

  Notice the blue dots next to the [!UICONTROL Typography], [!UICONTROL Border], and [!UICONTROL Size] options in the preceding illustration. These dots indicate that you have changed these sections. If you open these section panels, blue dots display next to the specific options that you changed.

  You can type your own code if your desired style is not available by default in the [!UICONTROL Styles].

  The CSS Editor shows details for the current session only. If you save changes and then reopen the editor, details about your previous change do not display in the editor, even if you select the same element again.

  >[!IMPORTANT]
  >
  >You can apply a background image using the CSS Editor, but it might cause flicker. Test your changes before deployment.

### [!UICONTROL CSS Class]

Specify the predefined CSS class used for the element. If more than one element is selected, separate multiple CSS classes with a space.

Available for [!UICONTROL A/B], [!UICONTROL Automated Personalization], and [!UICONTROL Multivariate Test] activities.

### [!UICONTROL Link]

Change the URL in the link.

Use Edit Link to update the selector to point to the same image element. However, linking to a different image element is not supported. To link to a different image element, delete the original action from the code editor and use the [!UICONTROL Visual Experience Composer] to apply the action on the other image element.

## [!UICONTROL Insert Before]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], and [!UICONTROL Text]

Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.

Select an element on the page, then click [!UICONTROL Insert Before] and choose whether you want to insert an image, HTML, or text. The inserted element appears before the selected element.

The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.

[!UICONTROL Recommendations] supports [!UICONTROL Insert Before] the contents of DIV, SECTION, and ARTICLE tags.

**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Insert After]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], and [!UICONTROL Text]

Add any kind of element to your page in addition to modifying existing content. Add text, code, lists, and more to create entirely different experiences to test.

Select an element on the page, then click [!UICONTROL Insert After] and choose whether you want to insert an image, HTML, or text. The inserted element appears after the selected element.

The behavior of the inserted element depends on the structure of your page, your CSS, and other page configuration options. Valid HTML is required to make your page appear correctly. Always test your page after inserting an item to make sure it appears as expected.

[!UICONTROL Recommendations] supports [!UICONTROL Insert After] the contents of DIV, SECTION, and ARTICLE tags.

**Note:** Inserting an image requires that [!DNL Adobe Scene7 Publishing System] is enabled so you have access to the image library.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Replace Content]

The following options are available:

### [!UICONTROL Offer Decision]

Add an [offer created in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} to present the best offer and experience to your customers using offer decisioning.

**Note:** This option is available when editing or creating [manual [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) or [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activities only. This option is not available for other activity types.

For more information, see [Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image]

Select a different image from the Content Library. The images available for swapping include the images uploaded to the Experience Cloud assets folder or uploaded in the Content Library in Target.

During initial activity creation, the URL displayed is not the URL used for delivery. Upon activity synching, that URL is updated to a production Scene7 URL.

For example, the initial URL might look like the following example:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

After activity syncing, the delivery URL might look like the following example:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations supports Replace With in DIV, SECTION, and ARTICLE tags.

**Note:** Swapping images requires an Adobe Scene7 Publishing System Account.

### [!UICONTROL HTML Offer]

Select a different offer from the [!UICONTROL Content Library].

**Note:** HTML Offers are stored on [!DNL Target] servers.

An HTML offer can be up to 256 KB.

### Recommendation

Include recommendations inside A/B Test (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities. For more information, see [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Insert experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization. For more information, see [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Layout]

The following options are available:

### [!UICONTROL Rearrange]

Drag the element to another location inside the same parent element or DIV. Other elements shift location to make space for the rearranged element.

**Note**: Click-tracking does not work on rearranged items.

Currently, certain VEC actions, such as [!UICONTROL Rearrange] and [!UICONTROL Move], assume that the sibling elements of the source and destination parent elements are completely loaded. If lazy loading occurs under the parent DOM elements (source or destination), these VEC actions can cause inconsistent behavior. We are working on a more reliable approach to make VEC actions work in lazy-loaded DOM elements. As a temporary workaround, you can use [!UICONTROL Custom Code] in these scenarios to render your experiences.

### [!UICONTROL Resize]

Resize an element on your page. When you select [!UICONTROL Resize], a handle appears in the bottom-right corner of the element that lets you drag that corner to resize. Hold the Shift key to retain the same aspect ratio.

**Note:** Inline elements cannot be resized.

### [!UICONTROL Move] {#move}

Move elements on your page. Unlike the [!UICONTROL Rearrange] option, [!UICONTROL Move] does not shift other elements to make room for the element being moved. Use the arrow keys to fine tune the move. (Planned enhancement: support to ensure moved elements are not hidden behind other elements.)

In certain situations, such as when a CSS restriction requires an element to remain inside its parent element, you cannot move the element outside its parent. An element cannot be moved outside of a container that has following CSS property: `overflow: hidden`.

See [!UICONTROL Rearrange] above for more information about inconsistent behavior with the [!UICONTROL Move] and [!UICONTROL Rearrange] actions due to lazy loading of DOM elements.

### [!UICONTROL Hide]

Hide the element. The white space remains, but the content is removed.

### [!UICONTROL Remove]

Remove the element. The white space behind the image is removed and the space where the element was is collapsed.

**Note:** Items within a "classic" mbox (an mbox created within a Target Classic campaign) cannot be removed using this option.

## [!UICONTROL Expand Section]

Select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times.

## [!UICONTROL Navigate to Link]

Open the destination of the link.

## [!UICONTROL Undo]/[!UICONTROL Redo]

Undo changes you make to your activities during an editing session. You can also redo changes that have been previously undone.

## Considerations {#considerations}

* If an offer contains HTML content, see "How at.js renders offers with HTML content" in [How at.js works](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank} for more information.

## Custom element support {#custom}

The VEC supports [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components) to let you create and test personalized experiences and offers on custom elements and on elements inside custom elements. This functionality is available in the VEC for all [!DNL Target] activity types.

>[!NOTE]
>
>VEC support for custom elements is supported in [at.js version](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} 2.7.0 (or later){target=_blank}. Ensure that your website has the required version deployed. If you are using the [Visual Experience Composer helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), it must also have the required version of at.js deployed. The VEC options described above are not visible and available for use with non-supported versions of at.js.
>
>VEC support for custom elements is currently not supported with the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

Most VEC actions are supported on custom events and inside custom events, with the following exceptions: 

The following actions are not available on custom elements:

* [!UICONTROL Edit]
  * [!UICONTROL Text/HTML]
  * [!UICONTROL Link]
  * [!UICONTROL Edit Source]

* [!UICONTROL Replace Content]

The following action is not available inside custom elements:

* [!UICONTROL Layout]
  * [!UICONTROL Rearrange]-->
