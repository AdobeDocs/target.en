---
keywords: Release notes;prerelease notes;future enhancements;future fixes;future features;upcoming release
description: View a list of features, enhancements, and fixes included in previous releases of Adobe Target.
title: What Features Are Included in 2025 Previous Releases?
feature: Release Notes
TQID: 'https://experienceleague.adobe.com/cjheajZKokzwCNspfQckh6PHh5ecetdj7vZrrq9IqXw'
---
# Release notes for previous releases

Release notes for previous [!DNL Adobe Target] releases, including release notes for [!DNL Target Standard/Premium], the [!DNL Target] platform, and the [!DNL Target] Javascript library (at.js). 

Release notes are listed in descending order by month and year of release. 

>[!NOTE]
>
>See [Target release notes (current)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) for information about the current month's Target releases (platform and Target Standard/Premium).

## Release notes - 2025

### [!DNL Target Standard/Premium] 25.11.2 (November 14, 2025)

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

### [!DNL Target Standard/Premium] 25.10.1 (October 22, 2025)

This release contains the following updates and fixes:

**Activities**

+++ See details
* **Resolved a usability issue in the updated UI**. [!UICONTROL Observers] can now preview activities using the [!UICONTROL View Activity] option, just like in the legacy UI. (TGT-51741)
* **[!UICONTROL Observer] users can now view activity content in the updated UI.** Restored visibility for Observer-role users in the updated Activity UI. Previously, Observers were unable to view modifications, offers, and content changes—functionality that was available in the legacy UI. (TGT-53785)
* **[!UICONTROL Approver] users can now edit activity goals without editor privilege error.** Resolved a permissions issue in the Activity Create UI that blocked Approver-level users from saving changes to advanced goal settings. Affected users received a `403 Forbidden.Resource` error requiring editor privileges, despite having sufficient access. (TGT-53819)

+++

**Audiences**

+++See details

* **Multi-Audience Selection Restored in "This Activity Only" Reporting.** Resolved an issue in the Activity Create UI that prevented users from selecting multiple audiences under the [!UICONTROL This activity only] section in [!UICONTROL Goals & Settings]. (TGT-53283)
* **Audience-based reporting graphs now display conversion data correctly.** Resolved an issue in the [!UICONTROL Reports] tab that caused graphs to fail when selecting non-default audiences. While data and confidence metrics were available, the visual graph showed only a solid line, making analysis difficult. (TGT-53769)
* **The [!UICONTROL Targeting] UI now clearly indicates excluded audience rules.** Resolved an issue in the [!UICONTROL Targeting] section of the Activity Create UI where audience rules set to [!UICONTROL Exclude] were not clearly displayed. This led to confusion when reviewing targeting logic, especially for audiences excluding specific URLs. (TGT-53809)
* **Audience definition values now selectable and copyable in the [!UICONTROL Targeting] tab.** Resolved an issue in the Activity Create interface that prevented users from selecting and copying audience rule values in the [!UICONTROL Targeting] tab. This functionality was available in the legacy UI but missing in the updated UI. (TGT-53856)

+++

**Localization**

+++See details

* **Corrected mistranslation of "quote" in zh_CN page editor context.** Corrected a contextual translation error in the zh_CN locale where the term "quote" was inaccurately translated as "报价", implying a commercial price quotation. In the Typography > Heading style > Blockquote section, the intended meaning refers to a formatting element—quotation block—not pricing. (TGT-53841)
* **Corrected mistranslation of "quote removed" in zh_CN page editor context.** Corrected a translation error in the zh_CN locale where "quote removed" was inaccurately rendered as "移除了报价", implying a commercial price quotation. In the Typography > Heading style > Blockquote section, the term refers to a formatting element—quotation block—not pricing. (TGT-53843)
* **Corrected mistranslation of "quote rearranged" in zh_CN page editor context.** Corrected a contextual translation error in the zh_CN locale where "quote rearranged" was inaccurately translated as "重新排列了报价", implying a commercial price quotation. In the Typography > Heading style > Blockquote section, the term refers to a formatting element—quotation block—not pricing. (TGT-53844)
* **Corrected mistranslation of "quote changed" in zh_CN page editor context.** Corrected a translation error in the zh_CN locale where "quote changed" was inaccurately rendered as "更改了报价", suggesting a commercial price quotation. In the Typography > Heading style > Blockquote section, the term refers to a formatting element—quotation block—not pricing. (TGT-53845)

+++

**Recommendations**

+++See details

* **CSS selector changes for recommendations now save correctly.** Resolved an issue in the Activity Create UI that prevented users from updating the CSS selector for recommendation placements. Changes reverted after saving, blocking updates to targeting containers. (TGT-53835)
* **Page load event selection now persists in recommendation modifications.** Resolved an issue in the Activity Create UI that prevented users from saving changes when switching a recommendation's event type from [!UICONTROL View] to [!UICONTROL Page Load]. Although the selection appeared successful, it reverted after navigating away, blocking activity publication. (TGT-53957)

+++

**Reports**

+++See details

* **"[!UICONTROL Export order details to CSV]" now downloads complete data.** Resolved an issue in the updated [!UICONTROL Overview] UI that caused the "[!UICONTROL Export Order details to CSV]" option to download empty files, even when valid report data was present. (TGT-53787)

+++

**Security**

+++See details

* **IMS prefilter added to protect GQL endpoints from cross-org data exposure.** Resolved a security vulnerability in the Admin tab affecting the licenseGroups and targetProperties GraphQL endpoints. The issue stemmed from using the JIL API with an admin client token that could be exploited to access cross-org product data. (TGT-53837)

+++

**Visual Experience Composer (VEC)**

+++See details

* **Authoring stability restored in the Activity Create UI.** Resolved an intermittent issue in the VEC UI that caused authoring to fail and links to become unexpectedly clickable, redirecting users away from the page. (TGT-53153)
* **Editing restored for saved activities in the Activity Create UI.** Resolved an issue that prevented users from editing activities after saving modifications. Affected activities remained stuck in "[!UICONTROL Applying initial modifications]", blocking further updates and hiding the [!UICONTROL Cancel] button. (TGT-53631)
* **The VEC no longer stalls on "[!UICONTROL Applying initial modifications]."** Resolved a performance issue in the VEC that caused long delays when loading experiences with a high number of modifications. Affected users saw the UI stuck on "[!UICONTROL Applying initial modifications]" for several minutes, especially in Experience B scenarios. (TGT-53727)
* **The VEC now loads modifications without root elements.**
Resolved an issue in the VEC that caused experiences to stall when loading modifications that lacked a clear root element. These modifications previously caused the UI to hang indefinitely on "A[!UICONTROL pplying initial modifications]." (TGT-53799)
* **Saving changes in activities now works as expected.** Resolved a permissions-related issue in the New Create UI that prevented users from saving changes when editing goals and advanced settings in activities. Affected users saw a red error ribbon and a "Forbidden.Resource" message, despite having appropriate access. (TGT-53816)
* **VEC UI now preserves experience modifications across views.** Resolved multiple issues in the updated VEC that impacted experience development. Modifications were not persisting correctly, especially when using HTML offers or switching between views. (TGT-53825)
* **All views now correctly display when a modification spans multiple experiences.** Resolved an issue in the Activity Create UI where only one view was shown when a modification was applied across multiple views. The hover tooltip failed to list all associated views, even though the modification was correctly applied. (TGT-53827)
* **The VEC no longer intermittently stalls on "[!UICONTROL Applying initial modifications]."** Resolved an intermittent issue in the VEC where experiences failed to load and remained stuck on "[!UICONTROL Applying initial modifications]." This behavior was inconsistent and sometimes triggered redirect loops or required manual cache clearing. (TGT-53916)
* **VEC loading issue could not be reproduced.** We investigated a reported issue where the VEC remained stuck on "[!UICONTROL Applying initial modifications]" when editing existing activities. The behavior was suspected to be related to HTML content lacking a parent element. We'll continue monitoring for recurrence and recommend using structured containers for HTML offers to ensure stability. (TGT-53972)
* **[!UICONTROL Design] mode in the VEC no longer behaves like [!UICONTROL Browse] mode intermittently.** Resolved an issue in the UI where [!UICONTROL Design] mode intermittently behaved like [!UICONTROL Browse] mode, allowing clickable `<a>` links and preventing element selection. This caused the hover box to disappear and blocked modification workflows. (TGT-53136)
* **Button clicks in [!UICONTROL Composer] mode no longer trigger page redirection.** Resolved an issue in the updated VEC UI where clicking a button in [!UICONTROL Composer] mode caused an unexpected redirect to the button's target URL. This prevented users from editing call-to-action (CTA) elements and disrupted the authoring workflow. (TGT-53137)
* **Offer code updates in automated personalization activities now save without error.** Resolved an issue in the New Create UI that caused an "[!UICONTROL Invalid user input]" error when updating offer code in [!UICONTROL Automated Personalization] activities. The error blocked users from saving changes, even when the input was valid. (TGT-53586)
* **[!UICONTROL Design] mode in the VEC now blocks link navigation for editable components.** Resolved an issue in the updated VEC where clickable elements—such as buttons and links—triggered page redirection even while in [!UICONTROL Design] mode. This behavior mimicked [!UICONTROL Browse] mode and prevented users from modifying key components. (TGT-53696)
* **"[!UICONTROL Clicked an element]" metric now works without redirect or error.** Resolved an issue in the New Create UI that caused unexpected redirects and blank screens when selecting the "[!UICONTROL Clicked an element]" conversion metric. Clicking a button during setup triggered navigation instead of registering the element, resulting in an "[!UICONTROL element not found]" error. (TGT-53817)
* **Existing activities no longer get stuck in infinite loading loop during edit.** Resolved an issue in the New Create UI where editing an existing activity in the VEC caused the page to remain stuck in an infinite loading loop. This issue did not affect newly created activities and was triggered by pre-existing modifications on the page. (TGT-53913)
* **Existing activity pages with modifications now load correctly in the VEC.** Resolved an issue in the updated VEC that caused pages to remain stuck in the loading phase when editing an existing activity with saved modifications. New activities loaded without issue, but previously configured activities failed to render. (TGT-53967)

+++

### [!DNL Target Standard/Premium] 25.9.3 (September 30, 2025)

This release contains the following enhancements and fixes.

+++[!UICONTROL Audiences]

* **Audience exclusion rules were incorrectly displayed as inclusion in the [!DNL Target] UI.** Audiences configured with exclusion rules appeared as included when editing targeting within an activity. Although the exclusion logic was applied correctly during execution, the UI failed to reflect the rule accurately, omitting the "excluding" label. The [!DNL Target] UI now correctly displays exclusion rules in both audience configuration and targeting workflows, ensuring clarity and consistency for campaign setup. (TGT-53808)
* **The [!UICONTROL Targeting] section did not indicate that an audience rule was set to exclude.** Audiences configured with exclusion logic were incorrectly displayed as inclusion in the [!UICONTROL Targeting] section of the activity-create UI. Although the backend correctly applied the exclusion rule, the UI failed to visually represent it, omitting the "Exclude" label and causing confusion during campaign setup. The [!UICONTROL Targeting] section now clearly displays exclusion rules, ensuring consistency between audience configuration and targeting visualization. (TGT-53809)

+++

+++Localization

* **Fixed a terminology inconsistency in the Simplified Chinese translation of "Full details view."** 
Previously, the term "Details" was incorrectly translated as "详情" in the Simplified Chinese (zh_CN) locale, violating established terminology guidelines. This has been corrected to "详细信息" to ensure consistency with the termbase. (TGT-53741)

+++

+++[!UICONTROL Recommendations]

* **Recommendation boxes were difficult to locate and select in the VEC.** After adding a recommendations offer in the (VEC), clicking the modification in the left panel did not highlight or scroll to the corresponding recommendation box on the page. This made it difficult to locate and edit the offer, especially when hidden under selectors or styled minimally. Clicking a recommendation modification now correctly highlights and scrolls to the associated element, improving usability and editing efficiency in the updated activity-create process. (TGT-52571)
* **Recommendation selectors were incorrectly rewritten after saving an activity.** When adding a recommendation to an element in the VEC, the selector was initially correct, but after saving and reopening the activity, it changed to a generic selector. Attempts to manually restore the original selector resulted in validation errors. Recommendation selectors now persist accurately after saving, ensuring reliable targeting and editability in the updated activity-create process. (TGT-53709)
* **Criteria content could not be edited when modifying an existing activity.** When editing an activity, the [!UICONTROL Criteria] content section appeared disabled, with buttons greyed out and unresponsive. This issue was resolved by ensuring that [!UICONTROL Criteria] configurations are fully editable during activity updates. Customers can now modify [!UICONTROL Criteria] content without needing to switch selections or use workarounds, improving flexibility and usability in the updated activity-create process. (TGT-53812)
* **Criteria could not be edited within an activity.** The [!UICONTROL Edit Criteria ]and [!UICONTROL Remove Criteria] options were disabled when accessing criteria from within an activity. However, the same criteria could be edited successfully via the [!UICONTROL Recommendations] tab. Criteria are now fully editable from both the activity-edit workflow and the [!UICONTROL Recommendations] tab, ensuring a consistent and efficient editing experience. (TGT-53814)

+++
 
+++[!UICONTROL Reports]

* **Generating ad-hoc offers in A[!UICONTROL utomated Personalization] activities caused reporting inconsistencies.** Using the Generate ad-hoc offers feature in [!UICONTROL Automated Personalization] (AP) activities led to inaccurate reporting. Specifically, offer IDs were reused across locations, causing reporting data to be misattributed or overwritten. Ad-hoc offers now generate with distinct identifiers per location, ensuring accurate tracking and reporting across all configured experiences. (TGT-53757)
* **Activity reports failed to load due to a JavaScript error.** Customers encountered a "Something went wrong" message when accessing the [!UICONTROL Reports] tab for certain activities. The error was caused by a JavaScript exception: Cannot read properties of undefined (reading 'indexOf'), triggered during the `getAnalyticsReportSummary` GraphQL call. Reports now load correctly, and error handling has been improved to prevent similar failures in the updated activity-create workflow. (TGT-53797)
* **Reports crashed after interacting with the scrollbar.** Clicking the scrollbar in the [!UICONTROL Reports] tab caused the page to crash, accompanied by a JavaScript error:
`SyntaxError: Failed to execute 'querySelector' on 'Element': '[data-key="a-currentcopy"hiretalent""]' is not a valid selector.` Reports now load and scroll correctly without triggering errors or crashes. (TGT-53828)
* **eRports did not display the primary metric.** The primary metric, configured as a conversion metric using an mbox was missing from the activity reports. Searching by metric name or mbox name yielded no results, preventing visibility into key performance data. Primary metrics now appear correctly in the [!UICONTROL Reports] tab, ensuring accurate tracking and analysis of campaign performance. (TGT-53773)
* **The [!UICONTROL Reports] tab in the updated UI crashed when interacting with the horizontal scroll bar.** The [!UICONTROL Reports] view intermittently crashed with a "Something went wrong" error when using the horizontal scroll bar to access metrics out of view. The scroll bar now functions reliably, allowing customers to view and analyze all metrics without needing workarounds such as zooming out or using shift-scroll. (TGT-53824)

+++

+++[!UICONTROL Visual Experience Composer] (VEC)

* **Clicking breadcrumbs in the VEC did not consistently display the edit menu.**
When selecting HTML elements via the breadcrumbs in the (VEC), the edit menu would intermittently fail to appear or disappear quickly, making element selection unreliable. The edit menu now consistently displays when navigating via breadcrumbs, improving the element selection workflow in the updated activity-create process. (TGT-52873)
* **The context menu intermittently failed to appear in the VEC.** The context menu in the updated VEC UI did not consistently appear when clicking on elements, making it difficult to access editing options. The context menu now reliably displays upon element selection, improving the editing workflow and overall usability in the updated activity-create process. (TGT-53015)
* **The context menu failed to appear for certain elements in the VEC.** The context menu did not display when selecting specific elements in the updated VEC, making it difficult to apply modifications. The context menu now consistently displays for all supported elements, improving the reliability and usability of the editing experience in the updated activity-create workflow. (TGT-53248)
* **Context menu disappeared on the first click when using breadcrumbs in the VEC.** Selecting a parent element via the breadcrumbs in the VEC caused the context menu to briefly appear and then disappear, making it difficult to access editing options. The context menu now remains visible and functional when navigating elements through breadcrumbs, improving the reliability of the element selection workflow in the updated activity-create process. (TGT-53424)
* **The context menu did not appear for top-level elements in the VEC.** Selecting top-level elements—such as `<div>` or `<main>` tags—via the breadcrumbs in the VEC did not trigger the context menu, preventing further editing actions. The context menu now consistently appears for all supported elements, including top-level containers, improving the flexibility and usability of the activity-create workflow. (TGT-53770)
* **Elements on a specific page were not editable in the VEC.** Certain elements on the page could not be selected or edited in the updated VEC. This issue was isolated to that page and did not affect other pages within the same account. All elements on the page are now selectable and editable as expected, restoring full functionality in the activity-create workflow. (TGT-53353)
* **Improved the workflow when viewing child elements during element selection in the VEC.** To improve usability and precision during activity creation, the VEC now displays child elements when hovering over or selecting a parent HTML element. This enhancement allows customers to better understand the structure of the page and make more accurate modifications, streamlining the editing workflow in the updated UI. (TGT-53416)
* **Elements in existing activities could not be edited using the modification bar.** When editing previously created activities, the modification bar failed to activate for certain elements on the page, preventing updates. This issue was primarily observed in modified activities and was difficult to reproduce in newly created ones. The modification bar now consistently displays and allows editing of all supported elements, improving reliability and usability in the updated activity-create workflow. (TGT-53013)

