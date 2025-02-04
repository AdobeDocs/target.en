---
keywords: reports;block ip address;block visitor from ip address;download reports;csv;reporting
description: Optimize your activities by mastering [!DNL Adobe Target]'s reporting features to enhance decision-making and boost ROI.
title: How Do I View Reports?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
---
# Reports

Reports provide information about the progress and results of your [!DNL Adobe Target] activities that help you make decisions based on data. Report data can help you decide when to end an activity, show you which experience or offer is the winner, and provide insights or learnings you need to determine next actions.

## Display a report {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. Click **[!UICONTROL Activities]**, then click the desired activity from the list.

   If you have many activities, you can click the Filter icon ( ![Filter icon](/help/main/assets/icons/Filter.svg) ) to filter the list by selecting options from the [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], [!UICONTROL Decisioning Method], and [!UICONTROL Activity Source] lists.

   For example, you could select [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] from the [!UICONTROL Type] drop-down list and [!UICONTROL Live] from the [!UICONTROL Status] drop-down list to display only [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] activities that are in an active state.

   The following illustration shows the [!UICONTROL Type] drop-down list with two types selected: [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting]. Note that the three types of A/B Tests (Manual, [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), and [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) are selected by default. You can deselect one or more types as needed.

   ![Filter reports by type](/help/main/c-reports/assets/report-filters-refresh.png)

1. Click the desired activity from the list to display its [!UICONTROL Overview] page.

1. Click the **[!UICONTROL Reports]** tab in the left rail.

   ![A/B report](/help/main/c-reports/assets/reports-refresh.png)

   Each report includes a legend to help you understand the report.

   The legend displays the following information:

    * The activity status, including the date range when the activity ran.
    * The [projected winning experience](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (if available). 

   >[!NOTE]
   >
   >Experience results appear after at least one entrant has seen the experience.

1. (Optional) [Configure the report](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA) by clicking the Report Settings icon ( ![Report Settings icon](/help/main/assets/icons/Setting.svg) ).
1. (Optional) Click the Download Reports icon ( ![Download Reports icon](/help/main/assets/icons/Download.svg) ) to [download the report in CSV format](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) for analysis in Excel and other tools.

   The following options are available:

    * [!UICONTROL Export Report to CSV]
    * [!UICONTROL Export Order Details to CSV]

1. (Optional) Click the **[!UICONTROL Table View]** ( ![Table View icon](/help/main/assets/icons/Table.svg) ) and **[!UICONTROL Graph View]** ( ![Graph View icon](/help/main/assets/icons/GraphTrend.svg) ) icons to switch between reporting formats.

   Depending on the type of report you selected, other views and reports might be available:

   |Report Type|View|
   | --- | --- |
   |[[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)|Click the **[!UICONTROL Automated Segments]** ( ![Automated Segments report](/help/main/assets/icons/AutomatedSegment.svg) ) or **[!UICONTROL Important Attributes]** ( ![Important Attributes icon](/help/main/assets/icons/ViewList.svg) ) icons.<ul><li>The [[!UICONTROL Automated Segments] report](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) shows how different visitors respond differently to the offers and experiences in your [!UICONTROL Automated Personalization] or [!UICONTROL Auto-Target] activity. This report shows how different automated segments defined by the [!DNL Target] personalization models responded to the offers and experiences in the activity.</li><li>The [[!UICONTROL Important Attributes] report](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) shows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance.</li></ul>|
   |[[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP)|In addition to the [[!UICONTROL Automated Personalization Summary] reports](/help/main/c-reports/personalization-reports/reports-ap.md), you can click the **[!UICONTROL Automated Segments]** ( ![Automated Segments report](/help/main/assets/icons/AutomatedSegment.svg) ) or **[!UICONTROL Important Attributes]** ( ![Important Attributes icon](/help/main/assets/icons/ViewList.svg) ) icons.<ul><li>The [[!UICONTROL Automated Segments] report](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) shows how different visitors respond differently to the offers and experiences in your [!UICONTROL Automated Personalization] or [!UICONTROL Auto-Target] activity. This report shows how different automated segments defined by the [!DNL Target] personalization models responded to the offers and experiences in the activity.</li><li>The [[!UICONTROL Important Attributes] report](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) shows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance.</li></ul>|
   |[[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT)|In addition to the [[!UICONTROL Experience Performance] report](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), you can click the [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) ( ![Location Contribution icon](/help/main/assets/icons/LocationContribution.svg) ) icon to switch the report to show contribution by location.|

## Additional reporting information for specific activity types {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

In addition to the general reporting information in this topic and its subtopics, additional information specific to individual activity types is available elsewhere in this guide:

| Activity Type | Details |
|--- |--- |
|[[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)|To understand lift and confidence and the statistical approaches used in [!DNL Target], see [Plan an A/B Test](/help/main/c-activities/t-test-ab/sample-size-determination.md).|
|[Interpret [!UICONTROL Auto-Allocate] reports](/help/main/c-activities/automated-traffic-allocation/determine-winner.md)|Interpret the results of an [!UICONTROL Auto-Allocate] A/B activity by examining important indicators, including lift and confidence, in the [!DNL Target] UI.|
|[[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT)|Information about the [!UICONTROL Summary] report for AT activities. For more information, see [[!UICONTROL Auto-Target Summary] Report](/help/main/c-reports/personalization-reports/auto-target-summary-report.md).<br>Information about the two [!UICONTROL Personalization Insights] reports for AT and AP activities: [!UICONTROL Automated Segments] report and [!UICONTROL Important Attributes] report. For more information, see [Personalization Insights Reports](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md).|
|[[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP)|Information about the two [!UICONTROL Automated Personalization Summary] reports for AP activities: [!UICONTROL Activity Level] report and [!UICONTROL Offer Level] report. For more information, see [Automated Personalization Summary Reports](/help/main/c-reports/personalization-reports/reports-ap.md).<br>Information about the two [!UICONTROL Personalization Insights] reports for AT and AP activities: [!UICONTROL Automated Segments] report and [!UICONTROL Important Attributes] report. For more information, see [Personalization Insights Reports](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md).|
|[[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT)|Information about the two reports for MVT activities: [!UICONTROL Experience Performance] report and [!UICONTROL Location Contribution] report. For more information, see [Experience Performance Report](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) (MVT) and Location Contribution Report](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT).|
|[[!DNL Adobe Analytics] as the Reporting Source for Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T)|Information about using [!DNL Adobe Analytics] as the reporting source for [!DNL Target] (A4T). A4T gives you access to [!DNL Analytics] reports for your [!DNL Target] activities. For more information, see [Analytics for Target (A4T) Reporting](/help/main/c-reports/analytics-for-target-a4t-reporting.md).|
|[[!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md)|Information about the integration between [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} and [!DNL Target] that provides powerful analysis and timesaving tools for your optimization program.|

## Block reporting data from specified IP addresses

You can block visitors from specified IP addresses from being counted in reports. This option is helpful, for example, to block reporting data from your internal visitors.

[Contact Client Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to set up IP filters. This filtering does not apply when using [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T) as your reporting source.
