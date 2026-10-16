---
keywords: Release notes;prerelease notes;future enhancements;future fixes;future features;upcoming release
description: View a list of features, enhancements, and fixes included in previous releases of Adobe Target.
title: What Features Are Included in Previous Releases?
feature: Release Notes
---
# Release notes for previous releases

Release notes for previous [!DNL Adobe Target] releases, including release notes for [!DNL Target Standard/Premium], the [!DNL Target] platform, and the [!DNL Target] Javascript library (at.js). 

Release notes are listed in descending order by month and year of release. 

>[!NOTE]
>
>See [Target release notes (current)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) for information about the current month's Target releases (platform and Target Standard/Premium).

## Release notes - 2024

### [!DNL Adobe Experience Platform Web SDK] `__view__` scope optimization (October 22, 2024)

Between July 22, 2024 and August 15, 2024, the [!DNL Target] team optimized the `__view__` scope, enhancing the accuracy of activity impression, visit, and visitor reporting. This optimization aims to automatically capture reporting data for auto-rendered propositions and should be transparent to most accounts.

All new [!DNL Adobe Experience Platform Web SDK] customers will have this optimization enabled. However, customers who migrated from at.js and have not followed the implementation steps below have the optimization disabled. We urge these customers to review their implementations by February 3, 2025. After this date, we will enable the optimization for all customers. Failure to review and adjust implementations by then might impact reports, as mentioned below. Please contact [!DNL Adobe Customer Care] if you need to confirm whether your implementation is affected or if you require more time to adjust your implementation.

>[!IMPORTANT]
>
>If you cannot complete your implementation review and resolve any issues by February 3, 2025, you can request a one-time, six-month extension. Ensure that your request is submitted by January 31, 2025. Adobe will review and decide on your request.

To benefit from this optimization in case of manual proposition rendering, review your [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep/aep-web-sdk-overview){target=_blank} to ensure that you are sending notifications after manually rendering experiences or when using the `applyPropositions` method (or the corresponding [!DNL Launch] action as a helper) to render experiences.

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

### at.js version 2.11.6 (September 29, 2024)

* Fixed an issue that prevented [!DNL Target] from operating correctly with redirect offers within the [!UICONTROL Visual Experience Composer] (VEC) or [!UICONTROL Form-Based Experience Composer].

For more information about at.js releases, see [at.js version details](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank} in the *Adobe Target Developer Guide*.

### [!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics] (May 8, 2024)

The integration between [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} and [!DNL Target] provides powerful analysis and timesaving tools for your optimization program.

The primary benefits of using [!DNL Customer Journey Analytics] as the reporting source for [!DNL Target] are:

* Marketers can dynamically apply [!DNL Customer Journey Analytics] success metrics to [!DNL Target] activity reports at any time. It is not required to specify everything before running the activity. 
* Marketers can take advantage of [!DNL Customer Journey Analytics] features, such as the [Experimentation Panel](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, to further analyze their website personalization.  

For more information, see [Target reporting in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

### [!UICONTROL Visual Experience Composer] helper extension (April 23, 2024)

The legacy [!DNL Target] Visual Experience Composer helper extension was created using Manifest V2. [!DNL Google] announced that it will no longer allow extensions created using Manifest V2 starting in June 2024. For more information, see [[!UICONTROL Visual Experience Composer] helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] recommends that customers move to the newer [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) as soon as feasible.

### Updates for `Browser:iPad` and `Browser:iPhone` in [!UICONTROL Browser] audience attributes (April 30, 2024)

|Updates|Details|
|--- |--- |
|[!UICONTROL Browser:iPad] and [!UICONTROL Browser:iPhone] updated in [Browser attributes](/help/main/c-target/c-audiences/c-target-rules/browser.md) used when creating audiences.|[!DNL Adobe Target] lets you [target on any of several category attributes](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), including visitors who use a specific [browser or browser options](/help/main/c-target/c-audiences/c-target-rules/browser.md) when they visit your page.<P>Starting with the [!DNL Target] Standard/Premium 24.3.1 (March 4-6, 2024), built-in audiences created using the Target UI, such as `Browser:iPad` and `Browser:iPhone` will be updated to perform proper targeting for [!DNL iPad] and [!DNL iPhone] using `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` and `profile.mobile.isTablet`.<P>This update requires no action on the customers' side.<p><B>Important</b>: For customers to perform proper targeting for [!DNL iPad] and [!DNL iPhone] in profile scripts (and JavaScript segments), manual changes must be made by the customer by **April 30, 2024**. For examples of alternate settings that must be manually changed, see [Updates for [!DNL iPad] and [!DNL iPhone] in [!UICONTROL Browser] audience attributes](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates).|

### [!UICONTROL Visual Editing Helper] extension (March 14, 2024)

This release contains the following enhancements and fixes for the [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) extension for [!DNL Google Chrome]:

* Enhanced the iFrame loading mechanism when performing authoring in customers' websites.
* Fixed an issue that caused the extension to duplicate cookies while performing authoring in the [!UICONTROL Visual Experience Composer] (VEC).

### [!DNL Target] Standard/Premium 24.3.1 (March 4-6, 2024)

This release contains the following enhancements and fixes:

* Fixed the logic that computes the number of unique selectors in an activity. (TGT-47878)
* Fixed an issue that caused [!UICONTROL Multivariate] (MVT) activities configured with [!UICONTROL Analytics for Target] (A4T) reporting to not display properly. (TGT-47490)
* Improved the warning message displayed in reporting when an experience with no traffic is used as the control experience. (TGT-47537)
* Added many backend and localization fixes.

### [!DNL Target] Standard/Premium 24.1.1 (January 22, 23, & 25, 2024)

This release contains the following enhancements and fixes:

* [!UICONTROL Analytics for Target] (A4T) activities with revenue goal metrics did not display "Revenue" as the column name and the revenue metric did not display in ($) format in reporting. This was a cosmetic issue that has been remedied. (TGT-46995)
* Fixed an issue that caused reporting date intervals to not work correctly. (TGT-47396)
* Fixed an issue that caused the incorrect status to display on the [!UICONTROL All Activities] page after customers activated or deactivated an activity using the [!UICONTROL More Actions] icon. (TGT-47367)
* Fixed an issue that caused the [!UICONTROL Important Attributes] report to not display for a single customer. (TGT-47272)
* Fixed an issue that caused an "Invalid payload" message to display when a single customer tried to enable "Require Authentication." (TGT-47195)
* Updated numerous localized strings in the [!DNL Target] UI.
