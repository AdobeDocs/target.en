---
keywords: Targeting;AP reports;automated personalization reports;auto-target;auto target;auto target report;auto-target report;personalization;insights;faq;frequently asked questions;important attributes
description: Learn how to use the [!UICONTROL Important Attributes] report that shows the top attributes that influenced the personalization model and their relative importance.
title: What Is the Important Attributes Report?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: c1069ca7-e221-4865-a82e-6cff5b4c0055
---
# Important Attributes report

Information about the [!UICONTROL Important Attributes] report, one of the two specialized reports available to users of [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] (AT) activities.

>[!NOTE]
>
>Consider the following when using [!UICONTROL Personalization Insights] reports:
>
>* AP and AT activities are available as part of the [!DNL Target Premium] solution. They are not included with [!DNL Target Standard] without a [!DNL Target Premium] license.
>
>* [!UICONTROL Personalization Insights] reports are available only for AP and AT activities that use a conversion optimization goal. Activities where the optimization goal was changed to conversion from revenue after the activity was already live are also not supported.
>
>* [!UICONTROL Personalization Insights] reports are available only if the [!UICONTROL Primary Goal] is selected from the the [!UICONTROL Report Metric] drop-down list.
>
>* [!UICONTROL Personalization Insights] reports are supported in the [default environment](/help/main/administrating-target/hosts.md) only.
>
>* [!UICONTROL Personalization Insights] reports are generated only for activities that are in the [!UICONTROL Live] status and have been activated and receiving traffic for at least 15 days.

In different activities, different attributes are more, or less, important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance.

## Access the [!UICONTROL Important Attributes] report {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Click **[!UICONTROL Activities]**, then click the desired [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) or [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activity from the list.

   If you have many activities, click the Filter ( ![Filter icon](/help/main/assets/icons/Filter.svg) ) icon to filter the list by selecting options from the [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], and [!UICONTROL Activity Source] drop-down lists. 

1. Click **[!UICONTROL Reports]**.

   The [Automated Personalization Summary](/help/main/c-reports/personalization-reports/reports-ap.md) or [Auto-Target Summary](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) report displays, which provides information about the performance of your activities, represented by the first screen icon. The two additional icons represent the two [!UICONTROL Personalization Insights] reports: **[!UICONTROL Automated Segments]** ( ![Automated Segments report](/help/main/assets/icons/AutomatedSegment.svg) ) and **[!UICONTROL Important Attributes]** ( ![Important Attributes icon](/help/main/assets/icons/ViewList.svg) ). 
   
   
   Note that [!UICONTROL Auto-Target] has an additional graph icon for the graphical view of the [!UICONTROL Summary] report.

   >[!IMPORTANT]
   >
   >The [!UICONTROL Important Attributes] report won't be available until at least 15 days after you've activated your activity. During this initial period, you won't be able to access this report or click the [!UICONTROL Important Attributes] icon. After 15 days have passed, assuming there is sufficient personalized traffic in your activity, the [!UICONTROL Important Attributes] report is available.

1. After 15 days from activating the activity, click the **[!UICONTROL Important Attributes]** ( ![Important Attributes icon](/help/main/assets/icons/ViewList.svg) )icon.

1. Select the desired date range.

   Unlike the [!UICONTROL Summary] report (performance reporting), [!UICONTROL Personalization Insights], including [!UICONTROL Important Attributes], is available only for fixed date ranges: 15 days, 30 days, and 60 days. 
   
   These fixed date ranges allow [!UICONTROL Personalization Insights] to use a large enough range of data to reduce the likelihood that you derive insights from a short-lived pattern in your activity. The two decisions you can make for your date range is the "End Date" and the "Duration." You'll notice that the "Start" is greyed out. The start date automatically changes based on your selections for the end date and duration.

   You can access the available fixed date ranges from the [!UICONTROL Preset Date Range] drop-down list.

1. Review the [!UICONTROL Important Attributes] report data.

1. (Optional) Click the Download ( ![Download icon](/help/main/assets/icons/Download.svg) ) icon to [download the report in CSV format](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) for analysis in Excel and other tools.

   >[!NOTE]
   >
   >The Personalization Insights UI report contains select information. The CSV download for the Important Attributes report contains additional details. The Important Attributes report download includes the full list of the top 100 attributes, while the UI report includes the top 10 only. If you are looking for a specific attribute on the report but it is not there, that doesn't mean that the attribute didn't influence the activity, it just didn't make the list for the top 100 attributes.

## Interpret the Important Attributes report

The following table explains how to interpret the report and describes its elements:

