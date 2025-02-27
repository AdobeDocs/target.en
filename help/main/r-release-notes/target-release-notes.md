---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: February 26, 2025**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.2.3 (February 26, 2025)

This release includes the following updates:

* Resolved an issue preventing activity updates post [!DNL Target] 25.2.1 release for some activities. (TGT-51781)
* Resolved an issue where all in-state audience changes were removed upon canceling the activity-creation process (selecting [!UICONTROL Cancel] instead of [!UICONTROL Add Audience]). (TGT-51769 & TGT-51770)
* Resolved an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to load for some activities, particularly when custom code was used.  issue led to the VEC displaying a blank screen or the [!DNL Target] UI reverting to its older version. (TGT-51758)
* Resolved an issue where modifications were discarded after editing page delivery for audiences. (TGT-51756)
* Resolved an issue where all non-metric audiences (page and experience audiences) were removed from activities upon changing a metric type on the [!UICONTROL Goals & Settings] page. (TGT-51753)
* Resolved an issue where clicking [!UICONTROL Cancel] while editing an activity navigated the Target UI to the [!UICONTROL Activities List] instead of the [!UICONTROL Activity Details] page. (TGT-51731)
* Resolved an issue preventing customers from downloading reports via the [!UICONTROL Export Reports to CSV] option. (TGT-51708)
* Resolved an issue in the Form-Based Experience Composer where [!DNL Target Standard] customers were incorrectly shown as using [!UICONTROL Properties], a [!DNL Target Premium] feature. (TGT-51678)
* Fixed an issue that blocked [!DNL Adobe Experience Platform] attributes from displaying when creating new offers. (TGT-51665)
* Moved all active filters for [!DNL Recommendations] inventory to the quick search, aligning the UI with [!UICONTROL Catalog Search] instead of the [!UICONTROL Filter] rail. (TGT-50723)

## at.js version version 2.11.7 (February 26, 2025)

This release includes the following update:

* Fixed Telemetry logging when `localStorage` is not available. Telemetry was causing an issue for some customers that had `localStorage` disabled in their browsers. 

For information about this and previous at.js releases, see [at.js version details](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}.

## [!DNL Target Standard/Premium] 25.2.1 (February 17, 2025)

This release includes the following updates:

* [!UICONTROL Activities] user interface update
* [!DNL Recommendations] user interface update

### [!UICONTROL Activities] user interface update

As the [!DNL Adobe Target] UI modernization effort continues, we are pleased to announce the general availability of the updated [!UICONTROL Activities] User Interface.

>[!NOTE]
>
>Starting February 17, customers will gradually have access to the new [!UICONTROL Activities]  UI. To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage will upgrade the initial group of [!DNL Target] customers to the new [!UICONTROL Activities] UI. Subsequent stages will upgrade the remaining customers.

Based on the latest [!DNL Adobe Spectrum] design system, the update standardizes previously inconsistent design patterns, while adding new enhancements, such as:

