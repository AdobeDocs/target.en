---
keywords: create recommendations;recommendations activity;new recommendations;recommendations overview
description: Learn how to use the Adobe [!DNL Target] Visual Experience Composer (VEC) to create a Recommendations activity directly on a [!DNL Target]-enabled page.
title: How Do I Create a Recommendations Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
---
# Create a Recommendations activity

Use the Target Visual Experience Composer (VEC) to create a Recommendations activity directly on a Target-enabled page and to modify portions of the page within Target.

1. Click **[!UICONTROL Activities]** > **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   ![Create Recommendations Activity dialog box](/help/main/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   If you prefer to use the Form-Based Experience Composer, select [!UICONTROL Form]. See [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >In addition to the VEC and Form-Based Experience Composer, Target offers the Single Page Application VEC and the VEC for Mobile Apps. For more information about the various composers, see [Experiences and Offers](/help/main/c-experiences/experiences.md).
   >
   >For troubleshooting information about the VEC, should you have problems, see [Troubleshooting the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >The [!UICONTROL [Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) option in the preceding illustration is a [Target Premium](/help/main/c-intro/intro.md) feature. Your organization has a Target Standard license if you do not see this option.

1. (Conditional) If you are a [Target Premium customer](/help/main/c-intro/intro.md#premium), choose a [workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specify an activity URL, and then click **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >[!DNL Target] does not differentiate between URL protocols ( [!DNL https] and [!DNL http]). As a result, [!DNL `http://www.adobe.com`] and [!DNL `https://wwww.adobe.com`] both match.

   The activity URL is the page where the recommendations will be displayed.

   When you click [!UICONTROL Next], the VEC opens and shows your page. You can replace a current element with recommendations, or insert recommendations.

1. Click an element on your page, then if recommendations are available where that element is located, click **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]**, or **[!UICONTROL Insert Recommendations After]**.

   Visitors to your site will see the recommended content only if they qualify for the recommendation. Visitors who do not qualify for the recommendation will see default content.

   ![Recommendations options](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Replace w/ Recommendations]**: Replacing an element with recommendations deletes the current content and replaces it with your recommendations. When visitors visit your site and qualify for the recommendation, they'll see the recommended items in the specified area instead of the existing content.
   * **[!UICONTROL Insert Recommendations Before]**: Inserting recommendations before the selected element places the recommended content before that element. Depending on your page construction, the recommendation displays above or to the left of the selected element.
   * **[!UICONTROL Insert Recommendations After]**: Inserting recommendations after the selected element places the recommended content after that element. Depending on your page construction, the recommendation displays below or to the right of the selected element.

   The **[!UICONTROL Expand Selection]** option lets you expand the selected location (parent container) to help you easily identify and include the desired page elements more easily.

1. Select a page type.

   Page types can include:

   * Cart Page
   * Category Page
   * Home Page
   * Landing Page
   * Product Page
   * Search Results Page
   * Thank You Page
   * Other

   ![Select Page Type options](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. Select one or more [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md).

   Criteria are displayed as cards that show information about each criteria. By default, the [!UICONTROL Select Criteria] screen displays criteria that are compatible with your industry vertical and the page type you selected in the previous step. You can change these options to display other criteria.

   >[!NOTE]
   >
   >Not every criteria will run correctly on every page. The page or mbox must pass in `entity.id` or `entity.categoryId` for current item/current category recommendations to be compatible. In general, it is best to show only compatible criteria. However, if you want incompatible criteria to be available for the activity, clear the **[!UICONTROL Compatible]** check box. The [!UICONTROL Compatible] option might not display, depending on your Recommendations settings ( **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]**). For more information, see [Settings](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

   ![Select Criteria dialog box](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   If you select multiple criteria, traffic is split evenly between the selected criteria. For example, if you have selected two criteria and your activity is designed to display default content to 20% of activity entrants, then 40% of activity entrants will see the recommendations controlled by each criteria. There is no option to change the percentages for each criteria.

   * To search for an existing criteria (for example, if a large number of criteria cards are displayed), type in the search field until the desired criteria appears, then select the criteria and click **[!UICONTROL Next]**.

     Some criteria are supplied with [!DNL Recommendations]. You and your team can also create your own custom criteria. 

   * To create a new criteria, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**, then fill in the information for the new criteria. For information about creating new criteria, see [Creating Criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md). 
   * You can also group criteria into sequences. To create a new criteria sequence, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. See [Create Criteria Sequence](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md) for more information.

1. Click **[!UICONTROL Next]**.
1. Select a [design](/help/main/c-recommendations/c-design-overview/design-overview.md).

   A design is a template that determines the look of the locations on your page. [!DNL Target] includes several pre-configured designs. You can also create your own custom designs. For more information, see [Create a Design](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) and [Customizing a Design](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![Select Design dialog box](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Each design shows a graphical representation of how it will look, and icons that show how many of your live and inactive activities currently use that design.

   * To select one or more existing designs, click the designs, then click **[!UICONTROL Next]**.

     If you selected multiple criteria, you can select only one design. 

   * To create a custom design, click **[!UICONTROL Create Design]**, then fill in the name and code for the new design. Click **[!UICONTROL Next]**, then select or upload an image and click **[!UICONTROL Done]** > **[!UICONTROL Done]**. For information about creating a new design, see [Create a Design](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Click **[!UICONTROL Next]**.

   You have the option to add promotions to your recommendations. For more information about adding front and back promotions, see [Adding Promotions](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Click **[!UICONTROL Save]**.

   The VEC screen displays the recommendation design on your page.

1. (Optional) Click **[!UICONTROL Preview]** to see how the activity will appear to visitors.

   [!UICONTROL Preview] mode allows you to interact with your recommendations, much as a visitor would.

   When you are finished previewing your recommendations, click **[!UICONTROL Compose]**.

1. Review your recommendation in the VEC, then click **[!UICONTROL Next]**.

1. Review your [!DNL Recommendations] activity in the flow diagram and make any necessary changes.

   ![Recommendations flow diagram](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   The flow diagram leads you through the steps of choosing the audience for the activity, setting up experiences, and specifying success metrics. 

   From the flow diagram, you can do the following:

   * Change the audience that will see the recommendations

     >[!NOTE]
     >
     >In addition to selecting an existing audience, you can [create an activity-only audience](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) or [combine multiple audiences](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) to create ad hoc audiences rather than creating a new audience.

     By default, all users see the recommendations. However, you can target recommendation to a specific audience.

     For a [!DNL Recommendations] activity, the control group sees the page without any recommendations. 

   * View the criteria 
   * Change the collection (next to the [!UICONTROL Criteria] label) 
   * Change the percentage of entrants who see the control experience 
   * View the design code 
   * Change or remove a design

1. Click **[!UICONTROL Next]** when finished.
1. Specify your activity settings.

   For example, type a name (required) and objective (optional) for the activity. For information about the settings, see [Recommendations Activity Settings](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB).

   >[!NOTE]
   >
   >If you specify a [!DNL Recommendation] activity name that already exists for another activity in [!DNL Recommendations Classic], the new activity is re-synced with a new name. The new name is the original name appended with a timestamp to make it unique. This new name is displayed in both [!DNL Target Standard/Premium] and [!DNL Recommendations Classic].

1. When finished, click **[!UICONTROL Save & Close]**.

   An overview of your activity is displayed. 

   From the [!UICONTROL Overview] page, you can:

   * Activate the activity 
   * Edit the activity 
   * Share the activity to your Experience Cloud feed
   * QA the activity 
   * View your experience URLs 
   * Download data 
   * Change the percentage of activity entrants who see the control experience 
   * Show or hide criteria details 
   * View the code for your designs

1. (Optional) Open the [!UICONTROL Reports] page to view the report that shows the performance of your [!DNL Recommendations] activity.

1. (Optional) Open the [!UICONTROL Collisions] page to view any [activity collisions](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) that might occur.

   Activity collisions occur when multiple activities are set to deliver content to the same page, and may cause unexpected content to be displayed.

## Training Video: Create a Recommendations activity (7:15) ![Tutorial badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
