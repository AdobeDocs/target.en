---
keywords: Targeting;experience;add experience;experience add
description: Use the [!UICONTROL Visual Experience Composer] (VEC) to add experiences to activities.
title: How Do I Add Experiences in an A/B Activity?
feature: A/B Tests
exl-id: c0f1b5a7-07b0-46c2-97f3-95dcc0fcbe3d
TQID: 'https://experienceleague.adobe.com/7qEiUXkfMbPmtB2eMio0LztOYM3naHxG-WRQZOyMmlU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Add experience {#ab-add-experience}

>[!BEGINSHADEBOX]

**On this page:** Learn how to add and design an experience in an A/B activity, and how to rename, redirect, duplicate, or delete it.

>[!ENDSHADEBOX]

The [!DNL Adobe Target] **[!UICONTROL Visual Experience Composer]** (VEC) provides a visual interface for adding and editing the experiences on your page. For additional detail about experiences, see [Experiences](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D).

## Add and design an experience {#add-experience}

To add an experience and change the page for that experience:

1. From the **[!UICONTROL Experiences]** page in the VEC, click the **[!UICONTROL Add]** icon ( ![Add icon](/help/main/assets/icons/Add.svg) ) at the top of the **[!UICONTROL Experiences]** pane.

   After you create a new activity, the VEC displays two tabs on the left side: Experience A and Experience B. Experience A is the control experience. You can add multiple experiences to the test.

1. Select the elements that you want to change and make the desired changes.

   As you hover over the elements on your page, the elements are highlighted. Any highlighted element can be altered using the VEC. If you created a [!DNL Target] request on the page using [!DNL Target Classic] (formerly [!DNL Test&Target]), that [!DNL Target] request appears as an element that shows the request name, and can be modified like any other element.

   For a list of actions that can be performed on an element on the displayed page to change the experience, see [Visual Experience Composer Options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

1. Click **[!UICONTROL Next]** when you are finished designing the experience.

>[!NOTE]
>
>If you deliver an image from a source other than your main page (such as an image hosted on `akamai.net` and delivered on `example.com`), that image does not display in the thumbnail of the page shown in the flow diagram.

## Rename an experience {#rename-experience}

To give an experience a new name:

1. Click the **[!UICONTROL Rename Experience]** icon ( ![Rename icon](/help/main/assets/icons/Rename.svg) ) next to the experience.

1. Specify a new name, then click **[!UICONTROL Save]**.

When you name or rename an experience, the following characters are not allowed:

| Character | Description |
|--- |--- |
|`/`|Forward slash|
|`?`|Question mark|
|`#`|Number sign|
|`:`|Colon|
|`=`|Equals to|
|`+`|Plus|
|`-`|Minus|
|`@`|At sign|

## Redirect an experience to a URL {#redirect-to-url}

To send visitors of an experience to another URL, see also [Redirect to URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md):

1. In the **[!UICONTROL Experiences]** pane, click the **[!UICONTROL More]** icon ( ![More icon](/help/main/assets/icons/MoreSmall.svg) ) next to the experience, then click **[!UICONTROL Redirect to URL]**.

1. Specify the URL to which you want to redirect the experience.

1. (Conditional) Select the **[!UICONTROL Include Current Query Parameters]** check box.

1. Click **[!UICONTROL Save]**.

## Duplicate an experience {#duplicate-experience}

You can copy an experience in an A/B test so you can make minor changes to it without having to recreate the experience. In the **[!UICONTROL Experiences]** pane, click the **[!UICONTROL More]** icon ( ![More icon](/help/main/assets/icons/MoreSmall.svg) ) next to the experience, then click **[!UICONTROL Duplicate]**.

## Delete an experience {#delete-experience}

In the **[!UICONTROL Experiences]** pane, click the **[!UICONTROL More]** icon ( ![More icon](/help/main/assets/icons/MoreSmall.svg) ) next to the experience, click **[!UICONTROL Delete]**, then click **[!UICONTROL Delete]** to confirm the action.