| Element | Details |
|--- |--- |
|Bar graph|The multi-colored bar graph at the top of the screen allows you to visualize these relative importance scores and maps to the dot's color beside each respective attribute in the table. You can also hover over a specific color in the bar chart to see the attribute it represents.  The importance scores across the top 100 attributes add to 100%. For more information about how to add more attributes that Target's personalization models can use, see [Uploading Data for Target's Personalization Algorithms](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).|
|Model Attribute Ranking chart|The Model Attribute Ranking includes the top 10 attributes that were most important to how Target's personalization model decided what content to show each visitor. The importance score shows, relative to the top 100 attributes, how important a specific attribute was to Target's personalization models in this activity.|

## Important Attributes FAQ {#section_740910A52FA646B4AC9452F98C2F5719}

Consult the following FAQs for answers to commonly asked questions about using the [!UICONTROL Important Attributes] report.

### Personalization Insights reports are not available yet for my activity. Why is that?

There are several reasons why the [!UICONTROL Personalization Insights] reports might not yet be available for your activity:

* 15 days has not passed since you activated the activity. Automated Segments and Important Attributes reports won't be available until at least 15 days after you've started your activity. During this initial period, you won't be able to access these reports or click the Automated Segments and Important Attributes icons. 
* Your activity has not had sufficient traffic during the specified time frame. After 15 days have passed, assuming there is [sufficient personalized traffic](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB) in your activity to build the personalization models, Automated Segments and Important Attributes reports will be available. 
* Your activity has a revenue optimization goal. At this time, [!UICONTROL Personalization Insights] is available only for conversion optimization goal activities. We will be adding support for revenue optimization goal activities in a future release.

### What is an attribute?

An attribute is information about a visitor or his or her specific visit used by the personalization algorithms to learn how to personalize traffic. For example, an attribute might be browser type, location, time of day of visit, and so forth.

For more information about what attributes [!DNL Target] uses in its personalization models, see [Data Collection for Target's Personalization Algorithms](/help/main/c-activities/t-automated-personalization/ap-data.md). For more information about how to upload new attributes into Target to use in Target's personalization models, see [Methods to get Data into Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}.

### I see one or more attributes that I don't want the model to use for training. Can I remove those attributes from the training model? {#models-api}

The [!UICONTROL Models API], also called the Blocklist API, lets users view and manage the list of attributes (also called features) used in machine learning models for [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] (AT) activities. If you want to exclude one or more attributes from being used by the models for AP or AT activities, you can use the Models API to add those attributes to the "blocklist."

For detailed information, see [Models API overview](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html){target=_blank} in the *Adobe Target Developer Guide*. To use the API to block attributes, see [Models API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api-overview.html){target=_blank}. 

### Is the information in the [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes] reports the same as in the CSV download?

No, the UI report contains select information. The CSV download contains additional details. The Automated Segment Insights report download includes additional Automated Segments beyond the top segments included in the UI, along with how those segments performed against your offers or experiences. The Important Attributes report includes the top 100 visitor attributes and their relative importance, while the UI only includes the top 10 visitor attributes.

### Can I see Personalization Insights for a custom date range?

Personalization Insights reporting (both [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes]) is available only for fixed date ranges: 15 days, 30 days, 45 days, 60 days, and 90 days. These fixed date ranges allow [!UICONTROL Personalization Insights] to use a large enough range of data to reduce the likelihood that you derive insights from a short-lived pattern in your activity. You can select these durations for any end-date (where these is enough data in the activity to satisfy the duration).

### How is [!UICONTROL Personalization Insights] created?

[!UICONTROL Personalization Insights] is created using an Adobe patent-pending technique called MAGIX (Model Agnostic Globally Interpretable Explanations). You can learn more about MAGIX in the Adobe research team's published paper on the [arXiv.org website](https://arxiv.org/abs/1706.07160).

### Are [!UICONTROL Personalization Insights] available for revenue-based modeling goals/primary goal?

At this time, [!UICONTROL Personalization Insights] is available only for conversion optimization goal activities. We will be adding support for revenue optimization goal activities in a future release.

### What is the attribute importance score in the Important Attributes report?

The importance score in the "Attribute Importance Ranking" part of the report provides input into what variables the algorithm used to learn were most important when it determined how to split all the visitors into the segments it identified. It assigned a percentage score to the top 100 attributes used by the model.

### Why are some offers/experiences with a lower conversion rate receiving a larger amount of traffic compared to other offers/experiences for a certain automated segment?

There are several potential reasons why you might see more visits to a lower-conversion offer/experience within an automated segment, including:

* A small number of views for some or all of the offers/experiences for a certain automated segment.
* Lower-volume activities in which certain offers or experiences do not have models built. 
* Lower-volume activities in which models were built sooner for some offers/experiences than others. For example, suppose an additional model was built on day 22, and you are looking at data from days 10-24.
* Targeting rules on a specific offer that limit which visitors can see which offers/experiences.
* There are no confidence intervals in the insight reporting. However, if conversion rates are close enough, the model might serve traffic so that it is higher in the point amount, but they aren't "statistically different" numbers.

Knowing how the model works that serves traffic can be helpful. Each individual is served based on his or her total profile. However, the Insights reports generalize this behavior to make it more interpretable by a human. As a result, segments are not mutually exclusive. This can lead to individual segments displaying this type of behavior because the same person can appear in multiple segments.

### What are different ways I can leverage the information in Personalization Insights?

* Discover new audiences to target: If you see a particular automated segment that performs particularly well, you might consider creating an audience so you can reuse that segment in other reports. 
* Test your hypotheses of what type of visitors will respond to which of your experiences. 
* Derive insight into what content worked for what kind of visitors: What offers were responsible for lift across which visitors. 
* Identify underperforming content. 
* Understand what attributes were most critical to how the model learned. 
* See which attributes are used in the personalization models and how important they are. 
* Identify opportunities for additional data points you can pass into Target to further inform your personalization.

## Known issues

The following issue is currently being investigated by the [!DNL Target] engineering team. 

* [!DNL Adobe Experience Platform] segment names do not display in the [!UICONTROL Important Attributes] report for [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] (AT) activities. (TOP-3813)
