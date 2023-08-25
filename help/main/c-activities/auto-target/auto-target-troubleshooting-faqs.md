---
keywords: auto-target;targeting;traffic allocation;frequently asked questions;faq;troubleshooting;trouble shooting;traffic
description: Explore troubleshooting topics and Frequently Asked Questions about [!UICONTROL Auto-Target] activities.
title: How Can I Troubleshoot [!UICONTROL Auto-Target] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
---
# [!UICONTROL Auto-Target] FAQs and troubleshooting

Troubleshooting and Frequently Asked Questions (FAQs) about [!UICONTROL Auto-Target] activities in [!DNL Adobe Target].

## [!UICONTROL Auto-Target] Frequently Asked Questions {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Consult the following FAQs and answers as you work with [!UICONTROL Auto-Target] activities:

### What are best practices to set up an [!UICONTROL Auto-Target] activity?

+++Answer
* Decide if the business value of a [!UICONTROL Revenue per Visit] (RPV) success metric is worth the additional traffic requirements. RPV typically needs at least 1,000 conversions per experience for an activity to work versus conversion.
* Decide on the allocation between control and personalized experiences before beginning the activity based on your goals.
* Determine if you have sufficient traffic to the page where your [!UICONTROL Auto-Target] activity runs for personalization models to build in a reasonable amount of time.
* If you are testing the personalization algorithm, you shouldn't change experiences or add or remove profile attributes while the activity is live.
* Consider completing an A/B activity between the offers and locations that you are planning to use in your [!UICONTROL Auto-Target] activity to ensure the locations and offers have an impact on the optimization goal. If an A/B activity fails to demonstrate a significant difference, [!UICONTROL Auto-Target] likely also fails to generate lift.

  If an A/B test shows no statistically significant differences between experiences, it is likely the offers you are considering are not sufficiently different from each other, the locations you selected do not impact the success metric, or the optimization goal is too far in the conversion funnel to be affected by your chosen offers.

* Try not to make substantial changes to the experiences during the activity.

+++

### Does [!UICONTROL Adobe] that you recommend using [!UICONTROL Auto Target] with a 90(Control)/10(Targeted) split until the models are built?

+++Answer 
Your optimal traffic allocation split depends on what you want to accomplish.

If your goal is to personalize as much traffic as possible, you can stick with 90% targeted allocation and 10% control for the lifetime of the activity. If your goal is to run an experiment comparing how personalized algorithms do versus the control, then a 50/50 split is best for the lifetime of the activity.

Best practice is to maintain the traffic-allocation split for the lifetime of the activity so that visitors don't switch between targeted and control experiences.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### If a visitor does **not** see the [!UICONTROL Auto-Target] activity and converts, does the conversion count in my activity?

+++Answer
No, only visitors who qualify for and view the [!UICONTROL Auto-Target] activity are counted in reporting.

+++

### Why doesn't my [!UICONTROL Auto-Target] activity seem to be generating any lift.

+++Answer
There are four factors required for an [!UICONTROL Auto-Target] activity to generate lift:

* The offers must be different enough to influence visitors.
* The offers must be located somewhere that makes a difference to the optimization goal.
* There must be enough traffic and statistical "power" in the test to detect the lift.
* The personalization algorithm must work well.

The best course of action is to first make sure the content and locations that make up the activity experiences truly make a difference to the overall response rates using a simple, non-personalized A/B test. Be sure to compute the sample sizes ahead of time to ensure there is enough power to see a reasonable lift and run the A/B test for a fixed duration without stopping it or making any changes.

If an A/B test's results show statistically significant lift on one or more of the experiences, then it is likely that a personalized activity will work. Of course, personalization can work even if there are no differences in the overall response rates of the experiences. Typically, the issue stems from the offers and locations not having a large enough impact on the optimization goal to be detected with statistical significance.

+++

### When should I stop my [!UICONTROL Auto-Target] activity?

+++Answer
[!UICONTROL Auto-Target] can be used as "always on" personalization that constantly optimizes. Especially for evergreen content, there is no need to stop your [!UICONTROL Auto-Target] activity.

If you want to make substantial changes to the content in your [!UICONTROL Auto-Target] activity, the best practice is to start a new activity so that other users reviewing reports do not confuse or relate past results with different content.

+++

### How long should I wait for models to build? {#how-long}

+++Answer
The time it takes for models to build in your [!UICONTROL Auto-Target] activity typically depends on the traffic to your selected activity locations and conversion rates associated with your activity success metric.

