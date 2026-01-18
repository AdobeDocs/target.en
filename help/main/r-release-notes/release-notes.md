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

## [!DNL Target Standard/Premium] 26.1.1 (January 18, 2026)

**Activities**

+++See details

* **Unable to copy activity - invalid user input.** The issue causing users to see an unhelpful "invalid user input" error when copying an activity has been fixed. Previously, when an activity was duplicated, its workspace‑specific property assignments were not preserved, causing the backend to reject the save request because ABActivity requires at least one property belonging to a non‑default workspace. This mismatch triggered a generic error in the UI, leaving users without guidance. The fix ensures that workspace assignments are correctly retained during copy operations, allowing users to save the copied activity without modification and preventing misleading validation errors. (TGT-54282) 
* **Enable workspace column the web editor offer.** This update addresses customer confusion caused by offers from the [!UICONTROL Default Workspace] appearing in other workspaces within the Web Editor. Although this behavior is working as designed, [!UICONTROL Default Workspace] offers are intentionally visible across all workspaces, customers reported that the UI did not make workspace origin clear, especially when creating activities in a non‑default workspace such as "Approvers." To improve clarity, the [!UICONTROL Workspace] column has now been enabled in the Web Editor's offer list, allowing users to easily distinguish which workspace each offer belongs to and preventing misinterpretation of the additional offers displayed. (TGT-54138)
* **Links with target="_blank" open in a new tab.** This fix resolves an issue where authored websites containing links with ~target="_blank"~ would open in a new browser tab when clicked in [!UICONTROL Browse] mode, disrupting the in‑editor preview experience. The behavior occurred because the authored page's native link attributes were not being intercepted by the extension's injected JavaScript, unlike in the legacy UI where anchor elements were transformed and their targets overridden to keep navigation inside the editor. The update ensures that links using ~target="_blank"~ are now properly handled within the Web Editor so they no longer open external tabs during authoring. (TGT-54134)
* **Deselect Property warning.** This update introduces a visual warning to clearly inform users when they deselect an auto‑detected property in the Activity Editor. Previously, removing an auto‑detected property provided no indication that the property would be permanently deleted, which c0uld lead to accidental loss of targeting configuration. The fix adds a warning icon, consistent with the behavior in the legacy UI, to notify users that deselecting the property removes it from the activity. (TGT-54121)
* **[!UICONTROL Workspaces] dropdown is limited to 20 in the [!UICONTROL Users] section.** This fix resolves an issue where the [!UICONTROL Workspaces] dropdown in the [!UICONTROL Administration] > [!UICONTROL Users] section displayed only 20 workspaces, even when a user had access to many more. The underlying GraphQL call for `licenseGroups` was also limited to 20 results, causing the UI to show an incomplete list despite the user having access to more workspaces in the organization. The update removes this hard limit so the full set of available workspaces is now returned and displayed correctly. (TGT-53820)
* **Fixed an issue where the offers modal did not show the workspace column.** Fixed an issue where the offers modal did not display the workspace column in the updated UI. This caused confusion for customers because offers from the [!UICONTROL Default Workspace] appeared alongside offers from the selected workspace without any indication of their origin. The workspace column is now enabled so customers can clearly identify which workspace each offer belongs to. (TGT-52320)

+++

**Properties**

+++See details
* **Activity edit should not add auto‑detected property if already removed.** This fix addresses an issue where editing an activity would automatically reintroduce an auto‑detected property that the user had previously removed. When reopening an activity for editing, the system incorrectly restored the removed property, leading to inconsistent behavior and confusion in the [!UICONTROL Properties List]. The update ensures that once an auto‑detected property is removed, it remains removed during all subsequent edits and does not reappear unless the user explicitly adds it back. (TGT-54182)
* **Do not add auto‑detected properties if already removed.** This fix ensures that once a user manually removes an auto‑detected property from an activity, the system no longer reintroduces it during subsequent navigation within the activity editor. Previously, if a user deselected an auto‑detected property, moved to the [!UICONTROL Targeting] step, and then returned to [!UICONTROL Experiences], the editor would repopulate the removed property based on the auto‑detected list stored in the Activity Editor state slice. The updated logic now compares the auto‑detected properties against the current properties in the ~ActivityState~ slice and prevents re‑adding any auto‑detected property that the user has already removed. This results in consistent behavior across steps and respects user intent. (TGT-54181)
* **Add Auto‑detected text into the properties list.** This enhancement updates the [!UICONTROL Properties List] to clearly label any property that was automatically detected by the system. When an auto‑detected property is also present in the user‑visible [!UICONTROL Properties List], it now displays the "(Auto‑Detected)" text next to its name, using the value stored in the ~ActivityEditorSlice~ state. This mirrors the behavior of the legacy UI and helps users easily distinguish between manually selected properties and those properties identified automatically. (TGT-54120)
* **Add Auto-detected [!UICONTROL Properties] into the state.** This update ensures that the ~ActivityEditorSlice.ExperienceEditor~ state consistently maintains an up‑to‑date list of all auto‑detected property IDs passed from the Web Editor into the Activity [!UICONTROL Experiences] tab. Each time the user navigates into the [!UICONTROL Experiences] tab, the state is refreshed with any newly detected properties while preventing duplicates, ensuring accurate tracking and reliable downstream behavior. (TGT-54119)

