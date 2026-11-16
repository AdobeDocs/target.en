---
keywords: auto-target;targeting;traffic allocation;frequently asked questions;faq;troubleshooting;trouble shooting;traffic
description: Explore troubleshooting topics and Frequently Asked Questions about [!UICONTROL Auto-Target] activities.
title: How Can I Troubleshoot [!UICONTROL Auto-Target] Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
TQID: 'https://experienceleague.adobe.com/LXOa1Ma0y8VbncCPN1Az33p-GDsd-bW-BDqJjSGbVQU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# [!UICONTROL Auto-Target] FAQs and troubleshooting {#auto-target-faqs}

>[!BEGINSHADEBOX]

**On this page:** Find answers to frequently asked questions about **[!UICONTROL Auto-Target]** activities and suggested solutions to common problems.

>[!ENDSHADEBOX]

This page answers frequently asked questions (FAQs) and describes troubleshooting steps for **[!UICONTROL Auto-Target]** activities in [!DNL Adobe Target].

## Frequently asked questions {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Consult the following questions and answers when you work with **[!UICONTROL Auto-Target]** activities.

+++ What are the best practices to set up an [!UICONTROL Auto-Target] activity?

* Decide whether the business value of a **[!UICONTROL Revenue per Visit]** (RPV) success metric is worth the additional traffic requirements. RPV typically needs at least 1,000 conversions per experience for an activity to work, compared to conversion.
* Decide on the allocation between control and personalized experiences before you begin the activity, based on your goals.
* Determine whether you have sufficient traffic to the page where your **[!UICONTROL Auto-Target]** activity runs for the personalization models to build in a reasonable amount of time.
* If you are testing the personalization algorithm, do not change experiences or add or remove profile attributes while the activity is live.
* Consider completing an A/B activity between the offers and locations that you plan to use in your **[!UICONTROL Auto-Target]** activity, to ensure that the locations and offers have an impact on the optimization goal. If an A/B activity fails to demonstrate a significant difference, **[!UICONTROL Auto-Target]** likely also fails to generate lift.

  If an A/B test shows no statistically significant differences between experiences, it is likely that the offers you are considering are not sufficiently different from each other, the locations you selected do not impact the success metric, or the optimization goal is too far in the conversion funnel to be affected by your chosen offers.

* Do not make substantial changes to the experiences during the activity.

+++

+++ Does Adobe recommend using Auto-Target with a 90 (control) / 10 (targeted) split until the models are built?

The optimal traffic allocation split depends on what you want to accomplish.

If your goal is to personalize as much traffic as possible, you can stay with 90% targeted allocation and 10% control for the lifetime of the activity. If your goal is to run an experiment that compares how the personalization algorithms do versus the control, a 50/50 split is best for the lifetime of the activity.

Best practice is to maintain the traffic-allocation split for the lifetime of the activity, so that visitors do not switch between targeted and control experiences.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There is no way to go back and see when a model was completed.
-->

+++

+++ If a visitor does not see the [!UICONTROL Auto-Target] activity and converts, does the conversion count in my activity?

No. Only visitors who qualify for and view the **[!UICONTROL Auto-Target]** activity are counted in reporting.

+++

+++ Why is my [!UICONTROL Auto-Target] activity not generating any lift?