+++

+++[!UICONTROL Workspaces]

* **Cloning an activity to a different workspace triggered an "Invalid User Input" error.** Attempting to clone an activity from one workspace to another resulted in an error: "InvalidProperty.Json – Unrecognized property name 'content'." This issue was caused by improper handling of activity metadata during the cloning process. Activities can now be successfully cloned across workspaces without triggering validation errors, ensuring smoother activity deployment workflows. (TGT-53731 & TGT-53736)

+++

### [!DNL Target Standard/Premium] 25.9.2 (September 22, 2025)

This release includes the following fixes and enhancements:

**[!UICONTROL Audiences]**

+++See details

* **Fixed an issue where activities could not be copied due to invalid audience IDs.** Customers attempting to copy activities in the updated activity-create process encountered an error caused by invalid audience IDs (for example, -1752722444307). This backend validation issue prevented duplication of activities within the same workspace. This issue has been resolved, and activities can now be copied successfully without audience-related errors. (TGT-53717)
* **Fixed an issue where invalid user input errors appeared for activity-only audiences in the [!UICONTROL Automated Personalization] activities the [!UICONTROL Manage Content] modal.** Customers encountered invalid user input errors when configuring activity-only audiences in the[!UICONTROL  Manage Content] modal for AP activities. This issue occurred despite the audiences being previously used successfully. Combined audience configurations now save correctly without triggering validation errors. (TGT-53749)

+++

**Documentation**

+++See details

* **Moved Target-specific Web SDK documentation pages to the Adobe Target repository.** As part of the Web SDK documentation restructuring, [!DNL Target]-specific content has been migrated from the general Web SDK docs to the [!DNL Adobe Target] [Developer guide](https://experienceleague.adobe.com/en/docs/target-dev/developer/a4t/overview-a4t?lang=en){target=_blank}. This change improves content discoverability and ensures that solution-specific guidance is maintained by the appropriate product team. (TGT-53374)

+++

**[!UICONTROL Offer Decisions]**

+++See details

* **Offer Decision option now consistently visible during initial activity creation.** Resolved an issue in the updated UI where the [!UICONTROL Offer Decision] option failed to appear during the first-time creation flow for A/B activities, particularly when accessed in incognito mode on tenants with Offer Decisions enabled. The option only appeared after navigating to the [!UICONTROL Targeting] step and back to [!UICONTROL Experiences]. This fix ensures that the [!UICONTROL Offer Decision] option is immediately available during initial setup, improving usability and reducing confusion. (TGT-51888)

+++

**[!UICONTROL Offers]**

+++See details

* **Fixed an issue where redirect offers did not include `redirectOptions` in the payload when `includeContent=true`.** Customers retrieving redirect offers with `includeContent=true `were missing the `redirectOptions` field in the response payload. This inconsistency affected workflows, such as offer copying and activity creation. Redirect offers now correctly include `redirectOptions` when content is requested. (TGT-53737)

+++

**[!DNL Recommendations]**

+++See details

* **Click tracking restored for [!UICONTROL Recommendations] activities created in the updated UI.** Resolved an issue where [!UICONTROL Recommendations] activities created in the updated UI failed to register click tracking, resulting in zero reported conversions. Activities built in the legacy UI tracked clicks correctly and reported conversions as expected. This fix ensures that Recommendations activities created in the updated UI now include the correct tracking attributes, restoring conversion reporting and alignment with A4T metrics. (TGT-53287)
* **Click tracking restored for Recommendation activities.** Resolved an issue where [!UICONTROL Recommendations] activities created in the updated UI failed to register click tracking, resulting in zero reported conversions. The legacy UI correctly applied a tracking ID (`at-track-click`) to [!UICONTROL Recommendations] content, while the updated UI mistakenly inserted a placeholder (`__recsClickTrackIdPlaceholder__`), preventing backend tracking. This fix ensures that [!DNL Recommendations] content now includes the correct tracking ID, restoring conversion reporting and alignment with A4T metrics. (TGT-53496)
* **Collection editor crash resolved in updated UI.** Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) UI where opening a collection from the Editor panel caused the page to crash with a TypeError: Cannot read properties of undefined (reading 'customLocale'). This error occurred across multiple activity types, including [!UICONTROL Recommendations] and A/B tests. (TGT-53703)
* **Option to remove selected collection restored in the VEC.** Fixed an issue in the VEC where users could only replace a selected collection in a [!UICONTROL Recommendations] activity but were unable to remove it entirely. This limitation blocked use cases requiring a clean removal of the collection without substitution. This fix introduces a clear option to remove the selected collection, allowing greater flexibility in activity setup and alignment with legacy UI behavior. (TGT-53652)
* **Custom criteria collections now display correctly in  the [!UICONTROL Recommendations] UI.** Fixed an issue in the Recommendations interface where collections built using custom criteria failed to display product results. While standard attribute-based collections worked as expected, those using custom filters returned "No Results Found" despite valid catalog matches. This fix ensures that collections using custom attributes now populate correctly in the [!UICONTROL Product] tab, restoring full functionality for personalized recommendations workflows. (TGT-53653)
* **Fixed an issue where collections did not display products when first opening the [!UICONTROL Products] page.** Customers accessing collections in the [!UICONTROL Recommendations] section experienced empty product results when first opening the [!UICONTROL Products] page. This issue was caused by a backend error in the GraphQL query, which failed to load product data for collections with custom criteria. The issue has been resolved, and products now appear correctly without requiring environment switching. (TGT-53694)
* **Fixed an issue where collections could not be removed in Form-based [!UICONTROL Recommendations] activities.** Customers creating [!UICONTROL Recommendations] activities using the [!UICONTROL Form-Based Experience Composer] were unable to deselect a previously chosen collection. The UI required a collection to be selected before saving, preventing users from reverting to "All Collections." This behavior has been updated to match the VEC functionality, allowing customers to save without a selected collection and defaulting to "All Collections" as expected. (TGT-53708)
* **Fixed an issue where promotions could not be set by attribute due to missing collection or filtering rule values.** Customers configuring promotions by attribute in the activity-create process encountered an error stating that a promotion was missing either a collection ID or filtering rule values. This validation issue blocked progression even when the setup appeared complete. Promotions can now be saved successfully when configured by attribute. (TGT-53750)
* **Fixed an issue where activities could not be saved due to duplicate experience names.** Customers encountered an invalid user input error when saving activities that included specific combinations of criteria and designs. The error was triggered by duplicate experience names, even when the setup appeared valid. Activities with distinct configurations can now be saved without naming conflicts. (TGT-53805)
* **Fixed an issue where validation remained invalid for promotions configured by attribute.** Customers encountered persistent validation errors when setting up promotions by attribute in the activity-create process, even when all required fields were correctly populated. This issue was caused by incorrect validation logic in the [!UICONTROL Recommendations] workflow. Attribute-based promotions now validate and save as expected. (TGT-53811)
* **Fixed an issue where applying a promotion to a live [!UICONTROL Recommendations] activity triggered an error.** Customers encountered the error "A Promotion is missing either a Collection ID or filtering rule values" when attempting to apply a front promotion to a live [!UICONTROL Recommendations] activity, even after providing valid configuration details. Promotions can now be applied successfully to live activities without triggering validation errors, ensuring a smoother experience in the updated activity-create UI. (TGT-53738)
* **Fixed an issue where products were not visible in collections within the [!UICONTROL Recommendations] UI.** Customers from a single tenant reported that product lists failed to load when viewing certain collections in the [!UICONTROL Recommendations] section of the New UI. The issue was temporarily resolved by switching environments, but this workaround led to a poor user experience. Product entities now load consistently without requiring environment toggling. (TGT-53783)
* **Fixed an issue where criteria and designs were not displayed on one line in the activity-create UI.** Previously, criteria and designs in the activity-create process were shown in a compressed format, making it difficult for customers to view and manage individual items. Each criterion and design now appear on its own line, improving readability and usability in the updated UI. (TGT-53818)

+++

**Reports**

+++See details

* **[!UICONTROL Total Revenue] metric is now included in CSV exports from activity reports.** Resolved an issue in the updated [!UICONTROL Overview] UI where total revenue was displayed correctly in the activity report view but was missing from the CSV export, showing as $0. This discrepancy prevented users from relying on exported data for offline analysis and reporting. (TGT-53325)
* **[!UICONTROL Total Sales] metric is now included in CSV exports from activity reports.** Resolved an issue in the updated UI where the [!UICONTROL Total Sales] metric appeared correctly in the activity report view but was missing from the CSV export. This discrepancy prevented users from accessing complete performance data in downloaded reports. This fix ensures that [!UICONTROL Total Sales] values are now accurately included in CSV exports, restoring consistency between in-app reporting and offline analysis. (TGT-53330)
* **Improved error messaging for [!UICONTROL Graph View] when metrics are not enabled.** Fixed an issue in the VEC where the [!UICONTROL Graph View] displayed a generic "Something went wrong" message when a requested metric was not enabled in the associated [!DNL Analytics] report suite. This issue was triggered by a `not_enabled_metric` error in the backend GraphQL response. This fix replaces the vague error with a more informative message that helps users identify configuration issues in [!DNL Analytics], reducing confusion and unnecessary support escalations. (TGT-53577)
* **Fixed an issue where the report duration exceeded the supported limit of 90 days.** Customers using the "[!UICONTROL Last X Days]" filter in the [!UICONTROL Reports] section were able to select durations longer than 90 days, which could lead to performance issues and incomplete data. The filter has been updated to enforce a maximum range of 90 days, ensuring consistent and reliable reporting. (TGT-53795)
* **Fixed an issue where performance CSV reports were generated using the default environment instead of the selected one.** Previously, when customers changed the environment in report settings and generated a performance report, the resulting CSV contained data from the default environment rather than the selected one.  The UI now correctly passes the `environmentId` parameter, ensuring that the report reflects the chosen environment. Additionally, error handling has been improved. If GraphQL errors occur during CSV generation, the UI now displays a clear error message instead of producing an empty CSV file. (TGT-53064)
* **Fixed an issue where Analytics for Target (A4T) reporting failed to display data in [!UICONTROL Graph View].** Customers using [!DNL Target] with A4T integration encountered a "Something went wrong" error when switching to Graph View in the Reporting tab of A/B test activities. Although the [!UICONTROL Table View] loaded correctly, [!UICONTROL Graph View] failed to render metric trends over the selected time range. [!UICONTROL Graph View] now displays performance data as expected for all supported metrics, improving visibility and reporting accuracy in the updated UI. (TGT-53573)

+++

**Visual Experience Composer (VEC)**

+++See details

* **Element metadata is now visible on hover in the breadcrumb menu.** Improved the breadcrumb menu in the VEC to show additional element details such as ID, class, and name when hovering over an item. This enhancement helps users identify and differentiate elements more easily during activity setup. (TGT-53409)
* **Breadcrumb hover now highlights the corresponding element in the VEC.** Improved the [!UICONTROL Visual Experience Composer] to highlight the corresponding element in the editor when hovering over items in the breadcrumb menu. The element type is also displayed, such as container, bold text, or button. This behavior applies to sibling elements and excludes unsupported types like SVG, based on the validation list. (TGT-53411)
* **Unsaved changes alert restored in VEC modification workflows.** Fixed an issue in the VEC where users were no longer notified about unsaved changes in custom code modifications. Unlike the legacy UI, the new experience lacked prompts when navigating away or closing the personalization editor, which led to accidental loss of progress. This fix restores alerts for all modification types, including custom code, and ensures that users are warned before exiting without saving. (TGT-53435).
* **Custom code changes now persist during page refresh in the VEC.** Fixed an issue in the VEC where custom code modifications were lost during website refreshes. This issue occurred on pages with multiple reloads, causing the editor to reset and revert unsaved changes. The fix ensures that custom code edits remain intact even if the page reloads during editing, preventing accidental loss of progress. (TTGT-53501)
* **Login issue resolved for site access within the VEC.** Fixed an issue where users were unable to log in to their site while accessing it through the VEC. The login flow repeatedly redirected users back to the login page, preventing activity setup and preview. This fix ensures that the VEC no longer interferes with login behavior, restoring expected access for authenticated users. (TGT-53524)
* **Cookie duplications issue resolved in VEC Helper extension.** Fixed an issue where the [!UICONTROL Adobe Experience Cloud Visual Editing Helper] extension was duplicating the `at_qa_mode` cookie during QA via preview links. When manually switching preview indices, multiple cookies were created with conflicting values across domains, preventing testers from reliably switching variants. This behavior was observed even outside the Target UI and affected both internal and client accounts. This fix ensures consistent cookie handling by preventing duplicate entries and aligning domain scope, allowing seamless variant switching without requiring manual cookie cleanup. (TGT-53579)
* **Fixed an issue where clicking elements on a certain homepage caused memory leaks.** Customers creating activities on this homepage experienced memory leaks when interacting with page elements. The issue was linked to excessive console warnings and increasing memory usage in subframes, particularly related to malformed srcset attributes. Memory usage now remains stable during interaction. (TGT-53761)
* **Fixed an issue where the VEC crashed and displayed a blank screen when loading certain activities.** Customers from a specific tenant reported that the editor failed to load specific activities. The VEC remained stuck on "Applying initial modifications" before crashing and showing a blank screen. The VEC now loads affected activities without errors in the updated activity-create process. (TGT-52932)
* **Fixed an issue where the [!UICONTROL Manage Content] rail in [!UICONTROL Automated Personalization] activities displayed inconsistent location labels.** Customers reported that the [!UICONTROL Manage Content] rail showed mismatched location numbers across the [!UICONTROL Experiences] and [!UICONTROL Offers] tabs. (for example, Location 2 and Location 4 in Experiences, and Location 1 and Location 2 in Offer) even when only two locations were configured. Location labels are now consistent and accurately mapped to modifications, improving clarity and usability in the activity-create process. (TGT-52934)
* **Fixed an issue where modifications in the VEC were lost after saving.** Customers reported that after saving a modification in the VEC, the page would refresh and revert the change to its previous version. This issue caused the most recent updates to be lost unless the entire activity was saved immediately. Modifications now persist correctly after saving, and the editor no longer reverts changes unexpectedly, ensuring a reliable experience in the activity-create workflow. (TGT-53500)
* **Enhanced element selection in the VEC by displaying element type on hover and selection.** To improve usability during activity creation, the VEC now decorates HTML elements with their type when hovered over or selected. This enhancement helps customers more easily identify and select the correct elements. Selected elements are highlighted with a distinct color, and hovered elements are outlined in blue. The element type is also displayed, providing clearer context during editing. (TGT-53502)

+++

### Datastream updates (September 19, 2025)

Datastream ID and sandbox combination must be unique for [!DNL Adobe Target] destination connections.

Updated validation logic for [!DNL Target] destination connections to enforce that the combination of datastream ID and sandbox name must be unique within an IMS Org. This means:

* The same datastream ID + sandbox name pair cannot be reused across multiple [!DNL Target] destination connections.
* The same datastream ID can be used for different connections only if they are configured in different sandboxes.
* This rule applies to all datastream selections, including when "None" is selected.

This update ensures consistent configuration and prevents conflicts across multi-sandbox environments. For more information, see [Adobe Target connection](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} in the *Experience Platform Destinations* guide.

### [!DNL Target Standard/Premium] 25.9.1 (September 5, 2025)

This release contains the following updates and fixes:

**[!UICONTROL Experience Fragments]**

+++See details

* **Improved user attribution for [!UICONTROL AEM Experience Fragment] offers.** Resolved an issue in the VEC where the "[!UICONTROL Last updated]" field for [!UICONTROL AEM Experience Fragment] (XF) offers incorrectly displayed a Code ID instead of the user name. This discrepancy occurred during offer selection in the updated UI, creating inconsistency with the legacy UI and HTML offers, which correctly showed the name of the last editor. This fix ensures consistent user attribution across offer types, improving transparency and alignment with expected behavior. (TGT-52880 & TGT-52898)

+++

**Offer Decisioning**

+++See details

* **Offer Decision error resolved for ODE offers.** Resolved an issue where Offer Decision Engine (ODE) offers injected through [!DNL Target] returned a 400 error due to missing format metadata. The error message indicated that the MIME type was null, preventing successful processing of offer decisions. This fix ensures proper handling of offer metadata, restoring functionality for personalized content delivery and enabling uninterrupted execution of marketing campaigns. (TGT-53635)
* **ODS offer rendering issue resolved.** Resolved an issue where [!DNL Offer Decision Service] (ODS) offers created via [!DNL Adobe Journey Optimizer] (AJO) were not rendering when activities were built using the VEC in the updated UI. The same configuration worked correctly in the legacy UI, leading to confusion and blocked campaign execution. This fix ensures consistent offer delivery across both UI versions, restoring expected behavior for AJO-driven personalization.

+++

**Reports**

+++See details

