---
keywords: audience;audience rules;create audience;creating audience
description: Learn how to create customized audiences and save them to the [!DNL Adobe Target] [!UICONTROL Audiences] library for use in activities.
title: How Do I Build Audiences?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
---
# Build audiences in [!DNL Target]

Create customized audiences and save them to the [!DNL Adobe Target] [!UICONTROL Audiences] library for use in your activities. You can also copy an existing audience that you can then edit to create a similar audience and combine multiple audiences.

## Audience overview

Audiences are defined by rules that determine who is included or excluded from a [!DNL Target] activity. An audience definition can include multiple rules and each rule can include multiple parameters. Complex audience definitions use the boolean operators AND and OR to combine rules and parameters to give you detailed control over which site visitors are counted as activity entrants.

When you combine rules or parameters with AND, any potential audience member must meet *all* defined conditions to be included as an entrant. For example, if you define an OS rule AND a browser rule, only visitors using both the defined OS *and* the defined browser are included in the activity.

When you combine rules or parameters with OR, any potential audience member need only meet any single defined condition to be included as an entrant. For example, if you define multiple mobile rules connected by OR, visitors meeting *any* of the defined criteria are included in the activity.

You can mix both boolean operators to create complex rules; however, operators at the same rule level must match. The user interface automatically applies the correct operator.

For example, the following rule targets visitors who use either [!DNL Chrome] *or* [!DNL Firefox] on a [!DNL Windows] computer:

![Create audience](assets/audience_create.png)

>[!NOTE]
>
>Be careful to avoid creating rules that exclude all potential audience members. For example, it is not possible for someone to visit a page using [!DNL Chrome] *and* [!DNL Firefox] simultaneously.

## Create an audience

1. Click **[!UICONTROL Audiences]** in the top menu bar.

   ![audiences_list image](assets/audiences_list.png)

1. From the [!UICONTROL Audiences] list, click **[!UICONTROL Create Audience]**.

   Or

   To copy an existing audience, from the [!UICONTROL Audiences] list, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallListVert.svg) ) for the audience that you want to copy, then click **[!UICONTROL Duplicate]**. You can then edit the audience to create a similar audience. 

1. Type a unique, descriptive audience name and an optional description.

   Audience names cannot start with the following characters:

   `=  +  -  !  @`

   Audience names cannot contain any of the following character sequences:

   `;=  ;+  ;-  ;@  ,=  ,+  ,-  ,@  ["  "]  ['  ]'`

1. Drag and drop the desired attributes from the **[!UICONTROL Attributes]** list on the left to the audience builder pane.

   ![Drag and drop attributes](assets/drag-attribute.png)

   Each rule type has its own parameters. See [Categories for Audiences](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) for more information on configuring each type of audience rule.

1. Define the rule parameters.

   For example, the following audience targets visitors from Utah using the [!DNL Macintosh] operating system.

   ![Utah/Macintosh audience](assets/adience-builder.png)

1. (Conditional) Continue adding and defining the desired attributes.

   To create another container, click **[!UICONTROL Add container]** or simply drag another attribute into the Audience Builder pane. You can then adjust the operator (AND or OR) using the drop-down list.

1. Click **[!UICONTROL Done]**.

   Newly created audiences appear in the list after a few seconds of processing delay. If the audience does not display immediately in the list, try searching for the audience or refresh the list. 

## Training video: Creating Audiences ![Overview badge](/help/main/assets/overview.png)

This video includes information about creating audiences.

* Create audiences 
* Define audience categories

>[!VIDEO](https://video.tv.adobe.com/v/17392)
