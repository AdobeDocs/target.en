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

Explore the latest features, enhancements, and fixes in [!DNL Adobe Target]. These release notes also cover updates to [!DNL Target] APIs, SDKs, the [!DNL Adobe Experience Platform Web SDK], at.js, and other platform components when applicable.

(The issue numbers in parentheses are for internal [!DNL Adobe] use.)

## Time-sensitive updates you need to know {#time-sensitive}

[!BADGE Important]{type=Informative}

For time-sensitive updates related to [!DNL Adobe Target] and your implementation, [!DNL Adobe ]provides detailed release notes and documentation through [!UICONTROL Experience League]. Here are some key highlights relevant to your implementation:

### [!DNL Target] UI version toggle deprecation

+++See details
The [!DNL Target] team is offering a temporary feature that lets you switch between the updated [!DNL Target] UI and the legacy version using a toggle button. This option is available only during the final phase of the UI rollout.

![Target UI version toggle](/help/main/r-release-notes/assets/toggle.png)

Once the rollout is complete, the toggle will be removed, and all users will transition permanently to the updated UI. [!DNL Adobe] recommends planning ahead, as this feature will be phased out soon.

#### Deprecation timeline

Due to recent issues identified, primarily related to complex customer customizations, the [!DNL Target] team has adjusted the deprecation timeline:

* **June 17, 2025**: All IMS Organizations have been enabled for the updated [!DNL Target] UI, either for specific users or organization-wide, to begin testing the new experience.

