---
keywords: activities;activity;activity types;edit activity;edit;draft
description: Learn about the different ways that you can edit an existing activity, including saving an activity in draft form.
title: How Do I Edit an Activity or Save As Draft?
feature: Activities
exl-id: 5f2a930a-9950-430e-a898-50af1f917ec1
---
# Edit an activity or save as a draft

Learn how to edit existing activities in [!DNL Adobe Target], including how to save changes as drafts. This article covers the different methods available in the [!DNL Target] interface for modifying activities. Whether you're updating experiences, adjusting targeting rules, or configuring goals, Target ensures that your changes are saved safely before activation.

[!DNL Target] provides various places in the UI where you can edit existing activities. The process varies depending on the method that you choose.

## Edit an activity by using the hover [!UICONTROL More Actions] icon on the Activities page {#section_29EE2ECA6B88473A8F9AC5600FFBB174}

1. From the **[!UICONTROL Activities]** page, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) next to the activity you want to edit, then click [!UICONTROL **Edit**].

   Target opens the activity in the [!UICONTROL Visual Experience Composer] (VEC) and you see the [!UICONTROL Experiences] page (the first step in the three-step guided workflow).

1. Edit the activity, as desired using the [VEC options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

1. Click the **[!UICONTROL Next]** to advance to the next step, then make any necessary edits.

1. When you get to the [!UICONTROL ]**Goals & Settings** page, you have the following options: 
 
    * **[!UICONTROL Save & Close]:** Click **[!UICONTROL Save and Close]** to save your changes and display the activity's [!UICONTROL Overview] page. 
    * **Save:** Click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallListVert.svg) ), then select **[!UICONTROL Save]** to save your changes and remain in the VEC where you can continue to make changes. Wait for the save to complete before making additional changes. The VEC reloads with the refreshed changes after the save is complete.

## Edit an activity by clicking its name from the [!UICONTROL Activities] page {#section_176180DAD17E40CEA441903F39E0AA1C}

1. To avoid having to step through the workflow, click the desired activity from the [!UICONTROL Activities] page to open it, select an option from the **[!UICONTROL Edit Activity]** drop-down list, then select the desired option.

    * **Edit Experiences:** Takes you directly to the [!UICONTROL Experiences] page (the first step in the three-step guided workflow).
    * **Edit Targeting**: Takes you directly to the [!UICONTROL Targeting] page (the second step in the three-step guided workflow).
    * **[!UICONTROL Goals & Settings]**: Takes you directly to the [!UICONTROL Goals & Settings] page (the third step in the three-step guided workflow).  
    
1. Make your desired changes, then save the activity.

    * **[!UICONTROL Save & Close]:** Click **[!UICONTROL Save and Close]** to save your changes and display the activity's [!UICONTROL Overview] page. 
    * **Save:** Click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallListVert.svg) ), then select **[!UICONTROL Save]** to save your changes and remain in the VEC where you can continue to make changes. Wait for the save to complete before making additional changes. The VEC reloads with the refreshed changes after the save is complete.

## Work with legacy activities created in [!DNL Recommendations Classic] {#classic}

The [!UICONTROL Activities] list display activities created in various sources, including [!DNL Recommendations Classic]. The following actions are available when working with legacy activities created in [!DNL Recommendations Classic]:

* [!UICONTROL Activate]
* [!UICONTROL Deactivate]
* [!UICONTROL Archive]
* [!UICONTROL Copy]
* [!UICONTROL Delete]

You cannot edit a [!DNL Recommendations] activity directly. If you want to edit the activity, you should create a copy of the activity using [!DNL Target Premium] and then save the newly created activity. This newly created activity can then be edited as necessary.

## Save an activity in draft form {#section_968CD7A63027432EBD8FAE3A0F7404C3}

When you are creating a new activity that has not yet been saved, or you are editing an activity that was previously saved in draft form, the [!UICONTROL Save Draft] options display in the split button.

You can save an activity in draft mode if the activity setup has been started but it is not ready to run.

1. Create a new activity or edit an existing activity that is in draft form. 
1. Select the desired option from the split button:

    ![Save Draft](/help/main/c-activities/assets/save_draft.png)

    * **Next:** To edit another page in the three-step workflow, click **[!UICONTROL Next]** to advance to the desired step. 
    * **Save Draft & Close:** Make the desired changes on the current step, click the drop-down on the split button, then select **[!UICONTROL Save Draft and Close]** to save your changes and display the activity's [!UICONTROL Overview] page. 
    * **Save Draft:** Make the desired changes on a step, click the drop-down on the split button, then select **[!UICONTROL Save Draft]** to save your changes and remain on that step.

## Copying/editing an activity when using workspaces {#section_45A92E1DD3934523B07E71EF90C4F8B6}

A workspace lets an organization assign a specific set of users to a specific set of properties. In many ways, a workspace is similar to a report suite in [!DNL Adobe Analytics].

>[!NOTE]
>
>Workspaces are part of the Properties and Permissions functionality available as part of the [!DNL Target Premium] solution. They are not available in [!DNL Target Standard] without a [!DNL Target Premium] license.

If you are part of a multi-national organization, you might have a workspace for your European web pages, properties, or sites and another workspace for your American web pages, properties, or sites. If you are part of a multi-brand organization, you might have a separate workspace for each of your brands.

For more information about workspaces and the Enterprise User Permissions functionality, see [Enterprise User Permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838).

If you have Enterprise User Permissions enabled in your environment, you can copy activities to the same workspace or to another workspace. You cannot currently move an activity from one workspace to another. To copy an activity to another workspace, from the [!UICONTROL Activities] page, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) next to the activity that you want to copy then click [!UICONTROL **Copy**]. 

Consider the following information when using the copy/edit functionality with workspaces:

* When you copy an activity within the same workspace, the first step of the creation flow of the newly copied activity opens in edit mode. 
* When you copy an activity to a different workspace, the activity is copied to the other workspace without opening it in the activity creation flow. After the activity is copied successfully, a message displays indicating that the activity was copied successfully and includes a link to open the new activity.

If your environment does not have the Enterprise User Permissions functionality enabled, all activities open in edit mode before copying.