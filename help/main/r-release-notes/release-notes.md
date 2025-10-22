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

## [!DNL Target Standard/Premium] 25.10.1 (October 22, 2025)

This release contains the following updates and fixes:

**Activities**

+++ See details
* **Resolved a usability issue in the updated UI**. [!UICONTROL Observers] can now preview activities using the [!UICONTROL View Activity] option, just like in the legacy UI. (TGT-51741)
* **[!UICONTROL Observer] users can now view activity content in the updated UI.** Restored visibility for Observer-role users in the updated Activity UI. Previously, Observers were unable to view modifications, offers, and content changes—functionality that was available in the legacy UI. (TGT-53785)
* **[!UICONTROL Approver] users can now edit activity goals without editor privilege error.** Resolved a permissions issue in the Activity Create UI that blocked Approver-level users from saving changes to advanced goal settings. Affected users received a `403 Forbidden.Resource` error requiring editor privileges, despite having sufficient access. (TGT-53819)

+++

**Audiences**

+++See details
* **Multi-Audience Selection Restored in "This Activity Only" Reporting.** Resolved an issue in the Activity Create UI that prevented users from selecting multiple audiences under the [!UICONTROL This activity only] section in [!UICONTROL Goals & Settings]. (TGT-53283)
* **Audience-based reporting graphs now display conversion data correctly.** Resolved an issue in the [!UICONTROL Reports] tab that caused graphs to fail when selecting non-default audiences. While data and confidence metrics were available, the visual graph showed only a solid line, making analysis difficult. (TGT-53769)
* **The [!UICONTROL Targeting] UI now clearly indicates excluded audience rules.** Resolved an issue in the [!UICONTROL Targeting] section of the Activity Create UI where audience rules set to [!UICONTROL Exclude] were not clearly displayed. This led to confusion when reviewing targeting logic, especially for audiences excluding specific URLs. (TGT-53809)
* **Audience definition values now selectable and copyable in the [!UICONTROL Targeting] tab.** Resolved an issue in the Activity Create interface that prevented users from selecting and copying audience rule values in the [!UICONTROL Targeting] tab. This functionality was available in the legacy UI but missing in the updated UI. (TGT-53856)

+++

**Localization**

+++See details
* **Corrected mistranslation of "quote" in zh_CN page editor context.** Corrected a contextual translation error in the zh_CN locale where the term "quote" was inaccurately translated as "报价", implying a commercial price quotation. In the Typography > Heading style > Blockquote section, the intended meaning refers to a formatting element—quotation block—not pricing. (TGT-53841)
* **Corrected mistranslation of "quote removed" in zh_CN page editor context.** Corrected a translation error in the zh_CN locale where "quote removed" was inaccurately rendered as "移除了报价", implying a commercial price quotation. In the Typography > Heading style > Blockquote section, the term refers to a formatting element—quotation block—not pricing. (TGT-53843)
* **Corrected mistranslation of "quote rearranged" in zh_CN page editor context.** Corrected a contextual translation error in the zh_CN locale where "quote rearranged" was inaccurately translated as "重新排列了报价", implying a commercial price quotation. In the Typography > Heading style > Blockquote section, the term refers to a formatting element—quotation block—not pricing. (TGT-53844)
* **Corrected mistranslation of "quote changed" in zh_CN page editor context.** Corrected a translation error in the zh_CN locale where "quote changed" was inaccurately rendered as "更改了报价", suggesting a commercial price quotation. In the Typography > Heading style > Blockquote section, the term refers to a formatting element—quotation block—not pricing. (TGT-53845)

+++

**Recommendations**

+++See details
* **CSS selector changes for recommendations now save correctly.** Resolved an issue in the Activity Create UI that prevented users from updating the CSS selector for recommendation placements. Changes reverted after saving, blocking updates to targeting containers. (TGT-53835)
* **Page load event selection now persists in recommendation modifications.** Resolved an issue in the Activity Create UI that prevented users from saving changes when switching a recommendation's event type from [!UICONTROL View] to [!UICONTROL Page Load]. Although the selection appeared successful, it reverted after navigating away, blocking activity publication. (TGT-53957)

+++

**Reports**

+++See details
* **"[!UICONTROL Export order details to CSV]" now downloads complete data.** Resolved an issue in the updated [!UICONTROL Overview] UI that caused the "[!UICONTROL Export Order details to CSV]" option to download empty files, even when valid report data was present. (TGT-53787)

+++

**Security**

+++See details
* **IMS prefilter added to protect GQL endpoints from cross-org data exposure.** Resolved a security vulnerability in the Admin tab affecting the licenseGroups and targetProperties GraphQL endpoints. The issue stemmed from using the JIL API with an admin client token that could be exploited to access cross-org product data. (TGT-53837)