* **June 30, 2025**: The [updated [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md) became the default experience for all IMS Orgs that have enabled the UI version toggle.

  * Customers who currently see the legacy UI, by default, now see the updated UI upon login.
  * The UI version toggle remains available through the end of July, allowing users to switch back if needed.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] strongly recommends using the updated [!DNL Target] UI. Switch back to the legacy UI only if a blocker issue occurs, due to [limitations of the toggle switch behavior](#limitations).

* **July 15 to July 30, 2025**: The UI version toggle will be permanently disabled in phases. Affected IMS Orgs are no longer able to revert to the legacy UI.
  
  * Exceptions are reviewed on a case-by-case basis.
  * Delays to the toggle deprecation are granted only briefly (a few days) while blocker issues are resolved.

Contact [Adobe Customer Care](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md) with any concerns or if you anticipate issues during this transition.

#### Limitations of the UI toggle behavior {#limitations}

The following information describes the limitations that you should be aware of when choosing to use the version toggle:

* **Visibility of new activities**: Activities created in the updated UI will not be visible if you switch back to the legacy UI.
* **Editing existing activities**: Changes made to existing activities (originally created in the legacy UI) while using the updated UI will be published to your website. However, these updates will not be visible in the legacy UI if you switch back; only the last updates made from the legacy UI will appear there.
* **Consistency of activity details**: The most recent changes, regardless of which UI you use, will be reflected on your live website. However, the legacy UI will only show the latest changes made from within that version. This might cause confusion if activities edited in the updated UI look different than what you see in the legacy UI.

#### More resources to learn about the updated UI

* [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md): This FAQ addresses common questions about the new [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC), including navigation changes, feature locations, and the deprecation of the temporary UI version toggle. Whether you're a marketer, developer, or admin, this FAQ helps you transition smoothly and make the most of the updated UI.
* [[!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Provides a summary of the key UI changes in [!DNL Target] for [!UICONTROL Activities], [!UICONTROL Recommendations], and the [!UICONTROL Visual Experience Composer] (VEC).
* [[!DNL Target Standard/Premium] 25.1.1 (January 9, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Provides a summary of the key UI changes in [!DNL Target] for the [!UICONTROL Offers Library].
* [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): Provides a brief overview to help you get familiarized with [!DNL Target] and provides links for more in-depth information and step-by-step instructions.
* [[!UICONTROL Visual Experience Composer] changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2015) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the legacy and updated versions of the VEC.
* [[!UICONTROL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): This article explains the updated VEC UI and its options.

+++

## [!DNL Target Standard/Premium] 25.7.1 (July 11, 2025)

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
<!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)
* Fixed an issue when viewing a [!DNL Recommendations] activity in the updated [!UICONTROL Overview] UI, the [!UICONTROL Goals & Settings] section fails to load when [!DNL Adobe Analytics] (A4T) is selected as the reporting source. The following error message was displayed: "Something went wrong. We cannot complete your request. Please contact Adobe Client Care if the problem persists." (TGT-52999)-->

+++

**[!UICONTROL Experiences] and [!UICONTROL Offers]**

+++See details
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* Fixed an issue where the [!UICONTROL Manage Content] feature did not properly validate the state of a location after all content options were removed. This could lead to inconsistent behavior or errors when attempting to save or proceed with the activity configuration. (TGT-52801)
* Fixed an issue where users encountered an "Invalid input" error when adding a new page and deleting specific elements within different experiences. The error was triggered by duplicate `LocalIds` being generated during element manipulation, particularly when switching between experiences and modifying shared page structures. (TGT-52720)
* Fixed an issue where using the [!UICONTROL Generate Adhoc Offer] feature resulted in undefined locations appearing in the [!UICONTROL Manage Content] panel. (TGT-53076 & TGT-53070)
* Clarified the behavior to the customer where modifications made using an HTML Offer might appear to be missing when navigating from the [!UICONTROL Targeting] step back to [!UICONTROL Experiences]. For this customer, the affected website dynamically generated multiple DOM selectors that changed with each page load. As a result, the selector originally used for the modification cannot be found when the editor is reopened, causing the modification to appear missing or invalid. This is working as designed. To ensure that modifications persist visually in the editor, it is recommended that clients use stable, consistent selectors that do not change across page reloads. (TGT-52874)
* Fixed an issue where attempting to delete or deactivate an offer that was part of an excluded experience triggered an "Invalid user input" error. This issue occurred even though the offer was not actively used in the included experiences. (TGT-52917)

+++

**Form-Based Experience Composer**

+++See details
* Fixed an issue in form-based activities where duplicating an experience and editing the custom code in one of the duplicated experiences would unintentionally apply those changes to all duplicated experiences. Each experience now retains its own custom code independently after duplication. (TGT-51600)

+++

**Localization**

+++See details
* Fixed a contextual translation issue in the Korean locale (ko-KR) for the string "Preview Experience". (TGT-52928)
* Fixed terminology inconsistencies identified in the Simplified Chinese (zh_CN) translation of several text strings. (TGT-52954 & TGT-52955)

+++

**[!DNL Recommendations]**

+++See details
* Added a new [!DNL Recommendations] feed [status](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (KB-2215)
* Fixed an issue affecting the activity-create workflow when adding [!DNL Recommendations] with [!UICONTROL promotions]. When users selected "[!UICONTROL Promote by Attribute]" and added a filtering rule (for example, [!UICONTROL Parameter Matching]), the selected rule type and operand values were not retained after saving and re-editing the activity. Upon reopening, the filtering rule type would change unexpectedly, and operand values would be missing. (TGT-53059)
* Fixed an issue in the [!DNL Recommendations] UI where any promotion created with a single rule was incorrectly interpreted and displayed as a "List of items" promotion type, regardless of the rule's logic. (TGT-53063)
* Fixed an issue when using the updated [!UICONTROL Overview ]UI, the "[!UICONTROL Download Recommendations Data]" button was missing for [!UICONTROL Experience Targeting] (XT) activities that include [!DNL Recommendations]. (TGT-52730 & TGT-52756)
* Previously, the Recommendations UI displayed only the number of entities successfully imported from a feed. However, the backend message format includes both the number of imported entities and the total number of entities in the format:  `# of entities imported / # of total entities`. Due to this discrepancy, users were only seeing the first value (imported count) in the UI, which led to confusion. The UI now displays both numbers. (TGT-53073)

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
* Fixed an issue where the [!UICONTROL Revenue] metric dropdown in the [!UICONTROL Goals & Settings] step would incorrectly default to [!UICONTROL Revenue per Visit] (RPVISIT), even after the user selected a different metric.  issue occurred when collapsing and re-expanding the metric configuration panel, causing the previously selected value to reset. (TGT-52811 & TGT-52878)
* Fixed several issues in the activity-create workflow related to offer naming and content translation in [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Multivariate Testing] (MVT) activities:

  Key Issues Addressed:

  * Creating multiple HTML Offers with the same name (for example, "Experience") triggered a "Duplicate offer names are not allowed" error, but the UI did not clearly indicate which offers were causing the conflict.
  * Renaming offers via the right panel updated the name in the UI, but the change was not reflected in the [!UICONTROL Manage Content] tab or the [!UICONTROL Offers] tab, causing persistent validation errors.
  * In MVT activities, although the duplicate name error did not persist after renaming, the UI still failed to reflect updated offer names consistently across tabs. (TGT-52933)

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
