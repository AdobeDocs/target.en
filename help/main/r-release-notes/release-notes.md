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

For time-sensitive updates related to [!DNL Adobe Target] and your implementation, [!DNL Adobe ]provides detailed release notes and documentation through [!UICONTROL Experience League]. Here are some keys highlights relevant to your implementation:

### [!DNL Target] UI version toggle deprecation

+++See details
The [!DNL Target] team is offering a temporary feature that lets you switch between the updated [!DNL Target] UI and the legacy version using a toggle button. This option is available only during the final phase of the UI rollout.

![Target UI version toggle](/help/main/r-release-notes/assets/toggle.png)

Once the rollout is complete, the toggle will be removed, and all users transition permanently to the updated UI. [!DNL Adobe] recommends planning ahead, as this feature will be phased out soon.

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
* **Editing existing activities**: Changes made to existing activities (originally created in the legacy UI) while using the updated UI are published to your website. However, these updates are not visible in the legacy UI if you switch back; only the last updates made from the legacy UI appear there.
* **Consistency of activity details**: The most recent changes, regardless of which UI you use, are reflected on your live website. However, the legacy UI only shows the latest changes made from within that version. This situation might cause confusion if activities edited in the updated UI look different than what you see in the legacy UI.

#### More resources to learn about the updated UI

* [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md): This FAQ addresses common questions about the new [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC), including navigation changes, feature locations, and the deprecation of the temporary UI version toggle. Whether you're a marketer, developer, or admin, this FAQ helps you transition smoothly and make the most of the updated UI.
* [[!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Provides a summary of the key UI changes in [!DNL Target] for [!UICONTROL Activities], [!UICONTROL Recommendations], and the [!UICONTROL Visual Experience Composer] (VEC).
* [[!DNL Target Standard/Premium] 25.1.1 (January 9, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Provides a summary of the key UI changes in [!DNL Target] for the [!UICONTROL Offers Library].
* [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): Provides a brief overview to help you get familiarized with [!DNL Target] and provides links for more in-depth information and step-by-step instructions.
* [[!UICONTROL Visual Experience Composer] changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2015) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the legacy and updated versions of the VEC.
* [[!UICONTROL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): This article explains the updated VEC UI and its options.

+++

## [!DNL Target Standard/Premium] 25.8.1 (August 7, 2025)

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
+ Fixed multiple issues when copying activities between workspaces in the updated [!DNL Target] UI. Customers encountered errors related to audience access—particularly with live activities—and incorrect privilege validation, even when the user had "[!UICONTROL Approver]" roles in both source and destination workspaces. (TGT-53002)
* Fixed an issue in the updated UI where copying activities within the same workspace unnecessarily duplicated associated offers and audiences. (TGT-53457)
* Fixed an issue to address cases where ad-hoc (anonymous) audiences were not correctly copied between non-default workspaces or from non-default to default workspaces. While earlier updates ensured proper duplication for default-to-non-default and same-workspace scenarios, this enhancement focused on preserving combined audience configurations that span multiple workspaces. The fix ensures consistent audience behavior and accurate targeting across all workspace transitions. (TGT-53268)

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
