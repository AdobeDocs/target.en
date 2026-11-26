---
keywords: Recommendations;offer
description: Learn how to use Adobe Recommendations as an offer in A/B Tests (including Auto-Allocate and Auto-Target) and Experience Targeting (XT) activities.
title: How Do I Use Recommendations as an Offer in Other Activity Types?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
TQID: 'https://experienceleague.adobe.com/ZMOb5RdY6bES331INSM7VF-w4be-5Xmjqon0YvfuNG4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Recommendations as an offer {#recommendations-as-an-offer}

>[!BEGINSHADEBOX]

**On this page:** Learn how to add, edit, and delete a recommendation as an offer in [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] (XT) activities.

>[!ENDSHADEBOX]

In addition to [!UICONTROL Recommendations] activities, recommendations can be included inside [!UICONTROL A/B Test] (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) and [!UICONTROL Experience Targeting] (XT) activities. This allows the following:

* Test and target recommendations and non-recommendations content within the same activity.
* Experiment with the placement of recommendations on the page, including the order of multiple recommendations.
* Automatically push traffic to the best-performing recommendations experience with **[!UICONTROL Auto-Allocate]**.
* Dynamically assign visitors to tailored recommendations experiences based on their profile with **[!UICONTROL Auto-Target]**.

## Add a recommendation as an offer {#add-recs-offer}

A recommendation is added as an offer while an experience is created with the [!UICONTROL Visual Experience Composer] (VEC) in an [!UICONTROL A/B Test] or XT activity.

1. Start the three-step guided workflow of the VEC to create an [A/B Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) or [Experience Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) activity.

   >[!NOTE]
   >
   >For A/B Tests, the [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) option automatically pushes traffic to the best-performing recommendations, and the [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) option assigns visitors to tailored recommendations experiences based on their profile.

1. While creating an [experience](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), add the recommendation as an offer in one of the following ways:

   * Click the element to which the recommendation is added, click **[!UICONTROL Replace Content]**, then select **[!UICONTROL Recommendation]**.

     ![Visual Experience Composer with a heading selected and the Recommendation option highlighted in the menu, next to the HTML Offer and Experience Fragment options](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

   * In the **[!UICONTROL Components]** rail, select **[!UICONTROL Recommendation]** under **[!UICONTROL Dynamic]**, hover over an existing element on the page, then click **[!UICONTROL Insert before]** or **[!UICONTROL Insert after]** to place the recommendation before or after that element.

1. Access the **[!UICONTROL Show properties]** menu and click **[!UICONTROL Select a recommendation]**.

1. Select the desired [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md), then click **[!UICONTROL Next]**.

1. Select the desired [design](/help/main/c-recommendations/c-design-overview/design-overview.md), then click **[!UICONTROL Next]**.

1. In the **[!UICONTROL Options]** dialog box, specify the following:

   * Choose a [collection](/help/main/c-recommendations/c-products/collections.md).
   * If necessary, configure the [Front Promotion and Back Promotion](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md) options.

1. Click **[!UICONTROL Save]**.

1. Finish configuring the [!UICONTROL A/B Test] or XT activity with the three-step guided workflow.

## Edit a recommendations offer {#edit-recs-offer}

The criteria, design, collection, and promotions of a recommendations offer can be changed after the offer is added, from the **[!UICONTROL Recommendation]** pane.

1. Click the offer to edit and browse through the options in the right-pane menu.

   ![Recommendation pane with the criteria, design, and collection names and the Add promotion button of the selected offer](assets/create_reco_7.png)

1. Select one of the following options:

   * [Change Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Change Design](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Change Collection](/help/main/c-recommendations/c-products/collections.md)
   * [Change Promotion](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Make the edits.

## Delete a recommendations offer {#delete-recs-offer}

A recommendations offer that is no longer needed can be deleted from the **[!UICONTROL Recommendation]** pane.

Click the offer to remove, then click the bin icon ( ![Bin icon](assets/Smock_Delete_18_N.svg) ) in the **[!UICONTROL Recommendation]** pane.

![Recommendation pane with the bin icon highlighted](assets/create_reco_8.png)

## View the status of a recommendations offer {#status}

The status of the recommendations offer (algorithm) displays at the bottom of the **[!UICONTROL Overview]** page for [!UICONTROL A/B Test] and XT activities that contain recommendations offers. The status is one of the following:

* **[!UICONTROL Results Ready]**
* **[!UICONTROL Results Not Ready]**
* **[!UICONTROL Feed Failure]**

## Training video: Recommendations as an offer ![Overview badge](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
