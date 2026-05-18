---
keywords: Automated Personalization;ap;upload data;offline data;personalization algorithm;auto target;auto-target;best practices
description: Learn how to upload offline data when building personalization models in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] activities.
title: How Can I Upload Data for Personalization Algorithms?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
TQID: https://experienceleague.adobe.com/B1vwWrii4DfQzXftwcmgzbhBkDAZFo5mDRn3a7dULj0
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
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
