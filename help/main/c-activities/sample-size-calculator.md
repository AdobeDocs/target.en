---
keywords: sample size calculator;A/B;Auto Allocate;statistical significance;traffic volume
description: Use the Adobe Target Sample Size Calculator to estimate experiment duration, traffic volume, or minimum detectable effect.
title: Sample Size Calculator
feature: Activities
---
# Sample Size Calculator

>[!CONTEXTUALHELP]
>id="target_sample_size_ab_daily_traffic"
>title="Daily traffic"
>abstract="How many users enter the experiment each day. If you do not know this value, choose Traffic volume above, and the calculator will solve for it using the other inputs."

>[!CONTEXTUALHELP]
>id="target_sample_size_confidence_level"
>title="Confidence level"
>abstract="How certain you need to be that a result is not due to random chance before calling it significant. A 95% confidence level means there is at most a 5% chance of a false positive. Higher values reduce false positives, but they also require more data."

>[!CONTEXTUALHELP]
>id="target_sample_size_statistical_power"
>title="Statistical power"
>abstract="The probability of detecting a real effect if one exists. An 80% power level means there is an 80% chance of detecting a true effect. Higher power reduces false negatives, but it requires more traffic or a longer runtime."

>[!CONTEXTUALHELP]
>id="target_sample_size_setup_cja"
>title="Set up the test"
>abstract="These fields define the experiment, the expected outcome, and the confidence threshold for the result. The field tied to the value you selected above is solved automatically; complete the remaining fields with your expected values."


>[!AVAILABILITY]
>
>The Sample Size Calculator is available as a beta feature

The **[!UICONTROL Sample Size Calculator]** allows you to estimate the inputs needed to plan an experiment before you launch it. The calculator helps you determine how much traffic you need, how long the test should run, how many experiences to include, or what minimum effect you can reliably detect based on the values you provide.

To access the **[!UICONTROL Sample Size Calculator]**, go to the **[!UICONTROL Activities]** menu.

![](assets/calculator_menu.png)

## A/B (Target reporting)

>[!CONTEXTUALHELP]
>id="target_sample_size_bonferroni"
>title="Bonferroni correction"
>abstract="Adjusts the confidence level to account for comparing more than one offer against the control at the same time. This matters only when the number of offers is greater than two. It matches the same correction used in Adobe's public Target Calculator tool."

>[!CONTEXTUALHELP]
>id="target_sample_size_metric_type"
>title="Metric type"
>abstract="What kind of metric you are measuring. Use Percentage for binary outcomes, such as clicks or conversions, where each user either does or does not complete the action. Use Number for metrics like revenue or page views, where the values can vary widely from user to user."

>[!CONTEXTUALHELP]
>id="target_sample_size_number_offers"
>title="Number of offers"
>abstract="The number of experiences in the experiment, including the control. More than two offers automatically applies a Bonferroni correction (when enabled) to keep the overall confidence level accurate across all comparisons."

>[!CONTEXTUALHELP]
>id="target_sample_size_lift"
>title="Lift"
>abstract="The relative improvement over baseline that you want to detect. Enter it as a percentage of the baseline. For example, a 5% lift on an 11.8% baseline conversion rate targets 12.39%."

>[!CONTEXTUALHELP]
>id="target_sample_size_baseline_conversion_rate"
>title="Baseline conversion rate"
>abstract="Your current conversion rate before the experiment starts, which is the control arm average. This value is always required. For percentage metrics, enter a percentage such as 5 for 5%. For count metrics, enter the raw decimal value."

Estimate the inputs required to plan and run an A/B test. These values help you decide how much traffic you need, how long the test should run, and what effect size you can realistically detect.

1. Access the **[!UICONTROL A/B (Target Reporting)]** tab to calculate planning inputs for an A/B test.

1. Enable the **[!UICONTROL Apply correction]** option to adjust your confidence level to account for comparing more than one offer against the control at the same time.

1. Choose your **[!UICONTROL Metric type]**:

    * Conversion rate: use this for binary outcomes like clicks or purchases, where each visitor either does or does not complete the action.
    * Revenue per visitor: use this for revenue-style metrics, where values can vary widely from visitor to visitor.

        ![](assets/calculator-target_reporting_1.png)

1. Specify the **[!UICONTROL Daily traffic]**, the number of users entering the experiment each day.

1. Under **[!UICONTROL Set up the test]**, enter the remaining values:

    * **[!UICONTROL Number of offers]**: The number of experiences in your experiment, including the control. More than two offers applies a Bonferroni correction, when enabled, to maintain the overall confidence level.

    * **[!UICONTROL Lift]**: The relative improvement over baseline that you want to detect. Enter it as a percentage of the baseline, for example, a 5% lift on an 11.8% baseline conversion rate targets 12.39%.

        ![](assets/calculator-target_reporting_2.png)

1. Specify the **[!UICONTROL Baseline conversion rate]** for your current experience before the experiment starts.

