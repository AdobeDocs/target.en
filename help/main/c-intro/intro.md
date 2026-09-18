---
keywords: Target Standard;Recommendations;Target Premium;Automated Personalization;auto-target;auto target;permissions;what is adobe target;
description: Learn the basics of Adobe [!DNL Target] Standard and Adobe [!DNL Target] Premium. [!DNL Target] Premium includes advanced features not available in standard product.
landing-page-description: Personalize your customers' experience to maximize revenue on your web and mobile sites, apps, social media, and other digital channels.
short-description: Personalize your customers' experience to maximize revenue on your web and mobile sites, apps, social media, and other digital channels.
title: What is Target?
feature: Overview
exl-id: 0e729c71-618b-4ab8-93a3-d37e73ec2740
TQID: https://experienceleague.adobe.com/Mr8fwY1FNfJShSezC50YX1QeBagmuovUySsQUO8jPqo
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
---
# Introduction to [!DNL Target]


>[!CONTEXTUALHELP]
>id="target_sample_size_ab_daily_traffic"
>title="Daily traffic"
>abstract="How many users enter your experiment each day. If you do not know your daily traffic, choose \"Traffic volume\" above and the calculator will solve for it using your other inputs."

>[!CONTEXTUALHELP]
>id="target_sample_size_setup"
>title="Set up the test"
>abstract="These fields define your A/B test, what you expect to see and how confident you need to be in the result. The field tied to what you selected above will be solved for automatically. Fill in the rest with your expected values."

>[!CONTEXTUALHELP]
>id="target_sample_size_number_experiences"
>title="Number of experiences"
>abstract="Number of variants in your experiment, including the control. An A/B test has 2 arms. Five variants plus a control equals 6. More arms require proportionally more traffic to maintain statistical power."

>[!CONTEXTUALHELP]
>id="target_sample_size_duration"
>title="Duration of A/B test"
>abstract="How many days your experiment will run. Longer durations give your experiment more time to collect data, letting you reliably detect smaller effects. Shorter durations need larger effects or more daily traffic to reach a reliable result."

>[!CONTEXTUALHELP]
>id="target_sample_size_minimum_detectable_effect"
>title="Minimum Detectable Effect"
>abstract="The smallest improvement worth detecting, the minimum change in your metric that you would act on. This is the size of the lift in percentage points, not the percent change relative to your baseline. For example, if your baseline is 5% and a 1 percentage point lift matters, enter 1."

>[!CONTEXTUALHELP]
>id="target_sample_size_expected_improvement"
>title="Expected improvement"
>abstract="The improvement you expect the experiment to produce."

>[!CONTEXTUALHELP]
>id="target_sample_size_variance"
>title="Variance"
>abstract="How spread out your metric's values are, not its average. A metric like a click rate (mostly 0s and 1s) has low variance, a metric like revenue per user (a few high spenders, many low) can have much higher variance. If you are unsure, leave the default value of 1."

>[!CONTEXTUALHELP]
>id="target_sample_size_confidence_level"
>title="Confidence level"
>abstract="How confident you need to be that a result is not just random chance before calling it real, the threshold for statistical significance. A 95% confidence level means there is at most a 5% chance of a false positive. Higher values reduce false positives but require more data."

>[!CONTEXTUALHELP]
>id="target_sample_size_statistical_power"
>title="Statistical power"
>abstract="The probability of detecting an effect if one truly exists, the sensitivity of the experiment. 80% power means there is an 80% chance of detecting a real effect. Higher power reduces false negatives but requires more traffic or a longer runtime."

>[!CONTEXTUALHELP]
>id="target_sample_size_traffic_mode"
>title="Traffic mode"
>abstract="How users enter your experiment. Continuous: users enter daily over the experiment duration. Traffic automatically shifts toward better performing variants as results come in."

