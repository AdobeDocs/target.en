---
keywords: traffic estimator;automated personalization;ap;estimate traffic
description: Use the [!UICONTROL Traffic Estimator] to assess if you have enough traffic for a [!UICONTROL Automated Personalization] activity to be successful.
title: How Much Traffic Is Needed for a Successful [!UICONTROL Automated Personalization] Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
hide: yes
hidefromtoc: yes
---
# Estimate the traffic required for success

The [!DNL Adobe Target] [!UICONTROL Traffic Estimator] provides feedback that lets you know whether you have sufficient traffic for your [!UICONTROL Automated Personalization] (AP) activity to succeed.

Because [!UICONTROL Automated Personalization] activities use multiple offer combinations, it is important to know how much traffic is required to provide meaningful results. The [!UICONTROL Traffic Estimator] uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration necessary to make the activity successful.

The [!UICONTROL Traffic Estimator] determines if there is enough traffic to generate personalized models by comparing the estimated page impressions and typical conversion rate for the pages. Ideally, for a successful activity, the correct sample size ensures that personalized content is ready within 50% of the activity duration or 14 days, whichever is less. This process allows sufficient time for obtaining personalized content and learning which content to deliver.

Remember that [!DNL Target] randomly serves experiences until the personalization algorithms are built. The check mark icon beside each offer shows when the model for that offer is ready and [!DNL Target] is able to begin delivering personalized content. Because lift is expected only after the models are ready, the visual indication lets you set the right expectation. Use the [!UICONTROL Traffic Estimator] in the [!UICONTROL Visual Experience Composer] (VEC) to get a guideline of when the models are ready.

## Use the Traffic Estimator

1. From the [!UICONTROL Experiences] page of the [!UICONTROL Visual Experience Composer] in an [!UICONTROL Automated Personalization] activity, click the  **[!UICONTROL Traffic]** icon ( ![Traffic Estimator icon](/help/main/assets/icons/Gauge2.svg) ) in the top left corner of the Experiences page.

   The [!UICONTROL Traffic Estimator] opens.

   ![Traffic Estimator user interface](assets/ap-est.png)

    You can click the icon again to hide the [!UICONTROL Traffic Estimator].

1. Specify the typical conversion rate (or the conversion rate that you expect from this activity), estimated activity impressions per day, and test duration.

   |Metric|Description|
   | --- | --- |
   |**[!UICONTROL Number of Offers]**|This metric is calculated automatically based on the number of experiences being created as a part of your activity, after any exclusions.|
   |**[!UICONTROL Typical Conversion Rate]**|This metric is expressed as a percentage, based on your estimation or past data from your analytics system.|
   |**[!UICONTROL Estimated Visits Per Day]**|This metric is the number of visits per day from visitors who are able to view the activity, based on the targeting criteria. This metric could be based on your analytics data. This number must be visits, not unique visitors.|
   |**[!UICONTROL Test Duration]**|The number of days you want the activity to run.|

   The [!UICONTROL Traffic Estimator] uses these metrics to determine what adjustments are necessary to run a successful test.

   Near the top of the [!UICONTROL Traffic Estimator], the values you entered are calculated and the results are shown.

   ![Traffic Estimate with values and results displayed](assets/ap-est-no.png)

   As you change the numbers, the estimate changes. For example, if you are testing many combinations and your conversion rate and impressions are too low, the [!UICONTROL Traffic Estimator] shows how long the test must run to be successful. Or, if your traffic is low, the [!UICONTROL Traffic Estimator] could suggest a lower number of offer combinations so you can run the test the desired number of days.

   If you do not have sufficient traffic, consider the following:

   * Consider using an [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activity instead of [!UICONTROL Automated Personalization] to create experiences with several offer changes in one experience variation. 
   * Reduce the number of offer combinations within your [!UICONTROL Automated Personalization] activity. 
   * Increase the duration of the activity.

   Adjust the numbers until the [!UICONTROL Traffic Estimator] indicates that you have sufficient traffic, then design your test accordingly.

   ![Traffic Estimator showing sufficient traffic message](assets/ap-est-yes.png)

   If the traffic is sufficient, the [!UICONTROL Traffic] icon shows a green check. If it is insufficient, the icon shows a red warning label.

## Frequently Asked Questions about the Traffic Estimator

Consider the following FAQs as you work with the [!UICONTROL Traffic Estimator]:

### Why are personalized models not built even though my AP activity has enough traffic?

In certain circumstances, your traffic is large enough for a personalized model to be built, but that traffic could inform [!DNL Target] that there is no meaningful difference between the personalized model and random. Although the model is built in [!DNL Target] and tested, it is not deployed because the model is not any better than random.

A possible reason for the model not being better than random could be that the offers are not different enough from each other. If so, you can try making the offers more visually different if the messaging is similar, or you can try changing the messaging itself.