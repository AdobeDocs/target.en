---
title: Use context in audience rules
description: Learn how to use context attributes in audience rules for feature flags and feature groups in Flags.
hide: true
exl-id: 0367f475-9209-4d53-86b4-a739a73a23a7
---
# Use context in audience rules {#context-in-audience-rules}

Context attributes are values provided by the client application at runtime. They allow you to target users based on dynamic, session-level information such as the user's active language, device type, or application state.

Context attributes are relevant for web and mobile clients.

## How context attributes work {#how-context-attributes-work}

Your application passes context attributes to Flags when evaluating a feature flag. You define rules in the console that check these values, and the platform uses them at the time of evaluation to determine whether the user qualifies.

## Adding a context attribute {#adding-context-attribute}

To add a context attribute to an audience rule:

1. Open the feature flag or feature group in the console.
2. Go to the **Audience** tab.
3. Under **Context**, add a new condition.
4. Select the context attribute, operator, and value.

If the context attribute you need does not appear in the list, you can create a new one — see [Creating your context attributes](creating-your-context-attributes.md).

## See also {#see-also}

* [Audience in feature flags and feature groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