* **Download option restored in reports section of the updated Reports overview UI.** Resolved an issue in the new overview UI where the [!UICONTROL Download] button was missing from the Reports section, preventing users from exporting attribute importance scores. This update restores full export functionality, enabling streamlined access to downloadable data for analysis and reporting. (TGT-53222)
* **[!UICONTROL Download full CSV report] button restored in the [!UICONTROL Important attributes] view.** Resolved an issue in the updated activity creation UI where the [!UICONTROL Download full CSV report] button was missing from the [!UICONTROL Important Attributes] section in the reports view. This fix restores access to downloadable insights, ensuring consistent functionality across both the updated and legacy UIs. (TGT-53238)
* **Resolved UI issues affecting [!UICONTROL Auto Target] reporting in the updated overview UI.** Fixed multiple UI issues in the updated overview interface impacting [!UICONTROL Auto Target] activity reporting. These fixes include:

  * Missing lift and confidence metrics in summary reports
  * Incorrect color indicator for the "models built" checkbox
  * Non-functional graph report despite data variance in [!DNL Analytics]
  * Missing download link for [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes] reports
  * Broken [!UICONTROL Automated Segments] report display

  These fixes restore expected reporting behavior and improve visibility into [!UICONTROL Auto Target] performance across the updated UI. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++See details

* **Form validation corrected for parameter presence conditions in updated UI.** Resolved an issue in the updated UI where selecting "[!UICONTROL Custom mbox parameter value is present]" or "[!UICONTROL Parameter is present]" incorrectly required customers to enter a value. This behavior conflicted with the intended logic, which simply checks for the existence of a parameter regardless of its value. The fix aligns form validation with expected behavior, enabling smoother activity setup and supporting full adoption of the updated UI. (TGT-53638)
* **Form logic corrected for parameter presence rules in page delivery."** Resolved an issue in the updated UI where selecting page delivery rules such as "[!UICONTROL Parameter is present]," "[!UICONTROL Parameter is not present],"[!UICONTROL Parameter value is present]," or "[!UICONTROL Parameter value is not present]" incorrectly required users to enter an additional parameter value. This behavior was inconsistent with the legacy UI and contradicted the intended logic of detecting parameter presence without specifying a value. This fix restores expected rule configuration behavior, streamlining activity setup and improving usability. (TGT-53640)
* **Validation logic improved for multi-page rule builder in the updated UI.** Resolved multiple validation issues in the multi-page rule builder within the updated UI. These fixes include:

  * Preventing rule creation when the mbox parameter is empty
  * Displaying appropriate error messages for invalid rule states
  * Correcting validation logic for unary and parameter-based operators that don't require operand values
  * Enabling hash fragment rules with unary operators by restoring save functionality

  These updates ensure accurate rule configuration and improve usability across complex page delivery scenarios. (TGT-53722)
* **Location rename issue resolved in A/B and MVT activities.** Fixed a bug in the updated UI where renaming a location in an [!UICONTROL A/B Test] or [!UICONTROL Multivariate Test] (MVT) activity did not persist after navigating between the location list, targeting, and back. This update ensures that location name changes are saved and consistently reflected throughout the activity workflow. (TGT-52367)
* **Location name persistence fixed for MVT and AP activities in the updated UI.** Resolved an issue in the updated UI where location names edited in [!UICONTROL Multivariate Test] (MVT) and [!UICONTROL Automated Personalization] (AP) activities were not saving correctly. After renaming a location, navigating between tabs, such as [!UICONTROL Targeting] and [!UICONTROL Experiences], caused the names to revert to their previous state. This fix ensures consistent location naming across tabs and improves reliability during activity setup. (TGT-52927)
* **Location labeling corrected in the manage experiences panel for MVT activities.** Resolved an issue in the updated UI where the [!UICONTROL Manage Experiences] panel in [!UICONTROL Multivariate Test] (MVT) activities displayed inconsistent location numbering. This fix ensures that location labels are sequential and correctly aligned with user-defined modifications, improving clarity and usability during experience setup. (TGT-52929)

+++

### [!DNL Target Standard/Premium] 25.8.4 (September 1, 2025)

This release contains the following updates and fixes:

**[!UICONTROL Activities]**

+++See details

* **Customers could not copy activity or document names from the [!UICONTROL Activity Overview]**: Previously, customers were unable to copy the name of an activity or the associated offer/document directly from the [!UICONTROL Activity overview] in the updated activity-create process. This limitation impacted usability, especially on smaller screens. Customers can now easily copy both activity and document names without workarounds. (TGT-51850)
* **Proactive ingestion of curated [!DNL Target] customer data during activity creation**: Improved the activity-create process by enabling the proactive collection of reports, content, and screenshots from [!DNL Target] customers. This enhancement addresses data gaps identified in existing use cases and helps ensure more accurate insights during activity and experiment setup. (TGT-52415)
* **AP activities did not fetch model-ready data in the [!UICONTROL Reports] section**: Customers viewing Automated Personalization (AP) activities in the [!UICONTROL Reports] section were unable to see model-ready indicators at the report group and offer level. This issue occurred because model-ready data was not being fetched correctly from the backend. The functionality has been restored, and model-ready data now appears as expected. (TGT-53600 & TGT-53601)
* **Activities scheduled for the future incorrectly displayed a "[!UICONTROL Live]" status in the [!UICONTROL Activity] overview**: Customers observed that activities scheduled to start in the future were incorrectly marked as "[!UICONTROL Live]" in the [!UICONTROL Activity] overview. This status mismatch was resolved, and scheduled activities now correctly display as "[!UICONTROL Scheduled]" without requiring a page refresh. (TGT-52835)

+++

**[!UICONTROL Recommendations]**

+++See details

* **Product list was not visible in the [!UICONTROL View Collection] dialog:** Previously, customers were unable to see the product list when viewing a collection in the [!UICONTROL Recommendations] tab. The [!UICONTROL View Collection] dialog now correctly displays the associated products, improving transparency and usability in the updated [!UICONTROL Recommendations] UI. (TGT-50531)
* **Fixed an issue that caused case-sensitive filtering in [!UICONTROL Product Catalog Search] advanced search**: The advanced search filtering in the [!UICONTROL Product Catalog Search] page now correctly ignores case sensitivity, aligning with the behavior of both the backend and GraphQL services. This update ensures consistent and accurate suggestion results for customers regardless of text casing. (TGT-53585)
* **Advanced search in the updated [!UICONTROL Product Catalog Search] UI did not provide suggestions**: Customers using the advanced search feature in the updated [!UICONTROL Product Catalog Search] UI were required to enter exact values with correct spelling, as no suggestions were displayed. This issue made it difficult to locate products efficiently. Suggestions now appear as expected during advanced search input. (TGT-52008)
* **Some approvers were unable to view products in [!UICONTROL Product Catalog Search]**: Customers with [!UICONTROL Approver] permissions were unable to see any products in [!UICONTROL Product Catalog Search], despite other users with identical roles having access. This issue was caused by a permissions inconsistency affecting catalog visibility. All approvers can now view products in the [!UICONTROL Recommendations] section as expected. (TGT-53617)

+++ 
 
**[!UICONTROL Reports]**

+++See details

* **Reports failed to load for the Desktop audience due to an invalid audience name error**: Customers encountered a GraphQL error when attempting to view reports for the one audience in the activity-create process. The system returned an "Invalid audience name: XXXXX" message, preventing access to reporting data. Reports now load correctly for the Desktop audience. (TGT-53371)
* **Switching audiences on the Reports page caused errors in the Target UI**: Customers encountered errors when selecting certain audiences in the [!UICONTROL Reports] section. This issue was caused by invalid audience handling in backend GraphQL calls, resulting in unexpected errors and missing data. The issue has been resolved, and desktop audiences now load without errors—even when no data is available. (TGT-53370)
* **[!UICONTROL Graph view] in the [!UICONTROL Reports] section did not display values from [!DNL Analytics]**: Customers accessing [!UICONTROL Graph view] in the Re[!UICONTROL ]ports section encountered missing data, with all values appearing as zero. This issue was caused by incorrect data retrieval from [!UICONTROL Analytics]. [!UICONTROL Graph view] now displays accurate values as expected. (TGT-52792)
+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Clicking "Accept Cookies" using the [!UICONTROL Enhanced Experience Composer] (EEC) failed due to a missing function**: Customers reported that attempting to accept cookies via the EEC resulted in a console error: `handleclickAcceptAllButton is not defined`. The cookie acceptance functionality now works as expected, ensuring a smoother experience during activity creation in the updated UI. (TGT-52794)
* **The new EEC UI failed to load certain pages that were previously supported in the legacy UI**: Customers reported that the new EEC could not load some pages, which were accessible in the legacy UI despite iframe-busting code present on the site. The updated activity-create process now supports loading these pages, restoring compatibility for activity creation workflows. (TGT-53061)
* **The VEC displayed a blank white screen when editing experiences**: Customers from a certain tenant reported that the VEC screen went blank when attempting to edit experiences in the updated VEC. This issue affected both newly created and older activities, preventing workflow continuity. The VEC now loads correctly, allowing customers to edit experiences without interruption. (TGT-53547)
* **The VEC crashed and displayed a blank screen when loading certain activities**: Customers from a certain tenant reported that the VEC failed to load specific activities. The experience editor remained stuck on "Applying initial modifications" before crashing and showing a blank screen. Console errors indicated a failure to read undefined properties. The editor now loads affected activities without errors in the updated VEC. (TGT-53548)
* **Clearing all date values using Backspace caused the page to crash**: Customers scheduling activities in the [!UICONTROL Goals & Settings] section experienced a crash when using Backspace to clear all values from the "[!UICONTROL Specified Date & Time]" fields. This issue was caused by a null reference error in the date-handling logic. The page now handles empty date inputs gracefully without crashing. (TGT-53624)
* **No products appeared in [!UICONTROL Product Catalog Search] due to an invalid payload**: Customers accessing the [!UICONTROL Recommendations] section in [!UICONTROL Product Catalog Search] encountered empty results caused by an invalid GraphQL payload. This backend error prevented product data from loading correctly. Products now display as expected in the updated UI. (TGT-53630)
* **[!DNL Scene7] images were saved with lower resolution in the updated VEC**: Customers editing experiences in the updated VEC noticed that [!UICONTROL Scene7] image URLs were saved without resolution parameters, resulting in lower-quality images being delivered (400×400 instead of the intended 800×800). Image URLs now retain the correct parameters to ensure proper resolution. (TGT-52631)
* **live activities could still be edited in the VEC**: Customers were able to access edit options for live activities in the updated VEC, which could lead to unintended changes. This issue has been resolved by disabling edit functionality for live activities. Edit buttons are now hidden in the activity list and overview for editors, while approvers and other roles remain unaffected. (TGT-53055)
* **Decommissioned the [!UICONTROL Failed] and [!UICONTROL Draft] activities section in the updated VEC**: The [!UICONTROL Failed] and [!UICONTROL Draft] activities options have been removed from the updated VEC. The new UI no longer supports draft states and failing campaigns are not stored in the backend. These options are no longer relevant. Related filters and backend fields (for example, `uiSyncFailed`, `errorMessage`) have also been removed to streamline activity management. (TGT-53150)
* **Unable to log in to the VEC for an activity**: Customers attempting to log in to their site through the VEC were repeatedly redirected to the login page, preventing access to activity editing. This issue was not reproducible internally and may have been related to site-side session handling. The login flow has been stabilized, and customers can now access the VEC without redirection errors. (TGT-53524)
* **Pressing the back button twice in [!UICONTROL Browse] mode caused the VEC to crash**: Customers navigating through [!UICONTROL Browse] mode in the VEC experienced crashes when pressing the browser's back button twice. This issue caused the editor to freeze and required a page refresh. The editor now handles back navigation reliably without crashing. (GT-53568)
* **Activities could not be edited due to undefined location mappings**: Customers encountered an error when attempting to edit activities, caused by undefined location IDs in the `LocationMapping.behaviorTargetedActivity` logic. This issue resulted in a 400 error and blocked activity updates. Activities can now be edited without location-related validation errors. (TGT-53607)
* **Saving activities triggered an invalid user input error**: Customers encountered an invalid user input error when attempting to save activities after making minor modifications in the updated VEC. The error was caused by mismatched location mappings in the backend validation logic. Activities can now be saved successfully without triggering location-related errors. (TGT-53603)

+++

### [!DNL Target Standard/Premium] 25.8.3 (August 21, 2025)

This release contains the following updates and fixes:

**[!UICONTROL Activities]**

+++See details

* **Fixed an issue where saving activities triggered an invalid user input error due to malformed property data**: Customers encountered a critical error when attempting to save existing activities. The error message indicated invalid user input, specifically referencing an unrecognized property name content in the JSON payload. Notably, new activities using the same property were saved successfully, suggesting the issue was isolated to legacy activity data. The activity-create process now correctly handles legacy property configurations, preventing invalid input errors and ensuring consistent save behavior across new and existing activities. (TGT-53507)
* **Fixed an issue that prevented customers from saving an activity due to an InvalidProperty.Json error**: Customers encountered an error when attempting to save an activity in the updated UI, even without making any modifications. The error message indicated an invalid JSON structure: "Invalid Json. Unrecognized property name 'content'. Location: line - 1, column - 432." This issue was caused by an unrecognized property in the request payload and has now been resolved. Customers can save activities successfully without encountering this error. (TGT-53513)
* **Fixed an issue where scheduled activities incorrectly displayed a [!UICONTROL Live] status until page refresh**: Customers observed that when scheduling an activity to go live at a future date and time, the status immediately appeared as [!UICONTROL Live] instead of [!UICONTROL Scheduled]. This caused confusion, even though the confirmation message correctly indicated that the activity was scheduled. Refreshing the page corrected the status display. This issue has now been resolved, and scheduled activities correctly show the Scheduled status without requiring a refresh. (TGT-52937)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details

* **Fixed an issue where customers could not type report suite names during the activity-create process**: Customers using [!DNL Adobe Analytics] as the reporting source during the activity-create process were unable to type into the [!UICONTROL Report Suite] drop-down list to search for specific report suites. This impacted workflows for organizations with large numbers of report suites, where manual scrolling significantly delayed setup. The drop-down list was not alphabetically ordered and did not consistently respond to typed input, making it difficult to locate report suites like "Office + Store - Web - Prod." This issue has been resolved, and customers can now efficiently search by typing report suite names. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++See details

* **Fixed an issue where expired "Time Frame" audiences blocked activity saving even after removal**: Customers were unable to save activities in the updated UI due to an error related to expired "Time Frame" audiences. Even after removing the affected audience, the error message persisted: "Activity contains audience with invalid time frame." This issue occurred because the system continued to validate the activity-only audience, even when it was no longer in use. The behavior was further complicated by time-zone discrepancies. The validation logic has been corrected, and customers can now save activities without encountering this error. (TGT-53517)

+++

**[!UICONTROL Experience Fragment]s**

+++See details

* **Fixed an issue that prevented customers from inserting Experience Fragments using [!UICONTROL Insert Before] or [!UICONTROL Insert After] in the UI** Customers encountered an error when attempting to insert [!UICONTROL Experience Fragments] into an activity using the "Insert Before" or "Insert After" options in the updated UI. The error message displayed was: "Offer content must contain exactly one HTML element." This issue was specific to the updated UI and did not occur in the previous version. This issue has now been resolved, and customers can successfully insert [!UICONTROL Experience Fragments] without encountering this error. (TGT-53442)

+++

**[!UICONTROL Offer decisions]**

+++See details

* **Fixed an issue preventing customers from editing decision offers and selecting specific page elements in the updated UI**: In the updated activity-create process, customers were unable to edit existing decision offers or select specific page elements in the Visual Experience Composer (VEC). Decision offers were incorrectly displayed as HTML offers, and changes made during editing were not saved. Additionally, certain regional URLs, such as the Japan site, failed to load properly in VEC, blocking activity creation and updates. Decision offers now display correctly, page elements are selectable as expected, and regional URLs load properly in the VEC, restoring full editing functionality. (TGT-53425)
* **Fixed an issue where [!UICONTROL Offer Decision] selectors could not be modified and changed unexpectedly after saving**: In the updated activity-create process, customers were unable to modify the [!UICONTROL Offer Decision] selector as intended. Attempts to change the selector were unsuccessful, and the selector reverted to an incorrect value after saving. This behavior caused the decision offer to disappear from the Visual Experience Composer (VEC), blocking further edits. Selector changes are now preserved correctly, and decision offers remain visible and editable in the VEC after saving.(TGT-53433)
* **Fixed an issue where [!UICONTROL Offer Decisions] disappeared from the activity after saving**: [!UICONTROL Offer Decisions] added during the activity-create process were not retained after saving and reopening the activity. This issue occurred when editing dynamic content and inserting [!UICONTROL Offer Decisions ]with specific selectors and properties. [!UICONTROL Offer Decisions] now persist correctly after saving, and selectors remain intact, ensuring consistent targeting and editing behavior. (TGT-53434)

+++

**[!DNL Recommendations]**

+++See details

