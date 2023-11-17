---
keywords: target documentation change log;documentation updates;new topics;edits;updates;update 
description: Keep up to date with important additions and changes to the [!DNL Adobe Target] documentation.
title: Where Can I See Documentation Updates for [!DNL Target]?
feature: Release Notes
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
---
# Documentation changes

This page lists significant changes made to the [!DNL Adobe Target] product documentation.

## [!DNL Target] Standard/Premium 23.11.1 (November 13 & 14, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|November 17|[Administrator first steps](/help/main/administrating-target/start-target.md)|Added the following important note:<ul><li>Users with [!UICONTROL Product Admin] or [!UICONTROL System Admin] rights in the [!DNL Adobe Admin Console] can edit or change all settings on the [!UICONTROL Administration] page of [!DNL Target], regardless of their [!DNL Target] role. Users without [!UICONTROL Product Admin] or [!UICONTROL System Admin] rights in the [!DNL Adobe Admin Console] must have the specific [!DNL Target] role to make these changes.1</li></ul>|
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
||[Initialize the Java SDK](https://experienceleague.corp.adobe.com/docs/target-dev/developer/server-side/java/initialize-sdk.html){target=_blank}|Added the following new parameters to the table:<ul><li>`connectionTtlMs`</li><li>`idleConnectionValidationMs`</li><li>`evictIdleConnectionsAfterSecs`</li></ul>|
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

## [!DNL Target] Standard/Premium 23.6.1 (June 27-29, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|July 20|[Content Security Policy (CSP) directives](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/content-security-policy.html){target=_blank}|Added the following FAQ to the *Adobe Target Developer Guide*: How do I allow or prevent my site from being embedded as an iFrame under foreign domains?|
|July 10|[Considerations and known limitations](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/known-limitations.html){target=_blank}|Added information to the *Target Delivery API* documentation about HTTP/2 enforcing lowercase header names.|
|June 27|[Activity QA](/help/main/c-activities/c-activity-qa/activity-qa.md)|Activity QA is now available for all Target activity types, including [!UICONTROL Automated Personalization] (AP) activities. Removed information about preview links.|
||Preview URLs|Because all activity types now support Activity QA, this topic was deleted and redirected to the [Activity QA](/help/main/c-activities/c-activity-qa/activity-qa.md) topic.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.6.1 release.|

## [!DNL Target] Standard/Premium 23.5.1 (May 23-25, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|June 26|[Target for mobile apps](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/overview.html){target=_blank}|Added link to the Implement [!DNL Adobe Experience Cloud] in mobile apps tutorial.|
|June 12|[Adobe Target cookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-target.html){target=_blank}|Updated article in the *Experience Cloud Central Interface Components Guide* explaining cookies used by [!DNL Target].|
||[Initialize the Java SDK](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/java/initialize-sdk.html){target=_blank}|Added information about the "environment" parameter.|
||[Initialize the Python SDK](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/python/initialize-sdk.html){target=_blank}|Added information about the "environment" parameter.|
|June 5|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Updated information for the following events:<ul><li>Updated the registration link for the [!DNL Adobe Target Recommendations] Coffee Break (Wednesday, June 7, 2023)</li><li>Added information about the recent webinar "Mobile Experience Optimization and Personalization for Authenticated Environments" and added a link to the recording.</li></ul>|
||[Apply a reporting audience to a success metric](/help/main/c-target/apply-reporting-audience-success-metric.md)|Updated the "Considerations" section and added the "Example" section.|
||[Targets and audiences FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md#url-targeting)|Updated the "URL targeting" section.|
|May 30|[[!DNL Target] release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.5.2 release.|
||[Integrate with [!DNL Real-Time Customer Data Platform]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md)|Updated article with information about sharing [!UICONTROL Real-Time CDP Profile Attributes] with [!DNL Target] for use in HTML and JSON offers.|
||[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following upcoming Coffee Break events:<ul><li>[!DNL Adobe Target Recommendations] Coffee Break (June 7)</li><li>Personalization Program Readiness Webinar follow-up (June 21)</li></ul>|
|May 23|[Allowlist Target edge nodes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank}|Updated Important note.|
||[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Updated prerelease notes for upcoming releases.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.5.1 release.|

## [!DNL Target] Standard/Premium 23.4.1 (April 25-27, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|May 22|[Integrate with [!DNL Real-Time Customer Data Platform]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#videos-blogs)|Added the following new videos:<ul><li>Configure the [!DNL Adobe Target] destination in [!DNL Real-Time Customer Data Platform]</li><li>Activate segments and profile attributes</li><li>Use [!DNL Real-Time CDP] segments in [!DNL Target]</li><li>Use [!DNL Real-Time CDP] profile attributes in [!DNL Adobe Target]</li></ul>|
||[Allowlist Target edge nodes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank}|Updated Important note.|
|May 19|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Updated prerelease notes for upcoming releases.|
|May 17|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the [!UICONTROL Adobe Target Community] Q&A Coffee Break on Wednesday, May 24, 2023.|
|May 16|[Entity attributes](/help/main/c-recommendations/c-products/entity-attributes.md)|Indicated that "spaces" are not allowed in `entity.id` values.|
||[targetGlobalSettings()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}|Updated `viewsEnabled` description.|
||[Single Page Application implementation](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/target-atjs-single-page-application.html){target=_blank}|Made the following updates:<ul><li>Added Note after Step 2 under "Implementing Adobe Target Views."</li><li>Updated Step 2 "Execute Target request" under "Order of operations for initial page load."</li></ul>|
|May 4|[Configure authentication for Adobe Target APIs](https://experienceleague.adobe.com/docs/target-dev/developer/api/configure-authentication.html){target=_blank}|Added note explaining the need to migrate from a JWT credential to an OAuth Server-to-Server credential.|
|May 3|[View reports - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#activity-impressions)|Added the following FAQ:<ul><li>How do I track activity impressions in [!DNL Analysis Workspace] when using [!UICONTROL Analytics for Target] (A4T)?</li></ul>|
|April 26|[AEM [!UICONTROL Experience Fragments] and [!UICONTROL Content Fragments] overview](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md)|The [!UICONTROL AEM Content Fragments] feature is now available for all [!DNL Target customers].|
||[AEM [!UICONTROL Content Fragments]](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md)|The [!UICONTROL AEM Content Fragments] feature is now available for all [!DNL Target customers].|
||[*Adobe Target Developer Guide*](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html){target=_blank}|The *Adobe Target Developer Guide* has been relocated to *[!UICONTROL Adobe Experience League]*. The move to *[!UICONTROL Experience League]* aids in localization of text in additional languages, unifies search within *Experience League* to span and offer search results from both the *[!UICONTROL Adobe Target Business Practitioner Guide]* and the *[!UICONTROL Adobe Target Developer Guide]*, and provides additional benefits.<P>You will be redirected from the previous location to *[!UICONTROL Experience League]* automatically. Please update your bookmarks as necessary.|
|April 24|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following Adobe Target Community Coffee Break Q&A:<ul><li>Mobile experience optimization & personalization for authenticated environments</li></ul>|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.4.1 release.|

## [!DNL Target] Standard/Premium 23.3.1 (March 28-30, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|April 19|[[!UICONTROL Location Contribution] report (MVT)](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md)|Updated information in note.|
|April 13|[[!DNL Target] release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added information about the [!DNL Target] Standard/Premium 23.4.1 release (April 25-27, 2023).|
|April 12|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added link to register for the following webinar:<ul><li>Deliver personalized customer experiences, every time!</li></ul>|
||[Important Attributes report](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md#models-api)|Added the following FAQ:<ul><li>I see one or more attributes that I don't want the model to use for training. Can I remove those attributes from the training model?</li></ul>|
||[Enterprise user permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#multiple-roles)|Added the following FAQ:<ul><li>What happens if a user has multiple roles and permissions?</li></ul>|
||[AEM Content Fragments](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md)|New topic. Note that this feature is in the "prerelease" status for testing purposes.|
|April 5|[Use offer decisions](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md)|Added text indicating that [!UICONTROL Analytics as the reporting source] (A4t) is not supported in activities that use offer decisions.|
|April 3|[[!DNL Adobe Target] announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the [!UICONTROL Adobe Target Community] Coffee break scheduled for Wednesday, April 12, 2023.|
||[Allowlist Target edge nodes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank}|Added note to allowlist all [!DNL Adobe Analytics] IP address blocks.|
|March 30|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Updated release notes for the release of the Optimized A4T metrics for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] feature that lets you you choose metrics based on binomial events or metrics based on continuous events when using [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities.|
||[A4T support for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported)|Updated the "Supported goal metrics" section to include information about the supported (and unsupported) metrics for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities using [!UICONTROL Analytics for Target] (A4T)|
||[Adobe Target Tutorials](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html){target=_blank}|Updated the following tutorials:<ul><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li><li>[Setting up A4T reports in [!DNL Analysis Workspace] for [!UICONTROL Auto-Target] activities](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul>|
||[Target release notes (prerelease)](/help/main/r-release-notes/target-release-notes.md)|Added information for the [!DNL Adobe Experience Manager] (AEM) and [!DNL Adobe Target] [!UICONTROL Content Fragments] release. (April 6, 2023)|
|March 28|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 23.3.1 release.|

## [!DNL Target] Standard/Premium 22.15.1 (March 8 & 9, 2023) 

|Date|Topic|Changes|
| --- | --- | --- |
||[Edit an activity or save as draft](/help/main/c-activities/edit-activity.md)|Added a "Best practices" section.|
||[Modifications](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md)|Added the following note to the "Troubleshooting custom code" section:<ul><li>Custom Code offers in the VEC are not re-rendered when `triggerView()` is called with `{page: false}` as the option.</li></ul>|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added information about the at.js 2.10.2 release.|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.15.1 release.|

## [!DNL Target] Standard/Premium 22.13.3 (January 25, 2023)

|Date|Topic|Changes|
| --- | --- | --- |
|February 21|[Allowlist Target edge nodes](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank}|Updated list of IP addresses to allowlist for all regions in the [Adobe Target Developer Guide](https://experienceleague.corp.adobe.com/docs/target-dev/developer/overview.html){target=_blank}.|
||[Modifications](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md)|Added text explaining that the example using JQuery assumes that the customer's website has jQuery available on the page when [!DNL Target] executes the offers.|
|February 10|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.14.5 release.|
|February 8|[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for at.js 2.10.1.|
|February 2|[Troubleshooting issues related to the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md#section_FA2A18E8FD6A4274B2E395DBAA2FB407)|Updated the following section:<ul><li>The VEC appears broken when I use browse mode</li></ul>|
||[Build audiences in Target](/help/main/c-target/c-audiences/create-audience.md)|Added list of characters and character sequences that cannot be used in audience names.|
|January 31|[Limits](/help/main/r-troubleshooting-target/target-limits.md#mbox-names)|Added list of allowed and disallowed characters in mbox names.|
|January 25|[Create JSON offers](/help/main/c-experiences/c-manage-content/create-json-offer.md)|Indicated that support for JSON offers in [!UICONTROL Automated Personalization] (AP) activities using the Form-Based Experience Composer is now available.|
||[Adobe Target announcements and events](/help/main/r-release-notes/target-announcements.md)|Added information about the following event:<ul><li>[!DNL Adobe Target] Community Q&A Coffee Break: Mobile & Authenticated Use Cases for Experience Optimization</li></ul>|
||[Target release notes (current)](/help/main/r-release-notes/release-notes.md)|Added release notes for the [!DNL Target Standard/Premium] 22.13.3 release.|
