---
title: Reporting
description: Learn how to view feature flag reporting in Flags using Customer Journey Analytics.
hide: true
exl-id: edddca99-f263-461b-a16f-b46ee7c15f6c
---
# Reporting {#reporting}

Flags delivers reporting through **Customer Journey Analytics (CJA)**. A **Report** tab is available on every feature flag and feature group detail page. It lets you view a CJA report scoped to that specific flag or group, embedded directly in the page.

>[!NOTE]
>
>Reports open with a **30-day** reporting window by default. You can adjust the range from the panel header.

## Prerequisites {#prerequisites}

Before you can view reports, ensure that:

1. Reporting is set up for your application — see [Set up reporting with Customer Journey Analytics](#setup).
1. Your feature flag or feature group is active and has accumulated data.

## View a report {#view-report}

### Open the Report tab and pick a data view {#open-report-tab}

1. Open a feature flag or feature group and select the **Report** tab.
1. A **Select Data View** dialog opens, listing the CJA data views available to you. The first one is selected by default.
1. Choose the data view you want and select **View Report**. Select **Cancel** to close the dialog without loading a report.
1. The report loads inside the tab, scoped to that flag or group's entity ID.

![Report tab on a feature flag's detail page](assets/report-tab.png)

>[!NOTE]
>
>The dialog lists only the data views you have access to in the current sandbox. If none are available, the dialog shows a message and **View Report** stays disabled — check your data view permissions or switch sandbox.

![Select Data View dialog](assets/select-dataview.png)

### View the performance report {#view-performance-report}

The embedded **Flags Overview** dashboard displays:

* **Total People**, **People Participation by day**, and **People Participation by Variant** (control group vs. variant IDs)
* An **Overview** table listing each variant with its people count and participation percentage

Adjust the date range from the panel header to re-plot for a different window (default 30 days).

![Flags Overview performance report](assets/performance-report.png)

### Explore experimentation results {#explore-experimentation-results}

1. In the **Experimentation** panel, the **Experiment** (flag or group entity ID) and **Control variant** are pre-selected.
1. Add a **Success metric** using **Add metric**, and choose a **Normalizing metric** (default **People**) based on which graph you want plotted.
1. Optionally enable **Include confidence upper/lower bounds**.
1. Select **Build** to compute **Lift**, **Confidence**, and **Conversion rate** per variant for the selected metric.

![Experimentation panel with experiment, control variant, and metric selectors](assets/experimentation-selection.png)

See the [Experimentation panel documentation](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation) for more details on how these metrics are calculated.

![Experimentation results showing Lift, Confidence, and conversion rate by variant](assets/experimentation.png)

### Analyze in CJA (optional) {#analyze-in-cja}

Once a report is loaded, an **Analyze in CJA** button appears at the top-right of the Report tab. Selecting it opens the same report full-page in Customer Journey Analytics in a new browser tab, where you have the complete CJA toolset for deeper, ad-hoc analysis.

![Flags Overview report opened in the Customer Journey Analytics workspace](assets/cja-workspace.png)

>[!IMPORTANT]
>
>The report opens as a temporary, unsaved project. If you customize it in CJA (add metrics, change panels, adjust filters, and so on) and want to keep those changes, save it using **Project > Save as template**. Otherwise your edits are lost when you close the report.

![Project menu with Save as template highlighted](assets/save-as-template.png)

## Set up reporting with Customer Journey Analytics {#setup}

Reporting requires a Customer Journey Analytics dataset connected to your Flags application. Contact Flags support or your Adobe representative to enable reporting for your application.

>[!NOTE]
>
>The identity passed in the feature request does not need to be linked to a profile. Evaluation happens at runtime and the event is sent to Customer Journey Analytics.

## See also {#see-also}

* [Create your first feature flag](create-your-first-feature-flag.md)
* [A/B testing with feature flags](a-b-testing.md)
* [Create a feature group](create-a-feature-group.md)

<!-- -->
