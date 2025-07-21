---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: July 10, 2025**

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

+++

**Visual Experience Composer (VEC)**

+++See details

* Fixed an issue in the VEC where applying a modification to a view caused duplication and triggered an 'Invalid user input' error. (TGT-52886)
* Fixed an issue with [!UICONTROL Undo] functionality for the [!UICONTROL Insert Before] and [!UICONTROL Insert After] options when configuring image offers in the VEC. 

  Previously, undoing an [!UICONTROL Insert Before] or [!UICONTROL Insert After] action on image offers resulted in inconsistent behavior or failure to properly revert the modification, especially in activities created in the legacy [!DNL Target] UI. This issue has been resolved to ensure undo actions now work reliably for these modifications. (TGT-52809)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
