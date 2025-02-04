---
keywords: automated personalization;offers;target;audience;targeting rules;targeting
description: Discover how to target individual offers to specific audiences using [!UICONTROL Automated Personalization] (AP) activities.
title: How Can I Target [!UICONTROL Automated Personalization] Offers?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
---
# Target [!UICONTROL Automated Personalization] offers

In an [!DNL Adobe Target] [!DNL Automated Personalization] (AP) activity, you can target offers to specific audiences.

Using this functionality reduces the number of offers a specific visitor is qualified to see. For example, consider an [!UICONTROL Automated Personalization] activity that has three offers. Offer 1 has a targeting rule that limits its exposure to Audience A. Two visitors saw this activity.

| | Visitor 1 | Visitor 2 |
|--- |--- |--- |
|Audience qualification|Audience A|Audience B|
|Offer 1 Target personalization model score|90|90|
|Offer 2 Target personalization model score|50|70|
|Offer 3 Target personalization model score|80|60|

In this scenario, Visitor 1 sees Offer 1 (because this visitor qualifies as part of Audience A), which is that visitor's highest score. However, Visitor 2 sees Offer 2 even though the highest score is for Offer 1, because Visitor 2 is not part of Audience A. This example demonstrates why targeting rules should be used sparingly to meet business needs. Adding these rules can reduce the effectiveness of [!DNL Target] personalization models.

## Set up targeting rules 

1. Create or edit an [Automated Personalization activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) containing the offers that you want to target.
1. After setting up the offers for the activity in the [!UICONTROL Visual Experience Composer], click the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ).

   The [!UICONTROL Manage Content] dialog box displays.

1. Click the **[!UICONTROL Offers]** tab.

1. Select the desired offers, then choose the audiences you want to qualify to see that offer.

   To set up targeting for a single offer, click the More Info ( ![More Info icon](/help/main/assets/icons/MoreSmallList.svg) ) icon next to the desired offer, then click **[!UICONTROL Target Audience]** to display the [!UICONTROL Add Audiences] dialog box.

   To set up targeting for multiple offers, select the checkboxes for the desired offers, then click the **[!UICONTROL Target Audience]** link that displays at the bottom of the list.

1. In the [!UICONTROL Add Audiences] dialog box, select the desired audiences for the offers, then click **[!UICONTROL Assign Audience]** to return to the [!UICONTROL Manage Content] dialog box.

   >[!NOTE]
   >
   >In addition to selecting an existing audience, you can combine multiple audiences to create on-demand combined audiences rather than creating a new audience. For more information, see [Combining Multiple Audiences](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Click **[!UICONTROL Done]**.

>[!NOTE]
>
>You can set up 50 locations, and up to 250 offers per location.
