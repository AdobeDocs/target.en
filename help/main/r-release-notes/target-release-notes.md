---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: November 14, 2024**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Adobe Experience Platform Web SDK] `__view__` scope optimization (October 22, 2024)

Between July 22, 2024 and August 15, 2024, the [!DNL Target] team optimized the `__view__` scope, enhancing the accuracy of activity impression, visit, and visitor reporting. This optimization aims to automatically capture reporting data for auto-rendered propositions and should be transparent to most accounts.

All new [!DNL Adobe Experience Platform Web SDK] customers will have this optimization enabled. However, customers who migrated from at.js and have not followed the implementation steps below have the optimization disabled. We urge these customers to review their implementations by February 3, 2025. After this date, we will enable the optimization for all customers. Failure to review and adjust implementations by then might impact reports, as mentioned below. Please contact [!DNL Adobe Customer Care] if you need to confirm whether your implementation is affected or if you require more time to adjust your implementation.

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
