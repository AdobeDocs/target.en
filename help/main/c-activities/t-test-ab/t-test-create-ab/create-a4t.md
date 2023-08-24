---
keywords: Targeting;analytics;tracking server;analytics for target;a4t
description: Learn how to configure an activity in [!DNL Adobe Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).
title: How Can I Use [!DNL Analytics] Data in [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
---
# Using [!DNL Adobe Analytics] data

You can configure an activity in [!DNL Adobe Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).

For detailed information about setting up [!DNL Analytics] as the data source for [!DNL Target], see [Adobe Analytics as the Reporting Source for Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Before you set up an activity that uses [!DNL Analytics] as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks your shopping cart. Choose a final success metric for the activity. Although you can select additional metrics at any time in [!DNL Analytics], you must still specify a particular metric you expect this test to affect.

>[!NOTE]
>
>The [!DNL Adobe Analytics] option is available if you've linked your [!DNL Adobe Experience Cloud] account with both [!DNL Analytics] and [!DNL Target], even if integration between [!DNL Target] and [!DNL Analytics] has not been set up for your account.

When selecting [!DNL Analytics] as the reporting source for [!DNL Target], you select an [!DNL Analytics] report suite to receive [!DNL Target] activity data. To do specify a reporting source, first choose from any of the [!DNL Analytics] companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to [!DNL Adobe Target] are available for selection. If you don't see the report suite that you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again. If the report suite is still missing from the list, contact Customer Care.

[!UICONTROL Analytics for Target] (A4T) requires a tracking server to report results correctly. A default tracking server displays in the [!UICONTROL Tracking Server] field. If you use more than one tracking server, ensure that you include the correct tracking server in this field. See [Using an Analytics Tracking Server](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) for more information.

>[!NOTE]
>
>If you use [!DNL Adobe Analytics] as your activity's reporting source, you do not need to specify a tracking server during activity creation if you are using at.js version 0.9.1 (or later). The at.js library automatically sends tracking server values to [!DNL Target]. During activity creation, you can leave the [!UICONTROL Tracking Server] field empty on the [!UICONTROL Goals & Settings] page.

When setting up activity after setting up [!DNL Analytics] as your reporting source, there is no option to set up audiences for reporting. [!DNL Analytics] segments are available in the [!DNL Target] [!UICONTROL Activities] report.

You must select a success metric to use as a goal for each activity. Your activity goal is the conversion activity that signals a successful activity. It is best practice never to run a test without having a goal to improve in some specific way. You can choose any [!DNL Analytics] metric available in the [!DNL Analytics] metric selector.

Setting a goal doesn't mean you can't use another metric when evaluating test results. The goal is, however, a reminder of the one thing you want to improve with the test.

After a visitor completes your goal, that visitor is no longer included in the activity. If the visitor reenters your activity after completing an activity, that visitor is counted as a new visitor.
