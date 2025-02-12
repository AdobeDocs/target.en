---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates,current updates
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
---
# [!DNL Target] release notes (current)

These release notes provide information about features, enhancements, and fixes for each [!DNL Adobe Target Standard] and [!DNL Target Premium] release. In addition, release notes for [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform changes are also included, when applicable.

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## Target Standard/Premium 25.2.1 (February 12, 2025)

This release includes the following updates:

* [!UICONTROL Activities] user interface update
* [!DNL Recommendations] user interface update

### [!UICONTROL Activities] user interface update

As the [!DNL Adobe Target] UI modernization effort continues, we are pleased to announce the general availability of the updated [!UICONTROL Activities] User Interface.

>[!NOTE]
>
>Starting February 12, customers will gradually have access to the new [!UICONTROL Activities]  UI. To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage will upgrade the initial group of [!DNL Target] customers to the new [!UICONTROL Activities] UI. Subsequent stages will upgrade the remaining customers.

Based on the latest [!DNL Adobe Spectrum] design system, the update standardizes previously inconsistent design patterns, while adding new enhancements, such as:

* [Redesigned reporting](/help/main/administrating-target/reporting.md) for better insights into activity results.
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) page, now getting the information from the [[!DNL Audit Query API]](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} for real-time insights.
* [Customizable list views](/help/main/c-activities/activities.md) to for better flexibility across different team needs.
* [Enhanced quick info and detail screens](/help/main/c-activities/activities.md) for easier access to information.
* [Session-persistent search and filter options](/help/main/c-activities/activities.md).
* Completely [rebuilt [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) with support for latest security updates from browser providers and a modern user interface. For more information see [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) options.

  For information about how the updated VEC differs from the previous version, see [Visual Experience Composer changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md).

* [Updated [!DNL Chrome] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) supporting Manifest V3 for increased security and improved support for first-party cookies.

![Activities refresh](/help/main/r-release-notes/assets/activities-refresh.png)

### [!DNL Recommendations] user interface update

As the [!DNL Adobe Target] UI modernization effort continues, we are pleased to announce the general availability of the updated [!DNL Recommendations] User Interface. 

>[!NOTE]
>
>Starting February 12, customers will gradually have access to the new [!UICONTROL Recommendations]  UI. To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage will upgrade the initial group of [!DNL Target] customers to the new [!UICONTROL Activities] UI. Subsequent stages will upgrade the remaining customers.

Based on the latest [!DNL Adobe Spectrum] design system, the update standardizes previously inconsistent design patterns, while adding new enhancements, such as:

* The [product catalog search](/help/main/c-recommendations/c-products/catalog-search.md) now features an updated database allowing a real-time synchronization of products.
* [!UICONTROL Recommendations] objects ([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections], and [!UICONTROL Exclusions]) [created over API are now available in the UI](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [Recommendations settings](/help/main/administrating-target/recommendations-settings.md) have been consolidated under the [!UICONTROL Administration] section.
* Customizable list views for better flexibility across different team needs.
* Refreshed HTML and JSON code editors with [syntax highlighting and line numbering](/help/main/c-experiences/c-manage-content/create-json-offer.md). 
* Enhanced quick info and detail screens for easier access to information.
* Session-persistent search and filter options.

![Recommendations UI refresh](/help/main/r-release-notes/assets/recs-ui-refresh.png)

## Target Standard/Premium 25.1.1 (January 9, 2025)

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

For more information see [Offers](/help/main/c-experiences/c-manage-content/manage-content.md) and the sub-articles in this section. All Offers articles in this section have been updated to reflect these UI changes.

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

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|
     
## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|[Documentation Changes](/help/main/r-release-notes/doc-change.md)|View detailed information about updates to this guide that are not included in these release notes.|
|[Release notes for previous releases](/help/main/r-release-notes/release-notes-for-previous-releases.md).|View information about new features and enhancements in previous releases of Target Standard and Target Premium.|
|[Adobe Experience Cloud Release Notes](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank}|View the latest release notes for the Adobe Experience Cloud solutions.|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|[Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank}|Receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions.|
|[Target Release Notes - Prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank}|Information about the current month's Target releases, including prerelease information.|
