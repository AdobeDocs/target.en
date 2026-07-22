---
title: Complex audience rules
description: Learn how to work with large or complex audience rule sets in Flags, including bulk value limits and how to split rules across multiple conditions.
badge: label="Beta" type="Informative"
hide: true
exl-id: 37e037b6-45eb-4261-b580-30d94d8e55da
---
# Complex audience rules {#complex-rules}

## Using nested logic for complex rules {#nested-logic}

Nested logic lets you combine multiple audience conditions with precise AND/OR control. To enable it:

1. Add the audience conditions you need.
2. Enable **Nested Logic** in the audience rules section.
3. Each condition is assigned a number. Enter a logical expression that references these numbers, for example:
   * `1 and (2 or 3)`
   * `(1 and 2) or 3`
   * `(1 and 2) or (3 and 4)`

## See also {#see-also}

* [Audience in feature flags and feature groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
