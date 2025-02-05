---
keywords: activity settings;A/B goals and settings;reporting settings;goal metrics;success metrics;dependent success metrics;advanced settings;primary goal;additional metrics;objective;priority;duration;reporting solution;goal;audiences for reporting;Which success metric must be reached before incrementing this metric;What will happen after a user encounters this goal metric;notes
description: Discover how to use the [!UICONTROL Goals and Settings] page to define A/B activity goals.
title: How Do I Specify Goals and Settings in a [!DNL Target] A/B Activity?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
---
# Goals and settings

The [!UICONTROL Goals & Settings] page in [!DNL Adobe Target] is where you specify information about the goals of the activity.

The available settings depend on whether you use Target or [Analytics as the reporting source](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

The [!UICONTROL Activity Settings] section of the [!UICONTROL Goals & Settings] page lets you configure the following options:

| Settings | Description |
|--- |--- |
|[!UICONTROL Objective]|Type an optional objective. The objective can be any information that helps you and your team members identify the activity.|
|[!UICONTROL Priority]|Depending on your settings, the [!DNL Target] UI and options for [!UICONTROL Priority] vary. You can use the legacy settings of [!UICONTROL Low], [!UICONTROL Medium], or [!UICONTROL High], or you can enable fine-grained priorities from 0 to 999.<P>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.<P>If this option is not enabled in [!UICONTROL Administration] (the default), specify a priority: [!UICONTROL Low], [!UICONTROL Medium], or [!UICONTROL High].<P>To enable [fine-grained priorities](/help/main/administrating-target/reporting.md), click [!UICONTROL Administration] > [!UICONTROL Reporting], then toggle the [!UICONTROL Enable Fine-Grained Priorities] option to the "On" position. <P>If this option is enabled, specify a value from 0 through 999: 0 = [!UICONTROL Low] and 999 = [!UICONTROL High]. <P>For activities created in previous versions of [!DNL Target], [!UICONTROL Low] priority is converted to 0, [!UICONTROL Medium] is converted to 5, and [!UICONTROL High] is converted to 10. You can adjust these values as necessary.<P>Note: Before you can disable this option after using fine-grained priories, all priorities must be set back to 0, 5, and 10.|
|[!UICONTROL Duration]|The activity can start when approved, or you can set a specific date and time. Likewise, the activity can either end when it is deactivated or you can set a date and time. The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is set to the time zone configured in your browser. To use a different time zone, set your browser to another time zone and restart the browser.|

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

The [!UICONTROL Reporting Settings] section of the [!UICONTROL Goals & Settings] page lets you configure the following options:

| Settings | Description |
|--- |--- |
|[!UICONTROL Reporting Source]|Specify which solution data is collected from:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>If a reporting source is specified in your [account settings](/help/main/administrating-target/reporting.md), the specified source is used and this setting is not visible.<P>You cannot change your reporting source after the activity goes live to keep reports consistent.<P>**Adobe Analytics**: See [Adobe Analytics as the Reporting Source for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) to learn about the differences between the reporting solutions and the advantages of each. When selecting [!DNL Analytics] as the reporting source for [!DNL Target], you select an [!DNL Analytics] report suite to receive [!DNL Target] activity data.<P>To specify a reporting source, first choose from any of the [!DNL Analytics] companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to [!DNL Adobe Target] are available for selection. If you don't see the report suites that you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again. If the report suite is still missing from the list, contact Customer Care.<P><P>**Adobe Customer Journey Analytics**: See [[!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) for more information about the integration between [!DNL Adobe Customer Journey Analytics] and [!DNL Target].<P>[!DNL Target] reporting in [!DNL Customer Journey Analytics] is supported in A/B activities with manual traffic split. [!UICONTROL Auto-Target] and [!UICONTROL Auto-Allocate] A/B activities cannot use [!DNL Target] reporting in [!DNL Customer Journey Analytics].|
|[!UICONTROL Goal Metric]|Select the action taken by a visitor to achieve the goal. For example, choose a [!UICONTROL Conversion] metric, then set the parameters that determine when success is achieved. For more information about setting metrics, see [Set Metrics](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Note: If the reporting solution is set to [!DNL Analytics], the only available goal metric is [!UICONTROL Conversion]. [!DNL Analytics] metrics cannot be selected as a goal. When you select your success metric, a selector displays. Use this selector to choose the specifics for the success metric.<P>If enabled, the [!UICONTROL Estimated Value of the Conversion] field (not available for the [!UICONTROL Page Score] metrics) provides a value for your goal, but not for other metrics. This value enables [!DNL Target] to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. For all revenue metrics ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], and [!UICONTROL Orders]), the estimate uses [!UICONTROL Revenue per Visitor]. The data type is currency.<P>After reaching the activity goal, a visitor continues to see the activity content, unless that visitor qualifies for a higher-priority activity. If the visitor reaches the goal again, it is counted as another conversion. This is different from the default behavior in [!DNL Target Classic], which counted visitors as new if they see the activity again.|
|[!UICONTROL Additional Metrics]|Create additional success metrics. This setting is not available if the reporting solution is set to [!DNL Analytics]. In this case, the metrics defined for the [!DNL Analytics] report suite are applied.|
|[!UICONTROL Audiences for Reporting]|By default, reports show results for all qualified visitors. You can add report audiences to show information about only specific audiences. This setting is not available if you choose [!DNL Analytics] as your reporting solution. The audience defined for the [!DNL Analytics] report suite is applied.|

