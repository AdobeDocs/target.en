---
keywords: automated traffic allocation;targeting;winner;statistical guarantee;confidence;determine winner;lift;confidence;default;default experience;auto-allocate;auto allocate
description: Discover how to interpret [!UICONTROL Auto-Allocate] A/B activity results, focusing on key indicators like lift and confidence.
title: How Do I Interpret [!UICONTROL Auto-Allocate] Reports?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
---
# Interpret [!UICONTROL Auto-Allocate] reports 

Interpret the results of an [!UICONTROL Auto-Allocate] A/B activity in [!UICONTROL Adobe Target] by examining important indicators, including lift and confidence.

Many marketers make the mistake of prematurely declaring a winning experience before the results indicate the clear winner. [!DNL Target] makes it easier for you to determine the winner. 

For general information about declaring a winner, see [Ten common A/B testing pitfalls and how to avoid them](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## Identify the winning experience {#section_24007470CF5B4D30A06610CE8DD23CE3}

When using the [!UICONTROL Auto-Allocate] feature, [!DNL Target] displays a badge at the top of the activity's page indicating "No Winner Yet" until the activity reaches the minimum number of conversions with sufficient confidence.

![No Winner badge](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

When a clear winner is declared, [!DNL Target] displays the "Winner: Experience *X*" badge.

![Winner badge](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

>[!NOTE]
>
>[!UICONTROL Auto-Allocate] activities are designed to find the best experience among all options and not just to do pairwise comparisons with control.

## Statistical guarantees of [!UICONTROL Auto-Allocate] {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

At the end of an A/B activity, [!UICONTROL Auto-Allocate] guarantees that the determined winner has an effective false-positive rate of 5%. This means that only 5% of the time, the determined winner is not actually the best experience among all the experiences in the activity. For an [A/A test](/help/main/c-activities/t-test-ab/aa-testing.md) (with identical experiences), [!DNL Target] concludes a test less than 5% of the time. The expected behavior for an A/A test (with identical experiences) is for it to run indefinitely and so the winner badge should never appear.

[!DNL Target] does not use p-value based confidence for [!UICONTROL Auto-Allocate].

The [!UICONTROL Confidence] column in an [!UICONTROL Auto-Allocate] activity displays the probability of an experience being the winner within 1% margin of error. The algorithm uses a minimum detectable effect of 1% between the best and the second-best conversion rates. The algorithm uses [Bernstein Inequality](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) to compute this probability.

Normal A/B tests compute confidence based on p-values. [!UICONTROL Auto-Allocate] does not use p-values. P-values "loosely" compute the probability that a given experience is different from the control. These p-values can be used only to determine whether an experience might be different from the control. These values cannot be used to determine if an experience is different from another experience (not control).

>[!IMPORTANT]
>
>[!DNL Target] shows a winner after a predefined minimum number of conversions; however, the final decision to pick the winner should always be on the results of the [!DNL Adobe Target] Sample Size Calculator. [!DNL Target] does not consider the base conversion rates of a site and other important aspects that are fed into the calculator to determine the duration of the activity. As a result, [!DNL Target] might display a winner earlier than warranted based on a minimum number of conversions. For more information, see [Sample Size Calculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Understand Lift and Confidence reporting in [!UICONTROL Auto-Allocate] activities {#lift-confidence}

In [!UICONTROL Auto-Allocate] activities, the first experience (by default named Experience A) is always defined as a "Control" experience on the [!UICONTROL Reports] tab. This experience is not treated as a true statistical control in the modeling used to determine the performance of experiences, but it is treated as a reference or baseline for some figures in the report.

The "Lift" numeric value and 95% bounds for each experience are always calculated with reference to the defined "Control" experience. The defined "Control" experience cannot have lift relative to itself, so a blank "---" value is reported for this experience. Unlike in A/B tests, in [!UICONTROL Auto-Allocate] tests, if an experience performs worse than the defined control, a negative Lift value is not reported; instead "---" is displayed.

The displayed [!UICONTROL Confidence Interval] bars represent the 95% confidence interval around the mean estimate of an experience's conversion rate. These bars are also color-coded with respect to the defined "Control" experience. The "Control" experience's bar is always colored gray. The portions of confidence intervals below the "Control" experience's confidence interval are colored red and the portions of confidence intervals above the "Control" experience are colored green.

A winner is found when the leading experience's 95% [!UICONTROL Confidence Interval] is not overlapping with any other experiences. The winning experience is designated with a green star badge to the left of the experience name and in the "Winner" banner. When no star is visible, the banner reads "No Winner Yet" and a winner has not yet been found.

A "Confidence" number is also reported next to the currently leading or winning experience. This figure is reported only until the leading experience's [!UICONTROL Confidence] reaches at least 60%. If two experiences are present in the [!UICONTROL Auto-Allocate] activity, this number represents the confidence level that the experience is performing better than the other experience. If more than two experiences are present in the [!UICONTROL Auto-Allocate] activity, this number represents the confidence level that the experience is performing better than the defined "Control" experience. If the "Control" experience is winning, no "Confidence" figure is reported.

## Frequently Asked Questions {#section_C8E068512A93458D8C006760B1C0B6A2}

Consider the following answers to frequently asked questions:

### It has been a few days into the activity. Why are all confidence values still showing 0%?

Any of the following reasons describe why 0% displays in the report's [!UICONTROL Confidence] column for all activities:

* Manual A/B tests and [!UICONTROL Auto-Allocate] use different statistics to display [!UICONTROL Confidence] values.

  Manual A/B tests use p-values based on [Welch's t-test](https://en.wikipedia.org/wiki/Welch%27s_t-test). A P-value is the probability of finding the observed (or a more extreme) difference between an experience and the control, given that in reality there is no such difference. These P-values can be used only to determine whether observed data is consistent with a given experience and the control being the same. These values cannot be used to determine if an experience is different from another experience (not control).

  [!UICONTROL Auto-Allocate] shows the probability of a given experience being a true winner across all experiences in the activity. Only a winning experience (which is most likely to be the winner), has a non-zero confidence value. All others are most likely to be losers and display 0%. 

* [!UICONTROL Auto-Allocate] starts showing confidence only after the winning experience gathers 60% confidence. These confidence levels typically appear in about half the time that a normal A/B test would take to complete (although this time frame is not guaranteed). To determine how long a normal A/B test would run, use the [!DNL Adobe Target] [Sample Size Calculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): plug control's conversion-rate in "Baseline conversion rate," "5%" for "Lift," and 95% for "Confidence." Typically, confidence starts showing after each experience has amassed at least 50% of the required samples per-experience. This gives you an idea of when confidence starts appearing.

* If the report is showing 0% across the board, it is likely too early into the activity.

### Are the "No Winner," "Winner," and "star" badges available for [!UICONTROL Auto-Allocate] activities that use [!UICONTROL Analytics as the reporting source] (A4T)?

The "No Winner Yet" and "Winner" badges are currently not available in the [!UICONTROL A4T] panel in [!DNL Analysis Workspace]. These badges are also not available if the same report is viewed in [!DNL Target]. A winner "star" badge shown in a [!DNL Target] report for an [!UICONTROL Auto-Allocate] activity using A4T should be ignored. 

For more information about this and other limitations and notes, see [Auto-Allocate](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *A4T support for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities*.