+++

**Visual Experience Composer (VEC)**

+++See details
* **Authoring stability restored in the Activity Create UI.** Resolved an intermittent issue in the VEC UI that caused authoring to fail and links to become unexpectedly clickable, redirecting users away from the page. (TGT-53153)
* **Editing restored for saved activities in the Activity Create UI.** Resolved an issue that prevented users from editing activities after saving modifications. Affected activities remained stuck in "[!UICONTROL Applying initial modifications]", blocking further updates and hiding the [!UICONTROL Cancel] button. (TGT-53631)
* **The VEC no longer stalls on "[!UICONTROL Applying initial modifications]."** Resolved a performance issue in the VEC that caused long delays when loading experiences with a high number of modifications. Affected users saw the UI stuck on "[!UICONTROL Applying initial modifications]" for several minutes, especially in Experience B scenarios. (TGT-53727)
* **The VEC now loads modifications without root elements.**
Resolved an issue in the VEC that caused experiences to stall when loading modifications that lacked a clear root element. These modifications previously caused the UI to hang indefinitely on "A[!UICONTROL pplying initial modifications]." (TGT-53799)
* **Saving changes in activities now works as expected.** Resolved a permissions-related issue in the New Create UI that prevented users from saving changes when editing goals and advanced settings in activities. Affected users saw a red error ribbon and a "Forbidden.Resource" message, despite having appropriate access. (TGT-53816)
* **VEC UI now preserves experience modifications across views.** Resolved multiple issues in the updated VEC that impacted experience development. Modifications were not persisting correctly, especially when using HTML offers or switching between views. (TGT-53825)
* **All views now correctly display when a modification spans multiple experiences.** Resolved an issue in the Activity Create UI where only one view was shown when a modification was applied across multiple views. The hover tooltip failed to list all associated views, even though the modification was correctly applied. (TGT-53827)
* **The VEC no longer intermittently stalls on "[!UICONTROL Applying initial modifications]."** Resolved an intermittent issue in the VEC where experiences failed to load and remained stuck on "[!UICONTROL Applying initial modifications]." This behavior was inconsistent and sometimes triggered redirect loops or required manual cache clearing. (TGT-53916)
* **VEC loading issue could not be reproduced.** We investigated a reported issue where the VEC remained stuck on "[!UICONTROL Applying initial modifications]" when editing existing activities. The behavior was suspected to be related to HTML content lacking a parent element. We'll continue monitoring for recurrence and recommend using structured containers for HTML offers to ensure stability. (TGT-53972)
* **[!UICONTROL Design] mode in the VEC no longer behaves like [!UICONTROL Browse] mode intermittently.** Resolved an issue in the UI where [!UICONTROL Design] mode intermittently behaved like [!UICONTROL Browse] mode, allowing clickable `<a>` links and preventing element selection. This caused the hover box to disappear and blocked modification workflows. (TGT-53136)
* **Button clicks in [!UICONTROL Composer] mode no longer trigger page redirection.** Resolved an issue in the updated VEC UI where clicking a button in [!UICONTROL Composer] mode caused an unexpected redirect to the button's target URL. This prevented users from editing call-to-action (CTA) elements and disrupted the authoring workflow. (TGT-53137)
* **Offer code updates in automated personalization activities now save without error.** Resolved an issue in the New Create UI that caused an "[!UICONTROL Invalid user input]" error when updating offer code in [!UICONTROL Automated Personalization] activities. The error blocked users from saving changes, even when the input was valid. (TGT-53586)
* **[!UICONTROL Design] mode in the VEC now blocks link navigation for editable components.** Resolved an issue in the updated VEC where clickable elements—such as buttons and links—triggered page redirection even while in [!UICONTROL Design] mode. This behavior mimicked [!UICONTROL Browse] mode and prevented users from modifying key components. (TGT-53696)
* **"[!UICONTROL Clicked an element]" metric now works without redirect or error.** Resolved an issue in the New Create UI that caused unexpected redirects and blank screens when selecting the "[!UICONTROL Clicked an element]" conversion metric. Clicking a button during setup triggered navigation instead of registering the element, resulting in an "[!UICONTROL element not found]" error. (TGT-53817)
* **Existing activities no longer get stuck in infinite loading loop during edit.** Resolved an issue in the New Create UI where editing an existing activity in the VEC caused the page to remain stuck in an infinite loading loop. This issue did not affect newly created activities and was triggered by pre-existing modifications on the page. (TGT-53913)
* **Existing activity pages with modifications now load correctly in the VEC.** Resolved an issue in the updated VEC that caused pages to remain stuck in the loading phase when editing an existing activity with saved modifications. New activities loaded without issue, but previously configured activities failed to render. (TGT-53967)

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
