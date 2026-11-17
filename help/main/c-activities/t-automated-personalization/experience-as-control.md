---
keywords: experience;control;automated personalization;auto-target
description: Learn how to select an experience to be used as a control while creating an [!UICONTROL Automated Personalization] (AP) or [!UICONTROL Auto-Target] activity in [!DNL Adobe Target].
title: How Can I Use a Specific Experience as Control in an [!UICONTROL Automated Personalization] Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
TQID: 'https://experienceleague.adobe.com/a-lIVDWxeAi-VCp7-lLD-zaClCDCKJGfa25XMKF0vZA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Select the control experience {#experience-as-control}

>[!BEGINSHADEBOX]

**On this page:** Learn how to choose the control of an **[!UICONTROL Automated Personalization]** or **[!UICONTROL Auto-Target]** activity, and what to consider when you use a specific experience as the control.

>[!ENDSHADEBOX]

You can select a randomly served experience or a specific experience to use as the control while creating an [**[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/automated-personalization.md#automated-personalization-overview) (AP) or [**[!UICONTROL Auto-Target]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activity. The control traffic is routed to the relevant experiences based on the traffic allocation percentage configured in the activity, so that you can evaluate the performance reports of the personalized traffic against the control traffic.

In a manual **[!UICONTROL A/B Test]**, you can change what reporting shows as the control, and lift is calculated from that experience, because traffic is served randomly to all experiences whatever the control is. In **[!UICONTROL Automated Personalization]** and **[!UICONTROL Auto-Target]** activities, the control does impact how visitor traffic is served, so choose it carefully.

Two options are available for the control:

* **Randomly served:** The control percentage of traffic randomly serves all experiences in the activity, without considering the profile of the visitor. It works like an **[!UICONTROL A/B Test]** within your activity, and it shows the non-personalized conversion rate of each experience or offer, which helps you analyze the results.

* **Specific experience:** The control percentage of traffic randomly serves only that one experience. This option lets you compare the traffic served by the [!DNL Target] personalization models to a specific experience that you define, for example, your default homepage.

## Considerations {#considerations}

Keep the following points in mind when using a specific experience as the control:

* Changing the control experience in an already live activity is not advised. The latest control experience selected is named in reporting, even if older reports are based on another experience.

* Deleting the control experience is not advised.

* Adding many new offers or experiences to a live activity with a specific experience as the control is not advised.

* In **[!UICONTROL Automated Personalization]** activities, including targeting on the control experience that could further constrain who can see that experience is not advised.

* In **[!UICONTROL Automated Personalization]** activities, lift and confidence information is *not* available in the offer-level report if a specific experience is selected. This is because comparing the conversion rate of a specific experience to the conversion rate of an offer is not logical due to the difference in units. Lift and confidence information is available at the overall "targeted" versus "control" traffic level for the activity, and at all levels if "random" is selected as the control. The information available in an **[!UICONTROL Auto-Target]** activity is the same, no matter what type of control is selected.

* When you select a specific experience as the control, all control traffic goes to a single experience or set of offers. With a random control, the control traffic is split over the number of experiences or offers in your activity. As a result, you generally do not need as much traffic to flow to the control with a specific experience. 10% is a good place to start.

* If you do one of the following to a live activity with a specific experience as the control, the control is automatically reset to randomly served experiences (instead of the previously selected specific experience):

  * Delete an experience.
  * Remove a location or offer (**[!UICONTROL Automated Personalization]** only).
  * Exclude an experience manually, by removing duplicate offers, or through an exclusion group (**[!UICONTROL Automated Personalization]** only).


## Specify a specific experience as control {#specify-control}

Specifying a specific experience as the control gives the personalized traffic a known experience to be compared against, such as your current default experience, in the reports of the activity.

1. While creating or editing an [**[!UICONTROL Automated Personalization]** activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) or an [**[!UICONTROL Auto-Target]** activity](/help/main/c-activities/auto-target/create-auto-target.md#create-auto-target-activity), configure the experiences as desired.

1. On the **[!UICONTROL Targeting]** page (step 2 of the three-part guided workflow), click the control experience to display the **[!UICONTROL Control]** options in the right pane.

   ![Control pane](/help/main/c-activities/t-automated-personalization/assets/control.png)

1. From the **[!UICONTROL Control]** drop-down list, select **[!UICONTROL Random Experience]** or select the experience that you want to use as the control.

1. Click the **[!UICONTROL Traffic Allocation]** control, then specify the traffic allocation for the control experience and the other experiences.

   ![Traffic allocation rail](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation.png)

   For a specific experience control, 10% to 30% is advised.

1. Continue with the **[!UICONTROL Goals & Settings]** page.

Once the activity is live, its reports compare the personalized traffic with the control experience that you selected. Review the [considerations](#considerations) before you change a live activity, as some changes automatically reset the control to randomly served experiences.
