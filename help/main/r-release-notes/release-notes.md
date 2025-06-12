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

## Target UI version toggle deprecation (May 23, 2025) {#toggle}
 
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