1. You can expand **[!UICONTROL Advanced statistical settings]** to provide additional statistical inputs when they are available for the selected calculation.

    * **[!UICONTROL Confidence level]**: The likelihood that a result is not due to chance. A 95% level allows a 5% chance of a false positive.

    * **[!UICONTROL Statistical power]**: The likelihood of detecting a real effect. An 80% power reduces false negatives but requires more traffic or time.

1. Select **[!UICONTROL Run calculation]** to generate the estimate. Select **[!UICONTROL Reset]** to clear the current inputs and start again.

The **[!UICONTROL Result]** panel displays the estimate after you complete the required fields and run the calculation. If required fields are incomplete, the panel prompts you to enter the missing values.

![](assets/calculator-cja-analytics-3.png)

The calculator provides an estimate for planning an experiment. Use the result together with your experiment design, expected traffic, baseline performance, and statistical requirements when deciding how long to run the activity.

## A/B (CJA/Adobe Analytics)

>[!CONTEXTUALHELP]
>id="target_sample_size_number_experiences"
>title="Number of experiences"
>abstract="Number of variants in your experiment, including the control. An A/B test has 2 arms. Five variants plus a control equals 6. More arms require proportionally more traffic to maintain statistical power."

>[!CONTEXTUALHELP]
>id="target_sample_size_duration"
>title="Duration of A/B test"
>abstract="How many days your experiment will run. Longer durations give your experiment more time to collect data, letting you reliably detect smaller effects. Shorter durations need larger effects or more daily traffic to reach a reliable result."

>[!CONTEXTUALHELP]
>id="target_sample_size_expected_improvement"
>title="Expected improvement"
>abstract="The smallest improvement worth detecting, the minimum change in your metric that you would act on. This is the size of the lift in percentage points, not the percent change relative to your baseline. For example, if your baseline is 5% and a 1 percentage point lift matters, enter 1."

>[!CONTEXTUALHELP]
>id="target_sample_size_variance"
>title="Variance"
>abstract="How spread out the values of your metric are, not the average value. A metric such as click rate (mostly 0s and 1s) typically has low variance, while a metric like revenue per user can have much higher variance. If you are unsure, leave the default value at 1."

Estimate the planning inputs for an A/B activity that relies on Adobe Analytics or Customer Journey Analytics data. It helps you define the experiment size, expected lift, and test duration before you launch the activity.

1. Access the **[!UICONTROL A/B (CJA/Adobe Analytics)]** tab to calculate planning inputs for an A/B test.

1. Under **[!UICONTROL What do you want to know?]**, select the value you want the calculator to determine:

    * **[!UICONTROL Duration]**: You have an experiment in mind and want to know how long it would take to run and whether it is worth running.
    * **[!UICONTROL Number of experiences]**: You have a location to run an experiment and want to figure out how many treatments your traffic could support.
    * **[!UICONTROL Traffic volume]**: You have an experiment in mind and want to know how many visitors you need to reach statistical significance.
    * **[!UICONTROL Minimum Detectable Effect]**: You have an experiment you want to run but want to know how much of a lift you need to reach statistical significance. This helps you assess whether the experiment is worth running or planning.

    The fields in the form change depending on the value you select. The calculator uses the other inputs to determine the selected result.

    ![](assets/calculator-cja-analytics-1.png)

1. Specify the **[!UICONTROL Daily traffic]**, the number of users entering the experiment each day.

1. Under **[!UICONTROL Set up the test]**, enter the remaining values:

    * **[!UICONTROL Number of experiences]**: The number of variants, including the control. More variants require more traffic.

    * **[!UICONTROL Duration of A/B test]**: The number of days the experiment runs. Longer tests can detect smaller effects.

    * **[!UICONTROL Expected improvement]**: The improvement you expect the experiment to produce.

    * **[!UICONTROL Variance]**: How spread out your metric values are. A click-through rate typically has low variance, revenue per user can be much higher. If you are unsure, leave the default value at 1.

        Learn how to calculate a **[!UICONTROL Variance]** in [Analytics documentation](https://experienceleague.adobe.com/en/docs/analytics/components/calculated-metrics/calcmetrics-reference/cm-functions#variance)

        ![](assets/calculator-cja-analytics-2.png)

1. You can expand **[!UICONTROL Advanced statistical settings]** to provide additional statistical inputs when they are available for the selected calculation.

    * **[!UICONTROL Confidence level]**: The likelihood that a result is not due to chance. A 95% level allows a 5% chance of a false positive. Lower confidence levels mean less traffic is needed, but they also increase the risk of a false positive.

    * **[!UICONTROL Statistical power]**: The likelihood of detecting a real effect. An 80% power reduces false negatives but requires more traffic or time.

1. Select **[!UICONTROL Run calculation]** to generate the estimate. Select **[!UICONTROL Reset]** to clear the current inputs and start again.

The **[!UICONTROL Result]** panel displays the estimate after you complete the required fields and run the calculation. If required fields are incomplete, the panel prompts you to enter the missing values.

![](assets/calculator-cja-analytics-4.png)

The calculator provides an estimate for planning an experiment. Use the result together with your experiment design, expected traffic, baseline performance, and statistical requirements when deciding how long to run the activity.
