---
keywords: allowlist;remote offer;administration;URL patterns;validation;activities;offers;wildcard;regex
description: Learn how to view, search, add, and delete allowlisted URLs for remote offers in the Adobe Target Administration section, including validation behavior and account-wide scope.
title: Manage allowlisted remote offer URLs
feature: Administration & Configuration
topic: Implementation
role: Admin
level: Intermediate
solution: Target
product: Target
---
# Allowlisted URLs

Allowlisted URLs define trusted URL patterns where your organization can create and run [!DNL Adobe Target] experiences, including when you use remote or redirect offers. The list works alongside [host management](/help/main/administrating-target/hosts.md) and [environments](/help/main/administrating-target/environments.md), but applies specifically to allowed remote offer URL patterns and related validations.

To manage allowlisted URLs, click **[!UICONTROL Administration]** > **[!UICONTROL Allowlisted URLs]**.

![Allowlisted URLs page showing URL list, search field, and Add URL control](../administrating-target/assets/allowlist-1.png)

## Manage allowlisted URLs {#add-url}

The main table lists each allowlisted pattern in a single column. Supported entries can include exact URLs, wildcard paths, or pattern formats your organization accepts for remote experiences.

1. Click **[!UICONTROL Add URL]**.

    ![](../administrating-target/assets/allowlist-2.png)

1. In the dialog, enter the URL or pattern your organization must allow.

    ![](../administrating-target/assets/allowlist-3.png)

1. Save your changes.
    
    After the pattern is allowlisted, users can create or run activities and offers that rely on that URL, subject to your other [!DNL Target] rules.

1. Use the **[!UICONTROL Search URLs]** field to filter the table.

1. To delete a URL, find the row for the pattern you no longer need and click the ![Delete](../administrating-target/assets/do-not-localize/Smock_Delete_18_N.svg) icon.

    ![](../administrating-target/assets/allowlist-4.png)


