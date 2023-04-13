---
keywords: Real-time Customer Data Platform;rtcdp;personalization;aep audiences;adobe experience platform audiences
description: Learn how to use the [!DNL Target]/[!DNL Real-time Customer Data Platform] (RTCDP) integration to provide richer customer data and more impactful personalization.
title: How Do I Integrate [!DNL Target] with the [!DNL Real-time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
---
# Integrate with Real-time Customer Data Platform

Built on [!DNL Adobe Experience Platform], [!DNL Real-time Customer Data Platform] (RTCDP) helps companies bring together known and anonymous data from multiple enterprise sources in order to create customer profiles that can be used to provide personalized customer experiences across all channels and devices in real time.

For more information about RTCDP, see [Real-time Customer Data Platform overview](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}.

## Use audiences from [!DNL Adobe Experience Platform] {#aep}

Using audiences created in [!DNL Adobe Experience Platform] provide richer customer data that leads to more impactful personalization. The [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCDP), built on [!DNL Adobe Experience Platform], helps companies bring together known and anonymous data from multiple enterprise sources. This process lets you create customer profiles that can be used to provide personalized customer experiences across all channels and devices in real time.

By connecting [!DNL Target] to the [!DNL Real-time Customer Data Platform], customers can enrich their web personalization by unlocking new segments that might have been previously inaccessible to [!DNL Target] to enable real-time millisecond personalization on the first page of a customer's web visit. Using audiences and profile attributes created in [!DNL Adobe Experience Platform] lets you expand the available data points for richer personalization. 

This integration unlocks key use cases with Real-time CDP:

* Same-page / Next Hit personalization
* First-time / Unknown users personalization

Key features include:

* Direct [!DNL Target] integration with Real-time CDP/[!DNL Adobe Experience Platform] on the Edge (removing dependency on [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations Card] with governance and policy enforcement
* Real-time CDP Segments and Shared Profile Attributes

Real-time CDP Profile Attributes feature limitations and considerations:

* Attributes within a given offer must be from the same AEP Sandbox. (In other words, an offer cannot contain attributes from different AEP Sandboxes.)
* Attributes within a given offer may come from different Sources; namely, the Target profile and the AEP profile.(In other words, you can combine attributes whether they come from Target or from the AEP profile.)
* When defining an offer, you may assign default values for Real-time CDP Profile Attributes, in case the attribute does not have an explicit value. For example, if a consent or governance policy blocks the attribute being used in the personalization service, the default value may be used instead.
* When shared, Real-time CDP Profile Attributes are used in the Artificial Intelligence/Machine Learning personalization models for Auto-Target and Automated Personalization.

>[!NOTE]
>
>The Real-time CDP Profile Attributes feature is currently available in Beta for HTML Offers and [JSON Offers](/help/main/c-experiences/c-manage-content/create-json-offer.md).

For more information, see the following topics:

* [Destinations release notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} in the *Adobe Experience Platform release notes*
* [Configure personalization destinations for same-page and next-page personalization](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} in the *Destinations overview* guide.
* [Custom personalization connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html){target=_blank} in the *Destinations overview* guide
* [Adobe Target connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} in the *Destinations overview* guide
* [Configure personalization destinations for same page and next page personalization use cases](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank} in the *Destinations overview* guide

### Additional information

Consider the following information when using audiences from [!DNL Adobe Experience Platform]:

#### Personalization use cases

The following table shows which type of personalization use case (next-session or same-page) is available when using the [!DNL Adobe Experience Platform Web SDK] versus using at.js:

|Implementation|Solutions/Use Case Enabled|
| --- | --- |
|at.js|**Solutions**:<ul><li>[!DNL Adobe Audience Manager] (AAM) and [!DNL Target]</li><li>[!DNL RTCDP] (Premium or Ultimate) and [!DNL Target]</li><li>[!DNL RTCDP] (any SKU), [!DNL AAM], and [!DNL Target]</li></ul>**Use Case**:<ul><li>Next-session personalization</li></ul>|
|[!DNL Platform Web SDK] or [!DNL AEP Server-Side API]|**Solutions**:<ul><li>[!DNL RTCDP] (any SKU) and [!DNL Target]</li></ul>**Use case**:<ul><li>Next-session personalization</li><li>Same-page personalization via Edge</li><li>Governance enforced when sharing segments</li></ul>**Solutions**:<ul><li>[!DNL RTCDP] (any SKU), [!DNL AAM], and [!DNL Target]</li></ul>**Use case**:<ul><li>Next-session personalization</li><ul><li>[!DNL AAM] segments</li><li>3rd-party segments via [!DNL AAM]</li></ul><li>Same-page personalization via Edge</li><ul><li>[!DNL RTCDP] segments</li><li>Governance enforced when sharing segments</li></ul>|
|Mix of [!UICONTROL at.js] and [!DNL Platform Web SDK]|**Solutions**:<ul><li>[!DNL RTCDP] (any SKU) and [!DNL Target]</li></ul>**Use case**:<ul><li>Next-session personalization</li><ul><li>For all pages with [!UICONTROL at.js]</li></ul><li>Same-page personalization</li><ul><li>For all pages with [!DNL Platform Web SDK]</li></ul></ul>**Solutions**:<ul><li>[!DNL RTCDP] (any SKU), [!DNL AAM], and [!DNL Target]</li></ul>**Use case**:<ul><li>Next-session personalization</li><ul><li>For all pages with [!UICONTROL at.js]</li><li>[!DNL AAM] segments</li><li>3rd-party segments via [!DNL AAM]</li></ul>|

#### Segment evaluation time

The following table shows the segment evaluation time for events coming from different implementation scenarios:

|Scenario|Edge segment (millisecond evaluation)|Streaming segment (minute evaluation)|Batch segment evaluation|
| --- | --- | --- | --- |
|Events/data from [!DNL Adobe Experience Platform] SDKs|Yes|Yes|N/A|
|Events from [!UICONTROL at.js]|No|Yes|N/A|
|Events from [!DNL Target Mobile] SDKs|No|Yes|N/A|
|Events from batch upload|No|No|Yes|
|Events from offline data (stream)|No|Yes|Yes|

### Video: Next-hit personalization with Real-time CDP and [!DNL Adobe Target]{#RTCDP}

Learn how to personalize on the next hit with [!DNL Real-time Customer Data Platform] and [!DNL Adobe Target]. The [!DNL Adobe Target] destination in [!DNL Real-time CDP] allows you to use [!DNL Experience Platform] segments in [!DNL Adobe Target] for same page and next-page personalization with governance and privacy support.

For more information, see [Next-hit personalization with Real-time CDP and Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} in the *Platform Tutorials* guide.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Adobe Target blog and video:

[[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] and [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}

## Share Real-time CDP Profile Attributes with [!DNL Target] {#rtcdp-profile-attributes}

Real-time CDP Profile Attributes can be shared with [!DNL Target] for use in HTML offer and JSON offers. (Note this feature is currently in Beta.)

Sample use case: As an online marketer, Grace wants the AEP/Unified Profile to share attribute values with [!DNL Target] in order to provide real-time personalization. By using Real-time CDP Profile Attributes, Grace can display the value of the AEP attribute in a [!DNL Target] offer using token replace. For example, she can personalize according to a customer's favorite color using `${aep.profile.favoriteColor}`, or their loyalty tier and loyalty point value using the tokens `${aep.loyalty.tier}` and `${aep.loyalty.points}`.

![offer-json-aep-shared-attribute image](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

Note that assigning default values is optional.
