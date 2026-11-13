---
keywords: audience;select audience;choose audience;Selectors
description: Define which site visitors join your Adobe [!DNL Target] activity based on audience criteria.
title: How Do I Select an Audience in a [!DNL Target] A/B Activity?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
TQID: 'https://experienceleague.adobe.com/7W8BrRxk4mKlYlgGb-GSOuc0kRMRWBvSochz9STYrTs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Select audience {#select-audience}

>[!BEGINSHADEBOX]

**On this page:** Learn how to select, create, combine, view, edit, and copy the audience of an A/B activity, and how to set the percentage of visitors to include.

>[!ENDSHADEBOX]

The audience determines which qualifying visitors are entered into your [!DNL Adobe Target] activity.

The **[!UICONTROL Targeting]** step of the three-part guided workflow when [creating an activity](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) displays a flow diagram that leads you through the steps of assigning an audience and its traffic percentage, selecting the traffic allocation method, and specifying the traffic allocation for each experience in the activity.

![A/B Test Targeting step](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

For more information about all the options in the flow diagram, see [Create an A/B Test activity](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

## Select an audience for the activity

The audience controls who sees your activity. Only visitors who match the audience can enter it, and you decide what share of those visitors take part. By default, the activity targets all visitors. 

1. Click the **[!UICONTROL All Visitors]** control to select another audience for the activity.

   **[!UICONTROL All Visitors]** is the default audience. For an A/B test without specific audience targeting, keep the default. If you select another audience, its name displays in the leftmost control.

1. Click the **[!UICONTROL Replace] icon** ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ).

    ![](../../assets/audience_activity.png)

1. In the **[!UICONTROL Add Audience]** dialog box, browse through audiences selected from the **[!UICONTROL Audience Library]**, or you can create an activity-only audience. 

    The **[!UICONTROL Audience Library]** contains audiences that have previously been defined, including some common audiences that are pre-built as a part of [!DNL Target].

    ![](../../assets/audience_activity_2.png)

1. Click the **[!UICONTROL Information]** icon ( ![Info icon](/help/main/assets/icons/InfoOutline.svg) ) next to an audience to view details about that audience, including its source and attributes.

    ![](../../assets/audience_activity_3.png)

    You can also click **[!UICONTROL View Full Details]** to view additional details about the audience. 

1. (Conditional) Click **[!UICONTROL Combine Audiences]** to [create an audience that combines multiple audiences](/help/main/c-target/combining-multiple-audiences.md).

   +++ Steps to create a new audience

   To create a new audience that is not already in the **[!UICONTROL Audience Library]**, click **[!UICONTROL Create Audience]**, define the audience, then click **[!UICONTROL Done]**.

   During the [create-audience workflow](/help/main/c-target/c-audiences/audiences.md), you can choose from the following options:

   * **[!UICONTROL Audience Library]**: Create an on-demand audience that is saved to the **[!UICONTROL Audience Library]** and can be reused in other activities.
   * **[!UICONTROL This activity only]**: Create an [activity-specific audience](/help/main/c-target/creating-activity-only-audience.md) that is not saved to the **[!UICONTROL Audience Library]** and can be used in the current activity only.

   +++
  
1. You can edit or copy an audience by clicking the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/More.svg) ) next to the desired audience.

1. After selecting your Audience, click **[!UICONTROL Assign Audience]**.

1. Click **[!UICONTROL Visitor Percentage]** in the right pane, then specify the percentage of qualifying visitors to include in the activity.

1. When you are satisfied with your audience, click **[!UICONTROL Next]** to move to the third step of the three-step guided workflow.

>[!NOTE]
>
>Audiences are automatically imported in the background when you open the **[!UICONTROL Audience]** list and the imported audiences are more than 10 minutes old.
