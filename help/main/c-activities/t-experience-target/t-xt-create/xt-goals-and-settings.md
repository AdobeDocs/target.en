---
keywords: activity settings;experience targeting goals and settings;xt goals and settings;experience targeting;reporting settings;goal metrics;success metrics;dependent success metrics;advanced settings;primary goal;additional metrics;objective;priority;duration;reporting solution;goal;audiences for reporting;Which success metric must be reached before incrementing this metric;What will happen after a user encounters this goal metric;notes
description: Learn how to use the [!UICONTROL Goals & Settings] page in [!DNL Adobe Target] to specify information about the goals of an [!UICONTROL Experience Targeting] (XT) activity.
title: How Do I Specify [!UICONTROL Goals & Settings] in an [!UICONTROL Experience Targeting] Activity?
feature: Experience Targeting
exl-id: 80cb7eff-4e9c-43d7-a3d8-7a9de79c91b9
---
# Goals and Settings in [!UICONTROL Experience Targeting] (XT) activities

The [!UICONTROL Goals & Settings] page is where you enter information about the goals of the test:

* [!UICONTROL Activity Settings] 
* [!UICONTROL Reporting Settings] 
* [!UICONTROL Other Metadata]

The available settings depend on whether you use [!DNL Target] or [!DNL Analytics] as the reporting source.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

The following settings are available:

### [!UICONTROL Objective]

Type an optional objective. The objective can be any information that helps you and your team members identify the campaign.

### [!UICONTROL Priority]

Depending on your settings, the [!DNL Target] UI and options for [!UICONTROL Priority] vary. You can use the legacy settings of [!UICONTROL Low], [!UICONTROL Medium], or [!UICONTROL High], or you can enable fine-grained priorities from 0 to 999.

The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority is displays.

If this option is not enabled in [!UICONTROL Administration] (the default), specify a priority: [!UICONTROL Low], [!UICONTROL Medium], or [!UICONTROL High].

To enable fine-grained priorities, click **[!UICONTROL Administration]** > **[!UICONTROL Reporting]**, then toggle the [!UICONTROL Enable Fine-Grained Priorities] option to the "On" position.

If this option is enabled, specify a value from 0 through 999:

* 0 = Low
* 999 = High

For activities created in previous versions of [!DNL Target], [!UICONTROL Low] priority is converted to 0, [!UICONTROL Medium] is converted to 5, and [!UICONTROL High] is converted to 10. You can adjust these values as necessary.

>[!NOTE]
>
>Before you can disable this option after using fine-grained priories, all priorities must be set back to 0, 5, and 10.

### [!UICONTROL Duration]

The activity can start when approved, or you can set a specific date and time. Likewise, the activity can end when it is deactivated or you can set a date and time for the activity to end. The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is set to the time zone configured in your browser. To use a different time zone, set your browser to another time zone and restart the browser.

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

The following settings are available:

### [!UICONTROL Reporting Source]

Specify whether data is collected from [!DNL Target] or from [!DNL Adobe Analytics]. See [Adobe Analytics as the Reporting Source for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) to learn about the differences between the reporting solutions and the advantages of each.

When selecting [!DNL Analytics] as the reporting source for [!DNL Target] (A4T), you select an [!DNL Analytics] report suite to receive [!DNL Target] activity data. To do this, first choose from any of the [!DNL Analytics] companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to [!DNL Target] are available for selection. If you don't see the report suite that you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again. If the report suite is still missing from the list, contact [Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!DNL Analytics for Target] (A4T) requires a tracking server to report results correctly. A default tracking server displays in the [!UICONTROL Tracking Server] field. If you use more than one tracking server, ensure you include the correct tracking server in this field. See [Using an Analytics Tracking Server](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) for more information.

If a reporting solution is specified in your account settings, the specified solution is used and this setting is not visible.

>[!NOTE]
>
>You cannot change your reporting source after the activity goes live to keep reports consistent.

