---
title: Creating and using Rule Sets
description: Learn how to create a reusable Rule Set of audience context criteria in Flags and import it into feature flags and feature groups.
badge: label="Beta" type="Informative"
hide: true
---
# Creating and using Rule Sets {#creating-and-using-rule-sets}

A Rule Set is a reusable collection of audience context criteria. Create a Rule Set when multiple feature flags or feature groups need the same audience. You can then import the Rule Set instead of recreating the audience criteria for each feature.

## Rule Set requirements {#requirements}

| UI label | Use | Required |
| --- | --- | --- |
| **Enter Rule Set** | Enter a name for the Rule Set. | Yes |
| **Rule Set description** | Describe the purpose of the Rule Set. | No |
| **Context** | Define at least one audience criterion. Context attributes are named fields such as subscription tier, application version, or region. | Yes |

## Create a Rule Set {#create-rule-set}

### Step 1: Start a new Rule Set {#step-1-start}

In Flags, select **Rule set** from the left navigation, and then select **New Rule Set**.

The **My Rule Set** tab displays Rule Sets that you created. The **Team Rule Set** tab displays Rule Sets available to your team.

![Rule Set list with no Rule Sets created yet](assets/rule-set-list-empty.png)

### Step 2: Add the Rule Set details and criteria {#step-2-details}

1. Enter a name for the Rule Set.
1. Optionally, enter a description.
1. Under **Context**, define the audience criteria that you want to reuse.
1. Use **And** or **Or** to combine multiple criteria.
1. To create a more complex expression, select **Enable Nested Logic**.

![Rule Set creation form with example context criteria](assets/rule-set-create-context.png)

### Step 3: Save the Rule Set {#step-3-save}

Select **Save Settings**. The saved Rule Set appears under **My Rule Set**.

![Rule Set list showing a newly saved Rule Set](assets/rule-set-list-created.png)

## Use a Rule Set in a feature flag or feature group {#use-rule-set}

### Step 1: Open and enable the audience settings {#step-1-open}

Open the feature flag or feature group in which you want to use the Rule Set, select the **Audience** tab, and then turn on **Audience Rule** to enable audience criteria.

### Step 2: Select the Rule Set {#step-2-select}

Open the **Select Rule Set** dropdown. Choose the Rule Set from **My Rule Set** or **My Team Rule Set**.

![Select Rule Set dropdown open in the Audience tab](assets/rule-set-select-in-audience.png)

### Step 3: Review the imported criteria {#step-3-review}

The context criteria from the selected Rule Set are imported into the audience. Review the criteria, and then save the feature flag or feature group.

![Feature flag audience tab showing imported Rule Set criteria](assets/rule-set-imported-audience.png)

You can use the same Rule Set in multiple feature flags and feature groups that require the same audience.

### Step 4: Save the feature flag or feature group {#step-4-save}

After reviewing the imported audience criteria, select **Save Settings**.

>[!NOTE]
>
>Importing a Rule Set copies its audience criteria into the feature flag or feature group. If the audience criteria need to be updated later, update them separately in every feature flag and feature group where the Rule Set was imported. Updating the original Rule Set does not automatically update previously imported audiences.

## Create a Rule Set from a feature flag or feature group {#create-from-feature}

You can also create a Rule Set directly from the Audience screen of a feature flag or feature group:

1. Open the feature flag or feature group, and then select the **Audience** tab.
1. Turn on **Audience Rule**.
1. Define the context criteria that you want to reuse.
1. Select the **+** button in the upper-right corner, next to the **Select Rule Set** dropdown.
1. In the **Save Rule Set** dialog, enter a Rule Set name.
1. Select **Save Rule Set**.

## See also {#see-also}

* [Creating your context attributes](creating-your-context-attributes.md)
* [Use context in audience rules](using-context-in-audience-rules.md)
* [Audience in feature flags and feature groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
