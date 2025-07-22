---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: July 22, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.7.3 (July 24, 2025)

Due to recent issues identified, primarily related to complex customer customizations, this release includes the following fixes and updates:

**Activities**

+++See details
* Fixed an issue where the `buildViews` method in the builder class incorrectly set `viewMaxLocalId` to the total count of views, rather than to the highest `viewLocalId` assigned. (TGT-53207)
* Introduced a new API endpoint that allows users to restore previously deleted activity options from a secondary database. This functionality leverages the existing infrastructure provided by the `RemovedCampaignElements` and `RemovedOptionInfo` classes, ensuring seamless reintegration of deleted options into active activities. (TGT-52903)
* Fixed an issue in the updated [!DNL Target] UI where deleted offers in [!UICONTROL Automated Personalization] (AP) activities were shown as `Deleted option with ID: X` instead of their original names (for example, `Offer Name [Deleted]` as shown in the legacy UI). This fix restores meaningful labeling for deleted offers, improving clarity and making reporting more accurate and user-friendly. (TGT-52921)
* Fixed an issue in the backend persistence layer where deleted options were correctly stored but not accessible via existing API endpoints. As a result, frontend applications couldn't retrieve meaningful names for deleted options, impacting historical reporting views. This fix ensures that preserved deleted option data can now be surfaced properly in the UI. (TGT-52973)
*  Fixed an issue where some activities migrated from the Target frontend to Target Central had inconsistent metric configurations due to a previously fixed sync bug. Specifically, activities that originally used a conversion metric and were later updated to an analytics-based metric retained outdated values in the `primaryMetricType` and `successCriteria` fields. (TGT-52643)

+++

**Form-Based Experience Composer**

+++See details
* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] that caused the editor to crash after clicking the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ) when creating or editing an [!UICONTROL Automated Personalization] (AP) activity. (TGT-53047)

+++

**Recommendations**

+++See details
* Fixed an issue that prevented [!UICONTROL Catalog Search] from loading additional results when scrolling to the bottom of the list, restoring behavior consistent with the legacy UI. (TGT-53088)
* Fixed an issue where the [!UICONTROL Number of Products] column was missing from the [!UICONTROL Collections] page in the updated [!DNL Target] UI. The column now displays correctly, restoring expected functionality. (TGT-53168)
* Fixed an issue where [!UICONTROL Collection] rules were not filtering properly according to rules. (TGT-53254)
* Fixed an issue that blocked deleting items from the [!UICONTROL Criteria Details] dialog box. (TGT-53245)
* Fixed an issue that prevented opening or interacting with products that had no name. This issue occurred when selecting environments that returned unnamed results, preventing access to product details. (TGT-53007)
* Fixed an issue that caused the [!UICONTROL Catalog Search] page to crash and display a blank screen when selecting certain products. (TGT-53087)
* Fixed an issue where [!DNL Recommendations] activities containing metric names longer than 25 characters could not be opened or edited due to API limitations. This fix ensures compatibility with metric names exceeding the character limit, restoring full access to affected activities. (TGT-52839)
* Fixed an issue where users were unable to edit the site_cart_z1 [!DNL Recommendation] activity in the [!DNL Target] UI. Attempting to open the activity triggered an error on the [!UICONTROL Overview] page, blocking access to the editor. (TGT-53221)

+++

**Reporting**

+++See details
* Fixed an issue where the sandbox field in the activity database was not cleared when switching the reporting source from [!DNL Customer Journey Analytics] or [!DNL Analytics] to [!DNL Target]. Previously, the UI correctly sent sandbox: null, but the backend ignored this value, leaving outdated sandbox data in place. The backend now properly clears the sandbox field when null is received. (TGT-52798)
* Re-implemented the deleted options persistence layer in the Target backend to support accurate historical reporting in [!UICONTROL Automated Personalization] (AP) activities. Previously, when an option was deleted, its name was lost, making it difficult to interpret past performance data.

  **Key Improvements**:

  * Deleted options are now tracked using the existing `RemovedCampaignElements` and `RemovedOptionInfo` infrastructure.
  * When an option is removed from an AP activity, its metadata (for example, ID and name) is preserved.
  * The reporting UI can now display the original option name (for example, `Option Name [Deleted]`) alongside historical metrics, improving clarity and usability.

  This update ensures consistent and meaningful reporting, even after options are removed from an activity. (TGT-52986)

* Implemented a new migration endpoint to support the transfer of deleted activity options from JCR-based activities to [!DNL Target] Central. This functionality enables consistent tracking and reporting across systems. This feature ensures that deleted options are preserved and synchronized across the [!DNL Target] frontend and backend, improving historical reporting and data integrity. (TGT-53217)

+++

**Visual Experience Composer (VEC)**

+++See details

* Fixed an issue in the VEC where applying a modification to a view caused duplication and triggered an 'Invalid user input' error. (TGT-52886)
* Fixed an issue with [!UICONTROL Undo] functionality for the [!UICONTROL Insert Before] and [!UICONTROL Insert After] options when configuring image offers in the VEC. 

  Previously, undoing an [!UICONTROL Insert Before] or [!UICONTROL Insert After] action on image offers resulted in inconsistent behavior or failure to properly revert the modification, especially in activities created in the legacy [!DNL Target] UI. This issue has been resolved to ensure undo actions now work reliably for these modifications. (TGT-52809)

* Fixed an issue where the `contentEditable` attribute was unintentionally set to true and persisted in saved HTML content. This update ensures cleaner, expected HTML output without unintended editing behavior. (TGT-52319)
* To prevent permanent loss of deleted options and to ensure consistent behavior across services, soft delete functionality has been implemented for options in the  UI and related microservices.

  **Key Changes**:

  * Options are no longer permanently deleted. Instead, they are marked with a new deleted: true flag in the parameters XML object.
  * This flag is used only by the updated [!DNL Target] UI to exclude deleted options from rendering and to prevent them from being sent to edge services.
  * Deleted options remain part of the activity payload during edits, ensuring traceability while avoiding delivery of non-existent options to customers.

  This update improves data integrity and aligns with best practices for managing deletions in distributed systems. (TGT-52726)

+++

**Workspaces**

+++See details
* Fixed an issue when copying an activity from a non-default to default workspace or between non-default workspaces. Offers are now duplicated with enhanced tracking and naming to prevent conflicts.

  **Key Improvements**:
  * Offers are recreated in the destination workspace with updated IDs and metadata.
  * Copied offers are renamed using the format: "Offer Name Copy" plus a random number or timestamp to ensure uniqueness.
  * The system updates offer and activity states to reflect the new IDs.
  * This functionality prevents errors caused by multiple identical "Offer Copy" names during repeated copy actions.
  * Offers might not immediately appear in the destination workspace's offer list but are processed and surfaced appropriately.

  This update improves reliability and traceability when managing offers across multiple workspaces. (TGT-53080)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
