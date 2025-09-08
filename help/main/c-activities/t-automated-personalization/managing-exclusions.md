---
keywords: dedupe;allow duplicates;exclude duplicate offers;automated personalization;disallow duplicate offers;exclude;default content;
description: Manage exclusions in [!UICONTROL Automated Personalization] (AP) activities.
title: How Do I Manage Exclusions in [!UICONTROL Automated Personalization] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
---
# Manage exclusions

Manage exclusions by excluding duplicate offers, excluding specific experiences, and excluding default content in [!UICONTROL Automated Personalization] (AP) activities in [!DNL Adobe Target].

## Allow or disallow duplicate offers {#concept_4EF78013F80E48EFA024AE0274C9F037}

Prevent offers from the offer library from being duplicated when used in different locations in [!UICONTROL Automated Personalization] activities. 

You might have an activity, for example, with six locations on a page with 12 offers. There is a chance that the same offer could be placed in one or more locations in the activity. This feature lets you prevent duplicate offers from displaying at the same time in different locations within the same activity. 

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), click the **[!UICONTROL Configure]** icon ( ![Configure icon](/help/main/assets/icons/Setting.svg ) ) > click the **[!UICONTROL Allow Duplicate Offers]** to toggle this feature on and off, depending on your needs.

## Exclude specific experiences {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Exclude specific experiences if you want to exclude certain offer combinations from your [!UICONTROL Automated Personalization] activity. 

There might be certain combinations that don't work together, or you might be limiting the number of experiences tested to decrease traffic requirements for your activity. 

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), click the **Manage Content** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ).

   The [!UICONTROL Experiences] list shows each experience generated from the permutations of all content and location options. 

1. Exclude experiences, as desired.

   You can exclude specific experiences by clicking the [!UICONTROL **More Actions**] icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ), then clicking [!UICONTROL **Exclude**]. 

   Or you can batch exclude experiences by selecting the checkbox for the relevant experiences and then clicking **[!UICONTROL Exclude]**. The [!UICONTROL Exclude] icon displays when one or more experiences are checked. 

   ![Batch exclude experiences](/help/main/c-activities/t-automated-personalization/assets/exclude1.png)

   The experiences are now excluded from the activity and their [!UICONTROL Status] show as [!UICONTROL Excluded]. 

## Exclude default content {#task_DCB4528989DF4C05A3A4729E5891D18F}

Sometimes, you might not want to include your default content as part of your [!UICONTROL Automated Personalization] activity. You can use this method to have only one offer (different from your default content) in a location as part of your AP activity. 

Excluding default content is a great way to change the look and feel of the rest of the page to suit the offers you are testing with your AP activity. For example, suppose you want to match the color palette of the offers you are testing, you could change the background color of your page and exclude the default background color. 

**To exclude default content using the [!UICONTROL Visual Experience Composer] (VEC):** 

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), select the content you want to replace and click to access **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image Offer]**, or **[!UICONTROL Change Background Color]**. The available options vary, depending on the type of content.

   ![Change options](/help/main/c-activities/t-automated-personalization/assets/options.png)

1. Create your new content and uncheck **Include** to the right of the default content (or uncheck the Default Image/Video in the [!UICONTROL Select Content] screen).

   <!-- Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)-->
   
<!-- 1. Click **[!UICONTROL Save]**.

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

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)-->