* **Fixed issue in [!DNL Recommendations] UI where custom criteria CSV download returned 404 error**: Fixed an issue where customers were unable to download the custom criteria CSV in the activity-create process. The download link now functions correctly, allowing customers to export custom criteria as expected. (TGT-51966)
* **Fixed inconsistent image loading in [!UICONTROL Catalog Search]**: Fixed an issue where thumbnails and images in[!UICONTROL  Catalog Search] were not loading consistently in the activity-create process. Images failed to appear unless the "Thumbnail URL" column was visible and some product images loaded partially or not at all after navigation or search actions. Image loading behavior has been stabilized, and thumbnails now display reliably regardless of column visibility or navigation actions. (TGT-52778)
* **Fixed an issue where editing a recommendation in a duplicated experience impacted the original experience**: Customers reported that modifying a recommendation in a duplicated experience unintentionally altered the original experience. Specifically, after duplicating Experience B in the activity-create process and editing its design or criteria, the same changes were reflected in the original Experience B, despite being separate entities. Duplicated experiences now maintain separate configurations, ensuring that edits to one experience do not affect the original. (TGT-53369)
* **Fixed an issue where changes to a duplicated experience unintentionally affected the original experience in an activity**: Customers reported that when duplicating an experience within an activity and assigning a new audience, any changes made to the duplicated experience's design or criteria were also reflected in the original experience. This issue occurred even though no edits were made directly to the original version, impacting the ability to create independent variations within the same activity. The activity-create process now correctly isolates duplicated experiences, ensuring that edits made to one experience do not affect the original. (TGT-53361)
* **Fixed an issue where the [!UICONTROL Recommendation Catalog] intermittently failed to display complete product attribute data**: In the updated [!DNL Recommendations] UI, customers experienced an issue where certain product attributes, such as message, were not consistently displayed in the [!UICONTROL Catalog Search] results, even though the data existed in the feed. This issue required customers to manually reconfigure the column visibility to retrieve the missing values. [!UICONTROL Catalog Search] now reliably displays all configured attributes, eliminating the need for manual column resets. (TGT-52769)
* **Fixed an issue where a [!UICONTROL Front Promotion] could not be disabled in a live activity**: Attempts to disable a [!UICONTROL Front Promotion] in a live activity were not saved. After selecting [!UICONTROL Change Promotion] and disabling it, the promotion remained active upon re-editing the activity, preventing updates to recommendation configurations. Promotion settings now save correctly, allowing customers to disable or modify promotions in live activities as expected. (TGT-53231)
* **Fixed an issue where enabling a [!DNL Recommendations] [!UICONTROL Promotion] without data triggered an unclear error message**: Enabling a [!UICONTROL Front] or [!UICONTROL Back Promotion] in a [!DNL Recommendations] activity without specifying required values resulted in a generic "Invalid input error" message. The underlying issue was a missing configuration field, but the error message did not clearly indicate the cause, making troubleshooting difficult. The activity-create process now provides a clear and actionable error message when required fields, such as `collectionId` or rules, are missing, helping customers quickly identify and resolve configuration issues. (TGT-52616)
* **Fixed an issue that prevented the [!UICONTROL Product] list from displaying in the [!UICONTROL Edit] modal within the [!UICONTROL Recommendations] tab**: Customers were unable to view the filtered product list when editing a [!UICONTROL collection] or [!UICONTROL exclusion] in the [!UICONTROL Recommendations] tab. The list was expected to update in real time based on applied rules, but it did not appear as intended. This issue has been resolved, and the product list now displays correctly and updates dynamically as rules are modified. (TGT-53481)
* **Fixed an issue with the layout of the View Details dialog in the updated UI**: The layout of the View Details modal in the updated UI has been modified to improve clarity and usability. The dialog now includes two tabs:
  * [!UICONTROL Details] tab: Displays all relevant information for the selected item.
  * [!UICONTROL Inventory] tab: Shows all products filtered by the current collection and exclusion rules.

  This enhancement helps customers more easily navigate and understand item-specific data and inventory context within the activity-create process. (TGT-53503)

  * **Fixed an issue where removed promotions in recommendation activities reappeared after saving**: Customers reported that when [!UICONTROL front] or [!UICONTROL back] promotions were removed from [!DNL Recommendations] activities and the activity was saved, the promotions continued to appear upon reopening. This issue occurred in both staging and production environments and affected the updated activity-create process. The issue has been resolved. Promotions that are removed from an activity now persist correctly after saving. (TGT-53490)

+++

**Reports**

+++See details

* **Fixed an issue where the [!UICONTROL Automated Segments] report displayed null audience values**: Customers reported that [!UICONTROL Automated Segments] in activity reports were showing null for audience data, preventing accurate analysis of segment performance. This issue occurred when accessing the [!UICONTROL Reports] section and selecting [!UICONTROL Automated Segments], even though valid audience data was expected. [!UICONTROL Automated Segments] now correctly displays audience values, ensuring reliable reporting and segmentation insights. (TGT-52793)

+++

**Singe Page Applications (SPAs)**

+++See details

* **Fixed an issue where switching between [!UICONTROL Browse] and [!UICONTROL Design] modes reset SPA state in the updated UI**: Customers reported that switching between [!UICONTROL Browse] and [!UICONTROL Design] modes in the updated UI caused the web editor to reload, resetting the state of SPAs. This issue disrupted workflows and required customers to re-enter information. The issue has been resolved. SPA state is now preserved when toggling between modes, ensuring a smoother and more consistent experience during activity creation. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* **Fixed issue in the activity-create process that blocked progression to the [!UICONTROL Targeting] step in AP activities**: Fixed an issue in the activity-create process where customers were unable to proceed to the [!UICONTROL Targeting] step in [!UICONTROL Automated Personalization] (AP) activities unless two locations were added. This behavior differed from the previous experience, where a single location with multiple offers was sufficient. The requirement has been corrected, allowing customers to continue using single-location setups as part of their AP workflows. (TGT-53426)
* **Fixed an issue where the new activity-create process did not set the fmt=png-alpha parameter for transparent images**: In the updated UI, images inserted during the activity-create process no longer included the `fmt=png-alpha` parameter by default, resulting in loss of transparency. This behavior differed from the previous UI, which automatically appended the parameter to image URLs, preserving transparent backgrounds. The activity-create process now correctly applies the `fmt=png-alpha` parameter to image URLs when transparency is required, ensuring consistent rendering of transparent assets. (TGT-52615)
* **Fixed an issue that prevented customers from searching report suites in the updated UI**: In the updated UI, the [!UICONTROL Report Suites] drop-down list in the [!UICONTROL Goals & Settings] section did not allow customers to type and search, making it difficult to locate specific report suites, especially for tenants with a large number of entries. Unlike the previous UI, the list was not sorted and lacked input-based filtering. This issue has been resolved. Customers can now type to search and filter report suites, restoring the functionality available in the legacy UI. (TGT-53514)

+++

**[!UICONTROL Workspaces]**

+++See details

* **Fixed an issue where a customer restricted to a single workspace could view activities from other workspaces**: Customers with access limited to one workspace were unexpectedly able to view activities across all workspaces when selecting [!UICONTROL All Workspaces] in the activity-create process. This visibility posed a risk of unintended changes to live activities in other workspaces, potentially impacting website performance. Workspace access controls have been reinforced to ensure that customers can view and interact only with activities within their assigned workspace. (TGT-53101)
* **Fixed an issue where a customer could view activities from the [!UICONTROL Default Workspace] without having access:** A customer with access limited to the staging workspace was able to view activities from the [!UICONTROL Default Workspace] via the activity-create process. This behavior occurred despite correct backend configuration and access rights. Workspace access controls have been reinforced to ensure that customers can view activities only within their assigned workspace.(TGT-53297)

+++

### [!DNL Target Standard/Premium] 25.8.2 (August 14, 2025)

This release includes the following fixes and updates:

**[!UICONTROL Activities]**

+++See details

