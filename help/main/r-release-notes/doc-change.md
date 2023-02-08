---
keywords: target documentation change log;documentation updates;new topics;edits;updates;update
description: Keep up to date with important additions and changes to the [!DNL Adobe Target] documentation.
title: Where Can I See Documentation Updates for [!DNL Target]?
feature: Release Notes
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
---
# Documentation changes

This page lists significant changes made to the [!DNL Adobe Target] product documentation.

## [!DNL Target] Standard/Premium 22.13.3 (January 25, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|February 8|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for at.js 2.10.1.|
|February 2|[Troubleshooting issues related to the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md#section_FA2A18E8FD6A4274B2E395DBAA2FB407)|Updated the following section:<ul><li>The VEC appears broken when I use browse mode</li></ul>|
||[Build audiences in Target](/help/main/c-target/c-audiences/create-audience.md)|Added list of characters and character sequences that cannot be used in audience names.|
|January 31|[Limits](/help/main/r-troubleshooting-target/target-limits.md#mbox-names)|Added list of allowed and disallowed characters in mbox names.|
|January 25|[Create JSON offers](/help/main/c-experiences/c-manage-content/create-json-offer.md)|Indicated that support for JSON offers in [!UICONTROL Automated Personalization] (AP) activities using the Form-Based Experience Composer is now available.|
||[Adobe Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following event:<ul><li>[!DNL Adobe Target] Community Q&A Coffee Break: Mobile & Authenticated Use Cases for Experience Optimization</li></ul>|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.13.3 release.|

## [!DNL Adobe Target] Standard/Premium 22.10.1 (staggered release October 10-13, 2022)

|Date|Topic|Changes|
| --- | --- | --- |
|January 13|[Visual Editing Helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)|Added a Frequently Asked Questions section.|
|January 12|[Visual Experience Composer helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)|Updated Important note explaining the status of the current [!UICONTROL Visual Experience Composer] helper extension. |
||[Targets and audiences FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)|Added information explaining that audience URL targeting and URL targeting added via [!UICONTROL Template Rules] are evaluated as URL targeting.|
||[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease notes for the 22.13.3 release.|
|December 21|[Customize a design using Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md)|Clarified that entity attributes sent to [!DNL Recommendations] in the `productPage` mbox or the CSV upload can be displayed in a design, with the exception of "multi-value" attributes.|
|December 20|[Offer reporting groups in [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md)|Added additional information about reporting groups under "Caveats."|
|December 14|[Report settings](/help/main/c-reports/c-report-settings/report-settings.md#environment)|Added note under the "Environment" section about using [!DNL Adobe Experience Platform] (AEP) to send metric data to [!DNL Target].|
|November 29|[Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md)|Clarified text by adding the following paragraph:<ul><li>A visitor's geo information is determined from the originating IP address of a [!DNL Target] location request (mbox request). The IP-to-geo resolution is done for the first call of a new session. This means, if the IP address of a visitor changes mid session of a visit, the geo information is still based on the IP address of the first call.</li></ul>|
|November 28|[Models API (Blocklisting) Overview](https://developer.adobe.com/target/before-administer/models-api/){target=_blank} in the *Adobe Target Developer Guide*.|New Models API.<br>Features can be blocked from [!DNL Target] machine-learning algorithms, preventing them from being used in any [!UICONTROL Auto-Target] or [!UICONTROL Automated Personalization] model or activity.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the Models API release (November 23, 2022).|
|November 23|[Before you implement Analytics for Target (A4T) with at.js](/help/main/c-integrating-target-with-mac/a4t/before-implement.md)|Updated the link to the [Marketing Cloud Integrations Provisioning Form](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}.|
|November 16|[Adobe Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added registration information for the following event:<ul><li>[!DNL Adobe Target] Community Q&A coffee break (November 29)</li></ul>|
|November 8|[How long should you run an A/B Test?](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)|Added important note that to get accurate results you must reload the page before changing any parameter numbers in the [!DNL Adobe Target] [!UICONTROL Sample Size Calculator]. Also added a note in the actual [calculator](https://experienceleague.adobe.com/tools/calculator/testcalculator.html){target=_blank}.|
||[Redirect offers - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682)|Updated the description for the `adobe_mc_sdid` parameter in the table.|
||[Troubleshooting activities](/help/main/c-activities/c-troubleshooting-activities/troubleshooting-activities.md)|Added new section: "After activity conversion, the visitor is not in any experience."|
||[Custom parameters](/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md)|Added note that the mbox you select from the [!UICONTROL Filter By] drop-down list is not saved on activity creation. This option lets you filter the parameters based on the selected mbox.|
|November 2|Known issues and resolved issues|Removed page and relocated relevant issues to the appropriate pages so that information will be in context.|
|October 25|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.10.3 release.|
|October 19|[Category affinity](/help/main/c-target/c-visitor-profile/category-affinity.md#section_8B86C7FF50294208866ABF16F07D5EB9)|Added a note explaining scoring when several categories are are passed within a single mbox call.|
|October 18|[Create an [!UICONTROL Automated Personalization] activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)|Updated text to indicate that although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the [!UICONTROL Dissalow Duplicates] option.|
||[Automated Personalization FAQs](/help/main/c-activities/t-automated-personalization/automated-personalization-faq.md)|Updated text to indicate that although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the [!UICONTROL Dissalow Duplicates] option.|
|October 14|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added registration information about the [!DNL Adobe Target] Community Q&A Coffee Break (October 26, 2022).|
|October 10|[[!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)|New article.|
||[Troubleshooting issues related to the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md)|Updated the "[My page does not display in the VEC (VEC only)](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md#does-not-load)" section.|
|October 4|[Statistical calculations in A/Bn tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md)|New topic.<br>The information in this article replaces the *Adobe Target Calculations for A/B Testing* pdf file that was previously available for download on this site.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.10.1 release.|

## [!DNL Adobe Target] Standard/Premium 22.9.1 (staggered release September 13-15, 2022)

|Date|Topic|Changes|
| --- | --- | --- |
|October 3|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Updated the dates for the [!DNL Target Standard/Premium] 22.10.1 release.|
|September 22|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following event:<ul><li>[!DNL Adobe Target] Community Q&A coffee break (September 28, 2022)</li></ul>|
|September 15|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following webinar:<ul><li>Fine-Tuning AI-Powered Personalization: New Features in [!DNL Adobe Target] (October 11, 2022)</li></ul>|
|September 13|[Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md)|Added information about notifications when a [!DNL Recommendations] feed fails.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.9.1 release.|

## Adobe Target Standard/Premium 22.8.1 (staggered release: August 17-18, 2022)

|Date|Topic|Changes|
| --- | --- | --- |
|August 22|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added the information about the following announcement:<ul><li>[!DNL Target] named leader in Gartner Magic Quadrant for Personalization Engines (2022)</li></ul>Added information about the following upcoming events:<ul><li>[!DNL Adobe Target] Community Q&A coffee break (August 31, 2022)</li><li>Chef's Collection: Recipes for Personalization (August 30, 2022)</li><li>[!DNL Adobe Target] Skill Builders – Mobile Experience Optimization (September 6, 2022)</li><li>[!DNL Adobe Target] Skill Builders – AI-Driven Personalization and Recommendations (September 15, 2022)</li></ul>Added recording link for the following past webinar session:<ul><li>Adobe: Personalization Industry Insider - Retail (August 11, 2022)</li></ul>|
|August 22|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.8.1 release.|

## Adobe Target Standard/Premium 22.6.1 (staggered release: June 7-9, 2022)

|Date|Topic|Changes|
| --- | --- | --- |
|June 30|[Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}|Launched the *Adobe Target Developer Guide* to consolidate all [!DNL Target] developer content in one convenient portal. The portal includes information about implementing [!DNL Target] and [!DNL Recommendations], [!DNL Target] SDKs, and [!DNL Target] APIs.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.6.2 release.|
||[Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added recording links for past webinar sessions.|
|June 14|[Plan and implement Recommendations](https://developer.adobe.com/target/implement/recommendations/){target=_blank}|Updated code samples in the following sections:<ul><li>Cart adds/cart views/checkout pages</li><li>Exclude items already in the visitor's cart</li></ul>|
|June 7|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.6.1 release.|

## Adobe Target Standard/Premium 22.5.1 (staggered release; May 11-13, 2022)

|Date|Topic|Changes|
| --- | --- | --- |
|June 7|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information for the [!DNL Target Standard/Premium] 22.6.1 release.|
|May 31|[Target announcements and events](/help/main/r-release-notes/target-announcements.md#webinar-series)|Added information about the upcoming [!DNL Adobe Target] Community Coffee Break (June 29, 2022)|
|May 25|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the [!DNL Target] platform release (May 25, 2022) and the at.js 2.9.0 release (May 27, 2022).|
||[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Added information about the at.js 2.9.0 release.|
||[User-agent and Client Hints](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank}|New topic.|
||[Target announcements and events](/help/main/r-release-notes/target-announcements.md#webinar-series)|Added link for recording of the following webinar: Dick's Sporting Goods: Personalization and the Changing Landscape in Retail (May 19, 2022)|
|May 23|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease notes for at.js version 2.9.0 (May 25, 2022).|
|May 11|[Target announcements and events](/help/main/r-release-notes/target-announcements.md#webinar-series)|Added information and registration links for the following webinars:<ul><li>Dick's Sporting Goods: Personalization and the Changing Landscape in Retail</li><li>Adobe: Personalization Industry Insider - Financial Services and Insurance</li><li>City National Bank: How to Achieve the Top 1% in Digital Optimization</li><li>Adobe: Personalization with Precision - [!DNL Adobe Analytics] and [!DNL Target]</li><li>City National Bank: Zero to Hero - Starting & Scaling a Personalization Program</li><li>Adobe: Uncover High-Impact Optimization Opportunities</li><li>Adobe: Personalization Industry Insider - Retail</li></ul>Added the recording for the following webinar:<ul><li>Real-Time Personalization with [!DNL Adobe Target]</li></ul>|
||[Content Security Policy (CSP) directives](https://developer.adobe.com/target/before-implement/privacy/content-security-policy/){target=_blank}|Added FAQ section.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the [!DNL Target Standard/Premium] 22.5.1 and Target platform (May 11-13, 2022) releases.|

## Adobe Target Standard/Premium 22.4.1 (April 28)

|Date|Topic|Changes|
| --- | --- | --- |
|May 10|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information about the [!DNL Target Standard/Premium] 22.5.1 release.|
|April 28|[Enterprise user permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#move-audience)|Added the following FAQ:<ul><li>Can I move an audience from one workspace to another?</li></ul>|
||[[!UICONTROL Auto-Allocate] overview](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#section_0E72C1D72DE74F589F965D4B1763E5C3)|Added the following FAQs:<ul><li>Can an [!UICONTROL Auto-Allocate] activity adjust the lookback window over the course of a test to take into consideration changing trends over time?</li><li>Does [!UICONTROL Auto-Allocate] show a winning experience to a returning visitor if the winning experience is different from what the visitor saw when qualifying for the activity?</li></ul>|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the [!DNL Target Standard/Premium] 22.4.1 and Target platform (April 27, 2022) releases.|

## Adobe Target Standard/Premium 22.3.1 (April 5)

|Date|Topic|Changes|
| --- | --- | --- |
|April 26|[Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information for the following events:<ul><li>Webinar: Real-Time Personalization with Adobe Target (April 28, 2022)</li><li>[!DNL Adobe Target] Community Q&A Coffee Break (May 25, 2022)</li></ul>|
||[Redirect offers - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#discrepancies)|Added the following FAQ:<ul><li>How can I minimize discrepancies in traffic distribution when using redirect offers in A4T activities?</li></ul>|
||[AEM experience fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)|Added following section:<ul><li>Removing ClientLibs and extraneous HTML from Experience Fragments exported to Target</li></ul>|
|April 21|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information about the [!DNL Target] platform release scheduled for April 17, 2022.|
|April 20|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information about the [!DNL Target Standard/Premium] 22.4.1 release.|
|April 14|[Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)|Added information to the Rearrange section to explain how to deal with inconsistent VEC behavior with the [!UICONTROL Move] and [!UICONTROL Rearrange] actions due to lazy loading of DOM elements.|
|April 13|[Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following event:<ul><li>[!DNL Adobe Target] Community Q&A Coffee Break (April 27, 2022)</li></ul>|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release information about the [!DNL Target] Platform release.|
|April 4|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Updated information about the [!DNL Target Standard/Premium] 22.3.1 release.|

## Adobe Target Standard/Premium 22.2.1 (February 1, 2022)

|Date|Topic|Changes|
| --- | --- | --- |
|March 30|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release information about the [!DNL Target] Platform release.|
|March 28|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information about the [!DNL Target] Platform release.|
|March 22|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release information about the [!DNL Target Standard/Premium] customer engineering fixes release.|
||[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information about the [!DNL Target Standard/Premium] 22.3.1 release.|
|March 17|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information about the [!DNL Target Standard/Premium] customer engineering fixes release.|
||[Real-time profile syncing for mbox3rdPartyId](/help/main/c-target/c-visitor-profile/3rd-party-id.md)|Updated following sentence regarding profile syncing: "Updates are synced with the profile store every 5-10 minutes."|
|March 8|[Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following event:<ul><li>[!DNL Adobe Target] Community Q&A Coffee Break (March 30, 2022)</li></ul>|
|March 7|[Create audiences](/help/main/c-target/c-audiences/audiences.md#aep)|Added new section under "Use audiences from [!DNL Adobe Experience Platform]:"<ul><li>Personalization use cases</li></ul>|
|February 25|[A4T support for Auto-Allocate and Auto-Target activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)|Updated the following sections:<ul><li>[Auto-Allocate and Auto-Target](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#both)</li><li>[Auto-Allocate](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa)</li></ul>|
||[Interpret Auto-Allocate reports](/help/main/c-activities/automated-traffic-allocation/determine-winner.md)|Added new FAQ:<ul><li>Are the "No Winner," "Winner," and "star" badges available for [!UICONTROL Auto-Allocate] activities that use [!UICONTROL Analytics as the reporting source] (A4T)?</li></ul>|
||[Create an activity-only audience](/help/main/c-target/creating-activity-only-audience.md)|Added information in the "Considerations" section discussing exclude rules.|
|February 10|[Visual Experience Composer helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)|Added information about loading websites with Service Workers in the Visual Experience Composer (VEC).|
|February 7|[Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following event:<ul><li>[!DNL Adobe Target] Community Q&A Coffee Break (February 23, 2022)</li></ul>|
|February 3|[Create audiences](/help/main/c-target/c-audiences/audiences.md#RTCDP)|Added new section and video: "Video: Next-hit personalization with Real-time CDP and [!DNL Adobe Target]."|
|February 2|[Troubleshoot content delivery](/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#escape)|Added following section: "Escaping double quotes in [!DNL Target] profile attribute value is not working as expected."|
|February 1|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the [!DNL Target Standard/Premium] 22.2.1 release.|

## [!DNL Adobe Target Standard/Premium] 22.1.1 (January 12, 2022)

|Date|Topic|Changes|
| --- | --- | --- |
|January 31|[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease information about the [!DNL Target Standard/Premium] 22.2.1 release.|
|January 28|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the at.js 2.8.1 release.|
||[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Added information about the at.js 2.8.1 release.|
|January 27|[AEM experience fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)|Updated topic and added information about [!DNL AEM as a Cloud Service] and [!DNL Adobe I/0].|
|January 26|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the [!DNL Target Standard/Premium] 22.1.2 release.|
||[Create audiences](/help/main/c-target/c-audiences/audiences.md)|Added information about [!DNL Adobe Experience Platform] audiences.|
||[Combine multiple audiences](/help/main/c-target/combining-multiple-audiences.md)|Added information about [!DNL Adobe Experience Platform] audiences.|
|January 21|[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Added information about the at.js 1.8.3 release.|
|January 19|[Upgrading from at.js 1.*x* to at.js 2.*x*](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} |Added following section: "at.js 2.*x* does not support creating audiences using vst.* parameters"|
|January 12|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the [!DNL Target Standard/Premium] 22.1.1 release.|
||[Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}|Added link to tutorial with instructions to implement [!DNL Adobe Experience Cloud] with Web SDK.|
