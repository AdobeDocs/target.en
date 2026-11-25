---
keywords: visual experience composer;vec;wysiwyg
description: Understand the changes introduced in the Visual Experience Composer (VEC) in the Adobe Target 25.2.1 release (February 17, 2025).
title: What changes are introduced in the new Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 4c7a5657-93d9-4355-9d2b-c992b36bcb50
TQID: 'https://experienceleague.adobe.com/PZaKHKs1-GPnR1U-E0d3YQVNWhinmt9ctjOSnIbNrE0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# [!UICONTROL Visual Experience Composer] changes {#vec-changes}

>[!BEGINSHADEBOX]

**On this page:** Learn how the updated [!UICONTROL Visual Experience Composer] (VEC) introduced in the [!DNL Adobe Target Standard/Premium] 25.2.1 release differs from the previous version.

>[!ENDSHADEBOX]

The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2025) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the previous and updated versions of the VEC.

>[!IMPORTANT]
>
>The updated [!UICONTROL Visual Experience Composer] requires the [!DNL Adobe Experience Cloud] [**[!UICONTROL Visual Editing Helper]** extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) available in the [!DNL Chrome Web Store].

The VEC displays when an activity is created or an existing activity is edited.

## Major changes to the VEC

The following sections explain the major changes in the updated VEC compared to the previous version.

### [!UICONTROL Experiences] rail

As in the previous version, the **[!UICONTROL Experiences]** rail remains on the left side of the VEC. The **[!UICONTROL Experiences]** rail cannot be collapsed.

![Experiences rail](/help/main/c-experiences/c-visual-experience-composer/assets/experiences-panel.png)

Experiences are created, renamed, or removed using the **[!UICONTROL Experiences]** rail. 

Click the **[!UICONTROL Add]** icon ( ![Add icon](/help/main/assets/icons/Add.svg) ) to add a new experience. Click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) to duplicate, delete, or redirect an experience.

### [!UICONTROL Components] rail (new)

The new **[!UICONTROL Components]** rail adds a number of components to the web page, which can then be edited as needed.

![Components rail](/help/main/c-experiences/c-visual-experience-composer/assets/components-panel.png)

To add a new component, select the desired component from the **[!UICONTROL Components]** rail, hover over an existing element in the page, then choose to insert the component before or after the selected element.

If the **[!UICONTROL Modifications]** rail displays in this area instead of the **[!UICONTROL Components]** rail, click the **[!UICONTROL Show Components]** icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ). The **[!UICONTROL Show Components]** icon ( ![Show Components icon](/help/main/assets/icons/Add.svg) ) and the **[!UICONTROL Show Modifications]** icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) act as toggles that show the appropriate options.

To collapse the **[!UICONTROL Components]** rail and enlarge the **[!UICONTROL Design]** canvas while the **[!UICONTROL Components]** rail is open, click the ( ![Show Components icon](/help/main/assets/icons/Add.svg) ) icon.

### [!UICONTROL Modifications] rail

To open the **[!UICONTROL Modifications]** rail, click the **[!UICONTROL Show Modifications]** icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) in the **[!UICONTROL Components]** rail. The **[!UICONTROL Modifications]** rail changed position from the right side to the left side of the editing canvas.

![Modifications rail](/help/main/c-experiences/c-visual-experience-composer/assets/modifications-panel.png)

>[!NOTE]
>
>To collapse the **[!UICONTROL Modifications]** rail and enlarge the **[!UICONTROL Design]** canvas while the **[!UICONTROL Modifications]** rail is open, click the **[!UICONTROL Show Modifications]** icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ).

The **[!UICONTROL Modifications]** rail shows all changes that have been made to the page in the VEC, and allows additional changes (such as CSS Selector, Mbox, and Custom Code).

Click the **[!UICONTROL More Options]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) to add a modification, delete all modifications, or delete all invalid modifications. Click **[!UICONTROL Select]** to perform bulk operations: **[!UICONTROL Apply to All Pages]** or **[!UICONTROL Delete]**.

To display the **[!UICONTROL Modifications]** rail again, click the **[!UICONTROL Hide Modifications]** icon ( ![Show Modifications rail](/help/main/assets/icons/History.svg) ) in the **[!UICONTROL Modifications]** rail.

