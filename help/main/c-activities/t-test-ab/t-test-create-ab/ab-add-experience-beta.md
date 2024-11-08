---
keywords: Targeting;experience;add experience;experience add
description: Master using the [!UICONTROL Visual Experience Composer] (VEC) to add experiences to activities.
title: How Do I Add Experiences in an A/B Activity?
feature: A/B Tests
hide: yes
hidefromtoc: yes
exl-id: 4b2d6cc6-f280-4d65-8153-53e9cd61d15a
---
# Add experience

The [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) provides a visual interface for adding and editing the experiences on your page.

For additional detail about experiences, see [Experiences](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

1. From the **[!UICONTROL Experiences]** page in the VEC, click the [!UICONTROL Add] icon ( ![Add icon](/help/main/assets/icons/Add.svg) ) at the top of the [!UICONTROL Experiences] pane.

   The VEC displays two tabs on the left side after you create a new activity: Experience A and Experience B. Experience A is the control experience. You can add multiple experiences to the test.

1. Select the elements that you want to change and make the desired changes.

   As you hover over the elements on your page, the elements are highlighted. Any highlighted element can be altered using the VEC.

   If you created a [!DNL Target] request on the page using [!DNL Target Classic] (formerly [!DNL Test&Target]), that [!DNL Target] request appears as an element that shows the request name, and can be modified like any other element.

   For a list of actions that can be performed on an element on the displayed page to change the experience, see [Visual Experience Composer Options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >If you deliver an image from a source other than your main page (such as an image hosted on `akamai.net` and delivered on `example.com`), that image does not display in the thumbnail of the page shown in the flow diagram.

1. Click **[!UICONTROL Next]** when you are finished designing the experience.

## Rename experience

1. Click the **[!UICONTROL Rename Experience]** icon ( ![Rename icon](/help/main/assets/icons/Rename.svg) ) next to an experience to give the experience a new name.

2. Specify a new name, then click **[!UICONTROL Save]**.

   When you name or rename an experience, the following characters are not allowed: 

   | Character | Description |
   |--- |--- |
   |/|Forward slash|
   |?|Question mark|
   |#|Number sign|
   |:|Colon|
   |=|Equals to|
   |+|Plus|
   |-|Minus|
   |@|At sign|

## Redirect to URL

1. In the **[!UICONTROL Experiences]** pane, click the **[!UICONTROL More]** icon ( ![More icon](/help/main/assets/icons/MoreSmall.svg) ) next to an experience, then click **[!UICONTROL Redirect to URL]**.

   For more information, see [Redirect to URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).
   
1. Specify the URL to which you want to redirect the experience.

1. (Conditional) Check the **[!UICONTROL Include Current Query Parameters]** check box.

1. Click **[!UICONTROL Save]**.

## Duplicate an Experience

You can copy an experience in an [!UICONTROL A/B Test] so you can make minor changes to it without having to recreate the experience. 

1. In the **[!UICONTROL Experiences]** pane, click the **[!UICONTROL More]** icon ( ![More icon](/help/main/assets/icons/MoreSmall.svg) ) next to an experience, then click **[!UICONTROL Duplicate]**. 

## Delete an experience

1. In the **[!UICONTROL Experiences]** pane, click the **[!UICONTROL More]** icon ( ![More icon](/help/main/assets/icons/MoreSmall.svg) ) next to an experience, click **[!UICONTROL Delete]**, then click **[!UICONTROL Delete]** to confirm the action.
