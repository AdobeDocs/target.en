---
keywords: target user interface;user interface;ui;frequently asked questions;faq
description: Questions and answers about the updated [!DNL Target]t user interface.
title: Where Can I find FAQs about the updated [!DNL Target] UI?
feature: Overview
hide: yes
hidefromtoc: yes
---
# Updated Target UI FAQ

Find answers to common questions about the updated [!DNL Adobe Target] UI, with helpful tips and links to learn more.

{{updated-ui}}

## Is the updated UI available to all current [!DNL Target] customers, [!UICONTROL Standard] and [!UICONTROL Premium]? 

+++Details
The updated UI is available to all [!DNL Target] customers, [!UICONTROL Standard] and [!UICONTROL Premium]. No upgraded license or SKU is required.

The rollout of the new [!DNL Target] UI was completed on May 27, 2025. At that point, all customers have access to the latest UI version.

For more information about the rollout and deprecation of the temporary UI version toggle, see [Target UI version toggle deprecation (May 23, 2025)](/help/main/r-release-notes/release-notes-for-previous-releases.md#toggle) in *Release notes for previous releases*.

+++

## Will the current list of bugs be fixed before the legacy UI is deprecated?

+++Details
The [!DNL Target] team is actively addressing issues related to the new UI rollout. Updates and ongoing improvements are detailed in the release notes.

For more information about the rollout and deprecation of the temporary UI version toggle, see [Target UI version toggle deprecation (May 23, 2025)](/help/main/r-release-notes/release-notes-for-previous-releases.md#toggle) in *Release notes for previous releases*.

+++

## Can customers apply for the UI version toggle to remain for their accounts if they prefer to stay with the legacy UI?

+++Details
The UI version toggle is a temporary feature that lets you switch between the updated [!DNL Target] UI and the legacy version using a toggle button. This option is available only during the final phase of the UI rollout. Once the rollout is complete, the toggle will be removed, and all users will transition permanently to the updated UI on June 22, 2025. 

There are several limitations with using the UI version toggle, including visibility of new activities, editing of existing activities, and the consistency of activity details.

For more information about the rollout and deprecation of the temporary UI version toggle, see [Target UI version toggle deprecation (May 23, 2025)](/help/main/r-release-notes/release-notes-for-previous-releases.md#toggle) in *Release notes for previous releases*.

++++

## Can [!DNL Adobe] delay our migration to the updated UI until the full rollout is complete?

+++Details
[!DNL Target] does not offer the option to delay or customize the timing of the UI migrations. Customers are transitioned in phases, and the rollout schedule is managed by [!DNL Adobe]. For the latest updates, refer to the release notes.

There are several limitations with using the UI version toggle, including visibility of new activities, editing of existing activities, and the consistency of activity details.

For more information about the rollout and deprecation of the temporary UI version toggle, see [Target UI version toggle deprecation (May 23, 2025)](/help/main/r-release-notes/release-notes-for-previous-releases.md#toggle) in *Release notes for previous releases*.

+++

## How can I tell if an activity was created or edited in the legacy UI or in the updated UI?

+++Details
Activities created or edited in the updated UI follow the same guided, three-step workflow and might include UI-specific metadata or formatting not present in legacy-created activities. Although there's no visible tag or label in the interface, differences in layout, structure, or available options (such as enhanced targeting or preview features) can indicate which UI was used. For detailed identification, check the activity's change history or consult your implementation logs.

+++

## What are the differences between creating offers in the legacy versus the updated UI? Are additional attributes required?

+++Details
Muti, help needed.

+++

## What happened to the offer preview links in the updated UI?

+++Details
Muti, help needed.

+++

## I have to disable the !UICONTROL Enhanced Experience Composer when editing existing activities with the updated UI. Has [!DNL Adobe] observed similar behavior with other customers?

+++Details
Muti, help needed.

+++

## Can you point me the details of the new IPs for allowlisting? 

+++Details
For more information about IP addresses that you can allowlist, see the following articles:

* **Enhanced Experience Composer (EEC)**: See [The EEC won't load an internal QA URL that is not accessible on public IP](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#section_D29E96911D5C401889B5EACE267F13CF) in *Troubleshooting issues related to the Enhanced Experience Composer*
* **[!UICONTROL Recommendations]**: See [IP addresses used by Recommendations feed-processing servers](/help/main/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md).

+++

## We have had issues with Browse not working or allowing us to browse. Has [!DNL Adobe] observed similar behavior with other customers?

+++Details
Muti, help needed.

+++

### Does the environment reset to staging by default on the new Recommendations UI?

+++Details
Muti, help needed.

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




