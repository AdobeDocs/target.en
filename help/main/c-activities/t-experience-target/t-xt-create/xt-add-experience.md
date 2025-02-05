---
keywords: create experience;experience create;priority;audience;experience;visual experience composer
description: Learn how to use the [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) to create and edit experiences on your page in an [!UICONTROL Experience Targeting] (XT) activity.
title: How Do I Create Experiences in an [!UICONTROL Experience Targeting] Activity?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
---
# Create experience in [!UICONTROL Experience Targeting] (XT) activities

The [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] provides a visual interface for editing the experiences on your page in an [!UICONTROL Experience Targeting] (XT) activity.

1. Select the elements that you want to change and make the desired changes.

   While [creating an [!UICONTROL Experience Targeting] activity](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), step one of the three-part guided workflow ([!UICONTROL Experiences]) displays the default [!UICONTROL Experience A] with an [!UICONTROL All Visitors] audience.

   ![All Visitors audience](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors-new.png)

   Any changes you make now apply to [!UICONTROL Experience A]. In a step below, you click **[!UICONTROL Add Experience Targeting]** to create additional experiences.

   As you hover over the elements on your page, the elements are highlighted. Any highlighted element can be altered using the VEC. For a list of actions that can be performed on an element to change the experience, see [Visual Experience Composer Options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >By default, the VEC does not allow changes to elements containing JavaScript, such as rotating banners. You can disable JavaScript to alter those elements using the VEC.

1. To create additional experiences, click **[!UICONTROL Add]** ( ![Add button](/help/main/assets/icons/Add.svg) ).

   The [!UICONTROL Add Audience] dialog box displays. To target an experience to an audience, select the audience before you add the experience.

   The audience library contains audiences that have previously been defined, including some common audiences that are pre-built as a part of [!DNL Target]. You can select an audience from the library or [create a new audience](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   In addition to selecting an existing audience, you can combine multiple audiences to create on demand combined audiences rather than creating a new audience. For more information, see [Combining Multiple Audiences](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   When creating an audience, you can select a location and specify parameters for that location. Under [!UICONTROL Custom] ([!UICONTROL Create Audience] > [!UICONTROL Custom]), select the location, then specify the desired parameters.

   >[!NOTE]
   >
   >Audiences are automatically imported in the background when you open the audience list and the imported audiences are more than ten minutes old.

1. Select one or more audiences to target with the experience, then click **[!UICONTROL Assign Audience]**.

   Experience B now displays in the preceding illustration and this experience is targeted to the appropriate audience.

1. Select the elements that you want to change for this experience and make the desired changes, as explained in Step 1 above.

1. Repeat the preceding steps to create additional targeted experiences, as needed.

1. Click **[!UICONTROL Next]** when you are finished designing your experiences.

   The activity diagram displays:

   ![XT Targeting diagram](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-refresh.png)

   >[!NOTE]
   >
   >You can deliver an image from a source other than your main page (such as an image hosted on `akamai.net` and delivered on `adobe.com`). Images hosted elsewhere do not display in the thumbnail of the page shown in the flow diagram.

1. (Conditional) Drag and drop audience and experience pairs while creating or editing [!UICONTROL Experience Targeting] activities to arrange the pairs in the desired order.

   Click the Reorder icon ( ![Reorder icon](/help/main/assets/icons/Reorder.svg) ) to display the [!UICONTROL Experiences] column on the right side, then rearrange the experiences as desired.

   Visitors are evaluated for experiences in order, from top to bottom.

   [!UICONTROL Experience Targeting] assumes that order matters. If a visitor falls into the first audience and experience pair, the first experience is delivered.

   For example, suppose you were not aware that order matters while creating an [!UICONTROL Experience Targeting] activity. You later realize during testing that visitors that you think should qualify for experiences B or C are instead qualifying for experience A. This situation could be because the audiences are not mutually exclusive and are not in the proper order (for example, experience A = United States, experience B = San Francisco, and experience C = California). In this scenario, all users from the United States qualify for experience A, even if they are in San Francisco or elsewhere in California. You can reorder the audience and experience pairs from most restrictive to least restrictive (San Francisco > California > United States) without recreating the entire activity.

   If you have an [!UICONTROL All Visitors] audience, ensure that it is not the first audience in the diagram. An experience targeted to "[!UICONTROL All Visitors]" can be used as the last experience in the [!UICONTROL Experience Targeting] activity to "catch" any visitors that have not fallen into any other experience.

## Rename, edit, duplicate, or delete an experience

Click an experience in the diagram in an [!UICONTROL Experience Targeting] activity to display the [!UICONTROL Experiences] column on the right side.

![Rename and Edit options](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-refresh.png)

Choose from the following options, as necessary:

* **[!UICONTROL Rename]**: Type the desired name in the [!UICONTROL Name] field.
* **[!UICONTROL Edit]**: Click the Edit icon ( ![Edit icon](/help/main/assets/icons/Edit.svg) ), then make your desired changes.
* **[!UICONTROL Duplicate]**: Copy an experience in an [!UICONTROL Experience Targeting] activity so you can make minor changes to it without having to recreate the entire experience. Click the [!UICONTROL Duplicate] icon ( ![Duplicate icon](/help/main/assets/icons/Duplicate.svg) ), then edit the experience as necessary.
* **[!UICONTROL Delete]**: Click the [!UICONTROL Delete] icon (![Delete icon](/help/main/assets/icons/Delete.svg)  ), then confirm your deletion.

## Training videos:

The following videos contain more information about the concepts discussed in this article.

### From A/B Testing to [!UICONTROL Experience Targeting]

This video describes how to take A/B testing to the next level with [!UICONTROL Experience Targeting] (XT).

* Describe the three-step guided workflow to configure an [!UICONTROL Experience Targeting] activity 
* Describe how to deliver location-specific content to audiences in different geographic areas 
* Describe how to reorder experiences to ensure that the right content is delivered to the right audience

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Activity Types (9:03)

This video explains the activity types available in [!DNL Target]. [!UICONTROL Experience Targeting] is discussed beginning at 5:15.

* Describe the types of activities included in [!DNL Adobe Target] 
* Select the appropriate activity type to achieve your goals 
* Describe the three-step guided workflow that applies to all activity types

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Using the [!UICONTROL Visual Experience Composer]

This video provides information about using the [!UICONTROL Experience Targeting] (VEC) options.

* Change the content of a page 
* Change the layout of a page

>[!VIDEO](https://video.tv.adobe.com/v/17399)
