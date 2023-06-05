---
keywords: Targeting;audience;reporting;success metric
description: Learn how to choose a success metric in [!DNL Adobe Target] that qualifies the user for the reporting audience.
title: Can I Apply a Reporting Audience To A Success Metric?
feature: Success Metrics
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
---
# Apply a reporting audience to a success metric

Choose a success metric that qualifies the user for the reporting audience in [!DNL Adobe Target].

For all activities, the [!UICONTROL Applied At] drop-down list lets you apply an audience to a success metric so you can view reporting numbers after the metric has been reached and for subsequent actions.

![success_metric image](assets/success_metric.png)

For example, suppose you have created an activity for all visitors entering from your home page and reaching the conversion page, but you also want to drill down more on visitors who have added more than $50 into the cart before converting.

The [!UICONTROL Applied At] drop-down list potentially provides three categories: 

* Any visitors to the activity
* Only visitors who reach a certain step in the activity
* Only visitors who reach conversion 

Or, to phrase it another way, you can specify that a visitor must have reached an mbox on the entry page of the activity, an mbox that defines some point in the middle of the activity, or the conversion mbox at the end of the activity.

>[!NOTE]
>
>[Success metrics](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) are available only if you have configured them for your activity. If you have not defined success metrics, you see only two options from the drop-down list: [!UICONTROL Campaign Entry] and [!UICONTROL Conversion].


## Considerations

Consider the following information when applying a reporting audience to a success metric:

* Only success metrics starting from the one to which the audience is applied will show reporting data segmented by the audience
* Success metrics preceding the ones to which the audience is applied will not be segmented by the audience, and will show all visitor data
* The metrics are considered based on their order in the activity definition, with the [!UICONTROL Primary Goal] being the last.

## View segmentation in reporting

To view the segmentation in reporting, select the desired audience from the [!UICONTROL Audience] drop-down list in the activity's report.

![reporting_audience_dropdown image](assets/reporting_audience_dropdown.png)

## Example

Consider an activity that has Success Metric1, Success Metric2, Success Metric3, and the Primary Goal. 

Suppose you have reporting Audience1 set on "Entry" and reporting Audience2 set on Success Metric2. The audiences will filter the reporting data as follows:

||Visitors|Success Metric1|Success Metric2|Success Metric3|Primary Goal|
| --- | --- | --- | --- | --- | --- |
|Audience1|Applied|Applied|Applied|Applied|Applied|
|Audience2|Not applied|Not applied|Applied|Applied|Applied|
