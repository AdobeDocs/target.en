---
keywords: automated personalization;offer;reporting;group;reporting group;ap
description: Learn how to use offer reporting groups in [!DNL Adobe Target] [!UICONTROL Automated Personalization] activities.
title: Can I Use Offer Reporting Groups in [!UICONTROL Automated Personalization] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
TQID: 'https://experienceleague.adobe.com/VW3zVGXb3IuQMDaRyidbkjsbUrojvwFsvwP3yRVeHp4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: e8a43148-398f-56c7-9433-6564f96999c2
    internal-label: Reports
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Offer reporting groups in [!UICONTROL Automated Personalization] {#offer-reporting-groups}

>[!BEGINSHADEBOX]

**On this page:** Learn how offer reporting groups work in **[!UICONTROL Automated Personalization]** activities, how to set them up, and how to view them in reports.

>[!ENDSHADEBOX]

Reporting groups let you organize the offers of an [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) activity into groups. Reporting groups perform two key functions:

* They let you see your offers grouped in AP activity reporting.
* They play a key role in how the [!DNL Target] personalization models function.

When you use reporting groups, [!DNL Target] creates one personalization model for each reporting group, using the data from all offers in that group. Without reporting groups, [!DNL Target] creates a personalization model for each offer in your AP activity.

Reporting groups also reduce the data requirements to use **[!UICONTROL Automated Personalization]** when your activity setup does not have enough data to build a personalization model per offer. They help with the "cold start" problem of new offers, which are grouped with similar offers so that each model has more data to train on.

This approach works well when visitors respond the same way to all offers in a group, so group offers with similar conversion rates. Never put all offers into a single reporting group, and do not group offers with different conversion rates, because both choices are likely to reduce the effectiveness of the [!DNL Target] personalization models.

>[!NOTE]
>
>If an offer is removed from or replaced in a reporting group, the historical traffic that saw that offer is also deleted from the group, so deleted offers do not contribute to the data that the [!DNL Target] personalization models use to learn.


## Considerations

### Use reporting groups for live activities

Reporting groups affect how [!DNL Target] builds its models. As a result, [!DNL Adobe] recommends that you use reporting groups only if you plan to replace or add offers while an activity is live. If a new offer is introduced into a live activity, putting the new offer into a group with existing similar offers allows [!DNL Target] to use the data already collected for the other offers in the group to learn about the new offer.

### How data is recorded for offers and locations

AP activities have combinations of location and offer (modellables). When [!DNL Target] records data in reports, it considers these combinations, so it is clear from which event (display, click, and so forth) the offer came.

For example, an activity might have several locations and several offers, which might overlap. If a visitor sees more than one of these offers in different locations, [!DNL Target] records data for those offers only. If the same visitor later clicks an offer, [!DNL Target] records an event from that combination only (not for all combinations).

Similarly, if the click comes from a different location that is present in a metric but does not display an offer, the event is logged under the activity, but not for any combination of offer and location. As a result, this offer does not appear in the offer reporting group. This behavior occurs because the click might be made from a different mbox than the one that served the offer. In that case, the metric is associated with the activity, but not with the offer.

## Set up reporting groups

Assigning offers to reporting groups determines how [!DNL Target] builds its personalization models and how the offers display in the activity reports. Set up the groups while you build the activity, or later, if you add new offers to a live activity.

1. On the **[!UICONTROL Experiences]** page of an AP activity, click the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ).

1. Click the **[!UICONTROL Offers]** tab at the top of the **[!UICONTROL Manage Content]** dialog box.

    ![Configure icon](../assets/ap-offers-2.png)

1. (Conditional) Choose the offers to add to a reporting group.

   * To add a single offer, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) for the offer, then click **[!UICONTROL Reporting Group]**.
   * To add several offers at once, select the checkboxes for the offers, then click **[!UICONTROL Reporting Group]** at the bottom of the dialog box.

1. Assign the selected offers to a reporting group.

   * To assign the offers to an existing reporting group, select **[!UICONTROL Existing]**, select the reporting group from the drop-down list, then click **[!UICONTROL Confirm]**.
   * To create a reporting group for the offers, select **[!UICONTROL New]**, name the new reporting group, then click **[!UICONTROL Confirm]**.

To narrow the list of offers, filter it by location with the **[!UICONTROL Location]** list, or by reporting group with the **[!UICONTROL Report Group]** list. The **[!UICONTROL Report Group]** list also offers the **[!UICONTROL Unassigned Offers]** option, which displays the offers that do not belong to any reporting group yet, so that you can assign them to one.

For information about targeting an offer to specific audiences, see [Target **[!UICONTROL Automated Personalization]** offers](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#set-up-targeting-rules).

## View offers in a reporting group

The **[!UICONTROL Offer Level]** report shows how the offers of an activity perform, grouped by reporting group, so that you can compare the groups as well as the individual offers.

1. Click **[!UICONTROL Activities]**, click the **[!UICONTROL Automated Personalization]** activity in the list, then click the **[!UICONTROL Reports]** tab to display the [Offer Level](/help/main/c-reports/personalization-reports/reports-ap.md) report.

   If you have many activities, click the **[!UICONTROL Show Filters]** (funnel) icon, then select the **[!UICONTROL Automated Personalization]** checkbox to display only **[!UICONTROL Automated Personalization]** activities.

1. Click **[!UICONTROL Control]** or **[!UICONTROL Targeted]** in the table to display the ungrouped offers and the offers inside reporting groups.

   ![Offer groups: Control and Targeted](/help/main/c-reports/assets/offer-groups.png)

For information about using **[!UICONTROL Automated Personalization]** reports (including the **[!UICONTROL Offer Level]** report), see [Automated Personalization Summary reports](/help/main/c-reports/personalization-reports/reports-ap.md).