* **Fixed activity-loading issue in updated [!DNL Target] UI**: Fixed an issue in the updated [!DNL Target] UI where certain activities failed to load when attempting to edit. This issue caused customers leaving users in an indefinite loading screen. This issue impacted multiple activities and was reported to occur inconsistently across customers. With this fix, affected activities now load properly, allowing seamless editing and reducing disruption to activity workflows. (TGT-53209)
* **Fixed save error in activity-create process due to `optionLocalId` validation**: Fixed an issue in the activity-create process that prevented customers from saving changes due to a backend validation error: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` This issue occurred when modifying specific elements within an activity, resulting in a failed save operation. The fix ensures that `optionLocalId` references are now correctly validated, allowing customers to save activities without encountering this error. (TGT-53293)
* **Fixed crash in activity-create process caused by invalid option references when switching pages**: Fixed an issue in the activity-create process that caused the UI to crash after switching pages three times during editing. The crash was triggered by invalid option references, resulting in console errors such as "Option with localId '7' not found." With this update, customers can now switch between pages and apply modifications without encountering system failures or interruptions. (TGT-53295)
* **Fixed save error in activity-create process caused by invalid user input when editing experiences**: Fixed an issue in the activity-create process where customers were unable to save changes to an activity due to an invalid user input error. The error occurred when modifying experiences in the updated UI, preventing updates from being committed. The activity can now be saved successfully, allowing customers to edit and publish without interruption. (TGT-53267)
* **Fixed loading issue in activity-create process that blocked editing in updated UI**: Fixed an issue in the activity-create process where customers were unable to edit activities in the updated UI due to a continuous loading screen. Customers can now open and modify activities without encountering loading failures. (TGT-53415)
* **Fixed experience requirement issue in activity-create process for AP activities in updated UI**: Fixed an issue in the activity-create process where [!UICONTROL Automated Personalization] (AP) activities required two locations instead of two experiences in the updated UI. This behavior blocked use cases where customers configured a single location with multiple offers, which was previously supported. The requirement has been corrected to match the original functionality, allowing customers to proceed with AP activities using two experiences regardless of location count. (TGT-53429)
* **Fixed tracked element field behavior in Click Track mode to prevent unsaved input and improve clarity**: Fixed an issue in the activity-create process where the [!UICONTROL Tracked Element] field in [!DNL Click Track] mode was editable but did not retain the entered name, causing confusion for customers. The field is now disabled to prevent unsaved input, and the naming of selected elements has been clarified to improve goal configuration and tracking accuracy.** (TGT-53458)
* **Fixed issue in activity-create process that blocked naming of tracked components in [!UICONTROL Click Track] mode**: Fixed an issue in the activity-create process where customers were unable to name tracked components in [!UICONTROL Click Track] mode. After entering a name, the field appeared editable but did not retain the input, defaulting to generic labels like "MY PRIMARY GOAL 0" in edit mode. The tracked element field is now disabled, and naming behavior has been clarified to improve goal setup and tracking accuracy. (TGT-51396)

+++

**Experience Fragments (XFs)**

+++See details

* **Fixed issue in activity-create process that allowed unintended HTML editing of AEM-exported fragments**: Fixed an issue in the activity-create process that allowed customers to edit the HTML of [!DNL Experience Fragments] (XFs) exported from [!DNL Adobe Experience Manager] (AEM) within [!DNL Target]. This behavior was unintended, as XFs should remain locked for editing once published from AEM. The fix ensures that the "Edit HTML" option is no longer available for AEM-exported fragments, preserving content integrity and expected governance. (TGT-53286)
* **Fixed intermittent preview issue for XF content in activity-create process within updated UI**: Fixed an issue in the activity-create process where XF content intermittently failed to render in preview mode within the updated UI. Although the content delivered correctly, the preview did not consistently display, making it difficult for customers to validate offer setup. XF previews now load reliably, improving confidence and efficiency during activity configuration. (TGT-53318)

+++

**QA mode**

+++See details

* **Fixed issue in activity-create process where leading spaces in URLs caused broken QA links**: Fixed an issue in the activity-create process where leading spaces in the activity URL were not trimmed properly when saving. This caused invalid QA links and incorrect formatting in the back-end. After the update, URLs are now saved cleanly, preventing broken links and improving the reliability of QA workflows for customers. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++See details

* **Fixed issue in catalog search UI where advanced search failed to provide suggestions**: Fixed an issue in the new [!UICONTROL Catalog Search] UI where the [!UICONTROL Advanced Search] feature failed to provide suggestions. Users were required to input exact values with precise spelling, making the search experience cumbersome and error-prone. With this fix, the [!UICONTROL Advanced Search] now offers relevant suggestions as users type, improving usability and reducing friction in locating products. (TGT-52008)
* **Resolved multiple UI and filtering issues to improve responsiveness and entity interaction**: Resolved several issues, including poor responsiveness of criteria details on small-screen devices, lack of results when selecting "All host groups" in the Environment filter, and inability to interact with entities that have no name. These fixes improve usability across screen sizes, ensure accurate filtering, and allow full interaction with all product entities, enhancing the overall experience for users. (TGT-52992)
* **Fixed missing product IDs in Recommendations detail view during activity creation**: Fixed an issue in the [!DNL Recommendations] activity-create process where product IDs were missing from the product detail screen, making it difficult for customers to copy or reference product IDs during workflows. Product IDs now appear clearly in the detail view, improving visibility and supporting more efficient product management for customers. (TGT-51964)
* **Fixed issue in activity-create process where product messages failed to display in recommendations view**: Fixed an issue in the activity-create process where the [!UICONTROL Message] column in the [!DNL Recommendations] view did not display product data, even though messages were present. Customers had to manually remove and re-add the column to temporarily reveal the content, which would often disappear again when scrolling or searching. This update restores consistent visibility of product messages, improving catalog navigation and review workflows. (TGT-52777)
* **Fixed issue in activity-create process where selecting 'All host groups' returned no results in recommendations view**: Fixed an issue in the activity-create process where selecting the "All host groups" environment in the [!DNL Recommendations] view returned no results. Customers can now view product data across all host groups as expected, improving visibility and filtering accuracy during activity setup. (TGT-53006)
* **Fixed issue in activity-create process where front-promotion toggle did not persist after saving**: Fixed an issue in the activity-create process where disabling the front promotion toggle in activity settings did not persist after saving. Customers attempting to remove the front promotion found the toggle re-enabled upon revisiting the activity, preventing proper customization. This update allows changes to be saved reliably, giving customers full control over promotion settings. (TGT-53215)
* **Fixed inconsistent sorting by [!UICONTROL Last Updated] column:** Fixed an issue in the activity-create process where sorting the catalog by the [!UICONTROL Last updated] column produced inconsistent results. Customers were unable to reliably organize product data based on update timestamps, making catalog review and management more difficult. Sorting now works as expected, improving accuracy and usability in the updated UI. (TGT-53116)

+++

**Visual Experience Composer (VEC)**

+++See details

* **Fixed activity loading and [!UICONTROL Cancel] button issues in activity-create process**: Fixed an issue in the activity-create process where certain activities failed to load, leaving customers unable to access modifications. Additionally, the [!UICONTROL Cancel] button was unresponsive, preventing customers from stopping the loading process or exiting the edit view. This fix ensures that activities now load reliably and the [!UICONTROL Cancel] button functions as expected, improving overall stability and user experience in the Visual Experience Composer. (VEC)(TGT-53218)
* **Fixed experience switching issue in updated VEC UI that blocked editing and disabled [!UICONTROL Cancel] button**: Fixed an issue in the updated VEC UI where modifications failed to load when switching between experiences in an Experience Targeting (XT) activity. Customers were unable to edit experiences beyond the one they initially entered, and the [!UICONTROL Cancel] button was either missing or unresponsive. This fix ensures that modifications now load correctly across all experiences and that the [!UICONTROL Cancel] button functions reliably, even without the Helper extension, improving editing workflows and reducing frustration. (TGT-53256)
* **Fixed white screen issue when switching between multiple experiences in activity-create process**: Fixed an issue where switching between multiple experiences caused a white screen. Also fixed an issue in the activity-create process where customers encountered a white screen when attempting to modify multiple experiences within an activity. This issue occurred after applying changes to two experiences and then selecting a third experience, preventing further edits. The update ensures smooth transitions between experiences, allowing customers to make modifications without interruption. (TGT-53266)
* **Fixed issue in VEC where custom code changes were not reliably saved across editing sessions**: Fixed an issue where custom code modifications made in the Visual Experience Composer (VEC) were not reliably saved in a single attempt. Customers reported that changes, such as styling updates or HTML edit, were intermittently missing from the website and QA URLs, even after using both the [!UICONTROL Edit Content] and final [!UICONTROL Save] buttons. This regression has been resolved, ensuring that all custom code changes persist as expected across editing sessions.** (TGT-53418)
* **Fixed missing `triggerViews` in updated UI during activity creation**: Fixed an issue in the activity-create process where `triggerViews` were not appearing in the updated UI, even though they were correctly implemented on the page. This impacted multiple customers and made it difficult to validate view-based triggers during activity setup. `TriggerViews` now display as expected, allowing customers to complete and test their configurations reliably. (TGT-53239)
* **Fixed view-loading issue in activity-create process for specific webpages in updated UI**: Fixed an issue in the activity-create process where views were not loading in the updated UI for specific webpages, despite being correctly implemented and visible in delivery or interact calls. This affected multiple customers and made it difficult to validate view-based targeting. Views now populate consistently across supported pages, improving reliability during activity setup. (TGT-53246)
* **Fixed intermittent view loading issue in activity-create process in updated UI**: Fixed an issue in the activity-create process where views intermittently failed to appear in the updated UI during activity editing. Although the correct view name was present in the network payload, it was not consistently recognized in the interface, impacting customers' ability to configure view-based personalization. Views now appear reliably, supporting smoother setup and validation workflows. (TGT-53223)
* **Fixed issue in activity-create process where tracked action names were not saved in updated UI**: Fixed an issue in the activity-create process where tracked action metrics could not be saved in the updated UI. After naming a tracked element and saving the activity, the name would reset to a default label when reopened, causing confusion and disrupting goal configuration. Tracked actions now retain their assigned names, allowing customers to set and manage conversion metrics accurately. (TGT-53453)

+++

### [!DNL Target Standard/Premium] 25.8.1 (August 7, 2025)

This release includes the following enhancements and fixes:

**Activities**

+++See details

* Fixed several issues with the updated UI, including errors when deleting page types due to spacing in input values, unreliable activity copying between workspaces, and malfunctioning page delivery rules in QA environments. (TGT-52703)
* Fixed an issue in the updated [!DNL Target] UI where users with the [!UICONTROL Editor] role were able to access and attempt to edit live activities, which should be restricted. The activity list and overview screens incorrectly displayed edit options for live activities, leading to potential unintended changes. (TGT-53055)
* Fixed an issue in the [!UICONTROL Advanced Search] UI where selecting the "value is present" or "value is not present" operators prompted users to enter an operand, which should not be required for these conditions. (TGT-51961) 
* Fixed an issue in the updated UI where attempts to copy activities from the staging to production workspace consistently failed, even in sandbox environments. Customers encountered various error messages, including "Anonymous audience already used by the activity" and "Invalid audience ID," despite using valid configurations and having appropriate workspace permissions. (TGT-52394)

+++

**Experience Fragments (XFs)**

+++See details

* Fixed an issue where Experience Fragment (XF) content fails to render in the [!UICONTROL Visual Experience Composer] (VEC) preview, despite working correctly in content delivery. (TGT-53318)

+++

**Localization**

+++See details

* Fixed a localization issue where the "Add Promotion" button in the "Promotions" section appeared unlocalized across multiple language environments in the QA tenant. (TGT-53263)

+++

**Offers**

+++See details

* Fixed an issue where editing an existing HTML offer via the Visual Experience Composer (VEC) caused all modifications to be removed from content delivery. The changes appear grayed out in the modification tab and are not reflected in QA previews, despite being correctly applied in the legacy UI. (TGT-52863)
* Fixed an issue in the updated [!DNL Target] UI where HTML offer modifications made in the [!UICONTROL Visual Experience Composer] (VEC) did not persist after navigating from the [!UICONTROL Targeting] tab back to [!UICONTROL Experiences]. (TGT-52874)
* Fixed an issue in the updated [!DNL Target] UI where inserting one HTML offer before and another after the same selector caused incorrect location generation. When customers returned from the [!UICONTROL Targeting] tab to the [!UICONTROL Experience] tab, only one selector was retained, resulting in lost modifications and broken content delivery. This behavior differed from the legacy UI, which correctly preserved both modifications with distinct location identifiers. (TGT-52891)
* Fixed an issue in the updated [!DNL Target] UI where clicking an added offer within the [!UICONTROL Modifications] rail caused the right-hand [!UICONTROL Configuration] panel to intermittently appear and disappear, making it difficult to interact with the offer settings. (TGT-53288) 
* Fixed an issue where HTML offers added to audience-specific variations within an activity did not consistently save or appear in the modification section. After switching between audiences during editing, previously applied offers sometimes disappeared or failed to render, disrupting validation and delaying activity readiness. (TGT-53440)
* Fixed an issue where copying an activity that included offers resulted in duplicate offers being created in the new activity. This behavior caused unnecessary clutter and confusion, particularly when moving activities between workspaces. The fix ensures that [!DNL Target] offers are now correctly copied into the destination workspace without duplication, streamlining activity management and improving workflow efficiency. (TGT-53454)

+++

**Single Page Applications (SPAs)**

+++See details

* Fixed an issue in the updated VEC that prevented customers from applying modifications to [!UICONTROL Single Page Application] (SPA) views. While activities created in the old UI supported view-specific targeting, the new UI failed to detect or allow edits to those views, with the view-switching controls appearing disabled. (TGT-52556)

+++

**Visual Experience Composer (VEC)**

+++See details

* Fixed an issue where modifications made to experiences within the [!UICONTROL Visual Experience Composer] were either not visible or appeared inconsistently in the UI. (TGT-TGT-53381)
* Fixed an issue in the updated VEC where the [!UICONTROL Manage Content] section failed to display alt text for experience thumbnails. This issue made it difficult for users to identify documents, especially when filenames were long or truncated. (TGT-52291)
* Fixed an error where customers encountered incorrect validation errors when configuring [!UICONTROL page delivery] rules in VEC activities. Specifically, operators like "equals any of" and "does not equal any of" triggered "Invalid input for the operator type" when entering text values, even though text should be supported. (TGT-52629)
* Fixed several issues that caused inconsistent behavior in the [!UICONTROL Modifications] panel of the updated UI when selecting offers using the "Select an offer" button. Instead of replacing the existing offer, the UI added a duplicate, and attempted to interact with either offer resulted in console errors such as `selectorNotFound`. Additionally, some offers do not display the "Select an offer" button, showing only editable properties. (TGT-53321)
* Fixed an issue in the updated [!DNL Target] UI where HTML code changes made during activity setup did not persist on variation pages, even though they saved correctly for control groups. Despite multiple attempts and recreating tests without page groupings, the variation pages consistently failed to retain modifications, impacting content delivery and QA validation. (TGT-53436)
* Fixed an issue in the updated VEC where the "equals any of" operator in page delivery rules fails to accept input values. When configuring customer parameters across all mboxes, selecting this operator resulted in an "Invalid Input" error, preventing rule creation. (TGT-52623)

+++

**Workspaces**

+++See details

* Improved the workflow when copying activities between workspaces. Copy activities between workspaces previously led to sync errors due to missing audiences and unassigned properties. This update introduces a smarter, more intuitive workflow that ensures copied activities are properly configured and ready for publishing. (TGT-47094)
* Fixed an issue where customers were unable to copy activities between workspaces due to a failure in the `copyActivityBatchOperations` mutation. Attempts to duplicate activities resulted in a server error (500) and a null response payload. (TGT-52405)
* Fixed an issue where activities failed to sync when offers referenced in the configuration were not accessible within the selected workspace. This caused publishing errors and left activities in a failed state. (TGT-52535)
* Fixed multiple issues when copying activities between workspaces in the updated [!DNL Target] UI. Customers encountered errors related to audience access, particularly with live activities, and incorrect privilege validation, even when the user had "[!UICONTROL Approver]" roles in both source and destination workspaces. (TGT-53002)
* Fixed an issue in the updated UI where copying activities within the same workspace unnecessarily duplicated associated offers and audiences. (TGT-53457)
* Fixed an issue to address cases where ad-hoc (anonymous) audiences were not correctly copied between non-default workspaces or from non-default to default workspaces. While earlier updates ensured proper duplication for default-to-non-default and same-workspace scenarios, this enhancement focused on preserving combined audience configurations that span multiple workspaces. The fix ensures consistent audience behavior and accurate targeting across all workspace transitions. (TGT-53268)

+++

### [!DNL Target Standard/Premium] 25.7.4 (August 1, 2025)

This release resolves recent issues, primarily caused by complex customer customizations, and includes the following fixes and improvements:

**Activities**

+++See details

* Fixed an issue where a customer encountered an "Invalid user input" error when attempting to save a live activity, even without making changes. The GraphQL response indicates a duplicate LocalId issue. (TGT-53329 & TGT-53373 & TGT-53195)
* Fixed an issue that prevented creating a redirect experience in the updated VEC. The redirect URL was ignored and the original page was shown instead. (TGT-53306)

+++

**Localization**

+++See details

* Fixed a localization issue in the [!UICONTROL Create Criteria] modal, when selecting the "between following values" option in the [!UICONTROL Choose Price Rule] drop-down list, the string "to" was unlocalized in the [!UICONTROL Inclusion Rules] section. (TGT-49754)
* Fixed a localization issue with the string "[!UICONTROL All host groups]" in the [!UICONTROL Environment] drop-down list of the Feeds Creation wizard is not localized correctly. (TGT-46737)

+++

**QA**

+++See details

* Fixed an issue where the QA environment fails to load data across multiple tabs, rendering the interface unusable. (TGT-53377)
* Fixed an issue that prevented creating an activity in the QA environment. The process redirected to the [!UICONTROL Activities] page instead of completing successfully. (TGT-53328)

+++

**Recommendations**

+++See details

* Fixed an issue where hovering over the "deep-learning" operand while creating a collection in [!DNL Recommendations] caused the page to crash. (TGT-53305)
* Fixed an issue where filter suggestions in [!UICONTROL Catalog Search] in the updated UI were inaccurate. (TGT-52007)
* Fixed an issue in the [!DNL Recommendations] UI where the Operands filter appears when using the "value is present" or "value is not present" operators—though it should be hidden. (TGT-53012)

+++

**Visual Experience Composer (VEC)**

+++See details

* Fixed an issue when a user clicks [!UICONTROL Manage Content] and then clicks [!UICONTROL Done] while editing an Automated Personalization (AP) activity, the page goes blank and becomes unresponsive. (TGT-53047 & TGT-52993)
* Fixed an issue where selecting the [!UICONTROL Viewed an mbox] conversion metric under [!UICONTROL Goals & Settings] caused the page to crash. (TGT-53346, TGT-53343, & TGT-53348)
* Fixed an issue where the [!UICONTROL Redirect to URL] feature fails to function as expected—no redirection occurs even with valid URLs. (TGT-53307)

+++

**Workspaces**

+++See details

* Fixed an issue when copying activities between workspaces caused duplicate "Audience Copy" entries and ID conflicts. Audiences are now copied with unique IDs, workspace context, and recursive handling for combined audiences (up to 5 levels). (TGT-53081)
* Fixed an issue when the workspace is set to "[!UICONTROL All Workspaces]," copying an activity that already exists in the default workspace results in an incorrect error:

  "At least one property should be included for non default workspaces."

  Since the copy is within the default workspace, no property should be required. Attempting to add a property and save results in a second error:

  "Invalid User Input"

+++

### [!DNL Target Standard/Premium] 25.7.3 (July 24, 2025)

Due to recent issues identified, primarily related to complex customer customizations, this release includes the following fixes and updates:

**Activities**

+++See details

* Fixed an issue where the `buildViews` method in the builder class incorrectly set `viewMaxLocalId` to the total count of views, rather than to the highest `viewLocalId` assigned. (TGT-53207)
* Fixed an issue in the updated [!DNL Target] UI where deleted offers in [!UICONTROL Automated Personalization] (AP) activities were shown as `Deleted option with ID: X` instead of their original names (for example, `Offer Name [Deleted]` as shown in the legacy UI). This fix restores meaningful labeling for deleted offers, improving clarity and making reporting more accurate and user-friendly. (TGT-52921)
*  Fixed an issue where some activities migrated from the [!DNL Target] frontend to [!DNL Target] Central had inconsistent metric configurations due to a previously fixed sync bug. Specifically, activities that originally used a conversion metric and were later updated to an analytics-based metric retained outdated values in the `primaryMetricType` and `successCriteria` fields. (TGT-52643)
* Fixed an issue where the entire content of a QA preview page became editable due to the unintended inclusion of the `contentEditable` attribute in HTML modifications. This allowed users to click and edit any text on the page, potentially causing layout issues and confusion during QA. (TGT-53247)
* Fixed an issue where moving a modification from [!DNL Page Load] to a [!UICONTROL View] caused the modification to be duplicated, remaining in [!UICONTROL Page Load] while also appearing in the [!UICONTROL View]. Additionally, removing the modification from the [!UICONTROL View] would incorrectly remove it from [!UICONTROL Page Load ]as well. (TGT-53270)

+++

**APIs**

+++See details

* Fixed an issue in the backend persistence layer where deleted options were correctly stored but not accessible via existing API endpoints. As a result, frontend applications couldn't retrieve meaningful names for deleted options, impacting historical reporting views. This fix ensures that preserved deleted option data can now be surfaced properly in the UI. (TGT-52973)
* Implemented a new migration endpoint to support the transfer of deleted activity options from JCR-based activities to [!DNL Target] Central. This functionality enables consistent tracking and reporting across systems. This feature ensures that deleted options are preserved and synchronized across the [!DNL Target] frontend and backend, improving historical reporting and data integrity. (TGT-53217)
* Introduced a new API endpoint that allows users to restore previously deleted activity options from a secondary database. This functionality leverages the existing infrastructure provided by the `RemovedCampaignElements` and `RemovedOptionInfo` classes, ensuring seamless reintegration of deleted options into active activities. (TGT-52903)
* Fixed an issue where [!DNL Recommendations] activities containing metric names longer than 25 characters could not be opened or edited due to API limitations. This fix ensures compatibility with metric names exceeding the character limit, restoring full access to affected activities. (TGT-52839)

+++

**Form-Based Experience Composer**

+++See details

* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] that caused the editor to crash after clicking the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ) when creating or editing an [!UICONTROL Automated Personalization] (AP) activity. (TGT-53047)

+++

**Recommendations**

+++See details

* Fixed an issue that prevented [!UICONTROL Catalog Search] from loading additional results when scrolling to the bottom of the list, restoring behavior consistent with the legacy UI. (TGT-53088)
* Fixed an issue that blocked deleting items from the [!UICONTROL Criteria Details] dialog box. (TGT-53245)
* Fixed an issue that prevented opening or interacting with products that had no name. This issue occurred when selecting environments that returned unnamed results, preventing access to product details. (TGT-53007)
* Fixed an issue that caused the [!UICONTROL Catalog Search] page to crash and display a blank screen when selecting certain products. (TGT-53087)
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

### [!DNL Target Standard/Premium] 25.7.2 (July 18, 2025)

Due to recent issues identified, primarily related to complex customer customizations, this release includes the following fixes and updates:

**Activities**

+++See details

* Added an additional confirmation warning when canceling activity edits with unsaved changes: "Do you really want to save this activity? If you don't save, all your changes will be lost." This message helps prevent accidental data loss. (TGT-52865)
* Restored legacy functionality to the [!UICONTROL Priority] slider in [!UICONTROL Goals & Settings], allowing customers to enter a numeric value directly, as supported in the legacy UI. (TGT-53185 & TGT-53219)

+++

**Audiences**

+++See details

* Fixed an issue that prevented saving or editing activities containing custom audiences. Customers encountered the error message "We cannot complete your request. Please contact [!DNL Adobe Client Care] if the problem persists." when attempting to save changes, or even save without changes, to certain activities. (TGT-53189)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details

* Fixed an issue when customers viewed reports for specific activities on the [!UICONTROL Goals & Settings] page, the [!UICONTROL View in Analytics] link incorrectly points to the QA environment instead of the production environment. (TGT-53163)

+++

**[!UICONTROL Experiences] and [!UICONTROL Offers]**

+++See details

* Fixed an issue where invoking `triggerView` via custom code caused an infinite loop. (TGT-52885)
* Fixed an issue causing mismatches between `LocalIds` defined for activities and those `LocalIds` used in experience definitions. (TGT-52669)
* Fixed an issue where metric names were missing on the activity [!UICONTROL Overview] page, displaying only 'Offer' instead of the correct metric name. (TGT-53054)

+++

**Form-Based Experience Composer**

+++See details

* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] that prevented activity saving and triggered the error message: "Cannot read properties of undefined (reading 'map')". (TGT-53145)

+++

**Recommendations**

+++See details

* Fixed an issue where clicking a product from [!UICONTROL Catalog Search] displayed the error 'Failed to retrieve product details' and opened a modal without a close option. (TGT-53082)
* Fixed an issue where [recommendations as offers ](/help/main/c-recommendations/recommendations-as-an-offer.md) in [!UICONTROL A/B Test] activities did not update correctly when changing collections or promotions. (TGT-52884)
* Fixed an issue in the production environment where clicking an entity in the updated UI displayed the error: "Failed to retrieve product details. Please contact [!DNL Adobe Client Care] if this problem persists." (TGT-53071)

+++

**Reports**

+++See details

* Fixed an issue where saving order details to a CSV file resulted in an empty file. (TGT-52225)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* Resolved an issue on the [!UICONTROL Goals & Settings] page where selectors used in multiple experiences were not consistently highlighted as selected. (TGT-53062)
*  Fixed an issue that prevented activity editing and triggered the error message: "Cannot read properties of undefined (reading 'map')". (TGT-53161)

+++

**Workspaces**

+++See details

* Improved handling of ad-hoc offers when switching workspaces.
  * When switching from the default workspace to a non-default workspace (or between non-default workspaces), ad-hoc offers are now copied correctly. During initialization, the workspace context is updated and a new ID is assigned to the offer to ensure uniqueness.
  * No changes occur when staying within the same workspace. (TGT-53079)
* Fixed an issue that prevented customers from [copying activities between different workspaces](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6). (TGT-52753 & TGT-47094)
* Fixed an issue when changing properties between workspaces. 
  * When switching between the default workspace to a non-default workspace, if the current property exists in the destination workspace, the property is preserved. 
  * If the [!UICONTROL Properties] list displays a warning (likely to indicate some properties may not be compatible) and the customer clicks [!UICONTROL Add] or [!UICONTROL Remove] and then clicks [!UICONTROL Save], all properties not in the destination workspace are removed. If the customer clicks [!UICONTROL Cancel], all properties remain, even if they don't exist in the destination workspace. (TGT-47094)
  * If staying in the same workspace or switching from a non-default workspace to the default or another workspace, everything remains as is. (TGT-53078)
* Updated entity validation logic to respect the original workspace context of the activity. Entities such as [!UICONTROL Experience Fragments] (XFs) are now validated based on the workspace in which the activity was originally created. For example, if an XF exists in the default workspace and the activity is copied from workspace X to workspace Y, validation still passes as long as the XF is valid in the original (default) workspace. (TGT-53196)
* Enhanced support for copying ad-hoc audiences during activity duplication.
  * Ad-hoc audiences, including metrics, reporting, page, and activity-only types, are now automatically copied in the following scenarios: 
    * When copying an activity from the default workspace to a non-default workspace.
    * When copying an activity within the same workspace. (TGT-53197)

+++

### [!DNL Target Standard/Premium] 25.7.1 (July 11, 2025)

Due to recent issues identified, primarily related to complex customer customizations, this release includes the following fixes and updates:

**Activities**

+++See details

* Fixed an issue where the [!UICONTROL Activity QA] URL included an unnecessary query parameter: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* Fixed an issue where Preview URLs incorrectly included additional audiences beyond the one explicitly typed by the user. This behavior has been corrected to ensure that only the specified audience is applied when generating a QA or preview link. (TGT-52912)
* Fixed an issue that prevented users from creating [!UICONTROL Auto-Target] (AT) activities if [!UICONTROL Auto-Allocate] (AA) is selected first during traffic allocation setup. This issue resulted in a backend validation error and prevents the activity from being saved. (TGT-53096)

+++

**Audiences**

+++See details

* Fixed an issue where users with the [!UICONTROL Approver] role were unable to add or save activity-only audience refinements. Attempting to do so resulted in a 403 Forbidden error, stating that the "[editor]" privilege was required, even though the user had sufficient permissions to approve and manage activities. (TGT-52984)
* Fixed an issue when an activity-specific audience is removed using the [!UICONTROL Remove Audience Refinement] option, the audience no longer appears in the audience list for re-selection within the same activity. This behavior prevented users from re-adding the same audience unless it is recreated from scratch. (TGT-52979)
* Fixed an issue where activity-only audience refinements disappeared from the UI immediately after being removed from a location, even before the activity was saved. This behavior contradicted the expected functionality and the tooltip guidance, which states: "All unused audiences from this library will be deleted once the activity is saved." (TGT-52982)
* Fixed an issue when attempting to assign an audience other than [!UICONTROL All Visitors] to an activity. Upon saving, the following error message displayed: "We cannot complete your request. Please contact [!UICONTROL Adobe Client Care] if the issue persists." (TGT-53008)
* Fixed an issue that blocked saving an activity after creating and assigning a new audience within the activity editor. The error message displayed was: "We cannot complete your request. Please contact [!UICONTROL Adobe Client Care] if the problem persists." (TGT-52977)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++See details

* Fixed an issue where copying an existing activity and changing the reporting source to [!DNL Adobe Analytics] (A4T) would result in an "Invalid user input" error. The error was triggered when certain metric actions incompatible with [!DNL Analytics] reporting, such as `restart_same_experience`, `restart_random_experience`, and `restart_new_experience`, were retained from the original activity. (TGT-52900)
* Fixed an issue that blocked customers from creating or saving an activity when selecting [!DNL Adobe Analytics] (A4T) as the reporting source in the [!UICONTROL Goals & Settings] step. The issue occurred specifically when selecting a [!UICONTROL Custom Event] metric (for example, "Custom Event 16"), resulting in the following error: "Invalid User Input." (TGT-52910)
* Fixed an issue where clicking the "[!UICONTROL View in Analytics]" link redirected users to the homepage instead of the intended [!DNL Analytics] dashboard. (TGT-53092 & TGT-53093)
<!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* Fixed an issue when viewing a [!DNL Recommendations] activity in the updated [!UICONTROL Overview] UI, the [!UICONTROL Goals & Settings] section fails to load when [!DNL Adobe Analytics] (A4T) is selected as the reporting source. The following error message was displayed: "Something went wrong. We cannot complete your request. Please contact Adobe Client Care if the problem persists." (TGT-52999)

+++

**[!UICONTROL Experiences] and [!UICONTROL Offers]**

+++See details
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* Fixed an issue where the [!UICONTROL Manage Content] feature did not properly validate the state of a location after all content options were removed. This issue could lead to inconsistent behavior or errors when attempting to save or proceed with the activity configuration. (TGT-52801)
* Fixed an issue where users encountered an "Invalid input" error when adding a new page and deleting specific elements within different experiences. The error is triggered by duplicate `LocalIds` being generated during element manipulation, particularly when switching between experiences and modifying shared page structures. (TGT-52720)
* Fixed an issue where using the [!UICONTROL Generate Adhoc Offer] feature resulted in undefined locations appearing in the [!UICONTROL Manage Content] panel. (TGT-53076 & TGT-53070)
* Clarified the behavior to the customer where modifications made using an HTML Offer might appear to be missing when navigating from the [!UICONTROL Targeting] step back to [!UICONTROL Experiences]. For this customer, the affected website dynamically generated multiple DOM selectors that changed with each page load. As a result, the selector originally used for the modification cannot be found when the editor is reopened, causing the modification to appear missing or invalid. This scenario is working as designed. To ensure that modifications persist visually in the editor, it is recommended that clients use stable, consistent selectors that do not change across page reloads. (TGT-52874)
* Fixed an issue where attempting to delete or deactivate an offer that was part of an excluded experience triggered an "Invalid user input" error. This issue occurred even though the offer was not actively used in the included experiences. (TGT-52917)

+++

**Form-Based Experience Composer**

+++See details

* Fixed an issue in form-based activities where duplicating an experience and editing the custom code in one of the duplicated experiences would unintentionally apply those changes to all duplicated experiences. Each experience now retains its own custom code independently after duplication. (TGT-51600)

+++

**Localization**

+++See details

* Updated localization strings in the new UI for French (fr_FR), German (de_DE), Italian (it_IT), Korean (ko_KO), and Simplified Chinese (zh_CN).

+++

**[!DNL Recommendations]**

+++See details

* Added a new [!DNL Recommendations] feed [status](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (KB-2215)
* Fixed an issue affecting the activity-create workflow when adding [!DNL Recommendations] with [!UICONTROL promotions]. When users selected "[!UICONTROL Promote by Attribute]" and added a filtering rule (for example, [!UICONTROL Parameter Matching]), the selected rule type and operand values were not retained after saving and re-editing the activity. Upon reopening, the filtering rule type would change unexpectedly, and operand values would be missing. (TGT-53059)
* Fixed an issue in the [!DNL Recommendations] UI where any promotion created with a single rule was incorrectly interpreted and displayed as a "List of items" promotion type, regardless of the rule's logic. (TGT-53063)
* Fixed an issue when using the updated [!UICONTROL Overview ]UI, the "[!UICONTROL Download Recommendations Data]" button was missing for [!UICONTROL Experience Targeting] (XT) activities that include [!DNL Recommendations]. (TGT-52730 & TGT-52756)
* Previously, the Recommendations UI displayed only the number of entities successfully imported from a feed. However, the backend message format includes both the number of imported entities and the total number of entities in the format:  `# of entities imported / # of total entities`. Due to this discrepancy, users were only seeing the first value (imported count) in the UI, which led to confusion. The UI now displays both numbers. (TGT-53073)
* Fixed an issue where customers were unable to save a filtering rule when configuring a "[!UICONTROL Promote by attribute]" promotion in a form-based A/B activity with recommendations. After saving and reopening the activity, the filtering rule was missing, and the activity could not be saved successfully. (TGT-53057)

  +++

