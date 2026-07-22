---
title: Creating your context attributes
description: Learn how to create and organize context attributes and context groups in Flags so you can use them in audience criteria.
badge: label="Beta" type="Informative"
hide: true
---
# Creating your context attributes {#creating-your-context-attributes}

Context attributes are custom data fields that describe user, session, or application context (for example, subscription tier, app version, or region). Use context attributes to define audience criteria for feature flags.

Context groups organize related context attributes into a logical hierarchy. Use context groups to make attributes easier to find and manage during feature configuration.

| Term | Description | Used in |
| --- | --- | --- |
| **Context attribute** | A named field with a data type and optional predefined values. | Audience criteria, feature configuration |
| **Context group** | A category that organizes related context attributes. | Context selection when creating a feature |
| **UI label** | The display name shown in the user interface. | Audience criteria and administration pages |
| **ID** | A unique technical identifier. | Application requests |
| **Predefined values** | An optional list of allowed values with display labels. | Drop-down lists and audience rule builders |

## Prerequisites {#prerequisites}

Before managing context attributes and context groups, complete the following:

* You have access to the **Flags console** in the correct sandbox.
* You have the **Admin** role required to create and manage context attributes and context groups.

## Navigate to Context Attributes {#navigate}

1. Log in to the **Flags console**.
1. In the left navigation, under **Dashboards**, select **Context Attributes**.

You are now on the **Context Attributes** page. Use this page to create context groups and context attributes.

## Create a context group {#create-group}

Every context attribute must belong to a group.

1. In the left navigation, under **Dashboards**, select **Context Attributes**.
1. On the **My Context Attributes** tab, select **Add Group**.
1. Complete the required fields.
1. Select **Create**.

### Group fields {#group-fields}

| Field | Description |
| --- | --- |
| **Group name** | Enter a unique name for the group. |
| **Make a subgroup of** | Select a parent group to organize the hierarchy. You can also create a group while creating an attribute. |

## Create a context attribute {#create-attribute}

1. On the **My Context Attributes** tab, select **New Context Attribute**.
1. Complete the required fields.
1. Select **Submit**.

### Attribute fields {#attribute-fields}

| Field | Description |
| --- | --- |
| **UI Label** | Enter the display name used in audience criteria. |
| **ID** | Enter a unique technical identifier used in application requests. |
| **Context Group** | Select a group, or create a new group inline. |
| **Data Type** | Select the type that matches the data your application sends. |

| Data type | Example |
| --- | --- |
| STRING | `gold` |
| INTEGER | `42` |
| BOOLEAN | `true` |
| DECIMAL | `9.99` |
| DATE | `2026-07-17` |
| VERSION | `1.2.0` |

### Predefined values (optional) {#predefined-values}

Use predefined values to limit an attribute to a fixed set of values. Select **Add Predefined Values**.

| Field | Description |
| --- | --- |
| **UI Label** | Enter the display name. |
| **Value** | Enter the technical value sent by the application. |

Select **Save** to apply your changes.

## Troubleshooting {#troubleshooting}

| Issue | Resolution |
| --- | --- |
| **Create** is disabled | Complete both **Group name** and **Make a subgroup of**. |
| Cannot submit an attribute | Complete **ID** and **Context Group**. |
| Group not visible in the dropdown | Refresh the page, or create the group inline from the attribute form. |
| Predefined values not saved | Select **Save** in the modal before you submit the attribute. |

## See also {#see-also}

* [Creating and using Rule Sets](creating-and-using-rule-sets.md)
* [Use context in audience rules](using-context-in-audience-rules.md)
* [Audience in feature flags and feature groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
