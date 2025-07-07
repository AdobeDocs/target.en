---
keywords: target user interface;user interface;ui;frequently asked questions;faq
description: Questions and answers about the updated [!DNL Target]t user interface.
title: Where Can I find FAQs about the updated [!DNL Target] UI?
feature: Overview
exl-id: 75db4791-ca51-472d-99dd-583f7a74b222
---
# [!DNL Target] UI update FAQs

New in 2025, [!DNL Adobe Target]'s updated user interface introduces a streamlined, intuitive experience designed to enhance usability and efficiency across all roles. This FAQ addresses common questions about the new [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC), including navigation changes, feature locations, and the deprecation of the temporary UI version toggle. Whether you're a marketer, developer, or admin, this FAQ helps you transition smoothly and make the most of the updated UI.

## Has the timeline for the deprecation of the Target UI version toggle been updated?

+++Details
Yes. You can find the new timeline and important information in [Time-sensitive updates you need to know](/help/main/r-release-notes/release-notes.md#time-sensitive).

+++

## Where can I find more information about the updated [!DNL Target] UI?

+++Details
The following resources provide information to learn more about the updated [!DNL Target] UI:

* [[!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Provides a summary of the key UI changes in [!DNL Target] for [!UICONTROL Activities], [!UICONTROL Recommendations], and the [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium] 25.1.1 (January 9, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Provides a summary of the key UI changes in [!DNL Target] for the [!UICONTROL Offers Library].

* [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): Provides a brief overview to help you get familiarized with [!DNL Target] and provides links for more in-depth information and step-by-step instructions.

* [[!UICONTROL Visual Experience Composer] changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2015) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the legacy and updated versions of the VEC.

* [[!UICONTROL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): This article explains the updated VEC UI and its options.

+++

## Is the updated UI available to all current [!DNL Target] customers, [!UICONTROL Standard] and [!UICONTROL Premium]? 

+++Details
The updated UI is available to all [!DNL Target] customers, [!UICONTROL Standard] and [!UICONTROL Premium]. No upgraded license or SKU is required.

For more information about the rollout and deprecation of the temporary UI version toggle, see [Time-sensitive updates you need to know](/help/main/r-release-notes/release-notes.md#time-sensitive).

+++

## Will the current list of bugs be fixed before the legacy UI is deprecated?

+++Details
The [!DNL Target] team is actively addressing issues related to the new UI rollout. Updates and ongoing improvements are detailed in the release notes.

For more information about the rollout and deprecation of the temporary UI version toggle, see [Time-sensitive updates you need to know](/help/main/r-release-notes/release-notes.md#time-sensitive).

+++

## Can customers apply for the UI version toggle to remain for their accounts if they prefer to stay with the legacy UI?

+++Details
The UI version toggle is a temporary feature that lets you switch between the updated [!DNL Target] UI and the legacy version using a toggle button. This option is available only during the final phase of the UI rollout. Once the rollout is complete, the toggle will be removed, and all users will transition permanently to the updated UI. 

There are several limitations with using the UI version toggle, including visibility of new activities, editing of existing activities, and the consistency of activity details.

For more information, see [Time-sensitive updates you need to know](/help/main/r-release-notes/release-notes.md#time-sensitive).

++++

## Can [!DNL Adobe] delay our migration to the updated UI until the full rollout is complete?

+++Details
[!DNL Target] does not offer the option to delay or customize the timing of the UI migrations. Customers are transitioned in phases, and the rollout schedule is managed by [!DNL Adobe]. For the latest updates, refer to the release notes.

There are several limitations with using the UI version toggle, including visibility of new activities, editing of existing activities, and the consistency of activity details.

For more information, see [Time-sensitive updates you need to know](/help/main/r-release-notes/release-notes.md#time-sensitive).

+++

## How can I tell if an activity was created or edited in the legacy UI or in the updated UI?

+++Details
Activities created or edited in the updated UI follow the same guided, three-step workflow and might include UI-specific metadata or formatting not present in legacy-created activities. Although there's no visible tag or label in the interface, differences in layout, structure, or available options (such as enhanced targeting or preview features) can indicate which UI was used. For detailed identification, check the activity's change history or consult your implementation logs.

+++

## What are the differences between creating offers in the legacy versus the updated UI? Are additional attributes required?

+++Details
The [!UICONTROL Offer Library] UI requires consistent attribute definitions for all offers. When creating an activity-only (ad-hoc) offer, users must also specify an offer name. This information appears in the [!UICONTROL Form-based Experience Composer], making it easier to identify offers without reviewing the code or content.

+++

## What happened to the offer preview links in the updated UI?

+++Details
[!UICONTROL Experience Fragment] preview links are available in the [!UICONTROL Quick Info] popover, displayed when clicking the information icon ( ![Info icon](/help/main/assets/icons/InfoOutline.svg) ) corresponding to the selected fragment.

+++

## I have to disable the [!UICONTROL Enhanced Experience Composer] when editing existing activities with the updated UI. Has [!DNL Adobe] observed similar behavior with other customers?

+++Details
Yes. When using the [!DNL Adobe Experience Cloud] [!DNL Visual Editing Helper extension], you might need to disable the [!UICONTROL Enhanced Experience Composer] (EEC) . 

For more information, see [Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

+++

## Can you point me the details of the new IPs for allowlisting? 

+++Details
For more information about IP addresses that you can allowlist, see the following articles:

* **Enhanced Experience Composer (EEC)**: See [The EEC won't load an internal QA URL that is not accessible on public IP](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#section_D29E96911D5C401889B5EACE267F13CF) in *Troubleshooting issues related to the Enhanced Experience Composer*
* **[!UICONTROL Recommendations]**: See [IP addresses used by Recommendations feed-processing servers](/help/main/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md).

+++

## Does the environment reset to staging by default on the new Recommendations UI?

+++Details
Environments now default to the last one used by the customer. To switch environments, use the [!UICONTROL Environment] selector in the upper-right corner of the [!UICONTROL Catalog Search] UI.

![Environment switch](/help/main/c-intro/assets/environmnent.png)

+++

## How complex is it to connect [!DNL Adobe Analytics] or [!DNL Customer Journey Analytics] to [!DNL Target]?

+++Details
Integrating [!DNL Adobe Analytics] (AA) or [!DNL Customer Journey Analytics] (CJA) with [!DNL Target] can range from moderate to advanced effort, depending on your current setup. If you're using [!DNL Adobe Experience Platform] and have implemented the [!DNL Platform Web SDK], the integration is more streamlined. However, legacy implementations using at.js or AppMeasurement may require additional configuration, including:

* Enable the [Analytics for Target (A4T) integration](/help/main/c-integrating-target-with-mac/a4t/a4t.md)
* Integrate [[!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).
* Map report suites and data views
* Ensure consistent identity resolution (ECID)
* Validate data collection and attribution settings

+++