**Reports**

+++See details

* Fixed an issue where selecting "[!UICONTROL Export order details to CSV]" from the [!UICONTROL Reports] page resulted in an empty file being downloaded. This issue occurred even when valid order data was present in the activity. (TGT-52225)
* Fixed an issue when attempting to save an activity after creating and assigning a new reporting audience. The error message returned was: "Access denied. To perform this operation, all of the following privileges are required: [editor]." This issue occurred despite the user having approver-level access. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details

* Resolved an issue where applying a modification to a view would result in the view being duplicated and the activity returning an "Invalid user input" error. This fix ensures that view modifications are applied correctly without triggering duplication or validation errors. (TGT-52886)
* Fixed an issue where custom code modifications were incorrectly displayed for the wrong experience. Specifically, changes intended for one experience were shown in a different experience, leading to confusion and potential misconfiguration of live activities. (TGT-52776)
* Fixed an issue that prevented editing or saving custom code modifications in the New VEC UI. Specifically:

  * After editing a custom code block and saving, the changes were not reflected in the UI or in the QA preview.
  * In some cases, modifications could not be deleted unless the activity was closed and reopened.
  * As a workaround, users had to copy the code, delete the modification, and recreate it manually with the updated content. (TGT-53072)

* Fixed an issue where editing and saving custom code caused the [!UICONTROL Modifications] panel to become unresponsive. (TGT-53075)
* Fixed an issue where modifications made to custom code in variant experiences were unintentionally reflected in the [!UICONTROL Control] experience. This caused unintended changes in delivery behavior. The [!UICONTROL Control] experience now remains isolated from custom code edits made to other experiences. (TGT-52413)
* Fixed an issue where modifications made to one experience (for example, Experience B) were unintentionally duplicated to another experience (Experience A) if the user clicked on the second experience before the editor fully loaded. This behavior could also result in modifications being lost if the initially selected experience had no changes. (TGT-52597)
* Fixed an issue where changes made in the [!UICONTROL Modifications] step of activity creation were not consistently saved. In some cases, after completing all steps and clicking [!UICONTROL Save], the custom script added in the [!UICONTROL Modifications] section would not reflect on the live site, despite no visible errors during the save process. (TGT-52661)
* Fixed an issue where custom code changes were not saving correctly and were unintentionally mirrored across multiple experiences within the same activity. Additionally, users encountered access issues when opening or refreshing certain activities, resulting in blank screens. These issues have now been resolved to ensure stable activity editing and accurate experience isolation. (TGT-52594)
* Fixed an issue where users were unable to browse to a different URL while in [!UICONTROL Browse Mode]. This prevented testers and editors from validating or previewing alternate pages within the same activity session. (TGT-53052)
* Fixed an issue where multiple [!UICONTROL Visual Experience Composer] (VEC) instances opened simultaneously during activity creation. This issue occurred when users disabled the [!UICONTROL Enhanced Experience Composer] (EEC) and removed the trailing slash from the website URL in the [!UICONTROL Page Delivery] step. (TGT-52782)
* Fixed an issue where the [!UICONTROL Revenue] metric dropdown in the [!UICONTROL Goals & Settings] step would incorrectly default to [!UICONTROL Revenue per Visit] (RPVISIT), even after the user selected a different metric.  The issue occurred when collapsing and re-expanding the metric configuration panel, causing the previously selected value to reset. (TGT-52811 & TGT-52878)
* Fixed several issues in the activity-create workflow related to offer naming and content translation in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Multivariate Testing] (MVT) activities:

  Key Issues Addressed:

  * Creating multiple HTML Offers with the same name (for example, "Experience") triggered a "Duplicate offer names are not allowed" error, but the UI did not clearly indicate which offers were causing the conflict.
  * Renaming offers via the right panel updated the name in the UI, but the change was not reflected in the [!UICONTROL Manage Content] tab or the [!UICONTROL Offers] tab, causing persistent validation errors.
  * In MVT activities, although the duplicate name error did not persist after renaming, the UI still failed to reflect updated offer names consistently across tabs. (TGT-52933)

  +++

### [!DNL Target Standard/Premium] 25.6.4 (June 27, 2025)

This release includes the following fixes and updates:

* Added the [!UICONTROL Rearrange] option to the updated [!UICONTROL Visual Experience Composer] (VEC) UI to align with functionality available in the legacy VEC. (TGT-46957 & TGT-52876)
* Fixed an issue where modifications made to variant experiences (for example, Experience B) in an [!UICONTROL A/B Test] activity were not being retained. After switching between experiences, the changes to the variant would disappear. This issue did not affect the Control experience. (TGT-52664)
* Fixed an issue where certain customers were unable to create or save activities, while others could perform the same actions without issue. The problem was inconsistent across accounts.(TGT-52842)
* Fixed an issue where in the updated VEC, users were unable to move modifications to the [!UICONTROL Page Load event], a capability that existed in the legacy UI. (TGT-52617)
* Fixed an issue in the updated UI where [!UICONTROL page load] events were not visible in [!DNL Target] when creating changes; updates only applied to views. (TGT-52604)
* Fixed an issue that prevented some activity modifications from displaying properly in the updated VEC. (TGT-52818)
* Fixed a null pointer exception that occurred when fetching reporting data for [!UICONTROL Automated Personalization] (AP) activities. (TGT-52362)
* Fixed an issue that prevented offer-level details from appearing in the .CSV file for [!UICONTROL Automated Personalization] (AP) activities. (TGT-52675)
* Fixed an issue when applying modifications in the updated VEC, changes initially appear correctly, including the expected [!UICONTROL Experience Fragment]. However, upon switching experiences or making additional edits, some modifications fail to apply due to selector issues. (TGT-52679)
* Fixed an issue where when a new activity was created by cloning an existing one, the QA links in the cloned activity incorrectly retained the page URLs from the original activity. (TGT-52775)
* Fixed an issue that unintentionally prevented [!UICONTROL On-device Decisioning] from being available in the updated VEC. (TGT-52371)
* Fixed an issue that prevented editing a product [!DNL Recommendations] activity. When attempting to access the VEC via the Target UI, an error appeared on the [!UICONTROL Overview] page, preventing any edits. (TGT-52823)
* Fixed an issue that prevented saving a [!DNL Recommendations] activity when experience names exceeded 50 characters. (TGT-52619)
* Fixed an issue where customers were unable to save a Recommendations activity after modifying the criteria in the new UI. The issue appears to be permission-related and does not affect all users with similar roles. (TGT-52816)
* Fixed an issue where users with the [!UICONTROL Editor] role were unable to edit a [!DNL Recommendations] activity. Attempting to change the design and save the activity resulted in a 403 Forbidden error, stating that the "[editor]" privilege was required, even though the user already had that role in the relevant workspace. (TGT-52836)

### [!DNL Target Standard/Premium] 25.6.3 (June 20, 2025)

This release includes the following fixes and updates:

* Fixed an issue where copying an activity from one workspace to another workspace triggered errors such as "must not be null" or "Something went wrong." (TGT-52474)
* Fixed an issue where [!UICONTROL Automated Segments] and [!UICONTROL Important Attributes] reports were not generated for certain activities. (TGT-52904)
* Fixed an issue in the updated VEC where default content handling in [!UICONTROL Automated Personalization] (AP) activities did not match the legacy UI. The system now automatically adds a default `optionGroup` named "Default Content" with `optionGroupLocalId = 0` when no group is explicitly added. This group includes the default option (for example, `optionLocalId: 0`). If the default content is removed, the corresponding option group is also removed. (TGT-52651)
* Fixed an issue in [!UICONTROL Multivariate Test] (MVT) activities where reusing an `experienceLocalId` from previously removed experiences was incorrectly disallowed. (TGT-52672)
* Fixed an issue that prevented copying or editing activities containing an experience fragment. This triggered the error: `Enum "AemOfferType" cannot represent value: "html"`. (TGT-52635)
* Fixed an issue where URLs in activity locations failed to display query parameters due to invalid characters, such as slashes (/). (TNT52845)
* Improved the validation error message for [!DNL A/B Test] activity updates via the backend API. When duplicate location names are present, the message now clearly states: "Duplicate names are not allowed" for `locations.selectors`. (TGT-52589)
* Fixed an error that occurred when updating a live [!UICONTROL Recommendations] activity due to an unrecognized property in the request payload. The system now properly handles the "Invalid JSON. Unrecognized property name" error. (TGT-52723)
* Fixed an issue that prevented creating a [!DNL Recommendations] design. Clicking [!UICONTROL Create] triggered the message: "There should be at least 1 entity variable used inside the script." (TGT-52395 & TGT-52899)
* Fixed an issue where re-saving a [!DNL Recommendations] design without modifications was blocked. (TGT-52879)
* Fixed a backend validation error that caused a "400 Bad Request" error when saving a [!UICONTROL Recommendations] activity. (TGT-52716)
* Fixed an issue in the [!UICONTROL Form-Based Experience Composer] where hovering over an mbox with special characters in the [!UICONTROL Location] drop-down caused the editor to go blank and triggered a "Failed to execute 'querySelector' on 'Element'." error. (TGT-52717)
* Improved feed-status accuracy with a new "PARTIALLY_IMPORTED" indicator. Previously, feeds were marked as "success" even when not all rows in a file were imported, which was misleading. (TGT-52892)
* Fixed an error where, after migrating to AP V2, certain API calls to `/admin/rest/ui/v1/campaigns` returned client-side errors (HTTP 4xx). (TGT-52721)

### [!DNL Target Standard/Premium] 25.6.2 (June 12, 2025)

This release includes the following fixes and updates:

* Added a [new FAQ article](/help/main/c-intro/updated-ui-faq.md) to address common questions about the updated [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC).
* Fixed an issue where the "[!UICONTROL URL - does not contain]" rule in [!UICONTROL Page Delivery] was not working, allowing content to be shown even when it should have been blocked. (TGT-52754)
* Fixed an issue where [!UICONTROL Page Delivery] incorrectly displayed the error message: "Duplicate page URLs are not allowed. (TGT-52765)
* Fixed an issue where audiences for [!UICONTROL Page Delivery] URLs containing experience fragments were created with # erroneously appended. (TGT-52786)
* Fixed an issue where copying an activity and editing settings on the [!UICONTROL Goals and Settings] page caused the [!DNL Target] UI to become unresponsive. (TGT-52797)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) that incorrectly allowed redirecting an additional page in an [!UICONTROL A/B Test] activity to the same URL. (TGT-51838)
* Fixed an issue where changes to metrics on the [!UICONTROL Goals and Settings] page were not saved when editing an activity. (TGT-52799)
* Fixed an issue where adding a new experience while the web editor was still loading caused the new experience to duplicate content from the previous experience. (TGT-51397)
* Restored the ability to use custom code outside the `<head>` tag, a feature previously available in the legacy Target UI. (TGT-52304 & TGT-52300)
* Removed unnecessary validation when selecting the default workspace during activity creation. Mandatory property validation no longer applies to the default workspace, but remains in place for non-default workspaces. (TGT-52449)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) where `triggerView()` calls were not being detected. (TGT-52575)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) that prevented users from adding modifications to [!UICONTROL Single Page Application] (SPA) views. (TGT-52556)
* Fixed an issue in the updated [!DNL Target] UI that prevented customers from viewing offer details. (TGT-52607)
* Fixed an issue where updates made to offers in the [!UICONTROL Offers Library] were not reflected in the updated [!UICONTROL Visual Experience Composer] (VEC). (TGT-52637)
* Fixed an issue that prevented the Offers section from displaying properly while creating an activity. (TGT-52773)
* Added validation to ensure that all `optionLocalIds` referenced in `optionGroups` exist in the options array. Invalid references are automatically removed during activity creation. (TGT-52687)
* Fixed an issue where reporting groups and exclusions were not retained after adding a new offer. (TGT-52728)
* Fixed an issue where activities without an [!UICONTROL Activity QA] button displayed an empty option selector. (TGT-52733)
* Fixed an issue where QA links failed to render content properly. (TGT-52718)
* Fixed an issue where replacing an element with an experience fragment did not reflect changes correctly in the QA environment. (TGT-52762)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) that caused an "Invalid Input" error when users attempted to add experience fragments. (TGT-52701)
* Fixed an issue where the "Edit Audience" modal appeared empty when editing audience targeting in the updated [!UICONTROL Visual Experience Composer] (VEC). (TGT-52749)
* Added a message to inform users when an entity is not accessible in the selected workspace. (TGT-52767)
* Fixed an issue where the UI failed to allow manual assignment of an environment ID to a criteria. Instead, it defaulted to the ID for the [!UICONTROL Product Catalog Search] host group. This fix ensures that criteria changes are now applied across all environments, not just the default. (TGT-52817)
* Fixed an issue where the "[!UICONTROL Download Recommendations data]" option was missing for [!UICONTROL Experience Targeting] (XT) activities with recommendations. (TGT-52730 & TGT-52756)

### [!DNL Target Standard/Premium] 25.6.1 (June 6, 2025)

This release includes the following fixes and updates:

* Fixed an issue where QA links did not deliver the correct experience for the associated activity. (TGT-52163 & TGT-52790)
* Fixed an issue where QA links were missing the associated audience ID. (TGT-52722)
* Fixed an issue to ensure that experiences are delivered only when their configured Page Delivery URL conditions are accurately met. (TGT-52696)
* Fixed an issue that prevented customers from creating a [!DNL Recommendations] design template. Attempting to create a template triggered the error: "There should be at least 1 entity variable used inside the script." (TGT-52395)
* Fixed an issue that prevented saving [!DNL Recommendations] designs using Velocity arrays. The error message "There should be at least 1 entity variable used inside the script" was incorrectly triggered. (TGT-52734)
* Fixed an issue where modifications were inaccessible in the [!UICONTROL Visual Experience Composer] (VEC) when the page failed to load for internal web pages. (TGT-52488 &TGT-52470)
* Fixed an issue where the [!UICONTROL Modifications] panel was not visible on smaller screen sizes in the VEC. (TGT-52470)
* Fixed an issue in the updated VEC where switching from [!UICONTROL Browse] mode back to [!UICONTROL Design] mode caused a console error and prevented further interaction. (TGT-52532)
* Fixed an issue in the VEC where clicking certain elements unintentionally expanded their size. (TGT-52497)
* Fixed an issue where certain page elements failed to load or be recognized in the VEC, preventing interactions such as selecting buttons or banners and disrupting accurate event tracking in activities. (TGT-52663)
* Fixed an issue that prevented customers from deleting or removing offers in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52690)
* Fixed an issue that caused inconsistent activity qualification behavior in multi-page activities. (TGT-52694)
* Fixed an issue that caused the activity's [!UICONTROL Overview] page to show an invalid URL for the [!UICONTROL Activity Location]. (TGT-52695)
* Fixed an issue in the updated [!DNL Target] UI that caused duplicate entries to appear for activity locations. (TGT-52693)
* Fixed an issue that triggered a `getAudiencesV3` error, preventing customers from editing or copying activities. (TGT-52709)
* Fixed an issue that caused an invalid payload error when adding [!UICONTROL Experience Fragments] or HTML offers to an activity. (TGT-52779 & TGT-52773)
* Fixed an issue in the updated [!DNL Target] UI where E[!UICONTROL xperience Fragments] failed to display correctly due to an invalid input error. (TGT-52701)
* Fixed an issue that prevented customers from editing activities in the [!UICONTROL Form-based Experience Composer] due to an invalid user error. (TGT-52470)
* Fixed a localization issue in the Korean language where previous translations used characters outside the Basic Multilingual Plane. The updated translation uses appropriate characters that accurately convey the intended meaning. (TGT-52508 & TGT-52509)
* Fixed a localization issue in the Korean language where the translation for "date" was inconsistent when selecting start and end dates for an activity. (TGT-52510)

### [!DNL Target Standard/Premium] 25.5.4 (May 29, 2025)

This release includes the following fixes and updates:

* Fixed an issue that prevented adding or editing URLs in QA mode. (TGT-51941)
* Added a QA Mode Traffic setting under [!UICONTROL Reports] > [!UICONTROL Report Settings] ( ![Report Settings icon](/help/main/assets/icons/Setting.svg) ) to align with functionality from the legacy [!DNL Target] UI. (TGT-52228 & TGT-52329)
* Fixed an issue where the Form-based activity generated incorrect QA links. The activity URL/location included an unintended "1" at the end, which has now been removed to ensure accurate linking. (TGT-52355 & TGT-52358)
* Fixed an issue where the Form-based activity generated incorrect QA links. The activity URL included an unintended `http://pid-ppc` at the beginning of the URL, which has now been removed to ensure accurate linking. (TGT-52557)
* Fixed an issue where [!DNL Target] generated invalid QA links for Form-based activities. (TGT-52528 & TGT-52603)
* Fixed an issue where saving a modified activity appeared to process but never completed, and no error message was shown in [!DNL Target]. (TGT-52461)
* Fixed an issue where the updated [!UICONTROL Visual Experience Composer] (VEC) failed to auto-detect the `at_property` value. (TGT-52347)
* Fixed an issue that caused two modifications being recorded when only one is expected after switching between [!UICONTROL Browse] and [!UICONTROL Design] modes in the VEC while interacting with a form element. (TGT-52455)
* Fixed an issue that prevented selecting the [!UICONTROL Clicked an Element] setting in the updated VEC due to an error stating that  the selector was invalid, already used, or not visible. (TGT-52467)
* Fixed an issue where adding a [!UICONTROL Recommendation Offer] box in the updated VEC caused duplicate (ghost) boxes to display. Switching between Experience A and B repeatedly added more ghost boxes. (TGT-52505 & TGT-52519)
* Fixed an issue in the updated [!DNL Target] UI where changes to an HTML Offer made via the [!UICONTROL Offer] menu were not reflected in the associated activity, and vice versa. This behavior now matches the legacy UI, where updates sync correctly between the [!UICONTROL Offer] menu and the activity. (TGT-52540 & TGT-52541)
* Fixed an issue where recent updates to [!UICONTROL Experience Fragments] in the [!UICONTROL Offers Library] were not reflected when attempting to use them within an activity. (TGT-52659)
* Fixed a localization issue in the Simplified Chinese translation of a confirmation message. The previous version lacked quotation marks around the location name and used informal language, contrary to the customer's style guide. The updated translation now uses proper punctuation and a formal tone. (TGT-52364) 

### [!DNL Target Standard/Premium] 25.5.3 (May 22, 2025)

This release includes the following fixes and updates:

* Fixed an issue where the search-by-name feature in the [!UICONTROL Activities] list did not work correctly with multi-word queries. (TGT-52529)
* Fixed an issue that prevented excluding experiences from [!UICONTROL Automated Personalization] (AP) activities. (TGT-52383)
* Fixed an issue where the "[!UICONTROL Contains]" option was missing from [!UICONTROL Filter Rules] when managing content in AP activities. (TGT-52384)
* Fixed a reporting inconsistency in [!UICONTROL Automated Personalization] (AP) activities, specifically related to how default offers are tracked and reported using `optionLocalId` values from [!DNL Target]'s internal system.
* Fixed an issue where QA links failed to deliver the intended activity experience. (TGT-52163)
* Fixed an issue where users with [!UICONTROL Approver] permissions were incorrectly blocked from editing live activities, receiving an "Access denied" error message. (TGT-52416)
* Fixed an issue where audience refinements failed to display for certain activities in the updated [!DNL Target] UI. (TGT-52057)
* Fixed an issue that caused audience refinements and activity audiences to be reversed in the updated UI. (TGT-52158)
* Fixed an issue where generating ad-hoc offers resulted in duplicate offers. (TGT-51938)
* Fixed an issue that blocked offer updates and incorrectly displayed an "Invalid user" error. (TGT-52361)
* Fixed an issue that prevented saving existing activities, triggering an "Invalid User Input" error. (TGT-52422)
* Fixed an issue that blocked editing existing HTML offers, triggering an "Invalid User Input" error on save, even when no code changes were made. (TGT-52351)
* Fixed an issue that prevented [!DNL Target] from recognizing the "#" character in a website's URL. (TGT-52093)
* Fixed an issue that prevented editing [!DNL Recommendations] activities to add or update promotions, which caused save failures and duplicate promotions. (TGT-52343)
* Fixed an issue that prevented changes to criteria or designs in [!DNL Recommendations] activities, resulting in an "invalid JSON: unrecognized property name" error. (TGT-52375)
* Fixed an issue where sequence criteria failed to display correctly in the [!UICONTROL Visual Experience Composer] (VEC) for [!DNL Recommendations] activities. (TGT-52435)
* Fixed an issue where views were not correctly identified on SPA pages when using the [!DNL Adobe Experience Platform Web SDK]. (TGT-52106)
* Fixed an issue where On-Device Decisioning (ODS) details were not saved correctly, despite being included in the batch operation payload. (TGT-52406)
* Added an `audienceMetadata` field to activities, enabling it to be read and updated during editing. (TGT-51004)
* Added an error message to alert users when an audience timeframe is invalid. (TGT52522)
* Updated the activity structure to support duplicate audiences of different types. (TGT-51200)

<!--
### [!DNL Adobe Target] [!DNL AI Assistant] release (May 16, 2025)

We are thrilled to announce the launch of the [!DNL AI Assistant] in [!DNL Adobe Target]! This powerful user interface feature is designed to help you navigate and understand [!DNL Target] concepts with ease. Available across multiple products in [!DNL Adobe Experience Cloud], including [!DNL Target], [!DNL AI Assistant] is here to revolutionize your experience.

[!DNL AI Assistant] in [!UICONTROL Target] is a conversational tool that you can use to accelerate your workflows with [!DNL Experience Platform] applications and services. Use [!DNL AI Assistant] to boost your overall productivity and amplify your understanding of product knowledge

In [!DNL Target], the first phase of [!DNL AI Assistant] provides invaluable product knowledge grounded in [!DNL Experience League] documentation. Whether you're setting up a profile script, troubleshooting errors, or considering an upgrade to the AEP Web SDK, [!DNL AI Assistant] has you covered.

For more information, see [Coworker skills for Adobe Target](/help/main/c-intro/coworker-skills.md).
-->

### [!DNL Target Standard/Premium] 25.5.2 (May 8, 2025)

This release includes the following fixes and updates:

* [!DNL Target] users with [!UICONTROL Product Administrator] and [!UICONTROL System Administrator] rights can now edit all settings on the [!UICONTROL Administration] pages, regardless of their role in [!DNL Target]. Users without these permissions have read-only access to these settings. This update ensures stricter access control over [Administration settings](/help/main/administrating-target/administrating-target.md). (TGT-48179)
* Fixed a caching issue that prevented saving activity [Site Preferences](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings). (TGT-52213) 
* Fixed an issue where customers couldn't enable selection by ID and class in the [!UICONTROL Site Preferences] section after loading the site in the VEC. The [!UICONTROL Site Preferences] setting automatically reverted to disabled even after being enabled. (TGT-52207)
* Fixed an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to display the correct page when [page delivery](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) URLs ended with a forward slash (/). (TGT-52237)
* Fixed an issue that prevented the removal of custom code modifications when changing experiences. (TGT-52240)
* Fixed an issue where HTML modifications in the VEC overlaid existing page elements. (TGT-52265)
* Fixed an issue that prevented editing custom code in the updated VEC due to the existing custom code not being visible in the editor. (TGT-52272)
* Fixed an issue that caused a "Duplicate names are not allowed" error message when saving a Recommendations activity. (TGT-52318)
* Fixed an issue in the updated VEC that prevented customers from editing text elements or removing container objects. (TGT-52348)
* Fixed an issue that blocked [!DNL Customer Journey Analytics] from displaying correctly on an activity [!UICONTROL Overview] page. (TGT-52359)
* Fixed an issue that prevented reporting groups from persisting in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52368)
* Fixed an issue that prevented saving activities that include offer decisioning. (TGT-52390)
* Fixed an issue where the default offer was selected, but other offer content displayed in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Multivariate Test] (MVT) activities. (TGT-52372)
* Fixed GET permissions logic to check with OR between full org access and specific org + user access. (TGT-52374)
* Fixed an issue where audience names did not display after selecting an audience for [!UICONTROL Managed Content] and [!UICONTROL Reporting Audiences], even though [!UICONTROL Show Only Selected] was enabled. (TGT-52393)

### [!DNL Target Standard/Premium] 25.5.1 (May 5, 2025)

This release includes the following fixes and updates:

* Fixed an issue preventing audience refinements from displaying for certain activities in the updated UI. (TGT-52057)
* Fixed an issue that prevented the use of combined audiences in activities. (TGT-52346)
* Fixed an issue that prevented the creation of a new activity in a non-default workspace using an activity-only audience from the same workspace. (TGE-52349)
* Fixed an issue that caused activity-only audiences to disappear from the updated UI after creating and selecting a new audience. (TGT=52091)
* Fixed an issue that prevented the use of duplicate audiences in activities. (TGT-51200 & TGT-52057)
* Fixed an issue that caused audience refinements and activity audiences to be reversed in the updated UI. (TGT-52158)
* Fixed an issue that prevented the creation of a new activity due to the user input error: "non-default workspace not allowed for this user." (TGT-52267)
* Fixed an issue that prevented offers from displaying in the updated UI for both default and non-default workspaces. [!DNL Target] now displays offers from both workspaces. (TGT-52339)
* Fixed an issue where [!DNL Target] did not warn customers when editing an activity and changing a modified website element. (TGT-52100)
* Fixed an issue where editing an offer with ad-hoc offers created a new offer instead of updating the existing one. (TGT-52135)
* Fixed Fixed an issue that caused an invalid payload error when moving offers to folders. (TGT-52325)
* Fixed Fixed an issue that caused an user input error when moving offers to folders. (TGT-52296)
* Added an `audienceMetadata` field for each activity, and ensured it is read and updated when editing the activity. (TGT-51004)

### [!DNL Target Standard/Premium] 25.4.5 (April 25, 2025)

This release includes the following fixes and updates:

* Fixed an issue that caused discrepancies in audience listings between the [!UICONTROL Activity] settings page and the [!UICONTROL Reporting] overview page. (TGT-52203)
* Fixed an issue that prevented adding a new page to an activity due to an invalid user input error. (TGT-52263)
* Fixed an issue that caused `OptionLocalIDs` to incorrectly increment when the option remains unchanged. (TGT-52187)
* Fixed an issue that caused `location` and `OptionLocalIDs` to incorrectly increment when the option remains unchanged. (TGT-52188)
* Fixed an issue that caused the location on the activity's [!UICONTROL Overview] page to be incorrect. (TGT-52182)
* Fixed an issue where an invalid selector warning was not displayed for an invalid location. (TGT-52110)
* Fixed an issue so that downloaded reporting files correctly show data present in the reporting UI. (TGT-52068)
* Fixed an issue so that batch operations do not fail after adding page-delivery rules. (TGT-52097)
* Fixed an issue that caused [!DNL Target] to trim all query parameters from the website's URL. (TGT-52100)
* Resolved a console error that prevented customers from creating activities in both the legacy and updated [!DNL Target] UI. (TGT-52181)
* Fixed an issue that blocked customers from adding new pages, causing an invalid user input error. (TGT-52258)
* Fixed an issue that caused modifications to disappear after adding additional pages then navigating back to the [!UICONTROL Experiences] tab. (TGT-52264)
* Fixed an issue that blocked customers from changing the audience in an [!UICONTROL Experience Targeting] (XT) activity. (TGT-52191)
* Fixed an error that prevented editing of an XT activity due to an unsupported UI rule. (TGT-52273)
* Fixed an issue in the updated [!UICONTROL Visual Experience Composer] (VEC) where breadcrumbs were not always displayed at the bottom of the editor, causing difficulties in precisely selecting elements. (TGT-52169)
* Fixed an issue where the [!UICONTROL Audience] drop-down list failed to display all audiences due to pagination. (TGT-52204)
* Fixed an issue that caused an invalid user input message when adding new offers in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52210)
* Fixed an issue where [!UICONTROL Analytics for Target] (A4T) was incorrectly selected as the reporting source, even though the customer did not have access to A4T. (TGT-52226)
* Fixed an issue that prevented saving an activity with the [!UICONTROL View a Page] URL metric. (TGT-52260)
* Fixed an issue that blocked customers from selecting workspaces while creating offers within an activity. (TGT-52289)
* Fixed an issue that blocked customers from creating activities across all workspaces. (Tgt-52218)
* Fixed an issue where modifications from one experience were incorrectly displayed when switching to another experience. (TGT-52184)
* Fixed an issue where the default offer was incorrectly displayed in the [!DNL Target] UI when opening the activity. (TGT-52198)

