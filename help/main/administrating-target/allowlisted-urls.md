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

>[!NOTE]
>
>**Account scope:** URL allow listings apply to the entire account. Coordinate changes with your account administrators so all teams use consistent patterns.

![Allowlisted URLs page showing URL list, search field, and Add URL control](/help/main/administrating-target/assets/target_administration-configuration_allowlisted-urls-main.png)

## Manage allowlisted URLs {#add-url}

The main table lists each allowlisted pattern in a single column. Supported entries can include exact URLs, wildcard paths, or pattern formats your organization accepts for remote experiences. Use the footer controls to change pagination, such as items per page, when the list grows.


1. Click **[!UICONTROL Add URL]**.
1. In the dialog, enter the URL or pattern your organization must allow.
1. Save your changes.
    
    After the pattern is allowlisted, users can create or run activities and offers that rely on that URL, subject to your other [!DNL Target] rules.

1. Use the **[!UICONTROL Search URLs]** field to filter the table. Your search value persists after you reload the page so you can return to the same filtered view.

1. To delete a URL, find the row for the pattern you no longer need.

1. Click the **[!UICONTROL Delete]** icon for that row.

1. Confirm the deletion in the dialog.

    If no rows match your search criteria, the page shows an empty state. Adjust your search text or clear the search field to see the full list again.

When a user enters an activity URL or offer URL that does not match an allowlisted pattern, [!DNL Target] shows a clear error and asks them to add the URL under **[!UICONTROL Administration]** > **[!UICONTROL Allowlisted URLs]** or contact an administrator.

The following examples show the message in common workflows.

**Web activity creation**

![Error when activity URL is not allowlisted during A/B activity creation](/help/main/administrating-target/assets/target_administration-configuration_allowlisted-urls-activity-validation.png)

**Redirect offer**

![Error when redirect offer URL is not on the allowlisted URLs list](/help/main/administrating-target/assets/target_administration-configuration_allowlisted-urls-redirect-offer-validation.png)

**Remote offer**

![Error when remote offer URL is not on the allowlisted URLs list](/help/main/administrating-target/assets/target_administration-configuration_allowlisted-urls-remote-offer-validation.png)


