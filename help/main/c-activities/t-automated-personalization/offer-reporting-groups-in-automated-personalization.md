---
keywords: automated personalization;offer;reporting;group;reporting group;ap
description: Learn how to use offer reporting groups in [!DNL Adobe Target] [!UICONTROL Automated Personalization] activities.
title: Can I Use Offer Reporting Groups in [!UICONTROL Automated Personalization] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
---
# Offer reporting groups in [!UICONTROL Automated Personalization]

Information about using reporting groups in [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) activities.

Reporting groups perform two key functions:

* Reporting groups let you see your offers grouped in AP activity reporting. 
* Reporting groups play a key role with how the [!DNL Target] personalization models function.

When you use reporting groups, [!DNL Target] creates one personalization model for each reporting group using the data from all offers in that group. Without reporting groups, [!DNL Target] creates a personalization model for each offer in your AP activity.

If your activity setup doesn't have enough data for a personalization model to be built per offer, reporting groups help reduce the data requirements to use [!UICONTROL Automated Personalization]. Reporting groups can also help solve the "cold start" problem for new offers by grouping similar offers so that each model gets more data to train on. Modeling groups can also be used for activities where new offers are introduced regularly to your AP activity.

This approach works well if visitors respond the same way to all offers in a group. Best practice is to group offers that similar groups of visitors respond to in a similar way. In order words, group offers with similar conversion rates. You should never put all offers into a single reporting group. Grouping all offers or grouping offers with different conversion rates likely reduces the effectiveness of the [!DNL Target] personalization models.

>[!NOTE]
>
>If an offer is removed or replaced from a particular modeling group, the historical traffic that saw that specific offer is also deleted from the modeling group. In other words, deleted offers do not contribute to what data is used for the [!DNL Target] personalization models to learn.

## Set up reporting groups

1. On the **[!UICONTROL Experiences]** page of an AP activity, click the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) )
1. Click the **[!UICONTROL Offers]** tab at the top of the [!UICONTROL Manage Content] dialog box. 
1. (Conditional) Add specific experiences to a reporting group by clicking the [!UICONTROL More Actions] icon ( ![More Actions icon](/help/main/assets/icons/MoreSmall.svg) ) for the desired offer and then by clicking **[!UICONTROL Reporting Group]**.

1. (Conditional) Batch include experiences in a reporting group by selecting the checkboxes for the relevant experiences and then by clicking **[!UICONTROL Reporting Group]** at the bottom of the dialog box.

1. To assign the selected offer to an existing reporting group, select **[!UICONTROL Existing]**, select the desired reporting group from the drop-down list, then click **[!UICONTROL Confirm]**.

   Or

   To create a reporting group to assign the selected offer to, select **[!UICONTROL New]**, name the new reporting group, then click **[!UICONTROL Confirm]**.

You can use the [!UICONTROL Location] list to filter offers by location. Use the [!UICONTROL Report Group] list to filter offers by reporting groups. You can also use the [!UICONTROL Report Group] list to filter for [!UICONTROL Unassigned Offers] so you can assign a reporting group to an offer that is not currently assigned to any reporting group.

For information about targeting an offer to specific audiences, see [Target [!UICONTROL Automated Personalization] offers](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## Caveats

* It is important to understand that reporting groups impact how [!DNL Target] builds its models. As a result, [!DNL Adobe] recommends that you use reporting groups only if you plan to replace or add new offers while an activity is live. If a new offer is introduced into a live activity, putting the new offer into a group with existing similar offers allows the machine to use the data already collected for the other offers in its group to learn about the new offer. You should never put all offers into a single reporting group.

* AP activities have combinations of location+offer (modellables). When [!DNL Target] records data in reports, [!DNL Target] considers such combinations so it is clear from which event (display, click, and so forth) the offer came.

  For example, an activity might have several locations and several offers, which might overlap. If a visitor sees more than one of these offers in different locations, [!DNL Target] records data for those offers only. If the same visitor later clicks an offer, [!DNL Target] records an event from that combination only (not for all combinations).

  Similarly, if the click comes from a different location, which is present in a metric, but doesn't display an offer, this event is logged under the activity, but not for any offer+location combination. As a result, this offer does not appear in the offer reporting group.

  This behavior is because the click might be made from a different mbox and not the mbox that served the offer. Because of this, the metric is associated with the activity, but not with the offer. 

## View offers in a reporting group 

1. Click **[!UICONTROL Activities]**, click the desired [!UICONTROL Automated Personalization] activity from the list, then click the **[!UICONTROL Reports]** tab to display the [Offer Level](/help/main/c-reports/personalization-reports/reports-ap.md) report.

   If you have many activities, click the [!UICONTROL Show Filters] (funnel) icon, then select the [!UICONTROL Automated Personalization] checkbox to filter the list to display only [!UICONTROL Automated Personalization] activities.

1. Click **[!UICONTROL Control]** or **[!UICONTROL Targeted]** in the table to display the ungrouped offers and offers inside reporting groups.

   ![Offer groups: Control and Targeted](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

For information about using [!UICONTROL Automated Personalization] reports (including the [!UICONTROL Offer Level] report), see [Automated Personalization Summary reports](/help/main/c-reports/personalization-reports/reports-ap.md).