>[!CONTEXTUALHELP]
>id="target_sample_size_metric_type"
>title="Metric type"
>abstract="What kind of metric you are measuring. Percentage: use this for binary outcomes like clicks or conversions, where each user either does or does not do something. Number: use this for metrics like revenue or page views, where the value can vary widely from user to user."

>[!CONTEXTUALHELP]
>id="target_sample_size_auto_daily_traffic"
>title="Daily traffic"
>abstract="How many users enter your experiment each day. Used for continuous experiments that run over multiple days, with traffic automatically shifting toward better performing variants as results come in."

>[!CONTEXTUALHELP]
>id="target_sample_size_baseline_metric_rate"
>title="Baseline metric rate"
>abstract="Your current performance before the experiment starts, the control arm average. Always required. For percentage metrics, enter as a percentage: if 5% of visitors click Buy today, enter 5. For count metrics, enter the raw decimal value."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="Primary metric"
>abstract="The primary metric is automatically pulled from the reporting settings. To make changes, modify the goal metric under Goals & Settings."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="Hypothesis"
>abstract="The hypothesis is a statement you define that explains the expected outcome of the experiment. Include a description of what is being changed and where, then state which metric you expect to change and how."

>[!CONTEXTUALHELP]
>id="target_ai_insights_insights"
>title="Insights"
>abstract="Experiment insights are the learnings found by AI when the experiment data has met statistical significance."

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="Opportunities"
>abstract="Experiment opportunities are AI suggested treatment ideas based on patterns AI found in your experiment screenshots and results."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="Treatment details"
>abstract="Treatment details show images of what a treatment looks like when a user qualifies for it. You can review these images for all experiments. Some experiments may ask you to confirm the image or replace it if needed."

[!DNL Adobe Target], part of the [!DNL Adobe Experience Cloud], offers comprehensive tools to personalize customer experiences across web, mobile sites, apps, social media, and other digital channels. 

[!DNL Target] helps maximize revenue and can be licensed as [!DNL Target Standard] or [!DNL Target Premium].

## [!UICONTROL Target Standard] {#section_ACD5EFF17AAB4E979CBEFA0145CCD905}

[!DNL Target Standard] is the front end to [!DNL Adobe Target], enabling visual creation and management of A/B tests and rules-based targeting activities. [!DNL Target] supports custom code insertion within and outside the [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) workflow. [!DNL Target Standard] offers a simplified implementation strategy for your digital properties, with a single line of code on each page managing all communication between your site and [!DNL Target].

Industry best practices are integrated into [!DNL Target Standard], making it suitable for both new and experienced users. You can easily share data, results, and collaborate with team members using the [!DNL Adobe Experience Cloud].

## [!DNL Target Premium] {#premium}

[!BADGE Premium]{type=Positive}

[!DNL Target Premium] is an advanced offering that requires a license to add premium features to [!DNL Target Standard]. All [!DNL Target Premium] articles in [!DNL Target] guides include the [!UICONTROL Premium] badge at the top of each page or inline near the affected text. The [!UICONTROL Premium] badge is clickable and links to this section.

**[!DNL Target Premium] includes the following features:**

### [!UICONTROL Automated Personalization]

