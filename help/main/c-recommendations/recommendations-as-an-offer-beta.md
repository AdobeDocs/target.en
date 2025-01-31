---
keywords: Recommendations;offer
description: Learn how to use Adobe Recommendations as an offer in A/B Tests (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities.
title: How Do I Use Recommendations as an Offer in Other Activity Types?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
hide: yes
hidefromtoc: yes
---
# Recommendations as an offer

You can now include recommendations inside [!UICONTROL A/B Test] (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) and [!UICONTROL Experience Targeting] (XT) activities. 

This functionality opens up entirely new capabilities, such as:

* Test and target recommendations and non-recommendations content within the same activity.
* Easily experiment with the placement of recommendations on the page, including the order of multiple recommendations.
* Automatically push traffic to the best-performing recommendations experience using [!UICONTROL Auto-Allocate].
* Dynamically assign visitors to tailored recommendations experiences based on their profile using [!UICONTROL Auto-Target].

To get started, create an [!UICONTROL A/B Test] or [!UICONTROL Experience Targeting] activity using the [!UICONTROL Visual Experience Composer] and use the [!UICONTROL Recommend] action to add recommendations to an experience.

## Add a recommendation as an offer in an A/B Test or XT activity

1. Start the three-step guided workflow using the Visual Experience Composer (VEC) to create an [A/B Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) or [Experience Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) activity.
  
   >[!NOTE]
   >
   >For A/B Tests, remember that you can choose the [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) option to automatically push traffic to the best-performing recommendations or the [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) option to assign visitors to tailored recommendations experiences based on their profile.

1. While creating an [experience](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), click the element you want to add a recommendation to as an offer, click **[!UICONTROL Replace Content]** ( ![Replace Content icon](/help/main/assets/icons/Switch.svg) ), then select **[!UICONTROL Recommendation]**.

   ![Insert recommendation as an offer](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. From the [!UICONTROL Recommendation] rail on the right side, click **[!UICONTROL Select a Recommendation]** to display the [!UICONTROL Select Criteria] dialog box.

1. Click **[!UICONTROL Create Criteria]** or select an existing criteria.

1. (Optional) Click the **[!UICONTROL Filter]** icon ( ![Filter icon](/help/main/assets/icons/Filter.svg) ) to select from the following options to view popular recommendations criteria by page type:

   * Cart Page
   * Category Page
   * Home Page
   * Landing Page
   * Product Page
   * Search Results Page
   * Thank You Page
   * Other

1. Click **[!UICONTROL Create Criteria]** or select an existing [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md), then click **[!UICONTROL Next]** to display the [!UICONTROL Select Design] dialog box.

1. Click **[!UICONTROL Create Design]** or select an existing [design](/help/main/c-recommendations/c-design-overview/design-overview.md), then click [**!UICONTROL Next]**.

1. In the [!UICONTROL Options] dialog box, specify the following:

   * Choose a [collection](/help/main/c-recommendations/c-products/collections.md).
   * Configure the [Front Promotion and Back Promotion](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md) options, as necessary. 

1. Click **[!UICONTROL Save]**.
1. Finish configuring the A/B Test or XT activity using the three-part guided workflow.

## Edit a recommendations offer's configuration

1. From the [!UICONTROL Recommendation] rail, click the **[!UICONTROL Edit]** icon ( ![Edit icon](/help/main/assets/icons/Edit.svg) ) next to [!UICONTROL Criteria Name], [!UICONTROL Design Name], or [!UICONTROL Collection Name] to change the element.

## Delete a recommendations offer

1. Click the **[!UICONTROL Delete]** icon ( ![Delete icon](/help/main/assets/icons/Delete.svg) ) at the top of the [!UICONTROL Recommendation] panel.

### Viewing the recommendations offer's status {#status}

The recommendations offers (algorithm) status displays at the bottom of the activity's [!UICONTROL Overview] page for A/B Test and XT activities that contain Recommendations offers: 

* Results Ready
* Results Not Ready
* Feed Failure