+++

**Recommendations**

+++See details
* **[!UICONTROL Environment] drop‑down shows only 100 results.** This fix addresses a limitation where customers with more than 100 environments could only see the first 100 entries in the [!UICONTROL Environment] drop‑down within [!UICONTROL Recommendations]. The underlying GraphQL query (~getEnvironmentsV2~) was paginated with a hard‑coded page size of 100, causing the UI to display only a partial list even when additional pages were available. For customers who have more than 100 environments, this issue resulted in missing options and an incomplete selection experience. The update increases the limit so that all environments are returned and displayed, ensuring full visibility regardless of environment count. (TGT-53903)

+++

**Reports**

+++See details

* **Fixed an issue where the [!UICONTROL Reports] arrow did not clearly indicate expandable columns.** Fixed an issue where the reporting table did not clearly show that additional columns could be expanded in the updated UI. A disappearing tooltip has been added to the [!UICONTROL Reports] arrow near the column headers to help customers understand that more columns are available.

+++

**Views**

+++See details

* **Unable to delete modifications applied to views.** This fix resolves an issue where users were unable to delete modifications within an activity unless the modification had first been reapplied to additional views. When editing an activity (for example, activity ID 302467), attempts to delete any modification had no effect, preventing users from removing unwanted changes. However, once a modification was re‑applied using "Apply to more views" and assigned to a `Page Load` event, deletion suddenly worked as expected. (TGT-54088) 

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* **[!UICONTROL Experience Fragment] name was truncated in the new VEC UI** (TGT-54312)
* **Unable to use [!UICONTROL Advanced Settings] for [!UICONTROL Revenue] metric.** This fix resolves an issue where users encountered a 403 "Access denied" error when configuring [!UICONTROL Advanced Settings] for the [!UICONTROL Revenue] metric in [!UICONTROL Goals & Settings]. The problem occurred when adding a dependency condition tied to the primary goal; the backend incorrectly required the editor privilege even for users who already had sufficient permissions to create and edit activities. As a result, saving the activity failed despite valid configuration. The update corrects the permission check so that users with appropriate access can successfully add Revenue metric dependencies without triggering a forbidden‑resource error. (TGT-54092)
* **Fixed an issue where the Add button did not apply to selected images.** Fixed an issue that prevented customers from adding certain images when selecting or updating an image in the activity‑create process. When customers searched for specific assets, for example, images returned when searching for "ipp," clicking the [!UICONTROL Add] button did not apply the selected image and no modification was created. Selecting other images, such as `Homepage-banner-1-moz.jpg`, continued to work as expected. This update ensures that all valid images can be applied consistently in the updated UI. (TGT-53610)
* **Fixed an issue where deleting a URL condition reset the goal metric configuration.** Fixed an issue where removing a single URL condition in the [!UICONTROL Goal] metric caused the entire configuration to reset in the updated UI. When customers attempted to delete a saved URL condition under [!UICONTROL Conversion] > [!UICONTROL Viewed a Page], the goal type unexpectedly switched to [!UICONTROL Viewed an Mbox], and all previously configured settings were removed. This update ensures that only the selected URL condition is deleted, and all remaining goal settings stay intact. (TGT-53271)
* **Fixed an issue where search did not look through subfolders.** Fixed an issue where searching for offers did not return results from subfolders in the updated UI. Customers could only find an offer if they manually navigated to the folder where it was stored, making search behavior inconsistent with API capabilities. Search now supports recursively looking through folders so customers can locate offers without needing to open each folder individually. (TGT-51954)

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
