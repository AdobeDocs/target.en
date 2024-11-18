---
keywords: A/B;activity metrics;metrics;set metrics;goal metric;activity settings;success metric;conversion;revenue;engagement
description: Discover how to set metrics in an A/B activity to determine visit success, including [!UICONTROL Conversion], [!UICONTROL Revenue], and [!UICONTROL Engagement].
title: How Do I Set Goal Metrics in an A/B Activity?
feature: A/B Tests
hide: yes
hidefromtoc: yes
exl-id: b7955ed7-61b4-429f-80ff-8efcafc10542
---
# Set metrics

Use metrics in an [!DNL Adobe Target] A/B activity to determine when a visit is successful.

For detailed information about success metrics, see [Success Metrics](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924). 

1. In the **[!UICONTROL Reporting Settings]** section of the **[!UICONTROL Goals & Settings]** page, select a [success metric](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

   The [!UICONTROL Select Metrics] option lists the success metrics that you can choose for your activity. The success metrics are divided into the following categories:
   
   * [!UICONTROL Conversion] 
   * [!UICONTROL Revenue] 
   * [!UICONTROL Engagement]

   You can use any of the pre-built success metrics, or create a custom success metric. You can also mark a success metric as a primary metric. Reports and Experience Cloud cards default to show the primary metric, if one is set.

1. Specify the settings for your metrics.

   The available settings depend on the success metric you are using.

   If enabled, the [!UICONTROL Estimated Value of the Conversion] field (not available for the [!UICONTROL Page Score] metrics) provides a value for your goal. This value enables [!DNL Target] to calculate an estimated lift in revenue. This field is optional; however, incremental revenue for any non-revenue metric cannot be calculated without it. The data type is currency. This field is progressively shown after the user indicates the action taken to satisfy the goal. See [Estimating Lift in Revenue](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) for more information.

   The correct configuration of success metrics is critical for making sure you get the data that you expect.

   For more information, see [Success Metrics](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. (Optional) Add additional metrics.

When you name or rename a metric, the following characters are not allowed: 

| Character | Description |
|--- |--- |
|/|Forward slash|
|?|Question mark|
|#|Number sign|
|:|Colon|
|=|Equals to|
|+|Plus|
|-|Minus|
|@|At sign|
