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

## [!DNL Target Standard/Premium] 25.9.3 (September 30, 2025)

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

## [!DNL Target Standard/Premium] 25.9.2 (September 22, 2025)

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

## Datastream updates (September 19, 2025)

Datastream ID and sandbox combination must be unique for [!DNL Adobe Target] destination connections.

Updated validation logic for [!DNL Target] destination connections to enforce that the combination of datastream ID and sandbox name must be unique within an IMS Org. This means:

* The same datastream ID + sandbox name pair cannot be reused across multiple [!DNL Target] destination connections.
* The same datastream ID can be used for different connections only if they are configured in different sandboxes.
* This rule applies to all datastream selections, including when "None" is selected.

This update ensures consistent configuration and prevents conflicts across multi-sandbox environments. For more information, see [Adobe Target connection](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} in the *Experience Platform Destinations* guide.

## [!DNL Target Standard/Premium] 25.9.1 (September 5, 2025)

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