## Advanced Settings {#section_E2FE441AFB324E498793ABB025ED9974}

The [!UICONTROL Advanced Settings] section of the [!UICONTROL Goals & Settings] page lets you configure the advanced options.

To specify advanced settings, click the **[!UICONTROL More]** icon ( ![More icon](/help/main/assets/icons/MoreSmallList.svg) ) in the [!UICONTROL My Primary Goal] section, then click **[!UICONTROL Advanced Settings]**.

>[!NOTE]
>
>If you use [!DNL Adobe Analytics] as your reporting source, settings are managed by the [!DNL Analytics] server. The advanced settings option is not available.

The following options are available:

| Setting | Description |
|--- |--- |
|[!UICONTROL Which success metric must be reached before incrementing this metric?]|Use this option to only count someone as reaching the success metric if they've previously reached a different success metric. For example, an activity conversion might only be valid if the visitor clicks the offer, or reaches a particular page before converting. You can provide dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase. Define both (or multiple) success metrics before you can make one dependent on another. The [!UICONTROL Add Dependency] option allows the success metric to increment if another success metric has been reached or has not been reached. To add a dependency:<ul><li>After adding additional metrics, click [!UICONTROL Advanced Settings].</li><li>Click the [!UICONTROL Add Dependency] option:</li><li>Drag and drop the desired metrics from the left pane into the right pane, then click [!UICONTROL Reached] to toggle the setting between [!UICONTROL Reached] and[!UICONTROL  Not Reached].</li><li>You can edit or remove dependencies after adding them.</li></ul>|
|[!UICONTROL What will happen after a user encounters this goal metric?]|There are three options for what happens after a visitor reaches the goal metric:<ul><li>Select **[!UICONTROL Increment Count & Keep User in Activity]** to specify how the count is incremented.</li><li>Select **[!UICONTROL Increment Count, Release User & Allow Reentry]** to specify the experience the user sees if they reenter the activity.</li><li>Select **[!UICONTROL Increment Count, Release User & Bar from Reentry]** to specify what the user sees instead of the activity content.</li></ul>|
|[!UICONTROL How will the count be incremented?]|There are three options for how the count is incremented:<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul>|

See [Success Metrics](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) for more information about advanced settings.

## Other Metadata {#section_2E8917BEFB954480A4206B9E9E917F80}

The [!UICONTROL Other Metadata] section of the [!UICONTROL Goals & Settings] page lets you specify any information about your activity that is useful to keep on hand for yourself or other team members. The Notes pane is resizable.|