### Target permissions update (April 22, 2025)

This future update enhances organizational control over [!DNL Target] instance configurations, preventing accidental updates that could affect activity delivery across various testing and personalization teams.

Effective April 22, 2025, only [!UICONTROL Product] and [!UICONTROL Solutions] admins will be able to update settings in the [!UICONTROL Administration] sections, regardless of their roles in [!DNL Target] workspaces. Users without this permission will have read-only access to the [!UICONTROL Administration] sections.

For more information, see [Administer Target](/help/main/administrating-target/start-target.md).

### [!DNL Target Standard/Premium] 25.4.4 (April 17, 2025)

This release includes the following fixes and updates:

* Added an error message to guide users on resolving duplicate options in an activity. (TGT-51927)
* Fixed an issue where `ClickTrack` selectors were not removed when deleting pages or experiences with redirect offers. (TGT-51952)
* Fixed an issue caused by allowing empty `ClickTrack` selectors. [!DNL Target] now requires that the selector field must not be blank. (TGT-52107)
* Fixed an issue that incorrectly allowed metrics with duplicate names. Metrics now require unique names. (TGT-52201)
* Fixed an issue where audience definitions were not visible when editing offer-level targeting in [!UICONTROL Automated Personalization] (AP) activities. (TGT-52148)
* Fixed an issue that prevented customers with [!UICONTROL Editor] rights from saving activities. (TGT-52227)
* `OptionLocalIDs` no longer increment incorrectly when the option remains unchanged. (TGT-52139)
* Fixed an issue that caused an "Invalid `optionLocalIds`" message when trying to create an activity. (TGT-52154)
* Discrepancies between `OptionLocalIDs` defined for an activity and those used to define experiences have been fixed. (TGT-52215)
* Fixed an issue that caused a validation failure that occurred when trying to create an A/B activity. (TGT-51923)

### [!DNL Target Standard/Premium] 25.4.3 (April 11, 2025)

This release includes the following fixes and updates:

* Fixed an error that prevented customers from opening the audience information pop-up for certain [!UICONTROL Experience Targeting] (XT) activities. (TGT-52049)
* Fixed an issue where the audience setting reverted to "[!UICONTROL All Visitors]" following changes made in the [!UICONTROL Visual Experience Composer] (VEC). (TGT-52132)
* Fixed an issue where audience refinements were not displayed for specific activities (TGT-52057) 
* Fixed an issue that prevented customers from inserting an [!UICONTROL Experience Fragment] in the default workspace. (TGT-52073)
* Fixed an issue where an offer showed as "Content not found" and did not display on the [!UICONTROL Offers] page for an [!UICONTROL Automated Personalization] (AP) activity. (TGT-52150)
* Added the ability to allow duplicate audiences within an activity. (TGT-51200)
* Fixed an issue where the wrong mbox name displayed on the [!UICONTROL Goals & Settings] page for an XT activity after editing. (TGT-52026)
* Fixed an issue where `defaultContent` displayed in options despite not being in `experiences/optionLocations`. (TGT-52036)
* Fixed an issue to ensure that empty strings are not converted to null values. (TGT-52037)
* Fixed an issue requiring customers to reconfigure the [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] on the [!UICONTROL Goals & Settings] page after edits. (TGT-52071)
* Fixed an issue where an activity with no page-delivery rules displayed multiple rules on the [!UICONTROL Overview] page. (TGT-52084)
* Added an error message for users attempting to save an offer with characters outside the basic multilingual plane, such as emojis. (TGT-52105)
* Fixed an issue where opening an activity triggered the error message: "This Activity is using one or more audiences deleted at source." (TGT-52120)
* Fixed an issue where ClickTrack metrics were not displayed in the updated [!UICONTROL Visual Experience Composer] (VEC) during editing. (TGT-52152)
* Fixed an issue where a URL with a query parameter as the activity location did not display the query parameter on the activity's [!UICONTROL Overview] page. (TGT-51635)
* Fixed an issue that prevented the entire experience URL from displaying in [!UICONTROL Browse mode] within the [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* Fixed an issue where editing an activity caused page delivery to add a "/" to the end of the URL, rendering it invalid. (TGT-52114)
* Fixed an issue where the [!UICONTROL Activity QA] link in the [!UICONTROL Form-Based Experience Composer] incorrectly redirected to the [!DNL Adobe Experience Cloud] homepage. (TGT-52055)
* Fixed an issue where additional pages added to the [!UICONTROL A/B Test] activity were not retained after saving and reopening. (TGT-51994)
* Fixed an issue that prevented customers from deleting styles in the inline style section. (TGT-52070)
* Restored access to [audience definition cards](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) in the [!UICONTROL Activity QA] dialog box, similar to the legacy UI. (TGT-52056)
* The updated UI did not save pages or audiences without modifications. If customers added new pages or audiences to an activity but make no changes to them, [!DNL Target] discarded the unmodified audiences upon saving. Notifications have added in relevant places to inform users of this behavior. (TGT-52104)

### [!DNL Target Standard/Premium] 25.4.1 (April 2, 2025)

This release includes the following fixes and updates:

* Fixed an issue that caused experience audiences to disappear from activities. (TGT-52003)
* Fixed an issue that caused unexpected elements during delivery. (TGT-52011)
* Fixed an issue that blocked customers from viewing the audience in the targeting graph on the Ove[!UICONTROL r]view page and during activity editing. (TGT-52050)
* Fixed an issue that prevented customers from reordering experiences in order of priority in [!UICONTROL Experience Targeting] (XT) activities. (TGT-52054)
* Fixed an issue that caused incorrect rendering when undoing text style changes. (TGT-51876)
* Fixed an issue that when modifying a redirect offer, [!DNL Target] also removes any [!UICONTROL ClickTrack] selectors associated with that offer. (TGT-51936)
* Fixed an issue that caused [!DNL Target] to incorrectly save the selector when cancelling [!UICONTROL ClickTrack]. (TGT-51937)
* Fixed an issue that triggered an invalid name error after opening and closing the mbox picker on the [!UICONTROL Goals & Settings] page without making any changes. (TGT-51983)
* Fixed an issue that blocked editing ad hoc offers created in the legacy [!DNL Target] UI. (TGT-51984)
* Fixed an issue that blocked editing activities that have ad-hoc offers that contain custom code. (TGT-51995)
* Fixed an issue that caused exclusion rules to display as inclusion rules when editing combined audience definitions. (TGT-51999)
* Fixed an issue that prevented custom code from displaying correctly during experience editing. (TGT-52005)
* Fixed an issue that made the [!UICONTROL Insert Before] option unavailable for inserting content before the navigation bar. (TGT-52031)
* Fixed an issue that prevented correct highlighting of the default experience in reporting. (TGT-51716)
* Fixed an issue that triggered a `default message [Invalid optionLocalIds: xx]]` message when creating an activity. (TGT-52038)

### at.js version version 2.11.8 (March 31, 2025)

* Resolved CodeQL-identified vulnerability in string suffix validation to prevent edge cases during resize and move operations. (TNT-51516)

### [!DNL Target Standard/Premium] 25.3.8 (March 28, 2025)

This release includes the following fixes and updates:

* Resolved an issue that caused the [!UICONTROL Activities] page to load slowly. (TGT-51151)

### [!DNL Target Standard/Premium] 25.3.7 (March 26, 2025)

This release includes the following fixes and updates:

* Resolved an issue that blocked saving multi-page activities if a page was deleted after modifications. (TGT-51988)
* Resolved an error that occurred when editing an activity: `default message [Invalid optionLocalIds: xx]]`. (TGT-51985)
* Resolved an issue where adding new modifications to an activity removed existing modifications. (TGT-51981)
* Resolved an issue where replacing an audience with "[!UICONTROL All visitors]" during activity creation or editing caused a "Duplicate audiences are not permitted" error. (TGT-51978)
* Resolved an issue that caused an "Invalid user input" error when saving an [!UICONTROL A/B Test] activity. (TGT-51976)
* Resolved an issue that prevented calculated metrics from displaying correctly on the [!UICONTROL Goals & Settings] page. (TGT-51975)
* Resolved an issue that prevented matching `companyName` and `reportSuite` in the [!DNL Analytics] configuration for the `pageviews` metric. (TGT-51965)
* Resolved an issue where switching experiences in an activity removed modifications. (TGT-51945)
* Resolved an issue where removing a page audience also removed [!UICONTROL ClickTrack] selectors. (TGT-51935)
* Resolved an issue that made an activity uneditable after opening its [!UICONTROL Overview] page. (TGT-51931)
* Resolved an issue that caused an `[Unused optionLocalIds: 0]]` error during activity creation. (TGT-51920)
* Resolved an issue where some changes were not translated correctly after removing text style changes. (TGT-51876)
* Resolved an issue that prevented targeted audiences from updating correctly in the [!UICONTROL Form-Based Experience Composer]. (TGT-51845)
* Resolved an issue where the URL in the [!UICONTROL Visual Experience Composer] did not update correctly during activity navigation. (TGT-51832)
* Resolved an issue that prevented offers from appearing in the [!UICONTROL Offers] UI, despite displaying correctly when creating an activity and adding offers. (TGT-51805)
* Resolved an issue where some activities lacked a fallback screen to display default content when personalized or targeted content could not be delivered. (TGT-51638)
* Resolved an issue that prevented live offers and certain folders from displaying correctly in the [!UICONTROL Offers] UI. (TGT-51628)
* Resolved an issue that prevented some URL strings and goURLs from being localized correctly. (TGT-35741)
* Fixed an issue that prevented roles ([!UICONTROL Approver], [!UICONTROL Editor], and [!UICONTROL Observer]) from being localized correctly in the [!DNL Target] UI. (TGT-29925)

### [!DNL Target Standard/Premium] 25.3.6 (March 14, 2025)

This release includes the following fixes and updates:

* Resolved "Invalid user input" error in [!UICONTROL Visual Experience Composer] (VEC) activities with [!UICONTROL Click Tracking] enabled when the same [!UICONTROL ClickTrack] selector is used multiple times. (TGT-51921)
* Fixed "Invalid user input" error in VEC activities with shared locations (for example, HEAD selector) and identical offers. (TGT-51879)
* Fixed an issue that caused experience modifications to be shared across audiences. (TGT-51815)
* Resolved validation errors when creating activities due to segment ID conflicts. The errors occurred when [!DNL Target] detected existing activities using anonymous segments. (TGT-51784)
* Resolved issue preventing [!DNL Target] from saving activities with exclusion rules in an audience. (TGT-51581)
* Resolved issue preventing customers from creating, deleting, or moving folders without access to the default workspace. (TGT-51499)
* Resolved issue causing GET requests to fail when retrieving [!DNL Analytics] metrics list. (TGT-51106)

### [!DNL Target Standard/Premium] 25.3.5 (March 11, 2025)

This release includes the following fixes and updates:

* Resolved an issue that prevented users from changing offers in the [!UICONTROL Modifications] panel. (TGT-51800)
* Resolved an issue where actions were incorrectly displayed in the left panel for experiences and audiences, including in [!UICONTROL ClickTrack] mode. (TGT-51895)
* Resolved an issue where [!UICONTROL ClickTrack] selectors were not applied to the correct audience page. (TGT-51871)

### [!DNL Target Standard/Premium] 25.3.4 (March 7, 2025)

This release includes the following fixes and updates:

* Resolved an issue where activity-only audiences were not visible in the [!UICONTROL Audiences] panel, preventing their editing or reuse. (TGT-51860)
* Fixed an issue that blocked [!DNL Target Standard] customers from creating activities using [!UICONTROL Analytics for Target] (A4T) reporting. (TGT-51854)
* Fixed an issue that excluded local ID counters from the payload during batch create and edit operations. (TGT-51867)

### [!DNL Target Standard/Premium] 25.3.2 (March 6, 2025)

This release includes the following fixes and updates:

* Fixed an issue where copying an activity with an activity-only audience failed to create a new activity, mistakenly using the original activity's audience instead. (TGT-51855)
* Fixed an issue that prevented editing of [!UICONTROL Experience Targeting] (XT) activities with activity-only audiences. (TGT-51846)
* Fixed an issue where the [!UICONTROL Visual Experience Composer] (VEC) failed to apply modifications to an experience correctly on the first edit. (TGT-51843)
* Fixed an issue that triggered an 'ID' error when clicking on certain elements within the VEC. (TGT-51814)
* Updated error handling in the VEC during activity creation. (TGT-51759)
* Fixed an issue where a missing view in the [!UICONTROL Modifications] panel caused an 'invalid user input' error when saving the activity. (TGT-51827)
* Fixed an issue that prevented the creation of recommendations criteria. (TGT-51834)
* Added a confirmation message before redirecting to a different URL. (TGT-51703)
* Fixed issues with GraphQL integration tests within offers and folders. (TGT-51839)

### [!DNL Target Standard/Premium] 25.3.1 (March 3, 2025)

This release includes the following fixes and updates:

* A combined audience can include subgroups, each containing multiple audiences. This release fixed an issue that prevented subgroup audiences from displaying in the [!UICONTROL Rules] dialog box. (TGT-51813)
* Resolved an issue where some experience audiences were replaced with [!UICONTROL All Visitors] when opening older activities. (TGT-51812)
* Resolved an issue that prevented editing activities with activity-only audiences. (TGT-51807)
* Resolved an issue that prevented editing page head modifications in the updated [!DNL Target] UI. (TGT-51797)
* Resolved a null error that occurred when duplicating an experience, deleting another experience, and then trying to save the activity. (TGT-51796)
* Resolved an issue that prevented audience exclusion rules from displaying in the audience's info panel during the [!UICONTROL Targeting] step of creating activities. (TGT-51579)
* Updated error messages localized in Korean. (TGT-51701 & TGT-51699)

### [!DNL Target Standard/Premium] 25.2.3 (February 26, 2025)

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

### at.js version version 2.11.7 (February 26, 2025)

This release includes the following update:

* Fixed Telemetry logging when `localStorage` is not available. Telemetry was causing an issue for some customers that had `localStorage` disabled in their browsers.

For information about this and previous at.js releases, see [at.js version details](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}.

### Target Standard/Premium 25.2.1 (February 17, 2025) {#ui-update-2}

This release includes the following updates:

* [!UICONTROL Activities] user interface update
* [!DNL Recommendations] user interface update

#### [!UICONTROL Activities] user interface update

As the [!DNL Adobe Target] UI modernization effort continues, we are pleased to announce the general availability of the updated [!UICONTROL Activities] User Interface.

>[!NOTE]
>
>Starting February 17, customers will gradually have access to the new [!UICONTROL Activities]  UI. To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage will upgrade the initial group of [!DNL Target] customers to the new [!UICONTROL Activities] UI. Subsequent stages will upgrade the remaining customers.

>[!IMPORTANT]
>
>For important information about the [!DNL Target] UI version toggle end-of-life plan, see [[!DNL Target] UI version toggle deprecation](/help/main/r-release-notes/release-notes.md#toggle).

Based on the latest [!DNL Adobe Spectrum] design system, the update standardizes previously inconsistent design patterns, while adding new enhancements, such as:

* [Redesigned reporting](/help/main/administrating-target/reporting.md) for better insights into activity results.
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) page, now getting the information from the [[!DNL Audit Query API]](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} for real-time insights.
* [Customizable list views](/help/main/c-activities/activities.md) for better flexibility across different team needs.
* [Enhanced quick info and detail screens](/help/main/c-activities/activities.md) for easier access to information.
* [Session-persistent search and filter options](/help/main/c-activities/activities.md).
* Completely [rebuilt [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) with support for latest security updates from browser providers and a modern user interface.

  For information about how the updated VEC differs from the previous version, see:
  
  * [Visual Experience Composer changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md) 
  * [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [Updated [!DNL Chrome] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) supporting Manifest V3 for increased security and improved support for first-party cookies.

![Activities refresh](/help/main/r-release-notes/assets/activities-refresh.png)

#### [!DNL Recommendations] user interface update

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

### Target Standard/Premium 25.1.1 (January 9, 2025) {#ui-update-1}

This release includes the following updates:

#### [!UICONTROL Offers Library] user interface update

To enhance the user experience for [!DNL Adobe Target] users, this release updates the [!UICONTROL Offers Library] user interface. 

>[!NOTE]
>
>To ensure a seamless rollout for all customers, this release will be deployed in controlled stages. The first stage upgraded the initial group of Target customers to the new Offers UI. Subsequent stages will upgrade the remaining customers.

>[!IMPORTANT]
>
>For important information about the [!DNL Target] UI version toggle end-of-life plan, see [[!DNL Target] UI version toggle deprecation](/help/main/r-release-notes/release-notes.md#toggle).

Using the latest [!DNL Adobe Spectrum] design system, this update standardizes inconsistent design patterns and introduces new enhancements, including the following:

* **Bulk offer management**: Select and delete or move multiple offers simultaneously.

* **[!UICONTROL Code Editor] upgrades**: Refreshed HTML and JSON editors with syntax highlighting and line numbering.

* **Improved offer cards**: Enhanced quick information and detail cards for easier information access.

* **Persistent search and filters**: Adds session-persistent search and filter options.

For more information see [Offers](/help/main/c-experiences/c-manage-content/manage-content.md) and the sub-articles in this section. All Offers articles in this section have been updated to reflect these UI changes.

Here's a short video that highlights the changes in this release:

![Offers UI refresh video](/help/main/r-release-notes/assets/offers-video-v2.gif)