[[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) (AP) uses advanced machine learning algorithms to deliver personalized experiences and improve conversion rates for digital interactions.

AP records visitor activity, building profiles to target content to similar visitors. AP tracks responses to content for individuals and the population, using sophisticated modeling to automatically target each visitor based on everything known about them.

AP is fully automated, continuously learning with minimal human analysis. It builds models to determine which products a visitor is likely to be interested in, collecting and storing information in visitor profiles. Multiple algorithms ensure the best model for your system.

### [!UICONTROL Auto-Target]

[Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) uses advanced machine learning to identify high-performing marketer-defined experiences. It then delivers the most tailored experience to each visitor based on individual customer profiles and the behavior of previous visitors with similar profiles. [!UICONTROL Auto-Target] helps personalize content and drive conversions.

### Recommendations 

[Recommendations](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) activities automatically display products or content that might interest your customers based on previous user activity. [!UICONTROL Recommendations] help direct customers to relevant items they might otherwise not know about.

A recommendation determines how a product is suggested to a customer, depending on that customer's activities on the site. For example:

* Encourage people who purchase a backpack to consider buying hiking shoes and trekking poles.

  Create a recommendation that shows items that are often purchased together, using the "People who bought this also bought that" criteria.

* Increase the time visitors spend on your media site by recommending similar video content to what they are currently watching.

  Create a recommendation that suggests other videos, using the "People who viewed this viewed that" criteria.

* Suggest that customers who viewed information about savings plans at your bank also read about IRA accounts.

  Show other products people purchased after viewing one product without showing the first product in the recommendations, using the "people who viewed this also bought" criteria.

### Recommendations as an offer

[Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md) lets you include recommendations inside [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Experience Targeting] (XT) activities. 

This functionality opens up entirely new capabilities, such as:

* Test and target recommendations and non-recommendations content within the same activity.
* Easily experiment with placement of recommendations on the page, including the order of multiple recommendations.
* Automatically push traffic to the best-performing recommendations experience using [!UICONTROL Auto-Allocate].
* Dynamically assign visitors to tailored recommendations experiences based on individual profiles using [!UICONTROL Auto-Target].

### Enterprise User Permissions

[Enterprise User Permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838) functionality lets you create different projects (called "Product Profiles" in the [!DNL Adobe Admin Console for Enterprise]). [!UICONTROL Enterprise User Permissions] let you assign different permissions for a single user that dictate that user's access rights for each project. These distinct projects can be compared to the way that report suites work in [!DNL Adobe Analytics]. Each project can have specific users with specific roles that apply to a set of properties. The result is that customers are able to restrict the view, edit, approval, and publish access to their users. You can restrict users based on region, environment (dev/stage/prod), channel, or other custom criteria.

## Beta features {#beta}

[!BADGE Beta]{type=Informative}

The [!DNL Adobe Target] team often enables new features for select customers for testing and feedback purposes. After the testing period completes, these features are enabled for all customers in future [!DNL Target Standard/Premium] releases and announced in release notes.

Articles in [!DNL Target] guides describing Beta features include the Beta badge at the top of each page or inline near the affected text. The Beta badge is clickable and includes a link to this section.

## Recommendations Classic {#section_9554068100054D2DBDB298CBE5A0E413}

>[!IMPORTANT]
>
>[!DNL Recommendations Classic] is a legacy product and is no longer licensed to new customers. For the best [!DNL Recommendations] experience, upgrade to [!DNL Recommendations] activities available in [!DNL Adobe Target Premium], described above.

[!DNL Recommendations Classic] automatically displays products or content that might interest your customers based on previous user activity on your website. Recommendations help direct customers to items they might otherwise not know about, improving sales generated on your website.

For more information, see the [Recommendations Classic documentation](/help/main/assets/adobe-recommendations-classic.pdf).

## Experience League: The Adobe [!DNL Target] Welcome Kit {#kit}

Build your optimization and personalization program on [!DNL Adobe Target] with this Welcome Kit. The Welcome Kit includes key information, tools, and resources to help you prepare for and launch your first [!DNL Target] activity. The kit includes ideas for short-term quick wins and long-term optimization strategies.

[The Adobe Target Welcome Kit](/help/main/c-intro/target-welcome-kit.md)

## Training video: Activity Types (9:03) ![Overview badge](/help/main/assets/overview.png) 

The following video explains the activity types available in [!DNL Target Standard/Premium] and how the [!DNL Target] three-step guided workflow can help you achieve your site goals.

* Describe the types of activities included in [!DNL Adobe Target] 
* Select the appropriate activity type to achieve your goals 
* Describe the three-step guided workflow that applies to all activity types

>[!VIDEO](https://video.tv.adobe.com/v/17386)


