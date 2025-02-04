---
keywords: audience;select audience;choose audience;Selectors
description: The audience determines which site visitors are entered into your Adobe [!DNL Target] activity.
title: How Do I Select an Audience in a [!DNL Target] A/B Activity?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
---
# Select audience

The audience determines which site visitors are entered into your [!DNL Adobe Target] activity.

>[!NOTE]
>
>In addition to selecting an existing audience, you can combine multiple audiences to create ad hoc combined audiences rather than creating a new audience. For more information, see [Combining Multiple Audiences](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. In the [!UICONTROL Audience] box, click the **[!UICONTROL Edit]** icon (the vertical ellipsis), then click **[!UICONTROL Replace Audience]**.

   ![Replace Audience option](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/replace-audience.png)

   By default, all visitors are your audience. However, you can change the audience. Audiences are selected from the audience library or you can create an activity-only audience. The audience library contains audiences that have previously been defined, including some common audiences that are pre-built as a part of [!DNL Target]. 
   
1. Select or create the desired audience:

    * Select an audience from the library
    * [Combine multiple audiences](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)
    * [Create a new audience](/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1)
    * [Create an activity-only audience](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483). 
    
    For an A/B test without specific audience targeting, choose the default, [!UICONTROL All Visitors].

    You can also edit or copy an audience by hovering over the desired audience in the [!UICONTROL Add Audience] dialog box, as shown below. 

    Copying an audience is helpful if you want to create a similar audience to an existing audience. You can make a copy of the audience, make your edits, then save it as a new audience. This hover functionality exists in other activity types as well.

    ![Audience hover](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audience_picker_hover-new.png)

    When creating an audience, you can select a location (mbox) and specify parameters for that location. Under [!UICONTROL Custom Parameters], select the mbox, then specify the desired parameters.

   >[!NOTE]
   >
   >Audiences are automatically imported in the background when you open the audience list and the imported audiences are more than 10 minutes old.

1. (Conditional) Specify the percentage of qualifying visitors to include in the activity.

   For example, you might choose to include 50% of all visitors.

   ![Audience Percentage](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   You can also choose to let Target [allocate traffic automatically](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

## Training videos

The following videos contain more information about the concepts discussed in this article.

### Using Audiences in Adobe Target (6:21) ![Overview badge](/help/main/assets/overview.png)

This video explains how to use audiences in [!DNL Target Standard/Premium].

* Explain the term "Audience"
* Explain the two ways audiences are used for optimization 
* Find audiences in the Audiences list 
* Target an activity to an audience 
* Use audiences for passive reporting in an activity

>[!VIDEO](https://video.tv.adobe.com/v/17398)

### Activity Workflow - Targeting (2:14) ![Tutorial badge](/help/main/assets/tutorial.png)

This video includes information about setting up audiences.

* Assign an audience to your activity 
* Throttle traffic up or down 
* Select your traffic allocation method 
* Allocate traffic between different experiences

>[!VIDEO](https://video.tv.adobe.com/v/17385)

For detailed information, see [Audiences](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).
