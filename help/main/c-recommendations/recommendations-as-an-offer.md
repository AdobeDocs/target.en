---
keywords: Recommendations;offer
description: Learn how to use Adobe Recommendations as an offer in A/B Tests (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities.
title: How Do I Use Recommendations as an Offer in Other Activity Types?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
---
# Recommendations as an offer

You can now include recommendations inside [!UICONTROL A/B Test] (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) and [!UICONTROL Experience Targeting] (XT) activities. 

This functionality opens up entirely new capabilities, such as:

* Test and target recommendations and non-recommendations content within the same activity.
* Easily experiment with placement of recommendations on the page, including the order of multiple recommendations.
* Automatically push traffic to the best-performing recommendations experience using [!UICONTROL Auto-Allocate].
* Dynamically assign visitors to tailored recommendations experiences based on their profile using [!UICONTROL Auto-Target].

To get started, create an [!UICONTROL A/B Test] or [!UICONTROL Experience Targeting] activity using the [!UICONTROL Visual Experience Composer] and use the [!UICONTROL Insert Before], [!UICONTROL Insert After], or [!UICONTROL Replace With] action to add recommendations to an experience.

## Add a recommendation as an offer in an A/B Test or XT activity

1. Start the three-step guided workflow using the Visual Experience Composer (VEC) to create an [A/B Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) or [Experience Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) activity.
  
   >[!NOTE]
   >
   >For A/B Tests, remember that you can choose the [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) option to automatically push traffic to the best-performing recommendations or the [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) option to assign visitors to tailored recommendations experiences based on their profile.

1. While creating an [experience](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), click the element you want to add a recommendation to as an offer, click **[!UICONTROL Replace Content]**, then select **[!UICONTROL Recommendation]**.

   ![Insert recommendation as an offer](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Select from the following options to view popular recommendations criteria by page type:

   * Cart Page
   * Category Page
   * Home Page
   * Landing Page
   * Product Page
   * Search Results Page
   * Thank You Page
   * Other

1. Select the desired [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md), then click [!UICONTROL Next].
1. Select the desired [design](/help/main/c-recommendations/c-design-overview/design-overview.md), then click [!UICONTROL Next].
1. In the [!UICONTROL Options] dialog box, specify the following:

   * Choose a [collection](/help/main/c-recommendations/c-products/collections.md).
   * Configure the [Front Promotion and Back Promotion](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md) options, as necessary. 

1. Click [!UICONTROL Save].
1. Finish configuring the A/B Test or XT activity using the three-part guided workflow.

## Edit a recommendations offer's configuration

There are two ways you can edit an offer's configuration: 

* Using the [!UICONTROL Edit] menu
* Using the [!UICONTROL Modifications] panel 

### Edit a recommendations offer using the Edit menu

1. Click the offer you want to edit, then click **[!UICONTROL Edit]**.

   ![Edit recommendations offer](/help/main/c-recommendations/assets/recs-offer-edit.png)

1. Choose from the following options:

   * [Change Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Change Design](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Change Collection](/help/main/c-recommendations/c-products/collections.md)
   * [Change Promotion](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Make your edits.

### Edit a recommendations offer using the Modifications panel

1. Click the [!UICONTROL Modifications] icon  **( `</>` )** to display the [Modifications](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) pane.
1. Hover over the desired action, then click the **[!UICONTROL Edit]** icon.

   ![Modifications panel](/help/main/c-recommendations/assets/recs-offer-modifications.png)

1. Make your edits.

## Delete a recommendations offer

There are two ways to delete a recommendations offer:

* Using the [!UICONTROL Edit] menu
* Using the [!UICONTROL Modifications] panel

### Delete a recommendations offer using the Edit Menu

1. Click the offer you want to remove, then click **[!UICONTROL Layout > Remove]**.

   ![Remove](/help/main/c-recommendations/assets/recs-offer-remove.png)

### Delete a recommendations offer using the Modifications panel

1. Click the [!UICONTROL Modifications] icon **( </> )** to display the [Modifications](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) pane.
1. Hover over the desired action, then click the [!UICONTROL Delete] icon.

   ![Delete icon](/help/main/c-recommendations/assets/recs-offer-delete.png)

### Viewing the recommendations offer's status {#status}

The recommendations offer's (algorithm) status displays at the bottom of the [!UICONTROL Overview] page for A/B Test and XT activities that contain Recommendations offers: 

* Results Ready
* Results Not Ready
* Feed Failure

![Recommendations offer status](/help/main/c-recommendations/assets/recs-offer-status.png)

## Training video: Recommendations as an offer ![Overview badge](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