### [!UICONTROL Properties] rail (new)

The **[!UICONTROL Properties]** rail changes the properties of selected elements on the page, whether these elements are HTML elements or objects specific to [!DNL Target], such as recommendations or offers.

![Properties rail](/help/main/c-experiences/c-visual-experience-composer/assets/properties-panel.png)

Click the icons on top of the rail to edit HTML code or to delete, duplicate, or hide elements. Changes appear in the **[!UICONTROL Modifications]** rail.

![Property icons](/help/main/c-experiences/c-visual-experience-composer/assets/options-icons.png)

The **[!UICONTROL Properties]** rail is collapsible in the right rail. Click the **[!UICONTROL Show/Hide Properties]** icon ( ![Properties icon](/help/main/assets/icons/Propertie.svg) ) to the right of the rail to collapse or display the **[!UICONTROL Properties]** rail.

### Activity settings/configuration

Click the **[!UICONTROL Configure]** icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ) displayed on top of the design canvas to display the activity properties menu.

![Activity configurations options](/help/main/c-experiences/c-visual-experience-composer/assets/configure-options.png)

The different options assign properties, edit page delivery rules, specify site preferences, add additional pages, and enable or disable multi-page or multiple audience activities. Assign **[!UICONTROL Properties]** is a [[!DNL Target Premium]](/help/main/c-intro/intro.md#premium) feature.

The position and functionality are similar to the previous VEC UI.

### [!UICONTROL Design]/[!UICONTROL Browse] modes

Use the **[!UICONTROL Design]**/**[!UICONTROL Browse]** toggles displayed on top of the **[!UICONTROL Properties]** rail to switch between design and browse mode.

![Design and browse toggles](/help/main/c-experiences/c-visual-experience-composer/assets/design-browse-mode.png)

Use the **[!UICONTROL Browse]** mode to navigate the site and to pick the view or page to update. Switch back to **[!UICONTROL Design]** mode to add or edit changes.

### [!UICONTROL Undo]/[!UICONTROL Redo]

Changes can be undone by clicking the **[!UICONTROL Undo]** icon ( ![Undo icon](/help/main/assets/icons/Undo.svg) ).

![Undo icon in VEC](/help/main/c-experiences/c-visual-experience-composer/assets/undo.png)

To redo an action, expand the **[!UICONTROL Undo]**/**[!UICONTROL Redo]** button group and choose **[!UICONTROL Redo]**.

### [!UICONTROL Design] canvas

The **[!UICONTROL Design]** canvas allows selecting viewports, including fit-to-screen, **[!UICONTROL Desktop]**, **[!UICONTROL Tablet]**, **[!UICONTROL Mobile Landscape]**, and **[!UICONTROL Mobile Portrait]**.

![Viewport options](/help/main/c-experiences/c-visual-experience-composer/assets/viewports.png)

The updated VEC also allows zooming in or out by clicking the appropriate icon ( ![Zoom In icon](/help/main/assets/icons/ZoomIn.svg) or ![Zoom Out icon](/help/main/assets/icons/ZoomOut.svg) ).

## Visual illustration showing UI changes

The following illustration shows the high-level UI changes made to the updated VEC. The left side of the illustration shows the previous VEC UI, and the right side shows the updated UI. Matching numbers show where various elements have moved or changed.

![Side-by-side comparison of the previous and updated VEC layouts, with numbered callouts for the Experiences, Components, Modifications, and Properties rails, Configure, the Design and Browse toggles, Undo and Redo, the Design canvas, and the removed overlay toggle](/help/main/c-experiences/c-visual-experience-composer/assets/vec-comparison.png){width="800" zoomable="yes"}

## More information about the updated UI

* [[!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Provides a summary of the key UI changes in [!DNL Target] for **[!UICONTROL Activities]**, **[!UICONTROL Recommendations]**, and the [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium] 25.1.1 (January 9, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Provides a summary of the key UI changes in [!DNL Target] for the **[!UICONTROL Offers Library]**.

* [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): Provides a brief overview of [!DNL Target], with links for more in-depth information and step-by-step instructions.

* [[!UICONTROL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): Explains the updated VEC UI and its options.

* [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md): Addresses common questions about the new [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC), including navigation changes, feature locations, and the deprecation of the temporary UI version toggle.