[!UICONTROL Auto-Target] does not attempt to build a personalized model for a given experience until there are least 50 conversions for that experience. Furthermore, if the model built is of insufficient quality (as determined by offline evaluation on hold-out "test" data, using [a metric known as AUC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), the model is not used to serve traffic in a personalized manner.

Some further points to keep in mind about [!UICONTROL Auto-Target]'s model building:

* After an activity is live, [!UICONTROL Auto-Target] considers up to the last 45 days of randomly served data when attempting to build models. For example, control traffic, plus some extra randomly served data held out by the algorithm.
* When [!UICONTROL Revenue per Visit] is your success metric, these activities typically require more data to build models due to the higher data variance that typically exists in visit-revenue compared to conversion rate.
* Because models are built on a per-experience basis, replacing one experience with another experience means that sufficient traffic (at least 50 conversions) must be collected for the new experience before personalized models can be rebuilt.

+++

### One model is built in my activity. Are the visits to that experience personalized?

+++Answer
No, there must be at least two models built within your activity for personalization to begin.

+++

### When can I start looking at the results of my [!UICONTROL Auto-Target] activity?

+++Answer
You can begin looking at the results of your [!UICONTROL Auto-Target] test after you have at least two experiences with models built (green checkmark) for the experience that has models built.

+++

### Can I specify a specific experience to be used as control?

+++Answer
You can select an experience to be used as control while creating an [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activity.

This feature lets you route the entire control traffic to a specific experience, based on the traffic-allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against control traffic to that one experience.

For more information, see [Use a specific experience as control](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Can I change the goal metric midway through an [!UICONTROL Auto-Target] activity? {#change-metric}

+++Answer
Adobe does not recommend that you change the goal metric midway through an activity. Although it is possible to change the goal metric during an activity using the [!DNL Target] UI, you should always start a new activity. Adobe does not warranty what happens if you change the goal metric in an activity after it is running. 

This recommendation applies to [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Automated Personalization] activities that use either [!DNL Target] or [!DNL Analytics] (A4T) as the reporting source.

+++

### Can I use the [!UICONTROL Reset Report Data] option while running an [!UICONTROL Auto-Target] activity?

+++Answer
Using the [!UICONTROL Reset Report Data] option for [!UICONTROL Auto-Target] activities is not suggested. Although it removes the visible reporting data, this option does not remove all training records from the [!UICONTROL Auto-Target] model. Instead of using the [!UICONTROL Reset Report Data] option for [!UICONTROL Auto-Target] activities, create a new activity and de-activate the original activity. 

This guidance also applies to [!UICONTROL Auto-Allocate] and [!UICONTROL Automated Personalization] activities.

+++

### What happens if I remove a single experience from an [!UICONTROL Auto-Target] activity?

+++Answer
[!DNL Target] builds one model per experience, so removing one experience means [!DNL Target] builds one fewer model and does not affect models for the other experiences.

For example, suppose you have an [!UICONTROL Auto-Target] activity with eight experiences and you don't like the performance of one experience. You can remove that experience and it doesn't affect the models for the seven remaining experiences.

+++

## Troubleshooting [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Sometimes activities don't go as expected. Here are some potential challenges that you might face while using [!UICONTROL Auto-Target] and some suggested solutions.

### My [!UICONTROL Auto-Target] activity is taking too long to build models.

+++Troubleshooting suggestions
There are several activity setup changes that can decrease the expected time to build models, including the number of experiences in your [!UICONTROL Auto-Target] activity, the traffic to your site, and your selected success metric.

**Solution:** Review your activity setup and see if there are any changes you are willing to make to improve the speed at which models build.

* If your success metric is set to [!UICONTROL RPV], can you change to conversion? Conversion activities tend to require less traffic to build models. You will not lose activity data if you change the success metric from RPV to conversion.
* Is your success metric far down the sales funnel from your activity experiences? A lower activity conversion rate increases the traffic requirements needed for models to build, because a minimum number of conversions are required.
* Are there some experiences you can drop from your activity? Decreasing the number of experiences in an activity lessens the time to build models.
* Is there a higher-traffic page on which this activity would be more successful? The more traffic and conversions in your activity locations, the quicker models build.

+++

### My [!UICONTROL Auto-Target] activity isn't generating any lift.

+++Troubleshooting suggestions
There are four factors required for an [!UICONTROL Auto-Target] activity to generate lift:

* The offers must be different enough to influence visitors.
* The offers must be located somewhere that makes a difference to the optimization goal.
* There must be enough traffic and statistical "power" in the test to detect the lift.
* The personalization algorithm must work well.

**Solution:** First, make sure that your activity is personalizing traffic. If models aren't built for all of the experiences, your [!UICONTROL Auto-Target] activity is still randomly serving a significant portion of visits to attempt to build all models as quickly as possible. If models aren't built, [!UICONTROL Auto-Target] is not personalizing traffic.

Next, make sure that the offers and the activity locations truly make a difference to the overall response rates using a simple, non-personalized A/B test. Be sure to compute the sample sizes ahead of time to ensure there is enough power to see a reasonable lift and run the A/B test for a fixed duration without stopping it or making any changes. If an A/B test results show statistically significant lift on one or more of the experiences, then it is likely that a personalized activity works. Personalization can work even if there are no differences in the overall response rates of the experiences. Typically, the issue stems from the offers and locations not having a large enough impact on the optimization goal to be detected with statistical significance.

+++

### Any metric dependent on a conversion metric never converts.

+++Troubleshooting suggestions
This is expected.

In an [!UICONTROL Auto-Target] activity, once a conversion metric (whether optimization goal or post goal) is converted, the user is released from the experience, and the activity is restarted.

For example, there is an activity with a conversion metric (C1) and an additional metric (A1). A1 depends on C1. When a visitor enters the activity for the first time, and the criteria for converting A1 and C1 are not converted, metric A1 is not converted due to the success metric dependency. If the visitor converts C1 and then converts A1, A1 is still not converted because when C1 is converted, the visitor is released.

+++
