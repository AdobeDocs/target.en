---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease 
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Adobe Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last Updated: January 22, 2024**

>[!NOTE]
>
>Release dates, features, and other information are subject to change without notice.
>
>To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Deprecation of iPad and iPhone from Browser audience attribute (April 30, 2024)

|Deprecation|Details|
|--- |--- |
|[!DNL iPad] and [!DNL iPhone] to be deprecated from the [Browser attribute](/help/main/c-target/c-audiences/c-target-rules/browser.md) used when creating audiences.<p>Deprecation date:<P>April 30, 2024|[!DNL Adobe Target] lets you [target on any of several category attributes](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), including users who use a specific [browser or browser options](/help/main/c-target/c-audiences/c-target-rules/browser.md) when they visit your page.<P><B>Starting April 30, 2024, iPad and iPhone will be removed from the available [!UICONTROL Browser] type drop-down list when creating categories for audiences.</b><P>If you have audiences that target iPads or iPhones using the [!UICONTROL Browser] attribute, you must change these settings before April 30, 2024 to ensure that these audiences continue to function as expected.<p>For examples of alternate settings, see [Deprecation of iPad and iPhone from Browser audience attribute (April 30, 2024)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation).|

## [!DNL Target] Standard/Premium 24.1.1 (January 22, 23, & 25, 2024)

This release is scheduled for the following days:

* **January 22**: Europe, Middle East, and Africa (EMEA) region
* **January 23**: Asia-Pacific (APAC) region
* **January 25**: Americas region

This release contains the following enhancements and fixes:

* [!UICONTROL Analytics for Target] (A4T) activities with revenue goal metrics did not display "Revenue" as the column name and the revenue metric did not display in ($) format in reporting. This was a cosmetic issue that has been remedied. (TGT-46995)
* Fixed an issue that caused reporting date intervals to not work correctly. (TGT-47396)
* Fixed an issue that caused the incorrect status to display on the [!UICONTROL All Activities] page after customers activated or deactivated an activity using the [!UICONTROL More Actions] icon. (TGT-47367)
* Fixed an issue that caused the [!UICONTROL Important Attributes] report to not display for a single customer. (TGT-47272)
* Fixed an issue that caused an "Invalid payload" message to display when a single customer tried to enable "Require Authentication." (TGT-47195)
* Updated numerous localized strings in the [!DNL Target] UI.

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
