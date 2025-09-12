---
keywords: visual experience composer;vec;wysiwyg
description: Understand the changes introduced in the Visual Experience Composer (VEC) in the Adobe Target 25.2.1 release (February 17, 2025).
title: What changes are introduced in the new Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 4c7a5657-93d9-4355-9d2b-c992b36bcb50
---
# [!UICONTROL Visual Experience Composer] changes

The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2015) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the previous and updated versions of the VEC.

>[!IMPORTANT]
>
>The updated [!UICONTROL Visual Editing Composer] requires the [!DNL Adobe Experience Cloud] [[!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) available in the [!DNL Chrome Web Store].

The VEC displays when you create or edit an existing activity.

![Visual Experience Composer (VEC)](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Major changes to the VEC

The following sections explain the major changes in the updated VEC compared to the previous version.

### [!UICONTROL Experiences] rail

Like in the previous version, the [!UICONTROL Experiences] rail remains on the left side of the VEC. The [!UICONTROL Experiences] rail cannot be collapsed.

![Experiences rail](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

You can create, rename or remove experiences using the [!UICONTROL Experiences] rail. Click the **[!UICONTROL Add]** icon ( ![Add icon](/help/main/assets/icons/Add.svg) ) to add a new experience. Click the [!UICONTROL More Actions] icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) to duplicate, delete, or redirect an experience.

### [!UICONTROL Components] rail (new)

You can add a number of components to your web page and edit them as needed by using the new [!UICONTROL Components] rail.

![Components rail](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

To add a new component, select the desired component from the [!UICONTROL Components] rail, hover over an existing element in the page, then choose to insert the component before of after the selected element.

>[!NOTE]
>
>If you see the [!UICONTROL Modifications] rail in this area instead of the [!UICONTROL Components] rail, click the **[!UICONTROL Show Components]** icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ). The [!UICONTROL Show Components] icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ) and the [!UICONTROL Show Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) act as toggles to show the appropriate options.
>
>To collapse the [!UICONTROL Components] rail and enlarge the [!UICONTROL Design] canvas, while the [!UICONTROL Components] rail is open, click the ( ![Show Components icon](/help/main/assets/icons/Add.svg) ) icon.

### [!UICONTROL Modifications] rail

To open the [!UICONTROL Modifications] rail, click the [!UICONTROL Show Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) in the [!UICONTROL Components] rail. The [!UICONTROL Modifications] rail changed position from the right side to the left side of the editing canvas.

![Modifications rail](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

>[!NOTE]
>
>The [!UICONTROL Show Components] icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ) and the [!UICONTROL Show Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) act as toggles to show the appropriate options. 
>
>To collapse the [!UICONTROL Modifications] rail and enlarge the [!UICONTROL Design] canvas, while the [!UICONTROL Modifications] rail is open, click the [!UICONTROL Show Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) icon.

The [!UICONTROL Modifications] rail shows all changes that have been made to your page in the VEC and lets you make additional changes (such as CSS Selector, Mbox, and Custom Code).

Click the [!UICONTROL More Options] icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) to add a modification, delete all modifications, or delete all invalid modifications. Click [!UICONTROL Select] to perform bulk operations: [!UICONTROL Apply to All Pages] or [!UICONTROL Delete].

To display the [!UICONTROL Modifications] rail again, click the [!UICONTROL Hide Modifications] icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) in the [!UICONTROL Modifications] rail.

### [!UICONTROL Properties] rail (new)

The [!UICONTROL Properties] rail lets you change properties of selected elements on the page, whether these elements are HTML elements or objects specific to [!DNL Target], such as recommendations or offers.

![Properties rail](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

Click the icons on top of the rail to edit HTML code or delete, duplicate, or hide elements. Changes appear in the [!UICONTROL Modifications] rail.

![Property icons](/help/main/c-experiences/c-visual-experience-composer/assets/options-icons.png)

The [!UICONTROL Properties] rail is collapsible in the right rail. Click the [!UICONTROL Show/Hide Properties] icon ( ![Properties icon](/help/main/assets/icons/Propertie.svg) ) to the right of the rail to collapse or display the [!UICONTROL Properties] rail.

### Activity settings/configuration

Click the [!UICONTROL Configure] icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ) displayed on top of the design canvas to display the activity properties menu.

![Activity configurations options](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

The different options let you assign properties, edit page delivery rules, specify site preferences, add additional pages, and enable or disable multi-page or multiple audience activities. Assign [!UICONTROL Properties] is a [[!DNL Target Premium]](/help/main/c-intro/intro.md#premium) feature. 

The position and functionality is similar to the previous VEC UI.

### [!UICONTROL Design]/[!UICONTROL Browse] modes

Use the [!UICONTROL Design]/[!UICONTROL Browse] toggles displayed on top of the [!UICONTROL Properties] rail to switch between design and browse mode.

![Design and browse toggles](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

Use the [!UICONTROL Browse] mode to navigate your site and to pick the view or page you want to update. Switch back to [!UICONTROL Design] mode to add or edit your changes.

### [!UICONTROL Undo]/[!UICONTROL Redo]

You can undo changes made by clicking the [!UICONTROL Undo] icon ( ![Undo icon](/help/main/assets/icons/Undo.svg) ). 

![Undo icon in VEC](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

To redo an action, expand the [!UICONTROL ]Undo/[!UICONTROL Redo] button group and choose [!UICONTROL Redo].

### [!UICONTROL Design] canvas

The [!UICONTROL Design] canvas lets you select viewports, including fit-to screen, [!UICONTROL Desktop], [!UICONTROL Tablet], [!UICONTROL Mobile Landscape], and [!UICONTROL Mobile Portrait].

![Viewport options](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png)

The updated VEC also lets you zoom in or zoom out by clicking the appropriate icon ( ![Zoom In icon](/help/main/assets/icons/ZoomIn.svg) or ![Zoom Out icon](/help/main/assets/icons/ZoomOut.svg) ).

## Visual illustration showing UI changes

The following illustration shows the high-level UI changes made to the updated VEC. The top of the illustration shows the updated VEC UI and the bottom shows the previous UI. Arrows show where various elements have moved.

(Click the image to expand it to the full width of the browser.) 

![VEC comparison-new to previous UI](/help/main/c-experiences/c-visual-experience-composer/assets/vec-comparison.png){width="600" zoomable="yes"}

## More information about the updated UI

* [[!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Provides a summary of the key UI changes in [!DNL Target] for [!UICONTROL Activities], [!UICONTROL Recommendations], and the [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium] 25.1.1 (January 9, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Provides a summary of the key UI changes in [!DNL Target] for the [!UICONTROL Offers Library].

* [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): Provides a brief overview to help you get familiarized with [!DNL Target] and provides links for more in-depth information and step-by-step instructions.

* [[!UICONTROL Visual Experience Composer] changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2025) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the legacy and updated versions of the VEC.

* [[!UICONTROL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): This article explains the updated VEC UI and its options.

* [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md): This FAQ addresses common questions about the new [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC), including navigation changes, feature locations, and the deprecation of the temporary UI version toggle. Whether you're a marketer, developer, or admin, this FAQ helps you transition smoothly and make the most of the updated UI.