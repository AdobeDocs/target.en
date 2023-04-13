---
keywords: Real-Time Customer Data Platform;rtcdp;personalization;aep audiences;adobe experience platform audiences;profile attributes
description: Learn how to use the [!DNL Target]/[!DNL Real-Time Customer Data Platform] (RTCDP) integration to provide richer customer data and more impactful personalization.
title: How Do I Integrate [!DNL Target] with the [!DNL Real-Time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
---
# Integrate with [!DNL Real-Time Customer Data Platform]

Built on [!DNL Adobe Experience Platform], [!DNL Real-Time Customer Data Platform] (RTCDP) helps companies bring together known and anonymous data from multiple enterprise sources. RTCDP lets you create customer profiles that can be used to provide personalized customer experiences across all channels and devices in real time.

For more information about RTCDP, see [Real-Time Customer Data Platform overview](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}.

## Key features

Key features include:

* Direct [!DNL Target] integration with Real-Time CDP/[!DNL Adobe Experience Platform] on the Edge (removing dependency on [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations Card] with governance and policy enforcement
* Real-time CDP Segments and Shared Profile Attributes

## Implementation scenarios 

The following sections show which type of personalization use case (next-session or same-page) is available when using different implementation methods:

### at.js implementation

|Solutions|Use Case Enabled|
| --- | --- |
|<ul><li>[!DNL Adobe Audience Manager] (AAM) and [!DNL Target]</li><li>[!DNL RTCDP] (Premium or Ultimate) and [!DNL Target]</li><li>[!DNL RTCDP] (any SKU), [!DNL AAM], and [!DNL Target]</li></ul>|Next-session personalization|

### [!DNL Adobe Experience Platform Web SDK] or [!DNL Experience Platform Server-Side API] implementation

|Solutions|Use Case Enabled|
| --- | --- |
|<ul><li>[!DNL RTCDP] (any SKU) and [!DNL Target]</li></ul>|<ul><li>Next-session personalization</li><li>Same-page personalization via Edge</li><li>Governance enforced when sharing segments</li></ul>|
|<ul><li>[!DNL RTCDP] (any SKU), [!DNL AAM], and [!DNL Target]</li></ul>|<ul><li>Next-session personalization</li><ul><li>[!DNL AAM] segments</li><li>3rd-party segments via [!DNL AAM]</li></ul><li>Same-page personalization via Edge</li><ul><li>[!DNL RTCDP] segments</li><li>Governance enforced when sharing segments</li></ul>|

### Mix of [!UICONTROL at.js] and [!DNL Platform Web SDK] implementation

|Solutions|Use Case Enabled|
| --- | --- |
|<ul><li>[!DNL RTCDP] (any SKU) and [!DNL Target]</li></ul>|<ul><li>Next-session personalization</li><ul><li>For all pages with [!UICONTROL at.js]</li></ul><li>Same-page personalization</li><ul><li>For all pages with [!DNL Platform Web SDK]</li></ul>|
|<ul><li>[!DNL RTCDP] (any SKU), [!DNL AAM], and [!DNL Target]</li></ul>|<ul><li>Next-session personalization</li><ul><li>For all pages with [!UICONTROL at.js]</li><li>[!DNL AAM] segments</li><li>3rd-party segments via [!DNL AAM]</li></ul>|

## Segment evaluation time

The following table shows the segment evaluation time for events coming from different implementation scenarios:

|Scenario|Edge segment (millisecond evaluation)|Streaming segment (minute evaluation)|Batch segment evaluation|
| --- | --- | --- | --- |
|Events/data from [!DNL Adobe Experience Platform] SDKs|Yes|Yes|N/A|
|Events from [!UICONTROL at.js]|No|Yes|N/A|
|Events from [!DNL Target Mobile] SDKs|No|Yes|N/A|
|Events from batch upload|No|No|Yes|
|Events from offline data (stream)|No|Yes|Yes|

## Use audiences from [!DNL Adobe Experience Platform] {#aep}

Using [audiences](/help/main/c-target/c-audiences/audiences.md) created in [!DNL Adobe Experience Platform] provide richer customer data that leads to more impactful personalization. The [Real-Time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCDP), built on [!DNL Adobe Experience Platform], helps companies bring together known and anonymous data from multiple enterprise sources. This process lets you create customer profiles that can be used to provide personalized customer experiences across all channels and devices in real time.

By connecting [!DNL Target] to the [!DNL Real-Time Customer Data Platform], customers can enrich their web personalization. This integration lets you unlock new segments that might have been previously inaccessible to [!DNL Target] to enable real-time millisecond personalization on the first page of a customer's web visit. Using audiences and profile attributes created in [!DNL Adobe Experience Platform] lets you expand the available data points for richer personalization. 

This integration unlocks key use cases with Real-Time CDP:

* Same-page / Next Hit personalization
* First-time / Unknown users personalization

## Share Real-Time CDP Profile Attributes with [!DNL Target] {#rtcdp-profile-attributes}

Real-Time CDP Profile Attributes can be shared with [!DNL Target] for use in HTML offers and [JSON offers](/help/main/c-experiences/c-manage-content/create-json-offer.md). 

### Real-Time CDP Profile Attributes feature limitations and considerations 

>[!NOTE]
>
>The Real-Time CDP Profile Attributes feature is available in Beta for HTML Offers and [JSON Offers](/help/main/c-experiences/c-manage-content/create-json-offer.md).

Consider the following:

* Attributes within a given offer must be from the same [!UICONTROL Experience Platform] sandbox. (In other words, an offer cannot contain attributes from different [!UICONTROL Experience Platform] sandboxes.)
* Attributes within a given offer can come from different sources; namely, the [!DNL Target] profile and the [!UICONTROL Experience Platform] profile. (In other words, you can combine attributes whether they come from [!DNL Target] or from the [!UICONTROL Experience Platform] profile.)
* When defining an offer, you can assign default values for [!UICONTROL Real-Time CDP Profile Attributes], in case the attribute does not have an explicit value. For example, if a consent or governance policy blocks the attribute being used in the personalization service, the default value can be used instead.

### JSON sample use case

As an online marketer, you want the AEP/Unified Profile to share attribute values with [!DNL Target] to provide real-time personalization. By using [!UICONTROL Real-Time CDP Profile Attributes], you can display the value of the [!UICONTROL Experience Platform] attribute in a [!DNL Target] offer using token replace. For example, you can personalize according to a customer's favorite color using `${aep.profile.favoriteColor}`, or their loyalty tier and loyalty point value using the tokens `${aep.loyalty.tier}` and `${aep.loyalty.points}`.

To create a JSON offer to share AEP/Unified Profile attributes with [!DNL Target]:

1. While [creating a JSON offer](/help/main/c-experiences/c-manage-content/create-json-offer.md), from the **[!UICONTROL Select a source]** list, select **[!UICONTROL Adobe Experience Platform]**.
1. From the **[!UICONTROL Select a profile sandbox name]** list, select the desired sandbox.
1. From the **[!UICONTROL Select a profile attribute]** list, select the desired attributes.
1. (Optional) From the **[!UICONTROL Insert a default value]** list, select the desired values.
1. Click **[!UICONTROL Add]**.

The following illustration shows that two profile attributes: `loyalty.tier` and `loyalty.points` have been added to the JSON offer.

![offer-json-aep-shared-attribute image](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## Links to more information

For more information, see the following topics:

* [Destinations release notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} in the *Adobe Experience Platform release notes*
* [Configure personalization destinations for same-page and next-page personalization](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} in the *Destinations overview* guide.
* [Adobe Target connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} in the *Destinations overview* guide
* [Map attributes](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=en#map-attributes){target=_blank} in the *Destinations overview* guide.

## Videos and blog posts

The following videos and blog post provide more information about enhanced personalization with Target and RTCDP:

### Video: Next-hit personalization with Real-Time CDP and [!DNL Adobe Target]{#RTCDP}

Learn how to personalize on the next hit with [!DNL Real-Time Customer Data Platform] and [!DNL Adobe Target]. The [!DNL Adobe Target] destination in [!DNL Real-Time CDP] allows you to use [!DNL Experience Platform] segments in [!DNL Adobe Target] for same page-personalization and next-page personalization with governance and privacy support.

For more information, see [Next-hit personalization with Real-Time CDP and Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} in the *Platform Tutorials* guide.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### [!DNL Adobe Target] blog and video: Same-page enhanced personalization

[[!DNL Adobe] announces Same-Page Enhanced Personalization with [!DNL Adobe Target] and [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