### [!UICONTROL Goal Metric]

Select the action taken by a visitor to achieve the goal. For example, choose a [!UICONTROL Conversion] metric, then set the parameters that determine when success is achieved.

For more information about setting metrics, see [Set Metrics](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB).

>[!NOTE]
>
>If the reporting solution is set to [!DNL Analytics], the only available goal metric is [!UICONTROL Conversion]. [!DNL Analytics] metrics cannot be selected as a goal.

When you select your success metric, a selector displays. Use this selector to choose the specifics for the success metric.

If enabled, the [!UICONTROL Estimated Value of the Conversion] field (not available for [!UICONTROL Page Score] metrics) provides a value for your goal, but not for other metrics. This value enables [!DNL Target] to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. For all revenue metrics ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], and [!UICONTROL Orders]), the estimate uses [!UICONTROL Revenue per Visitor]. The data type is currency.

After reaching the activity goal, a visitor continues to see the activity content, unless that visitor qualifies for a higher-priority activity. If the visitor reaches the goal again, it is counted as another conversion. This behavior is different from the default behavior in [!DNL Target Classic], which counted visitors as new if they see the test again.

### [!UICONTROL Additional Metrics]

Create additional success metrics.

This setting is not available if the reporting solution is set to [!DNL Analytics]. In this case, the metrics defined for the [!DNL Analytics] report suite are applied.

### [!UICONTROL Audiences for Reporting]

By default, reports show results for all qualified visitors. You can add report audiences to show only information about specific audiences.

This setting is not available if you choose [!DNL Analytics] as your reporting solution. The audience defined for the [!DNL Analytics] report suite is applied.

## [!UICONTROL Other Meta Data]

Type any information about your activity that is useful for yourself or other team members. The [!UICONTROL Notes] pane is resizable.

## [!UICONTROL Advanced Settings] {#section_E2FE441AFB324E498793ABB025ED9974}

Advanced settings are available for [!UICONTROL Experience Targeting] goal metrics.

![Advanced Settings](/help/main/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>If you use [!DNL Analytics] as your reporting source, settings are managed by the [!DNL Analytics] server. The [!UICONTROL Advanced Settings] option is not available.

The following settings are available:

### [!UICONTROL Which success metric must be reached before incrementing this metric?]

Use this option to only count visitor as reaching the success metric if they've previously reached a different success metric. For example, a test conversion might only be valid if the visitor clicks the offer or reaches a particular page before converting.

You can provide dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase.

You must define both (or multiple) success metrics before you can make one dependent on another.

The [!UICONTROL Add Dependency] option allows the success metric to increment if another success metric has been reached or has not been reached.

To add a dependency:

1.  After adding additional metrics, click **[!UICONTROL Advanced Settings]**.
2.  Click **[!UICONTROL Add Dependency]**:

    ![Add dependency link](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3.  Drag and drop the desired metrics from the left pane into the right pane, then click **[!UICONTROL Reached]** to toggle the setting between [!UICONTROL Reached] and [!UICONTROL Not Reached].

    ![Add Metrics Dependency dialog box](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

You can edit or remove dependencies after adding them.

### [!UICONTROL What will happen after a user encounters this goal metric?]

There are three options for what happens after a visitor reaches the goal metric:

* Select [!UICONTROL Increment Count & Keep User in Activity] to specify how the count is incremented.
* Select [!UICONTROL Increment Count, Release User & Allow Reentry] to specify the experience the user sees if they reenter the activity.
* Select [!UICONTROL Increment Count, Release User & Bar from Reentry] to specify what the user sees instead of the activity content.

See [Success Metrics](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) for more information about advanced settings.

## Training video: Activity Settings (3:02)

This video includes information about activity settings.

* Enter an objective for your activity 
* Set the priority level of your activities 
* Schedule activity start and end times 
* Add audiences for reporting to create report filters 
* Enter notes for your activities

>[!VIDEO](https://video.tv.adobe.com/v/17381)
