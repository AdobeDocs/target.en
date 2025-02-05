---
keywords: reports;auto-target;auto target;AT;report
description: Learn how to interpret the Auto-Target Summary report in Adobe Target. You can switch to the Automated Segments and Important Attributes reports from this report.
title: How Do I Use the Auto-Target Summary Report?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
---
# [!UICONTROL Auto-Target Summary report]

Information about how to interpret the [!UICONTROL Auto-Target Summary] reports in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] is available as part of the [!DNL Target Premium] solution. It is not included with [!DNL Target Standard] without a [Target Premium license](/help/main/c-intro/intro.md#premium).

To display the [!UICONTROL Auto-Target Summary] reports:

1. From the [!UICONTROL Activities] page, click the desired [!UICONTROL Auto-Target] activity.

   If you have many activities, click the Filter ( ![Filter icon](/help/main/assets/icons/Filter.svg) ) icon to filter the list by selecting options from the [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], and [!UICONTROL Activity Source] drop-down lists. 

1. Click the **[!UICONTROL Reports]** tab, then click the desired icon:

   * **[!UICONTROL Table View]** ( ![Table View icon](/help/main/assets/icons/Table.svg) )
   * **[!UICONTROL Graph View]** ( ![Graph View icon](/help/main/assets/icons/GraphTrend.svg) )
   *  **[!UICONTROL Automated Segments]** ( ![Automated Segments report](/help/main/assets/icons/AutomatedSegment.svg) )
   * [!UICONTROL Important Attributes]** ( ![Important Attributes icon](/help/main/assets/icons/ViewList.svg) )

## Table View

Some tips and considerations as you interpret your [!UICONTROL Auto-Target] reports:

* The various rows in the table help you understand activity performance.

    * The top two rows in the table on the reporting page show the results of an A/B test between the visitors who were assigned to the control (that is, randomly served experiences) and the visitors who were assigned to the personalization algorithm. This information can be used to measure how the personalization algorithm performed compared to the randomly served control. 
    * The remaining rows show experience-level results. For each experience, there is a comparison between the average response of visitors who were shown that experience as a randomly served control, and the average response of visitors who were shown the experience using the personalization algorithm.

* The green check icon next to each experience in the report indicates that a personalized machine-learning model has been generated for that experience. The clock icon indicates that not enough traffic has been served to build the model.

    * Because the model is built per experience, it is possible to see a model for some experiences with a green check and others with a clock icon. 
    * In this case, to increase the speed of the activity having models built for all experiences, additional traffic is sent to experiences with unbuilt models. 
    * There must be at least two experiences with built models (green checkmark) for personalization to begin.

* Comparing the conversion rate of experience A with that of experience B is not the right comparison in [!UICONTROL Auto-Target]. The question is whether experience A performs better when served in an intelligent way versus a random way (in other words, versus the control). Marketers should also use caution about interpreting the lifts of individual experiences because the personalization algorithm is attempting to optimize for the success metric over the entire activity, not over each individual experience. 
* Experiences with the highest lift can be understood as having the highest differentiation within the population. That is, the algorithm has found a segment that likes that particular experience the most.
* The various columns in the table show the number of visits, conversion rate, average lift and confidence level, and confidence. For more information, see [Statistical calculations in A/B tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Graph View

Use the two drop-down lists to choose the desired metrics, counting methodology, and more. See [Report settings overview](/help/main/c-reports/c-report-settings/report-settings.md) for more information:

## Automated Segments

This report shows how different visitors respond differently to the offers/experiences in your AP/AT activity. This report shows how different automated segments defined by the [!DNL Target] personalization models responded to the offers/experiences in the activity.

For more information, see the [Automated Segments report](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Important Attributes

This report shows how, in different activities, different attributes are more (or less) important to how the model decides to personalize. This report shows the top attributes that influenced the model and their relative importance.

For more information, see the [Important Attributes report](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).
