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
>id="target_sample_size_expected_improvement"
>title="Expected improvement"
>abstract="The smallest improvement worth detecting, the minimum change in your metric that you would act on. This is the size of the lift in percentage points, not the percent change relative to your baseline. For example, if your baseline is 5% and a 1 percentage point lift matters, enter 1."

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
>id="target_sample_size_auto_daily_traffic"
>title="Daily traffic"
>abstract="How many users enter your experiment each day. Used for continuous experiments that run over multiple days, with traffic automatically shifting toward better-performing variants as results come in."

>[!AVAILABILITY]
>
>The Sample Size Calculator is available as a beta feature

Use the **[!UICONTROL Sample Size Calculator]** to estimate the inputs needed to plan an experiment. You can calculate the expected duration, number of experiences, traffic volume, or minimum detectable effect based on the values you provide.

The calculator is available as a standalone page in [!DNL Adobe Target]. To open it, select **[!UICONTROL Sample Size Calculator]** from the left navigation.

Select one of the following tabs:

* **[!UICONTROL A/B]**: Calculate planning inputs for an A/B test.
* **[!UICONTROL Auto Allocate]**: Calculate planning inputs for an Auto Allocate activity.

## For A/B activities

1. Access the **[!UICONTROL A/B]** tab to calculate planning inputs for an A/B test.

1. Under **[!UICONTROL What do you want to know?]**, select the value you want the calculator to determine:

    * **[!UICONTROL Duration]**
    * **[!UICONTROL Traffic volume (Audience size)]**
    * **[!UICONTROL Minimum Detectable Effect]**

    The fields in the form change depending on the value you select. The calculator uses the other inputs to determine the selected result.

1. Enter the values requested in the form. Depending on the experiment type and the calculation you selected, the form can include the following inputs:

    * **[!UICONTROL Daily traffic]**: The number of users entering the experiment each day.

1. Under **[!UICONTROL Set up the test]**, enter the remaining values:

    * **[!UICONTROL Number of experiences]**: The number of experiences, including the control.

    * **[!UICONTROL Duration of A/B test]**: The number of days the experiment runs.

    * **[!UICONTROL Minimum Detectable Effect]**: The smallest improvement worth detecting. Enter the lift in percentage points.

    * **[!UICONTROL Expected improvement]**: The improvement you expect the experiment to produce.

    * **[!UICONTROL Variance]**: How spread out the metric values are.

1. You can expand **[!UICONTROL Advanced statistical settings]** to provide additional statistical inputs when they are available for the selected calculation.

    * **[!UICONTROL Confidence level]**: The likelihood that a result is not due to chance. A 95% level allows a 5% chance of a false positive.

    * **[!UICONTROL Statistical power]**: The likelihood of detecting a real effect. An 80% power reduces false negatives but requires more traffic or time.

1. Select **[!UICONTROL Run calculation]** to generate the estimate. Select **[!UICONTROL Reset]** to clear the current inputs and start again.

The **[!UICONTROL Result]** panel displays the estimate after you complete the required fields and run the calculation. If required fields are incomplete, the panel prompts you to enter the missing values.

The calculator provides an estimate for planning an experiment. Use the result together with your experiment design, expected traffic, baseline performance, and statistical requirements when deciding how long to run the activity.

## For Auto-Allocate activity

>[!CONTEXTUALHELP]
>id="target_sample_size_traffic_mode"
>title="Traffic mode"
>abstract="How users enter your experiment. Continuous: users enter daily over the experiment duration. Traffic automatically shifts toward better-performing variants as results come in."

>[!CONTEXTUALHELP]
>id="target_sample_size_metric_type"
>title="Metric type"
>abstract="What kind of metric you are measuring. Percentage: use this for binary outcomes like clicks or conversions, where each user either does or does not do something. Number: use this for metrics like revenue or page views, where the value can vary widely from user to user."

>[!CONTEXTUALHELP]
>id="target_sample_size_baseline_metric_rate"
>title="Baseline metric rate"
>abstract="Your current performance before the experiment starts, the control arm average. Always required. For percentage metrics, enter as a percentage: if 5% of visitors click Buy today, enter 5. For count metrics, enter the raw decimal value."

1. Access the **[!UICONTROL Auto Allocate]** tab to calculate planning inputs for an Auto Allocate activity.

1. Under **[!UICONTROL What do you want to know?]**, select the value you want the calculator to determine:

    * **[!UICONTROL Duration]**
    * **[!UICONTROL Number of experiences]**
    * **[!UICONTROL Traffic volume]**
    * **[!UICONTROL Minimum Detectable Effect]**

    The fields in the form change depending on the value you select. The calculator uses the other inputs to determine the selected result.

1. Enter the values requested in the form. Depending on the experiment type and the calculation you selected, the form can include the following inputs:

    * **[!UICONTROL Traffic mode]**: How users enter. In continuous mode, users enter daily and traffic shifts to better-performing variants.
    * **[!UICONTROL Metric type]**: Use **[!UICONTROL Percentage]** for binary outcomes, or **[!UICONTROL Number]** for variable values.
    * **[!UICONTROL Daily traffic]**: The number of users entering daily in continuous experiments.
    * **[!UICONTROL Baseline metric rate]**: The control average before the experiment. Enter a percentage or raw decimal value, based on the metric type.

1. Under **[!UICONTROL Set up the test]**, enter the remaining values:

    * **[!UICONTROL Number of experiences]**: The number of variants, including the control. More variants require more traffic.

    * **[!UICONTROL Duration of A/B test]**: The number of days the experiment runs. Longer tests can detect smaller effects.

    * **[!UICONTROL Minimum Detectable Effect]**: The smallest improvement worth detecting. Enter the lift in percentage points.

1. You can expand **[!UICONTROL Advanced statistical settings]** to provide additional statistical inputs when they are available for the selected calculation.

    * **[!UICONTROL Confidence level]**: The likelihood that a result is not due to chance. A 95% level allows a 5% chance of a false positive.
    * **[!UICONTROL Statistical power]**: The likelihood of detecting a real effect. An 80% power reduces false negatives but requires more traffic or time.


1. Select **[!UICONTROL Run calculation]** to generate the estimate. Select **[!UICONTROL Reset]** to clear the current inputs and start again.

The **[!UICONTROL Result]** panel displays the estimate after you complete the required fields and run the calculation. If required fields are incomplete, the panel prompts you to enter the missing values.

The calculator provides an estimate for planning an experiment. Use the result together with your experiment design, expected traffic, baseline performance, and statistical requirements when deciding how long to run the activity.
