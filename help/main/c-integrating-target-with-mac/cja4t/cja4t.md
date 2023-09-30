---
keywords: cja4t;customer journey analytics;customer journey analytics for target;customer journey analytics reporting source;customer journey analytics as the reporting source for target
description: Use [!DNL Adobe Customer Journey Analytics] for [!DNL Target] (A4T) to create activities based on [!DNL Customer Journey Analytics] conversion metrics and audience segments and use [!DNL Customer Journey Analytics] reports to examine results.
title: What is [!DNL Adobe Customer Journey Analytics] for [!DNL Target] (CJA4T)?
feature: Integrations
hide: yes
hidefromtoc: yes
exl-id: 67b20bf6-ffbe-4220-9455-cb3886bb9227
---
# [!DNL Adobe Customer Journey Analytics] as the reporting source for [!DNL Adobe Target] (CJA4T)

The [!DNL Customer Journey Analytics for Target] (CJA4T) integration between [Adobe Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/docs/customer-journey-analytics.html){target=_blank} and [!DNL Target] provides powerful analysis and timesaving tools for your optimization program.

The primary benefits of using [!DNL Customer Journey Analytics] data in [!DNL Target] are:

* Marketers can dynamically apply [!DNL Customer Journey Analytics] success metrics to [!DNL Target] activity reports at any time. It is not required to specify everything before running the activity. 
* A single source of data minimizes the variance that occurs when collecting data in two separate systems.

## Considerations

Consider the following information before using the CJA4T integration:

* To use [!DNL Customer Journey Analytics] as the reporting source for [!DNL Target], both you and your company must have access to [!DNL Customer Journey Analytics] and to [!DNL Target]. If you need access to either solution, contact your organization's administrator or your account representative.
* To create [!DNL Target] activities with [!DNL Customer Journey Analytics] reporting, you must have either the "[!UICONTROL Approver]" or '[!UICONTROL Editor]" role in [!DNL Target].
  * If you have a [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) account, see [Specify roles and permissions](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Users*.
  * If you have a [Target Premium](/help/main/c-intro/intro.md#premium) account, see [Roles and permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Enterprise user permissions*.

* You must be part of a role in [!DNL Adobe Experience Platform] to set up a [!DNL Target] activity with [!DNL Customer Journey Analytics] as the reporting source. For more information, see [Add a Role in [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/configure-permissions.html){target=_blank} in *Configure permissions* in the *Data Architect and Engineer Tutorial.*
* Depending on your settings, reporting can be changed per activity or at an organization level. See [Reporting Cloud Solution](/help/main/administrating-target/reporting.md#solution) in *Configure reporting in Target*.
* Use one reporting source or the other. You cannot collect data for a single activity to multiple reporting sources. 
* When you set [!DNL Customer Journey Analytics] as your reporting source, you are prompted to specify the sandbox for reporting. During configuration, you see only the sandboxes to which you have access.
* Any existing [!DNL Target] activities continue to use [!DNL Target] data collection and are not affected by enabling CJA4T.
* CJA4T is only available if you have [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html){target=_blank} and [!DNL Target] implemented through the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}. Support for the [!DNL Analytics Data Connector] is planned for the future.
* For any questions about timing, see [Latency considerations](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#latency){target=_blank} in *Frequently Asked Questions* in the *Adobe Customer Analytics Guide*.

## Supported activity types {#supported-activities}

The following activity types are supported when using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} or the [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank} JavaScript library:

| Activity Types | CJA4T Compatible? |
|--- |--- |
|[A/B activity with manual traffic split](/help/main/c-activities/t-test-ab/test-ab.md)|Yes|
|[A/B activity with Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)|No|
|[A/B activity with Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md)|No|
|[Experience Targeting (XT)](/help/main/c-activities/t-experience-target/experience-target.md)|Yes|
|[Multivariate test (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)|Yes|
|[Automated Personalization (AP) activity](/help/main/c-activities/t-automated-personalization/automated-personalization.md)|No|
|[Recommendations activity](/help/main/c-recommendations/recommendations.md)|Yes|

## Create an activity that uses [!DNL Customer Journey Analytics] as the reporting source

Creating a [!DNL Target] activity that uses [!DNL Customer Journey Analytics] as the reporting source is similar to setting up a regular [!DNL Target] activity.

1. From the **[!UICONTROL Activities]** list, click **[!UICONTROL Create Activity]**, then select the activity type (according to the [supported activity chart above](#supported-activities)) and begin setting up the activity.
1. When you get to the **[!UICONTROL Goals & Settings]** page of the three-part activity creation workflow, select **[!DNL Customer Journey Analytics]** as the reporting source.

   ![Customer Journey Analytics as the reporting source option](/help/main/c-integrating-target-with-mac/cja4t/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >The reporting source cannot be changed after a [!DNL Target] activity goes live.

1. Select a sandbox.

   You can see only the sandboxes that you have access to in this drop-down list. If one or more of the sandboxes you have access to is missing from the list, verify that you have access to the sandbox. Contact [Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) if you continue to see issues. 

   ![Select sandbox option](/help/main/c-integrating-target-with-mac/cja4t/assets/sandbox.png)

1. Specify the activity goal.

   Select a success metric to use as a goal for each activity. You can choose one of the [!DNL Target] conversion metrics or use a [!DNL Customer Journey Analytics] metric. 

   ![Use a Customer Journey Analytics metric option under Goal Metric](/help/main/c-integrating-target-with-mac/cja4t/assets/goal-metric.png)

1. Click **[!UICONTROL Save & Close]**.

## Set up a [!DNL Customer Journey Analytics] connection

After a [!DNL Target] activity has been created, you must create a connection in [!DNL Customer Journey Analytics]. If you already have a connection set up, you can use your existing connection and skip to Step 4 below. The connection allows [!DNL Customer Journey Analytics] to start pulling data from the dataset for reporting.

1. In [!DNL Customer Journey Analytics], on the **[!UICONTROL Connections]** page, click **[!UICONTROL Create a new connection]**.

   ![Create new connection link in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/create-connection.png)

1. Configure your [connection and data settings](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html){target=_blank} with the correct information.
1. Add the event dataset that you used when configuring your datastream.
1. Add the **[!UICONTROL Adobe Target Classification Events]** lookup dataset, then click **[!UICONTROL Next]**.

   ![Add data sets dialog box in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/add-datasets.png)

1. Configure your event dataset.

   For more information, see [Add and configure datasets](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#add-dataset){target=_blank} in *Create a connection* in the *Adobe Customer Journey Analytics Guide*.

1. Configure your lookup dataset with the [!UICONTROL Key] field as "key" and the Matching key field with the following path:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Adobe Target Classifications event dialog box in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/classifications-events.png)

1. Click **[!UICONTROL Add datasets]**, then click **[!UICONTROL Save]** on the next screen to finish your connection.

## Set up data views

Set up a data view in [!DNL Customer Journey Analytics]. A data view ensures that the data from your connection can be used properly.

1. Set up your data view and make sure it points to the connection you created above.

   For more information, see [Create or edit a data view](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target=_blank} in the *Adobe Customer Journey Analytics Guide*.

1. To properly view your [!DNL Target] data in [!DNL Customer Journey Analytics], you must add the following fields from your Lookup Dataset as dimensions:

   * Experience Name
   * Experience ID
   * Activity Name
   * Activity ID

   ![Names and IDs options in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Finish setting up any other fields, then click **[!UICONTROL Save and continue]** when done.
