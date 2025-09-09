---
keywords: reports;download reports;csv;success metrics;order details
description: Learn how to download data from Adobe [!DNL Target] activities in a CVS format for quick import into Excel, Access, or other data analysis programs.
title: How Do I Download Report Data In A CSV File?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
---
# Downloading data in a CSV file

Download data in a .csv format for quick import into [!DNL Excel], [!DNL Access], or other data analysis programs.

To download data in a CSV file:

1. Click **[!UICONTROL Activities]**, then click the desired activity from the list.

   If you have many activities, click the Filter ( ![Filter icon](/help/main/assets/icons/Filter.svg) ) icon to filter the list by selecting options from the [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], and [!UICONTROL Activity Source] drop-down lists. 

1. Click the **[!UICONTROL Reports]** tab. 
1. Click the **[!UICONTROL Download]** ( ![Download icon](/help/main/assets/icons/Download.svg) ) icon, then select a report type to download for analysis in Excel and other tools.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

## [!UICONTROL Export Report to CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

The [!UICONTROL Success Metrics] report shows you information about your success metrics, and the following metrics that are not available in the [!DNL Target] UI:

* Mean time to conversion in hours, so you can see how long it takes the average visitor to reach the conversion point 
* Sum of revenues, squared, for offline statistical confidence calculations

Data is saved until the end of the activity.

>[!NOTE]
>
>The CSV report includes only raw data and does not include calculated metrics such as revenue per visitor, lift, or confidence used for A/B tests. To calculate these calculated metrics, download the [!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel file to input the activity's value, or review [Statistical calculations in A/Bn tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Export Order Details to CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

The [!UICONTROL Order Details] report shows you information about your orders, including:

* Order date and time 
* Order amount (if you inserted a Place Order mbox)

  The [!UICONTROL Order Details] report works only if you have orders. 

* Order flag (duplicate or extreme orders)

  An order is flagged as extreme if it is more than +/- 3 standard deviations from the average order value. This calculation uses the last month of data (up to the point in time in which the calculation was made). An activity will have its extreme orders excluded once the activity has run for an hour or until after 15 orders, whichever comes first. For more information, see [Excluding Extreme Orders](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA). 

* Product ID

  The total length of product IDs, concatenated with commas, should not exceed 255 characters or the IDs do not display properly in the report. For example, if your order had products with IDs "aa, bb" then the total length is "aa,bb" = 5. 

* Experience

  In the [!UICONTROL Order Details] report for [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT), and [!UICONTROL Multivariate Test] (MVT) activities, the [!UICONTROL Experience] column contains the experience `localId`. This is the value output from the `$campaign.recipe.id` in offer tokens.

  There is not an [!UICONTROL Experience] column for [!UICONTROL Automated Personalization] (AP) activities. The current [!UICONTROL Algorithm Name] column has been replaced with "Control" versus "Targeted" terminology, as shown elsewhere in [!DNL Target].

  There was no impact on [!UICONTROL Recommendations] activities.

>[!NOTE]
>
>* Order report data includes four weeks of data for the default environment (host group) and two weeks for all non-default environments.
>* Revenue metrics that are set to "[!UICONTROL Increment count and keep the user in the activity]" log order details only for the first order made by the same visitor. All subsequent orders increase conversion count, but do not add revenue to RPV/AOV/Sales, and are not included in the [!UICONTROL Order Details] report.

## CSV download format for popularity and key-based algorithms {#format}

The CSV download file consistently reflects results generated after backend criteria execution. 

**For popularity algorithms (non-key-based), the file includes:**

* A row of backup recommendations prefixed with *
* A separate row listing recommendations based on algorithm settings

**For key-based algorithms, the file includes:**

* A backup row similar to popularity algorithms
* Multiple rows in key-value format, where the first entry is the product ID of the key, followed by comma-separated product IDs representing recommendation candidates

## Best Practices

* To record an order record, the `orderTotal` parameter must be passed. 
* Values passed via the `ProductPurchasedId` mbox parameter are listed in the [!UICONTROL Order Details] report. 
* Best practice is to include an `orderID` and an `orderTotal`. This allows duplicate orders to automatically be ignored.

## Caveats {#section_49B9590904A645B18E694B4EFFFC1DEF}

The following information applies to the [!UICONTROL Download] option:

* You can download both reports for [!UICONTROL A/B Test], [!UICONTROL Automated Personalization], [!UICONTROL Experience Targeting], and [!UICONTROL Multivariate] activities. You cannot download the [!UICONTROL Success Metrics] report for [!UICONTROL Recommendations] activities. 
* The [!UICONTROL Download] option is not available for [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] activities created before [!DNL Target] version 15.7.1 (July  2015). 
* Experiences with no associated data are not recorded in the downloaded report.
* Audiences applied in the [!DNL Target] reporting UI do not carry over to the download report.
* Reports generated for download as .csv files are inconsistent if the activity uses more than one metric. The downloadable report is generated based on the report settings only and considers the same value for any other metrics used. The source of truth is always the displayed report in the [!DNL Target] UI.
