---
keywords: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Learn how to use the Traffic Estimator that lets you know if you have sufficient traffic for your [!DNL Adobe Target] [!UICONTROL Multivariate Test] activity to succeed.
title: How Much Traffic Is Needed for a [!UICONTROL Multivariate Test] (MVT) Activity?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
TQID: 'https://experienceleague.adobe.com/XHBXV7Jtvp87ve4NTd-016E2dFkHTbPu-8-nY8GE-VM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Estimate the traffic required for a successful [!UICONTROL Multivariate Test] activity {#traffic-estimator}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use the **[!UICONTROL Traffic Estimator]** to check whether your **[!UICONTROL Multivariate Test]** activity has sufficient traffic to succeed.

>[!ENDSHADEBOX]

A multivariate test compares multiple experiences, so it is important to know how much traffic is required to provide meaningful results. The **[!UICONTROL Traffic Estimator]** uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the test successful. It also provides feedback that lets you know whether you have sufficient traffic for the test that you designed to succeed.

The **[!UICONTROL Traffic Estimator]** predicts the sample size needed to ensure the following:

* **95% confidence.** This statistic means that the chance of reporting a false positive if there is no real lift is 5% (100% - confidence level).
* **80% statistical power.** This statistic means that the test has an 80% probability of detecting a true lift of 25% or more.
* **25% minimum reliably detectable lift.** [!DNL Target] computes the amount of traffic required to have an 80% chance of detecting a true lift of 25% or more.

The test uses the Bonferroni correction to correct for multiple comparisons. This method is known for being conservative, which is balanced out by enforcing a relatively large minimum reliably detectable lift.

## Use the Traffic Estimator {#use-traffic-estimator}

While you design a **[!UICONTROL Multivariate Test]**, the **[!UICONTROL Traffic Estimator]** lets you check whether the traffic to your page is sufficient for the number of experiences that you plan to test. Running this check before you launch the test helps you avoid a test that cannot reach enough visitors to produce meaningful results, and shows you how to adjust the number of combinations or the duration of the test if the traffic is not sufficient.

1. From the **[!UICONTROL Experiences]** page of the **[!UICONTROL Visual Experience Composer]** in a **[!UICONTROL Multivariate]** activity, click the **[!UICONTROL Traffic]** icon ( ![Traffic Estimator icon](/help/main/assets/icons/Gauge2.svg) ) in the top left corner of the page.

   The **[!UICONTROL Traffic Estimator]** opens. To hide it, click the icon again.

   ![Traffic Estimator user interface](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   Near the top of the **[!UICONTROL Traffic Estimator]**, the values that you entered are calculated and the results are shown.

1. (Optional) Provide the typical conversion rate, the estimated visitors per day, and the test duration.

   The **[!UICONTROL Traffic Estimator]** uses these statistics to determine what adjustments are needed to run a successful test.

   |Metric|Description|
   | --- | --- |
   |**[!UICONTROL Number of Content Combinations]**|This metric is calculated automatically, based on the number of experiences being created as a part of your activity, after any exclusions.|
   |**[!UICONTROL Typical Conversion Rate]**|This metric is expressed as a percentage, based on your estimation or past data from your analytics system.|
   |**[!UICONTROL Estimated Visitors Per Day]**|This metric is the number of visitors who are likely to view this page, based on the targeting criteria. This number could be based on your analytics data.|
   |**[!UICONTROL Test Duration]**|The number of days that you want the activity to run.|

1. Review the results. As you change the numbers, the estimate changes.

   For example, if you are testing many experiences and your conversion rate and impressions are too low, the **[!UICONTROL Traffic Estimator]** shows how long the test must run to be successful. Or, if your traffic is low, the **[!UICONTROL Traffic Estimator]** might suggest a lower number of experiences so that you can run the test for the desired number of days.

1. If you do not have sufficient traffic, do one or both of the following:

   * Reduce the number of combinations of offers and the number of locations.
   * Increase the duration of the test.

1. Adjust the numbers until the **[!UICONTROL Traffic Estimator]** indicates that you have sufficient traffic, then design your test accordingly.
