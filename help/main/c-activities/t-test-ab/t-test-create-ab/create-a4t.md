---
keywords: Targeting;analytics;tracking server;analytics for target;a4t
description: Learn how to configure an activity in [!DNL Adobe Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).
title: How Can I Use [!DNL Analytics] Data in [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
TQID: 'https://experienceleague.adobe.com/x38YsYI4a6-92oOr6Fs3RfKrJHbSaLNj0cki5CInPPg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: 891742a5-242d-5099-966a-ca76c17cd2d2
    internal-label: Analytics for Target (A4T)
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Using [!DNL Adobe Analytics] data {#create-a4t}

>[!BEGINSHADEBOX]

**On this page:** Learn how to configure an activity to use [!DNL Adobe Analytics] as the reporting source (A4T), what to prepare before you start, and how to choose the goal of the activity.

>[!ENDSHADEBOX]

Analytics for Target (A4T) measures the results of an [!DNL Adobe Target] activity with the data and metrics of [!DNL Adobe Analytics]. To use A4T, configure the activity so that [!DNL Analytics] is its reporting source. For detailed information about setting up [!DNL Analytics] as the data source for [!DNL Target], see [Adobe Analytics as the Reporting Source for Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## Before you begin {#before-you-begin}

>[!NOTE]
>
>The **[!UICONTROL Adobe Analytics]** option is available when your [!DNL Adobe Experience Cloud] account is linked to both [!DNL Analytics] and [!DNL Target], even if the integration between [!DNL Target] and [!DNL Analytics] has not been set up for your account.

Before you create the activity, establish its goal, for example improving revenue per visitor (RPV) or increasing clicks to your shopping cart. Then choose the final success metric that measures this goal. Additional metrics can be selected in [!DNL Analytics] at any time, but you must still specify the one metric that this test is expected to affect.

## Select Analytics as the reporting source {#select-reporting-source}

>[!NOTE]
>
>If you use at.js version 0.9.1 or later, you do not need to specify a tracking server when you create an activity that uses [!DNL Adobe Analytics] as the reporting source. The at.js library automatically sends the tracking server values to [!DNL Target]. The **[!UICONTROL Tracking Server]** field on the **[!UICONTROL Goals & Settings]** page can remain empty.

The reporting source is selected on the **[!UICONTROL Goals & Settings]** page of the activity. On this page, you choose an [!DNL Analytics] company and the report suite that receives the [!DNL Target] activity data, and you verify the tracking server. 

➡️ For the steps, the report suite requirements, and the tracking server details, see [Reporting Source](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source).

When [!DNL Analytics] is the reporting source, the activity does not offer an option to set up audiences for reporting. [!DNL Analytics] segments are available in the [!DNL Target] **[!UICONTROL Activities]** report instead.

## Set the goal of the activity {#set-goal}

Each activity requires a success metric as its goal. The goal is the conversion activity that signals a successful activity. Any metric that is available in the [!DNL Analytics] metric selector can be used. It is best practice never to run a test without a goal to improve in a specific way.

Setting a goal does not prevent you from using other metrics to evaluate the test results. The goal, however, identifies the one thing that you want to improve with the test.

After a visitor completes your goal, that visitor is no longer included in the activity. If the visitor reenters the activity after completing it, that visitor is counted as a new visitor.