* [Redesigned reporting](/help/main/administrating-target/reporting.md) for better insights into activity results.
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) page, now getting the information from the [[!DNL Audit Query API]](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} for real-time insights.
* [Customizable list views](/help/main/c-activities/activities.md) to for better flexibility across different team needs.
* [Enhanced quick info and detail screens](/help/main/c-activities/activities.md) for easier access to information.
* [Session-persistent search and filter options](/help/main/c-activities/activities.md).
* Completely [rebuilt [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) with support for latest security updates from browser providers and a modern user interface.

  For information about how the updated VEC differs from the previous version, see:
  
  * [Visual Experience Composer changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md) 
  * [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [Updated [!DNL Chrome] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) supporting Manifest V3 for increased security and improved support for first-party cookies.

![Activities refresh](/help/main/r-release-notes/assets/activities-refresh.png)

### [!DNL Recommendations] user interface update

As the [!DNL Adobe Target] UI modernization effort continues, we are pleased to announce the general availability of the updated [!DNL Recommendations] User Interface. 

>[!NOTE]
>
>Starting February 17, customers will gradually have access to the new [!UICONTROL Recommendations]  UI. To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage will upgrade the initial group of [!DNL Target] customers to the new [!UICONTROL Activities] UI. Subsequent stages will upgrade the remaining customers.

Based on the latest [!DNL Adobe Spectrum] design system, the update standardizes previously inconsistent design patterns, while adding new enhancements, such as:

* The [product catalog search](/help/main/c-recommendations/c-products/catalog-search.md) now features an updated database allowing a real-time synchronization of products.
* [!UICONTROL Recommendations] objects ([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections], and [!UICONTROL Exclusions]) [created over API are now available in the UI](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [Recommendations settings](/help/main/administrating-target/recommendations-settings.md) have been consolidated under the [!UICONTROL Administration] section.
* Customizable list views for better flexibility across different team needs.
* Refreshed HTML and JSON code editors with [syntax highlighting and line numbering](/help/main/c-experiences/c-manage-content/create-json-offer.md). 
* Enhanced quick info and detail screens for easier access to information.
* Session-persistent search and filter options.

![Recommendations UI refresh](/help/main/r-release-notes/assets/recs-ui-refresh.png)

## [!DNL Target Standard/Premium] 25.1.1 (January 9, 2025)

This release includes the following updates:

### [!UICONTROL Offers Library] user interface update

To enhance the user experience for [!DNL Adobe Target] users, this release updates the [!UICONTROL Offers Library] user interface. 
 
>[!NOTE]
>
>To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage upgraded the initial group of Target customers to the new Offers UI. Subsequent stages will upgrade the remaining customers.

Using the latest [!DNL Adobe Spectrum] design system, this update standardizes inconsistent design patterns and introduces new enhancements, including the following:

* **Bulk offer management**: Select and delete or move multiple offers simultaneously.

* **[!UICONTROL Code Editor] upgrades**: Refreshed HTML and JSON editors with syntax highlighting and line numbering.

* **Improved offer cards**: Enhanced quick information and detail cards for easier information access.

* **Persistent search and filters**: Adds session-persistent search and filter options.

For more information see [Offers](/help/main/c-experiences/c-manage-content/manage-content.md) and the sub-articles in this section.

Here's a short video that highlights the changes in this release:

![Offers UI refresh video](/help/main/r-release-notes/assets/offers-video-v2.gif)

## [!DNL Adobe Experience Platform Web SDK] `__view__` scope optimization (October 22, 2024)

Between July 22, 2024 and August 15, 2024, the [!DNL Target] team optimized the `__view__` scope, enhancing the accuracy of activity impression, visit, and visitor reporting. This optimization aims to automatically capture reporting data for auto-rendered propositions and should be transparent to most accounts.

All new [!DNL Adobe Experience Platform Web SDK] customers will have this optimization enabled. However, customers who migrated from at.js and have not followed the implementation steps below have the optimization disabled. We urge these customers to review their implementations by February 3, 2025. After this date, we will enable the optimization for all customers. Failure to review and adjust implementations by then might impact reports, as mentioned below. Please contact [!DNL Adobe Customer Care] if you need to confirm whether your implementation is affected or if you require more time to adjust your implementation.

>[!IMPORTANT]
>
>If you cannot complete your implementation review and resolve any issues by February 3, 2025, you can request a one-time, six-month extension. Ensure that your request is submitted by January 31, 2025. Adobe will review and decide on your request.

To benefit from this optimization in case of manual proposition rendering, review your [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} to ensure that you are sending notifications after manually rendering experiences or when using the `applyPropositions` method (or the corresponding [!DNL Launch] action as a helper) to render experiences.

The most-common scenarios when experiences are manually rendered include:

* Using JSON offers
* Using a custom decision scope in an activity created in the [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)
* Not using `renderDecisions: true` when fetching an activity created using the [!UICONTROL Form-Based Experience Composer] that uses the global `__view__` scope

If notifications are not implemented as documented in [Render personalized content](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} in the *Data Collection* guide, reporting data might be missing in [!DNL Target] and in [Analytics for Target reporting](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In certain scenarios, you might notice an incorrect traffic split because the reporting data is not captured. Or, in other scenarios, reporting the same event repeatedly.

Depending on your implementation, check for [!DNL Analytics] and A4T reporting impacts. 

The [!DNL Platform Web SDK] supports two implementation types for rendering experiences and personalizations:

* **Single call for personalization and measurement.**

  Initially recommended, the single-call approach for the [!DNL Platform Web SDK] is scheduled to be deprecated in favor of the split-call approach. Adobe advises all new implementations to use the new split-call approach and recommends that existing customers transition to the split-call method as well. 
  
  If you continue to use the single-call approach, you might notice the following unexpected changes in your [!DNL Analytics] reports:

  * A dip in bounces.
  * A4T and [!UICONTROL Page View] hits not stitched together, making it challenging to perform certain breakdowns and correlations of your A4T reports using [!DNL Analytics] eVars and events.

* **Split calls (also known as top and bottom of page events).**

  This implementation type is the new [split-call implementation approach](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank} recommended by [!DNL Adobe]. With this approach, the new optimization does not impact [!DNL Analytics] or A4T reports.

If you have questions, contact [Adobe Customer Care](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
