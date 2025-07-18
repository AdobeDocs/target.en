---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics;advanced settings;dependency;dependant;Increment Count & Keep User in Activity;Increment Count, Release user, & Allow Reentry;increment Count, Release User, & Bar from Reentry
description: Learn about success metrics that help you determine the success of an activity. Success metrics include Conversion, Revenue, Page Views, Custom Scoring, and Time on Site.
title: What Are Success Metrics?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
---
# [!UICONTROL Success metrics]

Success metrics in [!DNL Adobe Target] are key indicators that help measure the performance of your activities. These metrics capture important business outcomes such as conversions, revenue per visitor, and customer engagement, allowing you to evaluate the impact of specific experiences or offers.

For example, you can track whether a new promotion increases revenue per visitor or leads to more items added to shopping carts. Success metrics also help identify issues in user flows like registration, checkout, or purchase processes, while providing insights into overall visitor behavior.

## Overview

In [!DNL Target], success metrics are pre-configured with recommended settings to ensure accurate reporting and effective tracking.

By default, conversion events use the setting **[!UICONTROL Increment count & keep user in activity].** This setting means that each visitor is counted as a conversion only once. No repeat conversions are counted. These visitors continue to see the activity content throughout their session.

For revenue metrics using the same setting, only the first order from a visitor logs order details. While subsequent orders increase the conversion count, they do not contribute to revenue-based metrics such as [!UICONTROL Revenue per Visitor (RPV)], [!UICONTROL Average Order Value (AOV)], or [!DNL Total Sales]. These additional orders are also excluded from the [!UICONTROL Order Details] report.

>[!NOTE]
>
>For activities using [Analytics as the reporting source](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), the goal metric always uses the "[!UICONTROL Increment Count & Keep User in Activity]" and "[!UICONTROL On Every Impression]" settings. These settings are *not* configurable.

The following success metrics can be configured in the [!UICONTROL Reporting Settings] section on the [!UICONTROL Activity Settings page], under the [!UICONTROL Goals & Settings] step:

| Success Metric | Measurement Approach | Definition |
|--- |--- |--- |
|[!UICONTROL Conversion]|Conversion-based|Conversion is when a visitor performs an action on your site that you defined, such as <ul><li>Viewed a page</li><li>Viewed an mbox</li><li>Clicked an element</li></ul>A conversion can be counted once per visitor or each time any visitor completes a conversion.|
|[!UICONTROL Revenue]|Conversion-based|Revenue generated by the visit. You can choose only one revenue metric:<ul><li>Viewed an mbox</li></ul>For more information about changes in the updated [!DNL Target] UI as it pertains to revenue success metrics, see [Updated [!DNL Target] UI changes](#changes) below.|
|[!UICONTROL Engagement]|Engagement-based|Engagement generated by the visit. You can choose from the following engagement metrics:<UL><li>Page Views: Each unique visit is counted as a conversion.</li><li>[!UICONTROL Custom Scoring]: Aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the activity's first display [!DNL Target] request.</li>[!DNL Time on Site]: Time spent in the visit (in seconds) from the point the visitor sees the activity's first display [!DNL Target] request to the load of the final page with a request in the session.</UL>|

For engagement-based metrics (unlike for conversion-based and revenue-based metrics), visitors must re-qualify for the activity on each visit to increment the count for that session. The associated metric begins incrementing after re-qualification and stops at the end of each visitor's session. A session ends after 30 minutes of inactivity. Therefore, you don't see results immediately during testing; however, all results from that session are available within a few minutes of the session ending.

## Custom success metrics

You can also create custom success metrics.

After selecting the success metric, select the action taken by a visitor to achieve the goal. For example, choose a [!UICONTROL Conversion] metric, set it to be counted once per visitor, then set whether success is achieved when a visitor views a certain page (or set of pages), views a specific [!DNL Target] request, or clicks a specific link.

If enabled, the [!UICONTROL Estimated Value of one conversion] field (not available for the [!UICONTROL Page Score] metrics) provides a value for your goal, but not for other metrics. This value enables [!DNL Target] to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. For all revenue metrics ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], and [!UICONTROL Orders]), the estimate uses [!UICONTROL Revenue per Visitor]. The data type is currency. See [Estimating Lift in Revenue](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) for more information.

The success metrics that you choose for your activity are available in the report settings when you view a report for the activity.

Some metrics, such as [!UICONTROL Custom Scoring] and [!UICONTROL Revenue Per Visitor], require a customized implementation that passes in information, such as order totals and order IDs.

