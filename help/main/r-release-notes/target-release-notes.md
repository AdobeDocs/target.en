---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease
description: Learn about the new features, enhancements, and fixes included in the upcoming release of Adobe Target, including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# Target release notes (prerelease)

This article contains prerelease information. Release dates, features, and other information are subject to change without notice. 

**Last Updated: January 26, 2023**

To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages could be the same, depending on the timing of releases. The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target] Standard/Premium 22.13.3 (January 25-26, 2023)

This release will be available according to the following staggered schedule:

* **January 25**: Europe, Middle East, and Africa (EMEA) region
* **January 25**: Asia-Pacific (APAC) region
* **January 26**: Americas region

This release contains the following new features, enhancements, and fixes:

|Feature|Details|
| --- | --- |
|[JSON offer](/help/main/c-experiences/c-manage-content/create-json-offer.md) support in Automated Personalization (AP)|Added support for JSON offers in [!UICONTROL Automated Personalization] (AP) activities using the Form-Based Experience Composer. (TGT-41460)|
|[AEM experience fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)|Added the ability to distinguish between [!DNL Adobe Experience Manager] fragment (AEM XF) types that are exported to [!DNL Target]. Instead of the "Experience Fragment" option, [!DNL Target] now lets you filter and search by "HTML XF" and "JSON XF." (TGT-44132)|

* Fixed an issue that caused a "500 error" in [!UICONTROL A/B Test] and [!UICONTROL Experience Targeting] (XT) activities that contain recommendations. This issue was caused when [!DNL Target] failed to properly delete criteria objects from the [!DNL Target] UI and [!DNL Recommendations] backend that are no longer in use. (TGT-44383)
* Removed the location from the displayed offer name in the [!UICONTROL Offer Level] report for [!UICONTROL Automated Personalization] activities. This change makes the report more readable. (TGT-44294)
* Removed the 45-day and 90-day calendar options from the AP and [!UICONTROL Auto-Target] [!UICONTROL Personalization Insights] and [!UICONTROL Important Attributes] reports in the [!DNL Target] UI. Because of usage patterns and to improve performance, these date ranges have been deprecated. The UI has been updated to reflect the currently allowed ranges: 15, 30, and 60 days. (TGT-39357)
* Disallowed the ability to change the [!UICONTROL Same as Optimization Goal] setting on the [!UICONTROL Goals & Settings] page after the activity is live. (TGT-43923)
* Fixed an issue that caused issues with the default workplace in the [!DNL Target] backend when upgrading from [!DNL Target Standard] to [!DNL Target Premium]. (TGT-44081 & TGT-44306)
* Made a change to allow [!DNL Analytics] report suites that contain dot character "." in their names to be used in the [!DNL Target] UI to create [!DNL Analytics] classification feeds.
* Changed the link on the [!UICONTROL Implementation] page ([!UICONTROL Administration] > [!UICONTROL Implementation]) for "Implementation Methods with On-Device Decisioning" to point to the page that explains how to use on-device decisioning for all supported SDKs: Node.js, Java, .NET, and Python. For more information, see [Getting Started with Target SDKs](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Fixed an issue that caused file-upload issues when using [!DNL Scene7] and [!DNL Target].
* Enhanced the accessibility of the [!DNL Target] UI for persons with disabilities by using results from an internal usability audit. These accessibility enhancements include access to features that were previously not accessible via the keyboard, alt text enhancements, the ability to zoom parts of the UI to be more usable, improved keyboard focus, and more.   (TGT-42759) 
* Made various localization fixes throughout the [!DNL Target] UI.

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|


## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
