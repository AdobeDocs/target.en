---
title: Reporting
description: Learn how to view feature flag reporting in Flags using Customer Journey Analytics.
hide: true
exl-id: edddca99-f263-461b-a16f-b46ee7c15f6c
---
# Reporting {#reporting}

Flags delivers reporting through **Customer Journey Analytics (CJA)**. There is no in-console Results or Reports tab — instead, a **Report** button on each feature flag or feature group opens a scoped CJA dashboard for that item.

## Prerequisites {#prerequisites}

Before you can view reports, ensure that:

1. Reporting is set up for your application — see [Set up reporting with Customer Journey Analytics](#setup).
1. Your feature flag or feature group is active and has accumulated data.

## View a report {#view-report}

To open a report for a feature flag or feature group:

1. Navigate to the feature flag or feature group in the console.
1. Select **Report**.

A scoped Customer Journey Analytics dashboard opens, showing data for that flag or feature group. The dashboard includes:

* **Participants** — Total number of users who qualified for the feature (variant + control group combined)
* **Control group** — Number of users assigned to the control group (users who received the default experience)
* **Variant breakdown** — Cumulative count of users enrolled in each variant and the control group
* **Daily enrollment** — Day-level charts showing enrollment in each variant and the control group over time

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
