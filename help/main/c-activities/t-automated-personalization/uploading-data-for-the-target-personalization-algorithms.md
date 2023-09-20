---
keywords: Automated Personalization;ap;upload data;offline data;personalization algorithm;auto target;auto-target;best practices
description: Learn how to upload offline data when building personalization models in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] activities.
title: How Can I Upload Data for Personalization Algorithms?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
---
# Upload data for the [!DNL Target] personalization algorithms

Offline data, such as CRM information or customer churn propensity scores, can be incredibly valuable when building personalization models in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] activities.

 There are several ways to input data in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] personalization algorithms. In addition to the methods in [Methods to get Data into Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, [!DNL Experience Cloud] shared audiences ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]), and in-activity reporting audiences are also used in [!DNL Target] algorithms.

For information about the data automatically collected and used by [!UICONTROL Automated Personalization] and [!UICONTROL Auto-Target] personalization algorithms, see [Automated Personalization Data Collection](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best Practices {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

The following list presents best practices for uploading data for [!DNL Target] personalization algorithms:

* The more high-quality data that is available to [!DNL Target] personalization algorithms, the better the quality the resulting models in your [!UICONTROL Automated Personalization] and [!UICONTROL Auto-Target] activities. 
* Limit using multiple profile scripts or attributes that serve the same purpose. 
* Don't pass a unique Id, such as a session ID if not needed. 
* Review what data [!DNL Target] automatically collects ( [Data Collection for Target's Personalization Algorithms](/help/main/c-activities/t-automated-personalization/ap-data.md)) so that you don't send duplicate information. For example, [!DNL Target] uses IP addresses to determine visitors' ZIP codes. It is not necessary to pass this information as a separate variable. 
* Do not pass multiple values in the same attribute or variable. If multiple variables are concatenated, [!DNL Target] personalization algorithms treat each string as a unique value, reducing the value of the information for personalization. 
* Use a memorable and meaningful naming convention to make your [Personalization Insights Reports](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) more understandable.
