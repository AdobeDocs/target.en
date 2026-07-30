---
title: Create your first feature flag
description: Learn how to create a feature flag in Flags, set an audience, and test it before rolling out to users.
badge: label="Beta" type="Informative"
hide: true
exl-id: ae115120-8da9-465e-a556-c17591ea7054
---
# Create your first feature flag {#create-feature-flag}

## Prerequisites {#prerequisites}

Before creating a feature flag, complete the following:

* You have access to the Flags console — see [Log in to the console](../console/log-in-to-the-console.md)
* Your application is onboarded — see [Onboard your application](../applications/onboard-your-application.md)
* You have the **Product Release Owner** role

## Step 1: Create the feature flag {#create}

To create a new feature flag, follow these steps in the console:

1. Log in to the **Flags console**, go to the left panel, and select **Feature Flags**.
1. Select your application from the **Application** drop-down.
1. Select **New Feature Flags**.
1. Complete the form fields:

   | Field | Description |
   | --- | --- |
   | **Name** | A display label for the feature flag. Not used in code. |
   | **Key** * | The identifier used in your code to evaluate the flag. Cannot be changed after creation. |
   | **Description** | Optional description for documentation purposes. |
   | **Metadata** | Optional. Up to 1,024 characters. Use this field for any additional metadata to associate with the flag. |
   | **Tags** | Optional tags for documentation purposes. |
   | **Identity** * | The identity the flag is evaluated against (for example, ECID). This is the identity passed in the feature request. |
   | **Percentage rollout** | The percentage of your defined audience that is served this feature. Defaults to 100%. See [Set a feature to gradually roll out](set-feature-gradual-rollout.md). |

   Fields marked with * are required.

>[!IMPORTANT]
>
>The **Key** is the identifier used in your code and cannot be changed after creation. Keys **cannot contain spaces** and are **case-sensitive**. The **Name** is a display label only and is not used in code; the two are independent (the Name is not converted into the Key). Entering a space in the Key field produces the error: _"Invalid value for feature key."_

1. Optionally add an audience criteria (see Step 2).
1. Save your feature flag settings.

## Step 2: Add an audience criteria {#audience}

Audience criteria control which users see the feature. You can target users with **context attributes** — values your website or app sends in the feature request (for example `locale` or `platform`). Combine them with **AND**, **OR**, and **NOT**. See [Use context in audience rules](../audience/using-context-in-audience-rules.md).

To add audience criteria, go to the **Audience** tab when creating or editing a feature flag.

## See also {#see-also}

* [Set a feature to gradually roll out](set-feature-gradual-rollout.md)
* [Create a feature group](create-a-feature-group.md)

<!-- -->
