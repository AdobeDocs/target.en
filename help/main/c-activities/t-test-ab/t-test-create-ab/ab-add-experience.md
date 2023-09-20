---
keywords: Targeting;experience;add experience;experience add
description: Learn how to use the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target].
title: How Do I Add Experiences in a [!DNL Target] A/B Activity?
feature: A/B Tests
exl-id: c0f1b5a7-07b0-46c2-97f3-95dcc0fcbe3d
---
# Add experience

The [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) provides a visual interface for adding and editing the experiences on your page.

For additional detail about experiences, see [Experiences](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). 

1. From the **[!UICONTROL Experiences]** page in the VEC, click **[!UICONTROL Add Experience]**.

   ![Add Experience option](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/add-experience.png)

   >[!NOTE]
   >
   >If you are targeting an experience to an audience, you must select the audience before you can add an experience. A message appears to remind you to choose your audience.

1. Select the elements that you want to change and make the desired changes.

   As you hover over the elements on your page, the elements are highlighted. Any highlighted element can be altered using the VEC.

   If you created a [!DNL Target] request on the page using [!DNL Target Classic] (formerly [!DNL Test&Target]), that [!DNL Target] request appears as an element that shows the request name, and can be modified like any other element.

   For a list of actions that can be performed on an element on the displayed page to change the experience, see [Visual Experience Composer Options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >If you deliver an image from a source other than your main page (such as an image hosted on `akamai.net` and delivered on `example.com`), that image does not display in the thumbnail of the page shown in the flow diagram.

1. Click **[!UICONTROL Save]** when you are finished designing the experience.

## Rename experience

1. Click the **[!UICONTROL Rename Experience]** icon on an experience in an [!UICONTROL A/B Test] or [!UICONTROL Experience Targeting] (XT) activity to give the experience a new name.

   ![Rename experience](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/rename-experience.png)

2. Specify a new name.

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

1. Click the **[!UICONTROL More]** icon (the vertical ellipsis) icon on an experience in an [!UICONTROL A/B Test] or [!UICONTROL Experience Targeting] (XT) activity, then click **[!UICONTROL Redirect to URL]**.

   For more information, see [Redirect to URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

   **NOTE**: When you name or rename an experience, the following characters are not allowed: 

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
   
1. Specify the URL to which you want to redirect the experience.

1. (Conditional) Check the **[!UICONTROL Include Current Query Parameters]** check box.

## Duplicate an Experience

You can copy an experience in an [!UICONTROL A/B Test] so you can make minor changes to it without having to recreate the experience from scratch. 

1. On the **[!UICONTROL Experiences]** page (the first step in the three-step guided workflow), click the vertical ellipsis icon > **[!UICONTROL Duplicate]**. 

   ![Duplicate experience option](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/duplicate-experience.png)

## Delete an experience

1. On the **[!UICONTROL Experiences]** page (the first step in the three-step guided workflow), click the vertical ellipsis icon > **[!UICONTROL Duplicate]**.

   ![Delete experience option](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/delete-experience.png)

## Training video: Using the [!UICONTROL Visual Experience Composer]

The video below provides information about using the [!UICONTROL Visual Experience Composer] options. (7:17)

* Change the content of a page 
* Change the layout of a page

>[!VIDEO](https://video.tv.adobe.com/v/17399)
