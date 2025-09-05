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
