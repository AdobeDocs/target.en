---
keywords: release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates;current updates
description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
landing-page-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Target].
title: What Is Included in the Current Release?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
---
# [!DNL Target] release notes (current)

Explore the latest features, enhancements, and fixes in [!DNL Adobe Target]. These release notes also cover updates to [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform components when applicable. 

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## Time-sensitive updates you need to know {#time-sensitive}

[!BADGE Important]{type=Informative}

For time-sensitive updates related to [!DNL Adobe Target] and your implementation, [!DNL Adobe] provides detailed release notes and documentation through [!UICONTROL Experience League]. Here are some keys highlights relevant to your implementation:

### [!DNL Target] UI version toggle deprecation

For more information, see [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 25.11.2 (November 14, 2025)

**Decisioning offers**

+++See details
* **Offer decisions with hidden or invalid selectors not editable in updated UI.** Resolved an issue in the updated UI where offer decisions tied to hidden or invalid selectors could not be edited unless the element was visible in the Visual Experience Composer (VEC). Editing is now supported directly from the panel, restoring functionality available in the legacy UI and ensuring that offer decisions can be modified regardless of selector visibility. (TGT-53899)

+++

**Recommendations**

+++See details
* **Editing criteria in an activity caused the page to crash.** Resolved an issue in the updated UI where editing activity criteria caused the page to crash with console errors related to `useCrudActionsCtx`. The criteria editor now loads and functions correctly, ensuring activities can be edited without interruption. (TGT-53971)
* **[!UICONTROL Message] column intermittently failed to display product data in the updated UI.** Resolved an issue in the updated [!UICONTROL Recommendations] UI where the [!UICONTROL Message] column in [!UICONTROL Catalog Search] intermittently failed to display product data, even though values were present in the feed. The column now consistently shows the correct message values across all products, ensuring reliable visibility without requiring manual column reconfiguration. (TGT-52777)
* **[!UICONTROL Download Recommendations Data] button not visible after saving activity in updated UI.** Resolved an issue in the updated UI where the [!UICONTROL Download Recommendations Data] button did not appear for certain saved activities, even after re-saving. The button now displays consistently across all activities, ensuring users can reliably export recommendation data without needing workarounds. (TGT-53802)
* **Opening certain products from a collection returned "Requested resource was not found" and modal lacked a close option.** Resolved an issue in the updated Recommendations UI where opening certain products from a collection triggered a "Requested resource was not found" error and displayed a blank modal without a close option. The modal now loads product details correctly, and a close option is always available to exit gracefully. (TGT-53986)

+++

## [!DNL Target Standard/Premium] 25.11.1 (November 10, 2025)


**Analytics for Target (A4T)**

+++See details
* **[!UICONTROL Goals & Settings] error message when using [!DNL Adobe Analytics] as the reporting source in updated UI.** Resolved an issue in the updated [!UICONTROL Overview] UI where the Goals section displayed the error "Something went wrong. We cannot complete your request. Please contact [!DNL Adobe Client Care] if the problem persists" when [!DNL Adobe Analytics] (A4T) was selected as the reporting source. Goals now display correctly with [!UICONTROL Adobe Analytics] metrics, ensuring consistent visibility across reporting sources. (TGT-54021)

+++

**Audiences**

+++See details
* **Unable to select multiple reporting audiences in updated UI.** Resolved an issue in the updated UI where users could not select multiple newly created reporting audiences simultaneously when editing an activity. Multiple audiences can now be assigned at once, improving flexibility and efficiency in reporting setup. (TGT-53253)

+++

**Decisioning offers**

+++See details
* **Unable to edit or replace decisioning offers in updated UI.** Resolved an issue in the updated UI where decisioning offers could not be edited or replaced through the [!UICONTROL Modifications] panel, and offer names appeared blank. Decisioning offers are now fully accessible and editable, restoring parity with the legacy UI and ensuring that customers can manage offers directly within activities. (TGT-53884)

+++

**Localization**

+++See details
* **Corrected several localization errors in the Korean and Japanese UI.** (TGT-54003, TGT-54004, TGT-54006, TGT-54007, & TGT-54018)

+++

**[!UICONTROL Recommendations]**

+++See details
* **Promotion by Attribute with Entity Attribute Matching failed to load recommendation key after activity save.** Fixed an issue where promotions of type [!UICONTROL Promotion by Attribute] with rule type [!UICONTROL Entity Attribute Matching] did not load the recommendation key when edited after saving an activity. The issue was caused by the `customKeyId` not being requested through GraphQL. Recommendation keys now load correctly during promotion edits. (TGT-53117)
* **Recommendation persists visually when switching from ExpB to ExpA.** Resolved an issue where inserting a recommendation in Experience B and then switching to Experience A left the recommendation offer box visible. This was a visual inconsistency only; modifications now render correctly when switching between experiences, ensuring accurate UI behavior. (TGT-53911)
* **Recommendation key not loading for [!UICONTROL Promotion by Attribute] with [!UICONTROL Entity Attribute] Matching.** Resolved an issue where promotions of type [!UICONTROL Promotion by Attribute] with rule type [!UICONTROL Entity Attribute Matching] did not load the recommendation key when edited after saving an activity. The recommendation key is now correctly retrieved through GraphQL, ensuring promotions display and function as expected. (TGT-53917)
* **Editing recommendations on hidden HTML elements not working in updated UI.** Resolved an issue in the [!UICONTROL New Create] and VEC UI where recommendation activities applied to hidden HTML elements could not be edited. This functionality now works as expected, restoring parity with the legacy UI and ensuring recommendations can be modified regardless of element visibility. (TGT-53953)
* **Unable to edit recommendation activities on hidden HTML elements in updated UI.** Resolved an issue in the updated UI where recommendation activities applied to hidden HTML elements could not be edited. This functionality now works as expected, restoring parity with the legacy UI and ensuring recommendations can be modified regardless of element visibility. (TGT-53951)
* **Recommendation catalog intermittently missing attribute values in updated UI.** Resolved an issue in the updated [!UICONTROL Recommendations] UI where catalog search listings intermittently failed to display certain attribute values (e.g., message) even when present in the product feed. Attribute values now load consistently in search results without requiring column reconfiguration, improving reliability and efficiency for catalog management. (TGT-52769)
* **[!UICONTROL Download Recommendations] button missing for [!DNL Recommendations] activities in the updated UI.** Resolved an issue in the updated [!DNL Recommendations] UI where the [!UICONTROL Download Recommendations] button was not visible for A/B activities using recommendations. The button now appears correctly, allowing users to export recommendation data as expected, consistent with functionality in the legacy UI. (TGT-53768)
* **[!UICONTROL Download Recommendation Data] button missing in updated Overview UI.** Resolved an issue in the updated [!UICONTROL Overview] UI where the [!UICONTROL Download Recommendation Data] button was not visible for activities containing recommendations. The button now appears correctly, ensuring that users can export recommendations data directly without needing to toggle back to the legacy UI. (TGT-53772)
* **Editing activity criteria sometimes resulted in blank screen in the updated UI.** Resolved an issue in the updated UI where clicking [!UICONTROL Edit Criteria in Experiences] occasionally led to a blank screen for certain activities. The criteria editor now loads reliably across all activities, ensuring users can edit without interruption. (TGT-53961)
* **Unable to edit sequence criteria in updated UI.** Resolved an issue in the updated UI where attempting to edit [!UICONTROL Sequence Criteria] caused the criteria popup to remain stuck on loading and then display a blank screen. The criteria editor now loads correctly, allowing users to edit and update sequence criteria without interruption. (TGT-53985)

+++

**[!UICONTROL Reports]**

+++See details
* **[!UICONTROL Multivariate Test] (MVT) locations and graph reporting issue prevented report generation.** Resolved an issue where MVT activities failed to generate [!UICONTROL Location Contribution] and Graph reports in the Target UI, displaying the error "Something went wrong. We cannot complete your request." Reports now load correctly within the UI, ensuring full visibility. (TGT-53654)
* **MVT reports not loading due to [!UICONTROL Element] contribution report error.** Fixed an issue where MVT activity reports failed to load in the Target UI, showing the error "Element contribution report could not be fetched." Reports now display correctly, ensuring full visibility of element contributions. (TGT-53691)
* **Export order details to CSV issue for [!UICONTROL Experience Targeting] (XT) activities.** Fixed an issue where the [!UICONTROL Export Order Details to CSV] option incorrectly appeared for XT activities and returned an empty file. The option now only displays for AP activities, ensuring accurate export functionality and preventing confusion. (TGT-53798)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* **[!UICONTROL Delete Modification] button issue prevented removal of activity modifications.** Resolved an issue where the [!UICONTROL Delete Modification] button in the [!DNL Target] UI did not function, preventing users from removing modifications within activities. The button now works as expected, allowing modifications to be deleted reliably without delay. (TGT-53728)
* **Preferred selectors not recognized in updated UI.** Resolved an issue in the updated UI where preferred selectors, such as `data-target-component-id`, were not appearing in the CSS selector list within the VEC. Users can now reliably select preferred attributes instead of dynamically generated class names, ensuring stable targeting across SPA page updates. (TGT-53908)
* **Activity location alignment mismatch between [!UICONTROL Edit] and [!UICONTROL Overview] pages.** Resolved an issue where activity location numbering in the [!UICONTROL Overview] page did not align with updates made in the[!UICONTROL  Edit Experience] page. Locations now remain consistent across both views, ensuring accurate alignment and preventing missing or misnumbered positions. (TGT-53960 & TGT-53954)
* **Unable to switch back to [!UICONTROL Design] mode in updated VEC.** Resolved an issue in the updated VEC UI where users could not toggle back to [!UICONTROL Design] mode after navigating to a new page in [!UICONTROL Browse] mode. The [!UICONTROL Design] toggle now functions correctly, allowing modifications to be applied seamlessly across pages. (TGT-53988 & TGT-53993)
* **Query parameter not displayed in activity overview.** Resolved an issue in the updated UI where query parameters were not shown in the [!UICONTROL Overview] page for activities, causing discrepancies between the [!UICONTROL Overview] and page delivery URLs. Query parameters now display correctly, ensuring activity locations are fully represented and consistent across views. (TGT-53701)

+++

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
