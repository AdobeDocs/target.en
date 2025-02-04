---
keywords: audience;select audience;choose audience;Selectors
description: Define which site visitors join your Adobe [!DNL Target] activity based on audience criteria.
title: How Do I Select an Audience in a [!DNL Target] A/B Activity?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
---
# Select audience

The audience determines which qualifying visitors are entered into your [!DNL Adobe Target] activity.

The [!UICONTROL Targeting] step of the three-part guided workflow when [creating an activity](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) displays a flow diagram that leads you through the steps of assigning an audience and its traffic percentage, selecting the traffic allocation method, and specifying the traffic allocation for each experience in the activity.

![A/B Test Targeting step](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

For more information about all the options in the flow diagram, see [Create an A/B Test activity](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

## Select an audience for the activity

1. Click the **[!UICONTROL All Visitors]** control to select another audience for the activity.

   The [!UICONTROL All Visitors] audience is set as the default. If you select another audience, its name displays in the leftmost control.

   For an A/B test without specific audience targeting, choose the default, [!UICONTROL All Visitors].

   The right frame displays, which lets you add or delete an audience and assign the visitor percentage for the activity.

1. To change the audience, click the **[!UICONTROL Replace] icon** ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) in the right frame.

1. In the [!UICONTROL Add Audience] dialog box, [select the desired audience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), then click **[!UICONTROL Assign Audience]**.

   By default, all visitors are your audience. However, you can change the audience. Audiences are selected from the [!UICONTROL Audience Library] or you can create an activity-only audience. The [!UICONTROL Audience Library] contains audiences that have previously been defined, including some common audiences that are pre-built as a part of [!DNL Target]. 

1. (Conditional) Click **Combine Audiences** to [create an audience that combines multiple audiences](/help/main/c-target/combining-multiple-audiences.md). 

1. (Conditional) To create a new audience that is not already in the [!UICONTROL Audience Library], click **Create Audience**, define the audience, then click **[!UICONTROL Done]**. 

    During the [create-audience workflow](/help/main/c-target/c-audiences/audiences.md), you can choose from the following options:

    * **[!UICONTROL Audience Library]**: Create an on-demand audience that is saved to the [!UICONTROL Audience Library] that can be reused in other activities.
    * **[!UICONTROL This activity only]**: Create an [activity-specific audience](/help/main/c-target/creating-activity-only-audience.md) that is not saved to the [!UICONTROL Audience Library] and can be used in the current activity only.

1. Click **[!UICONTROL Visitor Percentage]** in the right pane, then specify the percentage of qualifying visitors to include in the activity.

1. When you are satisfied with your audience, click **[!UICONTROL Next]** to move to the third step of the three-step guided workflow.

>[!NOTE]
>
>Audiences are automatically imported in the background when you open the [!UICONTROL Audience] list and the imported audiences are more than 10 minutes old.

## View an audience's information

1. In the [!UICONTROL Add Audiences] dialog box, click the **[!UICONTROL Information]** icon ( ![Info icon](/help/main/assets/icons/InfoOutline.svg) ) next to an audience to view details about that audience, including its source and attributes.

1. Click **[!UICONTROL View Full Details]** to view additional details about the audience. Details include the audience's attributes; the audience's description, workspace, type, and source; and a list of activities that reference this audience. You can see information about each audience, including activity name, status, workspace, and when the audience was last modified and by whom.

## Edit or copy an audience

You can edit or copy an audience by clicking the [!UICONTROL More Actions] icon ( ![More Actions icon](/help/main/assets/icons/More.svg) ) next to the desired audience in the [!UICONTROL Add Audience] dialog box, then by clicking [!UICONTROL Edit] or [!UICONTROL Copy]. 

Copying an audience is helpful if you want to create a similar audience to an existing audience. You can make a copy of the audience, make your edits, then save it as a new audience.