For the four factors required to generate lift and the suggested solution, see the troubleshooting item [My Auto-Target activity is not generating any lift](#section_23995AB813F24525AF294D20A20875C8).

+++

+++ When should I stop my [!UICONTROL Auto-Target] activity?

**[!UICONTROL Auto-Target]** can be used as "always on" personalization that constantly optimizes. Especially for evergreen content, there is no need to stop your **[!UICONTROL Auto-Target]** activity.

If you want to make substantial changes to the content in your **[!UICONTROL Auto-Target]** activity, the best practice is to start a new activity, so that other users who review reports do not confuse or relate past results with different content.

+++

+++ How long should I wait for models to build?

The time it takes for the models to build in your **[!UICONTROL Auto-Target]** activity typically depends on the traffic to your selected activity locations and the conversion rates associated with your activity success metric.

**[!UICONTROL Auto-Target]** does not attempt to build a personalized model for a given experience until there are at least 50 conversions for that experience. Furthermore, if the model built is of insufficient quality (as determined by offline evaluation on hold-out "test" data, using [a metric known as AUC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), the model is not used to serve traffic in a personalized manner.

Keep the following points in mind about model building in **[!UICONTROL Auto-Target]**:

* After an activity is live, **[!UICONTROL Auto-Target]** considers up to the last 45 days of randomly served data when it attempts to build models. For example, control traffic, plus some extra randomly served data held out by the algorithm.
* When **[!UICONTROL Revenue per Visit]** is your success metric, these activities typically require more data to build models, because the variance in visit revenue is typically higher than in conversion rate.
* Because models are built on a per-experience basis, replacing one experience with another means that sufficient traffic (at least 50 conversions) must be collected for the new experience before the personalized models can be rebuilt.

If your models take too long to build, see [My Auto-Target activity is taking too long to build models](#section_23995AB813F24525AF294D20A20875C8).

+++

+++ One model is built in my activity. Are the visits to that experience personalized?

No. There must be at least two models built within your activity for personalization to begin.

+++

+++ When can I start looking at the results of my [!UICONTROL Auto-Target] activity?

You can begin looking at the results of your **[!UICONTROL Auto-Target]** activity after at least two experiences have models built (green checkmark).

+++

+++ Can I specify a specific experience to be used as control?

You can select an experience to be used as control while you create an [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activity.

This feature lets you route the entire control traffic to a specific experience, based on the traffic-allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against the control traffic to that one experience.

For more information, see [Use a specific experience as control](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

+++ Can I change the goal metric midway through an [!UICONTROL Auto-Target] activity?

Adobe does not recommend that you change the goal metric midway through an activity. Although it is possible to change the goal metric during an activity using the [!DNL Target] UI, you should always start a new activity. Adobe does not guarantee what happens if you change the goal metric in an activity after it is running.

This recommendation applies to **[!UICONTROL Auto-Allocate]**, **[!UICONTROL Auto-Target]**, and **[!UICONTROL Automated Personalization]** activities that use either [!DNL Target] or [!DNL Analytics] (A4T) as the reporting source.

+++

+++ Can I use the [!UICONTROL Reset Report Data] option while running an [!UICONTROL Auto-Target] activity?

Using the **[!UICONTROL Reset Report Data]** option for **[!UICONTROL Auto-Target]** activities is not recommended. Although it removes the visible reporting data, this option does not remove all training records from the **[!UICONTROL Auto-Target]** model. Instead of using the **[!UICONTROL Reset Report Data]** option, create a new activity and deactivate the original activity.

This guidance also applies to **[!UICONTROL Auto-Allocate]** and **[!UICONTROL Automated Personalization]** activities.

+++

+++ What happens if I remove a single experience from an [!UICONTROL Auto-Target] activity?

[!DNL Target] builds one model per experience, so removing one experience means that [!DNL Target] builds one fewer model and does not affect the models for the other experiences.

For example, suppose you have an **[!UICONTROL Auto-Target]** activity with eight experiences and you do not like the performance of one experience. You can remove that experience, and it does not affect the models for the seven remaining experiences.

+++

## Troubleshooting [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Sometimes activities do not go as expected. The following items describe potential challenges that you might face while you use **[!UICONTROL Auto-Target]**, with suggested solutions.

+++ My [!UICONTROL Auto-Target] activity is taking too long to build models.

Several activity setup changes can decrease the expected time to build models, including the number of experiences in your **[!UICONTROL Auto-Target]** activity, the traffic to your site, and your selected success metric.

**Solution:** Review your activity setup and see whether there are any changes you are willing to make to improve the speed at which models build.

* If your success metric is set to **[!UICONTROL RPV]**, can you change to conversion? Conversion activities tend to require less traffic to build models. You do not lose activity data if you change the success metric from RPV to conversion.
* Is your success metric far down the sales funnel from your activity experiences? A lower activity conversion rate increases the traffic requirements for models to build, because a minimum number of conversions is required.
* Are there some experiences you can drop from your activity? Decreasing the number of experiences in an activity lessens the time to build models.
* Is there a higher-traffic page on which this activity would be more successful? The more traffic and conversions in your activity locations, the quicker the models build.

For more information about the time that models need, see [How long should I wait for models to build?](#section_5C120A2B11D14D9BAF767BBAB50FED23).

+++

+++ My [!UICONTROL Auto-Target] activity is not generating any lift.

Four factors are required for an **[!UICONTROL Auto-Target]** activity to generate lift:

* The offers must be different enough to influence visitors.
* The offers must be located somewhere that makes a difference to the optimization goal.
* There must be enough traffic and statistical "power" in the test to detect the lift.
* The personalization algorithm must work well.

**Solution:** First, make sure that your activity is personalizing traffic. If models are not built for all of the experiences, your **[!UICONTROL Auto-Target]** activity is still randomly serving a significant portion of visits to attempt to build all models as quickly as possible. If models are not built, **[!UICONTROL Auto-Target]** is not personalizing traffic.

Next, make sure that the offers and the activity locations truly make a difference to the overall response rates, using a simple, non-personalized A/B test. Compute the sample sizes ahead of time to ensure that there is enough power to see a reasonable lift, and run the A/B test for a fixed duration without stopping it or making any changes. If the A/B test results show statistically significant lift on one or more of the experiences, it is likely that a personalized activity works. Personalization can work even if there are no differences in the overall response rates of the experiences. Typically, the issue stems from the offers and locations not having a large enough impact on the optimization goal to be detected with statistical significance.

+++

+++ Any metric dependent on a conversion metric never converts.

This is expected.

In an **[!UICONTROL Auto-Target]** activity, once a conversion metric (whether optimization goal or post goal) is converted, the user is released from the experience, and the activity is restarted.

For example, there is an activity with a conversion metric (C1) and an additional metric (A1). A1 depends on C1. When a visitor enters the activity for the first time, and the criteria for converting A1 and C1 are not met, metric A1 is not converted due to the success metric dependency. If the visitor converts C1 and then converts A1, A1 is still not converted, because when C1 is converted, the visitor is released.

+++
