---
keywords: AI insights;Experimentation Accelerator;opportunities;activity overview
description: Learn how to use AI-generated insights and optimization opportunities from Experimentation Accelerator in the Adobe Target Activity Overview.
title: AI insights in the Activity Overview
feature: Activities
---
# AI insights in the Activity Overview

>[!AVAILABILITY]
>
>The [!UICONTROL AI insights] tab is available only for organizations and activities enabled for the Experimentation Accelerator integration.

The **[!UICONTROL AI insights]** menu in your [!UICONTROL Activity Overview] provides access to insights and optimization opportunities from **[!UICONTROL Experimentation Accelerator]**. Use this tab to review experiment learnings, compare treatments, and identify changes that might improve conversion rates.

➡️ [Learn more in Experimentation Accelerator documentation](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/overview)

## Setup for AI insights and opportunities

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="Primary metric"
>abstract="The primary metric is automatically pulled from the reporting settings. To make changes, modify the goal metric under Goals & Settings."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="Hypothesis"
>abstract="The hypothesis is a statement you define that explains the expected outcome of the experiment. Include a description of what is being changed and where, then state which metric you expect to change and how."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="Treatment details"
>abstract="Treatment details show images of what a treatment looks like when a user qualifies for it. You can review these images for all experiments. Some experiments may ask you to confirm the image or replace it if needed."

The [!UICONTROL AI insights] tab can display AI-generated experiment insights and optimization opportunities in cards. The cards help you review the results of an experiment and identify potential follow-up treatments.

The available cards depend on how you set up your Goals & Settings. [Learn more](../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)

1. Open your activity in [!DNL Adobe Target].

1. Select the **[!UICONTROL AI insights]** menu.

1. Click **[!UICONTROL Open]** to add screenshot.

    ![](assets/ai-insights-1.png)

1. Select **[!UICONTROL Upload image]** to upload a preferred screenshot from your local files for your Treatments.

    ![](assets/ai-insights-2.png)

1. Once your treatment each has a screenshot, click **[!UICONTROL Confirm]**.

Once you finished configuring your AI insights and opportunities, you will to get valuable Insights and Opportunities.

Insights are generated after the experiment has sufficient data for statistical validation and the required experiment details have been confirmed.

## Supported activities and limitations

The [!UICONTROL AI insights] tab is limited to activity types supported by the Experimentation Accelerator integration. Insights and opportunities might not be available for every activity or until the activity meets the required data and statistical conditions.

The following conditions can affect what appears in the tab:

* The Experimentation Accelerator integration must be enabled for your organization.
* The activity must be an eligible experiment type.
* The experiment must contain the data required to generate an insight or opportunity.
* Statistical validation might be required before insights are generated.
* Some recommendations might be limited to experiments with text-based changes.

For information about planning experiment inputs, see [Sample Size Calculator](sample-size-calculator.md).

## Insights


>[!CONTEXTUALHELP]
>id="target_ai_insights"
>title="Insights"
>abstract="Experiment insights are the learnings found by AI when the experiment data has met statistical significance."

## Opportunities

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="Opportunities"
>abstract="Experiment opportunities are AI suggested treatment ideas based on patterns AI found in your experiment screenshots and results."
