---
keywords: multivariate;mvt;metrics;set metrics;goal metric;activity settings;success metric;conversion;revenue;engagement
description: Learn how to specify metrics in an [!DNL Adobe Target] [!UICONTROL Multivariate Test] activity to determine when a visit is successful, such as [!UICONTROL Conversion], [!UICONTROL Revenue], and [!UICONTROL Engagement].
title: How Do I Set Goal Metrics in a [!UICONTROL Multivariate Test] (MVT) Activity?
feature: Multivariate Tests
exl-id: 8530b3f1-5daa-4a03-a482-93b10eb23208
---
# Set metrics for a [!UICONTROL Multivariate Test] activity

Use metrics in an [!DNL Adobe Target] [!UICONTROL Multivariate Test] to determine when a visit is successful.

For detailed information about success metrics, see [Success Metrics](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924). 

1. Specify the goal of the activity.
1. Select a [success metric](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Set Metrics list](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_metrics-list.png)

   The [!UICONTROL Select Metrics] page lists the success metrics that you can choose for your activity. The success metrics are divided into the following categories:

   * [!UICONTROL Conversion] 
   * [!UICONTROL Revenue] 
   * [!UICONTROL Engagement]

   You can use any of the pre-built success metrics, or create a custom success metric. You can also mark a success metric as a primary metric. Reports and Experience Cloud cards default to show the primary metric, if one is set.

1. Specify the settings for your metrics.

   The available settings depend on the success metric that you are using.

   If enabled, the [!UICONTROL Estimated Value of the Conversion] field (not available for the [!UICONTROL Page Score] metrics) provides a value for your goal. This value enables [!DNL Target] to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. The data type is currency. This field is progressively shown after the user indicates the action taken to satisfy the goal. See [Estimating Lift in Revenue](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) for more information.

   The correct configuration of success metrics is critical for making sure you get the data you expect.

   For more information, see [Success Metrics](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

1. (Optional) Add additional metrics.
1. Click **[!UICONTROL Continue]** when you are finished setting your metrics.

When you name or rename a metric, the following characters are not allowed:

   | Character | Description |
   |--- |--- |
   |`/`|Forward slash|
   |`?`|Question mark|
   |`#`|Number sign|
   |`:`|Colon|
   |`=`|Equals to|
   |`+`|Plus|
   |`-`|Minus|
   |`@`|At sign|

## Training video: Activity Metrics (7:43) ![Tutorial badge](/help/main/assets/tutorial.png)

This video includes information about working with success metrics.

* Understand "goal" metrics 
* Understand and build [!UICONTROL Conversion], [!UICONTROL Revenue], and [!UICONTROL Engagement] metrics 
* Build a click-tracking metric

>[!VIDEO](https://video.tv.adobe.com/v/17380)
