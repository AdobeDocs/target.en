---
keywords: dedupe;allow duplicates;exclude duplicate offers;automated personalization;disallow duplicate offers;exclude;default content;
description: Manage exclusions in [!UICONTROL Automated Personalization] (AP) activities.
title: How Do I Manage Exclusions in [!UICONTROL Automated Personalization] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
TQID: 'https://experienceleague.adobe.com/ERpNwQPsIRBmU0vTZbGa-lYg30BYl-uJxA8UT0f6060'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Manage exclusions {#manage-exclusions}

>[!BEGINSHADEBOX]

**On this page:** Learn how to prevent duplicate offers, exclude specific experiences, and exclude default content in **[!UICONTROL Automated Personalization]** activities.

>[!ENDSHADEBOX]

Exclusions control which offers and experiences an **[!UICONTROL Automated Personalization]** (AP) activity serves. They prevent the same offer from displaying twice, remove offer combinations that do not work together, and remove default content, so that the activity delivers cleaner and more relevant experiences that align with your goals and your audience.

## Allow or disallow duplicate offers {#allow-duplicate-offers}

<a id="concept_4EF78013F80E48EFA024AE0274C9F037"></a>

Prevent offers from the offer library from being duplicated when used in different locations in AP activities.

An activity can have, for example, six locations on a page with 12 offers, so the same offer could be placed in more than one location. Disallowing duplicate offers prevents the same offer from displaying at the same time in different locations within the same activity.

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity), click the **[!UICONTROL Configure]** icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ).

1. Click **[!UICONTROL Allow Duplicate Offers]** to toggle this feature on or off, depending on your needs.

    ![Configure icon](../assets/exclusion-1.png)

## Exclude specific experiences {#exclude-experiences}

<a id="task_C17D36EF58AF4908B17A3D84CA6DE85A"></a>

Exclude specific experiences to remove certain offer combinations from your AP activity. Some combinations might not work together, or you might limit the number of experiences tested to decrease the traffic requirements of the activity.

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity), click the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ).

   The **[!UICONTROL Experiences]** list shows each experience generated from the permutations of all content and location options.

1. Exclude the experiences that you do not want to test.

   * To exclude a single experience, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ), then click **[!UICONTROL Exclude]**.
   * To exclude several experiences at once, select the checkbox for each experience, then click **[!UICONTROL Exclude]**. The **[!UICONTROL Exclude]** icon displays when one or more experiences are selected.

   ![Batch exclude experiences](/help/main/c-activities/t-automated-personalization/assets/exclude1.png)

   The experiences are now excluded from the activity, and their **[!UICONTROL Status]** shows as **[!UICONTROL Excluded]**.

## Exclude default content {#exclude-default-content}

<a id="task_DCB4528989DF4C05A3A4729E5891D18F"></a>

Exclude default content when you do not want it to be part of your AP activity, so that a location contains only one offer that differs from your default content. This approach also lets you change the look and feel of the rest of the page to suit the offers that you test. For example, to match the color palette of the offers, you can change the background color of the page and exclude the default background color.

1. While [creating or editing an AP activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity), select the content that you want to replace, then click **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image Offer]**, or **[!UICONTROL Change Background Color]**. The available options vary depending on the type of content.

   ![Change options](../assets/exclusion-1.png)

1. Create your new content.

1. Click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/Setting.svg) ), then click the **Exclude Default Offer/Include Default Offer** toggle to exclude or include the default offer.

   <!--
   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)
   -->

<!--
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
-->
