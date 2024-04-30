---
keywords: target documentation change log;documentation updates;new topics;edits;updates;update 
description: Keep up to date with important additions and changes to the [!DNL Adobe Target] documentation.
title: Where Can I See Documentation Updates for [!DNL Target]?
feature: Release Notes
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
---
# Documentation changes

This page lists significant changes made to the [!DNL Adobe Target] product documentation.

## [!DNL Target] Standard/Premium 24.3.1 (March 4-6, 2024)

|Date|Topic|Changes|
| --- | --- | --- |
|April 30|[Troubleshooting issues related to the [!UICONTROL Enhanced Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md)|Updated the list of IP addresses for Adobe's server used for the EEC proxy to allowlist.|
|April 23|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information explaining Google's plan to start disabling extensions created using Manifest V2. [!DNL Adobe] recommends that customers move to the new [!UICONTROL Visual Editing Helper] extension as soon as possible.|
|April 23|[[!UICONTROL Visual Experience Composer] helper extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)|Updated the Important note at the top of the page explaining Google's plan to start disabling extensions created using Manifest V2, which includes the extension documented in this article. [!DNL Adobe] recommends that customers move to the new [!UICONTROL Visual Editing Helper] extension as soon as possible.|
|April 9|[Troubleshooting issues related to the [!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md)|Updated the following section:<ul><li>My page does not display in the VEC (VEC only)</li></ul>Added the following new section:<ul><li>Issues caused by CSS conflicts in the [!UICONTROL Visual Experience Composer]</li></ul>|
||[Personalization Insights reports](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md)|Updated the Considerations section.|
|March 22|[Allowlist Target edge nodes](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/allowlist-edges){target=_blank}|Removed references to edge nodes 31 through 38 because this nodes no longer exist. Ensure that your allowlist is up to date.|
||[The impact of third-party cookie deprecation on Target (at.js)](https://experienceleague.adobe.com/docs/target-dev/assets/third_party_cookie_deprecation){target=_blank}|New blog post describing what Google's planned deprecation of third-party cookies means for your [!DNL Adobe Target] at.js implementation.|
|March 14|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Adobe Experience Platform Visual Editing Helper] for [!DNL Google Chrome].|
|March 13|[[!UICONTROL Time Frame]](/help/main/c-target/c-audiences/c-target-rules/time-frame.md)|Added information to note to re-save time-based audiences to account for Daylight Saving Time (DST).|
|March 6|[Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md)|Updated information in the following section: "Updates for [!DNL iPad] and [!DNL iPhone] in [!UICONTROL Browser] audience attributes (April 30, 2024)".|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Updated entire section: "Updates for `Browser:iPad` and `Browser:iPhone` in [!UICONTROL Browser] audience attributes (April 30, 2024)".|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 24.1.1 release.|

## [!DNL Target] Standard/Premium 24.1.1 (January 22, 23, & 25, 2024)

|Date|Topic|Changes|
| --- | --- | --- |
|February 28|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added information about the [!DNL Target] Standard/Premium 24.3.1 (March 4-6, 2024) release.|
|February 26|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the upcoming [!UICONTROL Adobe Target Community] Coffee Break (February 28, 2024).|
|February 23|[IP addresses used by [!DNL Recommendations] feed-processing servers](/help/main/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md)|Added the following important note and new IP addresses that you should allowlist.<P>**Important**: The [!DNL Target] team is currently updating the NAT gateway addresses for downloading [!DNL Recommendations] feeds. If you implement IP allowlisting, ensure that you allowlist the following new AWS hosts. The existing hosts are scheduled to be decommissioned on June 30, 2024. To ensure a smooth transition, allowlist all nine addresses. There is no urgency to remove the existing addresses. |
|February 8|[Prefetch](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/prefetch.html){target=_blank}|Added new section: "Prefetch mboxes with clickTrack metrics when using Analytics for Target (A4T)"|
|February 5|[Create an activity that uses Analytics as the reporting source](/help/main/c-integrating-target-with-mac/a4t/campaign-creation.md)|Added text specifying that you cannot use the same activity name for two activities from separate workspaces when using [!UICONTROL Analytics for Target] (A4T) as the reporting source.|
||[Activity settings - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-activity-setup.md)|Added text specifying that you cannot use the same activity name for two activities from separate workspaces when using [!UICONTROL Analytics for Target] (A4T) as the reporting source.|
||[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the Adobe Target Community Coffee Break scheduled for February 7, 2024.|
|January 24|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Added release notes for at.js version 2.11.4.|
||[Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation)|Announced that the two new profiles are not yet available. These notes will be updated when these profiles are available.|
||[at.js Frequently Asked Questions](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-faq.html){target=_blank}|Added FAQ regarding at.js in an Ionic App environment. This implementation is not tested or recommended.|
|January 22|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added important information about the deprecation of iPad and iPhone from the [!UICONTROL Browser] audience attribute that requires changes on your part prior to April 30, 2024.|
||[Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation)|Added new section: <ul><li>Deprecation of iPad and iPhone from Browser audience attribute (April 30, 2024)</li></ul>|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 24.1.1 release.|

## [!DNL Target] Standard/Premium 23.11.1 (November 13 & 14, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|January 18|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease notes for the upcoming [!DNL Target Standard/Premium] 24.1.1 release.|
|December 13|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the [!DNL Adobe Target] 2024 Personalization Maturity Webinar Series.|
||[targetGlobalSettings()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}|Added two new optional settings: <ul><li>aepSandboxId</li><li>aepSandboxName</li></ul>|
|December 4|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added registration information for the "Machine Learning & AI Reporting & Analysis" [!DNL Adobe Target Community] Coffee Break session: Wednesday, December 6, 2023.|
|December 1|[Adobe Target Profile Update APIs](https://experienceleague.adobe.com/docs/target-dev/developer/api/profile-apis/profile-api-overview.html){target=_blank}|Moved legacy API documentation to the following articles:<ul><li>[Adobe Target Profile APIs overview](https://experienceleague.adobe.com/docs/target-dev/developer/api/profile-apis/profile-api-overview.html){target=_blank}</li><li>[Adobe Target Single Profile Update API](https://experienceleague.adobe.com/docs/target-dev/developer/api/profile-apis/profile-single-api.html){target=_blank}</li><li>[Adobe Target Bulk Profile Update API](https://experienceleague.adobe.com/docs/target-dev/developer/api/profile-apis/profile-bulk-api.html?){target=_blank}</li></ul>|
|November 29|[Bulk Profile Update API](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/bulk-profile-update-api.html){target=_blank}|Clarified the differences about how [!DNL Target] handles customer attributes when creating a profile for a user [!DNL Target] has not yet seen when using the [!UICONTROL Bulk Profile Update API] v2 as opposed to v1.|
|November 21|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Added release notes for at.js 2.11.3.|
|November 17|[Administrator first steps](/help/main/administrating-target/start-target.md)|Added the following important note:<ul><li>Users with [!UICONTROL Product Admin] or [!UICONTROL System Admin] rights in the [!DNL Adobe Admin Console] can edit or change all settings on the [!UICONTROL Administration] page of [!DNL Target], regardless of their [!DNL Target] role. Users without [!UICONTROL Product Admin] or [!UICONTROL System Admin] rights in the [!DNL Adobe Admin Console] must have the specific [!DNL Target] role to make these changes.1</li></ul>|
||[Limits](/help/main/r-troubleshooting-target/target-limits.md#in-mbox)|Updated section with information about how [!DNL Target] handles truncation in at.js 2.*x* and the [!DNL Adobe Experience Platform Web SDK].|
||[Delivery API](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/overview.html){target=_blank}|Added redirects to the current Delivery API documentation and deprecated the legacy documentation (`http://developers.adobetarget.com/api/delivery-api/`). Please update bookmarks, as needed.|
|November 16|[Bulk profile update API](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/bulk-profile-update-api.html){target=_blank}|Added the following caveat: "Updates generally occur in under one hour, but may take as long as 24 hours to be reflected."|
|November 13|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.11.1 release.|

## [!DNL Target] Standard/Premium 23.10.2 (October 24, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|November 10|[Recommendations API Reference](https://developer.adobe.com/target/administer/recommendations-api/){target=_blank}|The [!DNL Adobe Target] [!DNL Recommendations] API has been relocated to the [!DNL Adobe Developer] website. Please update your bookmarks, if necessary.|
||[Time Frame](/help/main/c-target/c-audiences/c-target-rules/time-frame.md)|Added note that [!DNL Target] time audiences do not take into account Daylight Saving Time (DST) changes. You must manually update audiences to account for DST changes.|
|November 8|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease notes for the upcoming [!DNL Target Standard/Premium] 23.11.1 release.|
|October 28|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Added details about the at.js 2.11.2 release.|
|October 25|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the [!UICONTROL Activities] page user interface refresh (October 25, 2023)|
|October 24|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.10.2 release.|

## [!DNL Target] Standard/Premium 23.9.1 (September 6-11, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|October 17|[Reporting FAQ](/help/main/c-reports/reporting-frequently-asked-questions.md#section_E4722F6445884130951DF79981C8289B)|Updated the following FAQ: "Why is there no data available for my activity's report? "|
|October 11|[[!DNL Adobe Analytics] as the reporting source for [!DNL Adobe Target] (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA)|Updated information about A4T support for the [!DNL Adobe Experience Platform Web SDK].|
|October 10|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Added release notes for at.js version 2.11.0.|
|October 6|[Response tokens](/help/main/administrating-target/response-tokens.md)|Updated all code samples.|
||[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}|Updated entire tutorial in the *[!UICONTROL Adobe Target Tutorials]* guide.|
|October 4|[Activities](/help/main/c-activities/activities.md)|Updated text and images to reflect the UI refresh included in the [!DNL Target] 23.9.4 release.|
||[Feeds](/help/main/c-recommendations/c-products/feeds.md)|Updated text and images to reflect the UI refresh included in the [!DNL Target] 23.9.4 release.|
|October 2|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.9.3 release.|
||[[!DNL Recommendations] implementation pattern](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html){target=_blank}|The new *Recommendations implementation pattern using at.js* articles help you understand and create your [!DNL Adobe Target Recommendations] implementation when using the at.js JavaScript library.<P>For general information about [!DNL Target] patterns, see [Implementation patterns overview](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/pattern-overview.html){target=_blank} in the *Adobe Target Developer Guide*.<P>The new Recommendations implementation pattern is composed of the following articles:<ul><li>[Recommendations implementation pattern using at.js overview](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html){target=_blank}</li><ul><li>[Initialize SDKs](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/initialize-sdk.html){target=_blank}</li><li>[Configure data collection](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/data-collection.html){target=_blank}</li><li>[Render experiences](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/render-experiences.html?lang=en){target=_blank}</li><li>[Notify [!DNL Target]](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/notify-target.html?lang=en){target=_blank}</li></ul></ul>|
|September 29|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease notes for the [!DNL Target Standard/Premium] 23.9.3 release.|
||[Initialize the Java SDK](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/java/initialize-sdk.html){target=_blank}|Added the following new parameters to the table:<ul><li>`connectionTtlMs`</li><li>`idleConnectionValidationMs`</li><li>`evictIdleConnectionsAfterSecs`</li></ul>|
|September 22|[Troubleshooting issues related to the [!UICONTROL Enhanced Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#section_D29E96911D5C401889B5EACE267F13CF)|Updated the list of IP addresses to allowlist.|
|September 18|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.9.3 release.|
|September 15|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease notes for the [!DNL Target Standard/Premium] 23.9.3 release.|
|September 12|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.9.2 release.|
||[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Added release notes for the at.js version 2.10.3.|
|September 11|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added prerelease notes for the [!DNL Target Standard/Premium] 23.9.2 release.|
|September 6|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.9.1 release.|

## [!DNL Target] Standard/Premium 23.8.1 (August 9, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|September 1|[Environments](/help/main/administrating-target/environments.md##section_4F8539B07C0C45E886E8525C344D5FB0)|Updated note under "Set the default environment for reporting."|
|August 30|[Privacy](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/privacy.html#aep){target=_blank}|Added new section: "Datastream-level IP obfuscation when using the Adobe Experience Platform Web SDK"|
||[Activity settings - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-activity-setup.md#section_9F8092BE4225442896F926540292F221)|Corrected time frame to expect data to display in reports in the following FAQ: "I just created an activity. Why don't I see any data coming in?"|
|August 29|[Supported features for on-device decisioning](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/supported-features.html){target=_blank}|Added the list of Geo attributes supported for targeting when using on-device decisioning (ODD) client-side.|
||[On-device decisioning overview](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html){target=_blank}|Added the list of Geo attributes supported for targeting when using on-device decisioning (ODD) server-side.|
||[Implement Target with the AEP Mobile SDK in a native app with web views](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/native-app.html){target=_blank}|New article.|
||[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the upcoming Adobe Target Community Coffee Break (August 30, 2023): "Strategize for maximum ROI impact with peak season readiness" webinar follow-up.|
|August 14|[Activity QA](/help/main/c-activities/c-activity-qa/activity-qa.md)|Added information clarifying that loading a page on your site with an empty value does *not* remove the QA cookie from the browser when at.js 2.*x* is deployed.|
||[Statistical calculations in A/Bn tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md)|Updated the definition of "Confidence."|
||[Offers](/help/main/c-experiences/c-manage-content/manage-content.md)|Added note explaining that image offers are not part of the [!UICONTROL Enterprise User Permissions] model.|
|August 9|[Target mobile preview](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html){target=_blank}|Updated topic with information about the current versions of the [!DNL Adobe Experience Platform Mobile SDK].|
|August 9|[Target mobile preview](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html){target=_blank}|Updated topic with information about the current versions of the [!DNL Adobe Experience Platform Mobile SDK].|
||[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following webinar scheduled for August 17, 2023: *Strategize for maximum ROI impact with peak season readiness*.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.8.1 release.|

## [!DNL Target] Standard/Premium 23.7.1 (July 24-26, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
||[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following webinar scheduled for August 17, 2023: *Strategize for maximum ROI impact with peak season readiness*.|
|August 7|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Clarified information about supported versions of at.js.|
|July 25|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md#edge)|Added information about the planned edge infrastructure upgrade scheduled for August 9, 2023.|
||[Allowlist Target edge nodes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank}|Updated the NAT and IP/domains for edge deployments 41-48.|
|July 24|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.7.1 release.|
