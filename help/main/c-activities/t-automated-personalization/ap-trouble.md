---
keywords: Automated Personalization;ap;troubleshoot;troubleshooting;model;lift
description: Explore potential challenges that you might face while using [!UICONTROL Automated Personalization] (AP) activities in Adobe Target, along with suggested solutions.
title: How Do I Troubleshoot [!UICONTROL Automated Personalization] activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
TQID: 'https://experienceleague.adobe.com/1Qevyq-TiutN1dEZnfC1DDmUgXoHIxtBl-3RMPq-m-0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Troubleshoot [!UICONTROL Automated Personalization] {#ap-troubleshooting}

>[!BEGINSHADEBOX]

**On this page:** Find solutions to common issues with **[!UICONTROL Automated Personalization]** activities.

>[!ENDSHADEBOX]

Activities do not always go as expected. Use the following list to identify the cause of common problems in [!UICONTROL Automated Personalization] (AP) activities and to apply the suggested solution.

## Models and lift {#models-and-lift}

+++ My [!UICONTROL Automated Personalization] activity is taking too long to build models

Several activity setup choices affect the time that models need to build, including the number of experiences in your **[!UICONTROL Automated Personalization]** activity, the traffic to your site, and your selected success metric.

**Solution:** Review your activity setup and check whether you can make changes that improve the speed at which models build.

* If your success metric is set to RPV, can you change to conversion? Conversion activities tend to require less traffic to build models. You do not lose activity data if you change the success metric from RPV to conversion.
* Is your success metric far down the sales funnel from your activity experiences? A lower activity conversion rate increases the traffic requirements for models to build, as a minimum number of conversions is required.
* Are there some offers or experiences that you can exclude from your activity? Decreasing the number of experiences in an activity speeds up the time to build models.
* Is there a higher-traffic page where this activity would be more successful? The more traffic and conversions in your activity locations, the quicker models build.

+++

+++ My [!UICONTROL Automated Personalization] activity did not generate lift

Several factors are required for an **[!UICONTROL Automated Personalization]** activity to generate lift:

* The offers must be different enough to influence visitors.
* The offers must be located somewhere that makes a difference to the optimization goal.
* There must be enough traffic and statistical "power" in the test to detect the lift.
* The personalization algorithm must work well.

**Solution:** The best course of action is to first make sure that the content and locations that make up the activity experiences truly make a difference to the overall response rates, by using a simple, non-personalized A/B test. Compute the sample sizes ahead of time to ensure that there is enough power to see a reasonable lift, then run the A/B test for a fixed duration without stopping it or making any changes. If the A/B test results show statistically significant lift on one or more of the experiences, a personalized activity is likely to be successful. Personalization can work even if there are no differences in the overall response rates of the experiences. Typically, the issue stems from the offers or locations not having a large enough impact on the optimization goal to be detected with statistical significance.

+++

## Activity setup and reporting {#setup-and-reporting}

+++ My [!UICONTROL Automated Personalization] activity URL is showing offer content on incorrect pages

**Cause:** In **[!UICONTROL Automated Personalization]**, the URL and template testing rules are added to the [!DNL Target] request entry constraint (for example, target-global-mbox), where they are evaluated only once. After a visitor qualifies for an activity, the [!DNL Target] request-level targeting rules are not reevaluated, whereas the targeting audience is added to the location targeting rules.

**Solution:** Add the necessary template rules as the input audience of the activity. Audience evaluation happens upon each request (call).

+++

+++ Any metric dependent on a conversion metric never converts

This behavior is expected.

In an **[!UICONTROL Automated Personalization]** activity, once a conversion metric (whether an optimization goal or a post goal) is converted, the visitor is released from the experience, and the activity is restarted.

For example, an activity has a conversion metric (C1) and an additional metric (A1) that depends on C1. When a visitor enters the activity for the first time, and has converted neither C1 nor A1, A1 is not converted due to the success metric dependency. If the visitor converts C1 and then converts A1, A1 is still not converted, as the visitor is released when C1 is converted.

+++

+++ My Experience URLs are not working as expected

**Solution:** Use the following actions:

* If you are not able to see the preview in the new tab (due to the browser cache), try refreshing two or three times. You can also copy the link and open it in a new browser or a new session.
* If you changed any content, regenerate the Experience URL links and share the new links with your teammates.

+++