## Advanced Settings {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Use the advanced settings to manage how you measure success. Options include adding dependencies, choosing whether to keep the user in the activity or remove them, and whether to count the metric once per entrant or on every impression.

To access the [!UICONTROL Advanced Settings] options, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallListVert.svg) ), then click **[!UICONTROL Advanced Settings]**.

![Advanced Settings menu](/help/main/c-activities/r-success-metrics/assets/advanced-settings-refresh.png)

For more information about the [!UICONTROL Advanced Settings] options ("[!UICONTROL What will happen after a user encounters this goal]" and "[!UICONTROL How will the count be incremented]") see [What happens after a user encounters this goal metric](#what-happens)? 

>[!NOTE]
>
>If you use [!DNL Adobe Analytics] as your reporting source, settings are managed by the [!DNL Analytics] server. The [!UICONTROL Advanced Settings] option is not available. For more information, see [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Add dependency

You can use the advanced settings to create dependent success metrics, incrementing one metric only if a visitor reaches another metric first.

For example, a test conversion might only be valid if a visitor clicks the offer, or reaches a particular page before converting.

Dependency functionality is *not* supported for the following:

* [!UICONTROL Recommendations] activities. This functionality is supported for all other activity types.
* If you use [Analytics as your reporting source](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* The "Viewed a Page" metric type.
* The "Clicked an Element" metric type for Visual Experience Composer (VEC) activities.

Dependent success metrics do not convert in the following cases:

* If you create a circular dependency in which metric1 is dependent on metric2 and metric2 is dependent on metric1, neither metric can convert. 
* [!UICONTROL Automated Personalization] activities release users and restart the activity when conversion metrics are reached, so any metric dependent on the conversion metric does not convert.

### What will happen after a user encounters this goal metric? {#what-happens}

Use the advanced settings to determine what happens after a user reaches the goal metric. The following table shows the available options:

| After a User Encounters This Goal Metric | Options |
|--- |--- |
|[!UICONTROL Increment Count & Keep User in Activity]|Specify how the count is incremented:<ul><li>Once per entrant (default)</li><li>On every impression, excluding page refreshes</li><li>On every impression</li></ul>|
|[!UICONTROL Increment Count, Release user, & Allow Reentry]|Select the experience that the visitor sees if they reenter the activity:<ul><li>Same experience (default)</li><li>Random experience</li><li>Unseen experience</li></ul>|
|[!UICONTROL Increment Count, Release User, & Bar from Reentry]|Determine what the user sees instead of the activity content:<ul><li>Same experience, without tracking (default)</li><li>Default content, or other activity content</li></ul>|

>[!NOTE]
>
>If you configure a metric to one of the [!UICONTROL Increment Count] options (mentioned above), the metric count correctly increments once per entrant at the visitor level only. The metric count increments once per visit for every new session at the visit level.

### How is the count incremented:

Choose the desired behavior:

* Once per entrant
* On every impression (Excluding page refreshes)
* On every impression

## Known issues

* Success metrics with the advanced option "How will the count be incremented" set to "every impression" or "every impression (excluding refreshes)" cannot be used as a success metric that another metric depends on.

  When a success metric is set to increment on every impression, [!DNL Target] counts the visitor again every time the visitor visits this success metric. [!DNL Target] then resets the success metric "membership" to 0 so it can count again on the next impression. Thus, if another metric requires this metric to have been seen first, [!DNL Target] never recognizes that the user has seen the first metric.

## Updated [!DNL Target] UI changes {#changes}

The [[!DNL Target Standard/Premium] 25.2.1 release](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2), launched on February 17, 2015, introduced updated [!DNL Target] and [!UICONTROL Visual Experience Composer] (VEC) UIs. This section outlines the key differences between the legacy and updated UI, specifically as they relate to configuring and managing success metrics.

### UI changes related to [!UICONTROL Revenue] success metrics

In the updated [!DNL Target] interface, the [!UICONTROL Default View for Reporting] drop-down has been removed. This field was redundant, as it previously saved the default reporting view under [!DNL Overview] > [!UICONTROL Reports] in the legacy UI.

With the updated UI, the default reporting metric is now always set to [!UICONTROL Revenue per Visitor (RPV)]. You can still customize the view in the [!UICONTROL Reports] section to display metrics that are most relevant to your analysis.

This change does not affect delivery metrics. This change impacts only the default filter shown in the reporting view. Because RPV is the most commonly used metric among customers, this default was selected to streamline reporting workflows. You can switch to other metrics at any time within the [!UICONTROL Reports] section.