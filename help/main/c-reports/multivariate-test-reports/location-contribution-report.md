---
keywords: mvt;multivariate test;location contribution report
description: Learn how to use the Location Contribution report for Adobe [!DNL Target] [!UICONTROL Experience Targeting] activities that show the performance of each element and each offer.
title: How Do I Use the [!UICONTROL Location Contribution] Report for [!UICONTROL Multivariate Test] activities?
feature: Reports
exl-id: 2fb7d2b3-d981-44fd-9bb2-021903605a09
---
# [!UICONTROL Location Contribution] report (MVT)

The [!UICONTROL Location Contribution] report shows the performance of each element and each offer.

The top of the report shows the metric, start and end dates, and audience used in the report. You can change any of these factors.

>[!NOTE]
>
>Keep in mind the following information as you work with the [!UICONTROL Location Contribution] report:
>
>* The audience and metric pickers are available only if [!DNL Analytics] is used as the reporting source (A4T).
>
>* Data for the [!UICONTROL Location Contribution] report is fetched from the [!DNL Target] backend even if the activity is configured to use [!UICONTROL Analytics as the reporting source] (A4T).
>
>* Data for the [!UICONTROL Location Contribution] report is fetched for the "Production" environment even if a different default environment is defined at the [!DNL Target] account level.

The [!UICONTROL Location Contribution] report includes two tables.

The first table shows the relative influence of each element. This table shows you which of the elements where you have added offers is resulting in the most conversions.

![Location Contribution report in Adobe Target](/help/main/c-reports/assets/locationcontributiontop.png)

The second table provides an offer-level report. It shows the conversion rate, lift, and confidence for each offer in each element. This table helps you determine which offers are the most successful. The second column shows values for the selected metric (conversion rate, RPV, AOV, orders, or engagement metrics) of the offer and one standardization.

![Location Contribution report in Adobe Target](/help/main/c-reports/assets/locationcontributionbottom.png)

## Training video: Create an MVT Test ![Tutorial badge](/help/main/assets/tutorial.png)

This video demonstrates how to create a multivariate test using the Target three-step guided workflow. The Location Contribution report is described beginning at 8:45.

>[!VIDEO](https://video.tv.adobe.com/v/17395)
