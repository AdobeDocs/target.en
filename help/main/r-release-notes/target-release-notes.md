---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease;early access
description: Learn about the new features, enhancements, and fixes included in the upcoming release of [!DNL Target], including SDKs, APIs, and JavaScript libraries.
title: What New Features and Enhancements Are Included in the Upcoming [!DNL Target] Release?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
---
# [!DNL Target] release notes (prerelease)

This article contains prerelease information for upcoming [!DNL Adobe Target] releases, including SDKs, APIs, and JavaScript libraries.

**Last updated: August 15, 2025**

>[!NOTE]
>
>* Release dates, features, and other information are subject to change without notice. Information in this article is updated frequently, especially before releases.
>
>* To view information about the current release, see [Target Release Notes](release-notes.md). 
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.

## [!DNL Target Standard/Premium] 25.8.3 (August 21, 2025)

This release contains the following updates and fixes:

**Recommendations**

+++See details
* **Fixed issue in Recs UI where custom criteria CSV download returned 404 error**: Fixed an issue where customers were unable to download the custom criteria CSV in the activity-create process.
* **Fixed inconsistent image loading in [!UICONTROL Catalog Search]**: Fixed an issue where thumbnails and images in[!UICONTROL  Catalog Search] were not loading consistently in the activity-create process. Images failed to appear unless the "Thumbnail URL" column was visible and some product images loaded partially or not at all after navigation or search actions. (TGT-52778)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++See details
* **Fixed issue in activity-create process that blocked progression to [!UICONTROL Targeting] step in AP activities**: Fixed an issue in the activity-create process where customers were unable to proceed to the [!UICONTROL Targeting] step in [!UICONTROL Automated Personalization] (AP) activities unless two locations were added. This behavior differed from the previous experience, where a single location with multiple offers was sufficient. The requirement has been corrected, allowing customers to continue using single-location setups as part of their AP workflows. (TGT-53426)

+++

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n)|Details about changes in each version of the Platform Web SDK.|
|[at.js version details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}|Details about changes in each version of the [!DNL Adobe Target] at.js JavaScript library.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to [!DNL Target] and other [!DNL Adobe Experience Cloud] solutions, sign up for the [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
