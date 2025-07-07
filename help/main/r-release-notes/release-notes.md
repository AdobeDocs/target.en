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

## Important time-sensitive updates you need to know {#time-sensitive}

For time-sensitive updates related to [!DNL Adobe Target] and your implementation, [!DNL Adobe ]provides detailed release notes and documentation through [!UICONTROL Experience League]. Here are some key highlights relevant to your implementation:

+++See details: UI version toggle deprecation
### [!DNL Target] UI version toggle deprecation

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

## [!DNL Target Standard/Premium] 25.6.4 (June 27, 2025)

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

## [!DNL Target Standard/Premium] 25.6.3 (June 20, 2025)

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

## [!DNL Target Standard/Premium] 25.6.2 (June 12, 2025)

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

## [!DNL Target Standard/Premium] 25.6.1 (June 6, 2025)

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

## [!DNL Target] UI version toggle deprecation (May 23, 2025) {#toggle}

>[!IMPORTANT]
>
>The [!DNL Target] team has adjusted the timeline for the UI version toggle deprecation. See [Updated: [!DNL Target] UI version toggle deprecation (June 17, 2025)](#revised) for more information.

The rollout of the new [!DNL Target] user interface will be complete by **May 27, 2025**. At that point, all customers will have access to the latest UI version.

Starting **June 22, 2025**, the UI version toggle will be removed. All users will transition permanently to the new interface, with no option to revert to the previous version.

>[!NOTE]
>
>Customers with special cases who need to retain the toggle after June 22 can contact Adobe Customer Care for assistance.

### Important information about the UI version toggle

We're offering a temporary feature that lets you switch between the updated [!DNL Target] UI and the legacy version using a toggle button. This option is available only during the final phase of the UI rollout.

![Target UI version toggle](/help/main/r-release-notes/assets/toggle.png)

Once the rollout is complete, the toggle will be removed, and all users will transition permanently to the updated UI on **June 22, 2025**. Adobe recommends planning ahead, as this feature will be phased out soon.

### Limitations of the UI toggle behavior

* **Visibility of new activities**: Activities created in the updated UI will not be visible if you switch back to the legacy UI.
* **Editing existing activities**: Changes made to existing activities (originally created in the legacy UI) while using the updated UI will be published to your website. However, these updates will not be visible in the legacy UI if you switch back; only the last updates made from the legacy UI will appear there.
* **Consistency of activity details**: The most recent changes, regardless of which UI you use, will be reflected on your live website. However, the legacy UI will only show the latest changes made from within that version. This might cause confusion if activities edited in the updated UI look different than what you see in the legacy UI.

### More information about the updated UI

* [[!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Provides a summary of the key UI changes in [!DNL Target] for [!UICONTROL Activities], [!UICONTROL Recommendations], and the [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium] 25.1.1 (January 9, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Provides a summary of the key UI changes in [!DNL Target] for the [!UICONTROL Offers Library].

* [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): Provides a brief overview to help you get familiarized with [!DNL Target] and provides links for more in-depth information and step-by-step instructions.

* [[!UICONTROL Visual Experience Composer] changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2015) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the legacy and updated versions of the VEC.

* [[!UICONTROL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): This article explains the updated VEC UI and its options.

* [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md): This FAQ addresses common questions about the new [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC), including navigation changes, feature locations, and the deprecation of the temporary UI version toggle. Whether you're a marketer, developer, or admin, this FAQ helps you transition smoothly and make the most of the updated UI.

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
