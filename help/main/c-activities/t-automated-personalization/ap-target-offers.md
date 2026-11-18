---
keywords: automated personalization;offers;target;audience;targeting rules;targeting
description: Discover how to target individual offers to specific audiences using [!UICONTROL Automated Personalization] (AP) activities.
title: How Can I Target [!UICONTROL Automated Personalization] Offers?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
TQID: 'https://experienceleague.adobe.com/AVqyD-Von-gzuVXC09N9qHY5hEe1QLQwSavCE0mp7Ok'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Target [!UICONTROL Automated Personalization] offers {#target-ap-offers}

>[!BEGINSHADEBOX]

**On this page:** Learn how to target individual offers to specific audiences in an **[!UICONTROL Automated Personalization]** activity.

>[!ENDSHADEBOX]

In an [!DNL Adobe Target] **[!UICONTROL Automated Personalization]** (AP) activity, targeting rules let you limit an offer to specific audiences, so that only visitors who belong to those audiences can see it. Use targeting rules sparingly, and only when a business need requires them, because they reduce the number of offers a visitor qualifies to see and can lower the effectiveness of the [!DNL Target] personalization models.

For example, consider an AP activity that has three offers. Offer 1 has a targeting rule that limits its exposure to Audience A. Two visitors see this activity.

| | Visitor 1 | Visitor 2 |
|--- |--- |--- |
|Audience qualification|Audience A|Audience B|
|Offer 1 [!DNL Target] personalization model score|90|90|
|Offer 2 [!DNL Target] personalization model score|50|70|
|Offer 3 [!DNL Target] personalization model score|80|60|

Visitor 1 qualifies as part of Audience A, so this visitor sees Offer 1, which has the highest score. Visitor 2 is not part of Audience A, so this visitor sees Offer 2, even though the highest score is for Offer 1.

## Set up targeting rules {#set-up-targeting-rules}

<a id="task_F207ED7A41B84FD39BB6FCBFABF4B23E"></a>

Audience targeting rules control which visitors can see each offer, which allows you to meet a specific business need, such as reserving an offer for a customer segment. Every rule narrows the choices of the personalization model, so apply rules only to the offers that require them.

1. Create or edit an [Automated Personalization activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) that contains the offers that you want to target.

    You can set up 50 locations, and up to 250 offers per location.

1. After setting up the offers for the activity in the **[!UICONTROL Visual Experience Composer]**, click the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ). The **[!UICONTROL Manage Content]** dialog box displays.

    ![Manage Content icon](../assets/ap-offers-1.png)

1. Click the **[!UICONTROL Offers]** tab.

1. Choose the offers to target, then choose the audiences that qualify to see them.

   * To set up targeting for a single offer, click the More Info ( ![More Info icon](/help/main/assets/icons/MoreSmallList.svg) ) icon next to the offer, then click **[!UICONTROL Target Audience]** to display the **[!UICONTROL Add Audiences]** dialog box.
   * To set up targeting for multiple offers, select the checkboxes for the offers, then click the **[!UICONTROL Target Audience]** link that displays at the bottom of the list.

    ![Manage Content icon](../assets/ap-offers-2.png)

1. In the **[!UICONTROL Add Audiences]** dialog box, select the audiences for the offers, then click **[!UICONTROL Assign Audience]** to return to the **[!UICONTROL Manage Content]** dialog box.

   >[!NOTE]
   >
   >Instead of creating a new audience, you can combine multiple audiences with existing ones to create on-demand combined audiences. For more information, see [Combining Multiple Audiences](/help/main/c-target/combining-multiple-audiences.md).

1. Click **[!UICONTROL Done]**.

The targeting rules now apply to the selected offers, so only visitors who belong to the assigned audiences can see them.
