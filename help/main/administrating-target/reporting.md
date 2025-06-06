---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Use [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics] as the reporting source, specify the default time zone and currency format, add IP addresses to exclude from reporting, and more.
title: How Do I Configure Reporting in [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
---
# Configure reporting in [!DNL Target]

Configure general settings to use in [!DNL Adobe Target] reporting that apply to your entire [!DNL Target] account.

{{permissions-update}}

To access the [!UICONTROL Reporting] configuration page, click **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

You can specify the following settings on this page:

* The Adobe Experience Cloud solution to use for reporting
* The time zone to use for reporting
* The currency to use for reporting
* IP addresses to exclude from reporting
* Whether to show estimated lift in revenue in reporting
* Whether to enable fine-grained priorities

>[!NOTE]
>
>Be aware that the time zone, currency, and IP addresses to exclude settings apply to activities that use [!DNL Target] reporting. These settings do not apply to activities that use [Analytics for Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) or [!DNL Customer Journey Analytics] as the reporting source.

![Reporting page](/help/main/administrating-target/assets/reporting.png)

## Reporting Cloud Solution {#solution}

Set options that determine what data is used for your results and reports.

Select the reporting source for your activities, either [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics]. You can also choose to select the reporting source per activity as part of three-part guided workflow while creating the activity. 

Consider the following information as you choose your reporting source:

* **[!DNL Adobe Target]**: If the reporting source is set to **[!DNL Target]** here, you are not allowed to create or activate an activity that uses [!DNL Analytics] or [!DNL Customer Journey Analytics] as the reporting source. You must change the reporting source to **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Analytics]**: If the reporting source is set to **[!DNL Analytics]** here, you are not allowed to create or activate an activity that uses [!DNL Target] or [!DNL Customer Journey Analytics] as the reporting source. You must change the reporting source to **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Customer Journey Analytics]**: If the reporting source is set to **[!DNL Customer Journey Analytics]** here, you are not allowed to create or activate an activity that uses [!DNL Target] or [!DNL Analytics] as the reporting source. You must change the reporting source to **[!UICONTROL Select per activity]**.
* **Select per activity**: If the reporting source is set to **[!UICONTROL Select per activity]** here, you can create and activate activities that are supported by the selected reporting source.

When determining your reporting source, consider the following information:

* **[!DNL Analytics]**: For a matrix of supported activities using [!DNL Analytics] as the reporting source (A4T), see [Supported activity types](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics as the reporting source for Adobe Target (A4t)*.

    [!UICONTROL Automated Personalization] (AP) activity creation and activation are allowed irrespective of the reporting source selected. [!UICONTROL Automated Personalization] activities are not supported when you choose [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md). 
    
    Even if you specify [!DNL Analytics] as your reporting source, [!DNL Target] is used as the reporting source for [!DNL Automated Personalization] activities. 

* **[!DNL Customer Journey Analytics]**: For a matrix of supported activities using [!DNL Target] reporting in [!DNL Customer Journey Analytics], see [Supported activity types](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md#supported-activities) in *[!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics]*.

    [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate], and [!UICONTROL Auto-Target] activity creation and activation are allowed irrespective of the reporting source selected. These activities are not supported when you choose [Adobe Customer Journey Analytics as the reporting source](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md). 
    
    Even if you specify [!DNL Customer Journey Analytics] as your reporting source, [!DNL Target] is used as the reporting source for [!DNL Automated Personalization] activities. 
    
    If you specify [!DNL Customer Journey Analytics] as your reporting source for [!UICONTROL Auto-Allocate] or [!UICONTROL Auto-Target] activities, [!DNL Target] or [!DNL Analytics] can be used as the reporting source. 

## Timezone for Reporting

Specify the time zone to use for reporting.

## Currency for Reporting

Specify the currency to use for reporting.

## IPs to exclude from [!DNL Target] reporting data

Specify any IP addresses that you want to exclude from reporting data. For example, excluding internal company addresses is a good way to ensure that your reporting data reflects customer interactions on your website.

Enter each IP address on a new line.

## Show estimated lift in revenue

You can choose to show the estimated lift in revenue if you enter a monetary value for your goal. [!DNL Target] can estimate the revenue lift you would attain if all users view the winning experience. The estimated lift feature is disabled by default.

Only [!DNL Experience Cloud] Admin users can enable or disable this feature. If estimated lift is disabled, the corresponding fields do not appear in the interface. Disabling the feature does not result in a loss of data, including the data used for your estimates. The estimates are based on data that is collected whether or not the feature is enabled.

For detailed information, see [Estimating Lift in Revenue](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Enable fine-grained priorities

Allow numerical entries for priority ranging from 0-999.

Depending on your settings, the UI and options for Priority  vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999.

The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.
