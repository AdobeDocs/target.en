---
keywords: dedupe;allow duplicates;exclude duplicate offers;automated personalization;disallow duplicate offers;exclude;default content;exclusion group;
description: Manage exclusions in [!UICONTROL Automated Personalization] (AP) activities.
title: How Do I Manage Exclusions in [!UICONTROL Automated Personalization] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
hide: yes
hidefromtoc: yes
exl-id: 6debf1b8-a0e9-42ef-ba8d-20bd94266149
---
# Manage exclusions

Manage exclusions by creating exclusion groups, excluding duplicate offers, excluding specific experiences, and excluding default content in [!UICONTROL Automated Personalization] (AP) activities in [!DNL Adobe Target].

## Create exclusion groups {#task_AAAA6C7239A84F7696C8492F04B575A2}

Create exclusion groups in [!UICONTROL Automated Personalization] (AP) activities to ensure that experiences with the designated offers are automatically excluded. 

Exclusion groups are a great way to ensure that incompatible offers are not presented in the same experience in different locations. For example, suppose you have two offers: one is for a 20% discount for all merchandise and the other is for a 15% discount. You never want these two offers to be presented to visitors in the same experience. If you add these two offers to an exclusion group, you can ensure that this situation is never the case.

You can also limit which audiences can see specific offers in AP activities. For more information, see [Target Automated Personalization offers](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

**To create an exclusion group:** 

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), click the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ).

   The [!UICONTROL Manage Content] dialog box displays.

1. Click the **[!UICONTROL Experiences]** tab.

1. In the [!UICONTROL Manage Content] dialog box, click **[!UICONTROL Exclusion Groups]**.

   ![Manage Content > Exclusion Groups dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   If you have previously created exclusion groups, they display in the list. If you have not yet created an exclusion group, you are prompted to create one.

1. Click **[!UICONTROL Create Exclusion Group.]**

   ![Create Exclusion Group dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Required) Specify a descriptive name for the exclusion group.

   A descriptive name helps you or others quickly locate and understand a group's purpose.

1. Locate and select the desired offers that you want to add to the exclusion group.

   You can select multiple offers from the same location in an exclusion group.

1. Click **[!UICONTROL Save]**.

The offers in the exclusion group are automatically excluded from the same experiences going forward. 

## Exclude duplicate offers {#concept_4EF78013F80E48EFA024AE0274C9F037}

Prevent offers from the offer library from being duplicated when used in different locations in [!UICONTROL Automated Personalization] activities. 

You might have an activity, for example, with six locations on a page with 12 offers. There is a chance that the same offer could be placed in one or more locations in the activity. This feature prevents duplicate offers from displaying at the same time in different locations within the same activity. 

Click the **[!UICONTROL Configure]** gear option > **[!UICONTROL Duplicate Offers]**, then click **[!UICONTROL Allow Duplicates]** or **[!UICONTROL Disallow Duplicates]**. 

![Duplicate offers options](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Exclude specific experiences {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Exclude specific experiences if you want to exclude certain offer combinations from your [!UICONTROL Automated Personalization] activity. 

There might be certain combinations that don't work together, or you might be limiting the number of experiences tested to decrease traffic requirements for your activity. 

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), click **Manage Content** in the header bar.

   ![Manage Content link](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   The [!UICONTROL Experiences] list shows each experience generated from the permutations of all content and location options. 

1. Exclude experiences, as desired.

   You can exclude specific experiences by hovering over the desired experience and then clicking the exclude icon. 

   ![Exclude experience by hovering](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Or you can batch exclude experiences by selecting the checkbox for the relevant experiences and then clicking the **[!UICONTROL Exclude]** icon in the top-right corner of the dialog box. The [!UICONTROL Exclude] icon displays when one or more experiences are checked. 

   ![Batch exclude experiences](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   You can filter this list view to see only excluded or only included activities by clicking the [!UICONTROL Status] drop-down list. 

   The experiences are now excluded from the activity and their [!UICONTROL Status] show as [!UICONTROL Excluded]. 

   ![Excluded experiences](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Exclude default content {#task_DCB4528989DF4C05A3A4729E5891D18F}

Sometimes, you might not want to include your default content as part of your [!UICONTROL Automated Personalization] activity. How you access this setting is different from creating exclusion groups. You can use this method to have only one offer (different from your default content) in a location as part of your AP activity. 

Excluding default content is a great way to change the look and feel of the rest of the page to suit the offers you are testing with your AP activity. For example, suppose you want to match the color palette of the offers you are testing, you could change the background color of your page and exclude the default background color. 

**To exclude default content using the [!UICONTROL Visual Experience Composer] (VEC):** 

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), select the content you want to replace and click to access **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]**, or **[!UICONTROL Change Background Color]**.
1. In the dialog box, create your new content and uncheck **Include** to the right of the default content (or uncheck the Default Image/Video in the [!UICONTROL Select Content] screen).

   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)
   
1. Click **[!UICONTROL Save]**.

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_vec_4 image](assets/exclude_content_vec_4.png)

**To exclude default content using the [!UICONTROL Form-Based Experience Composer]:** 

1. While creating or editing an AP activity, click **[!UICONTROL Change Text/HTML]** or **[!UICONTROL Change Image Offer]** under **[!UICONTROL Content]**. 
1. In the dialog box, create your new content and uncheck **[!UICONTROL Include]** to the right of the default content (or uncheck the Default Image/Video in the [!UICONTROL Select Content] screen). 

   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![exclude_content_form_1 image](assets/exclude_content_form_1.png)

   For Image/Video content: 

   ![exclude_content_form_2 image](assets/exclude_content_form_2.png)

1. Click **[!UICONTROL Save]**. 

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)
