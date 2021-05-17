---
keywords: implementation;javascript library;js;atjs;on-device decisioning;on device decisioning;at.js;on-device;on device
description: Learn how to perform on-device decisioning with the at.js library
title: How Does On-device Decisioning Work with the at.js JavaScript Library?
feature: at.js
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
---
# On-device decisioning for at.js

Starting with version 2.5.0, at.js offers on-device decisioning. On-device decisioning lets you cache your [A/B Test](/help/c-activities/t-test-ab/test-ab.md) and [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md) (XT) activities on the browser to perform in-memory decisioning without a blocking network request to the [!DNL Adobe Target] Edge Network. 

[!DNL Target] also offers the flexibility of delivering the most relevant and up-to-date experience from your experimentation and Machine Learning-driven (ML-driven) personalization activities via a live server call. In other words, when performance is most important, you can choose to use on-device decisioning. However, when the most relevant, up-to-date, and ML-driven experience is needed, a server call can be made instead.

## What are the benefits of on-device decisioning?

The benefits of on-device decisioning include:

* **Deliver blazing fast decisions and experiences.** Bucketing and decisioning are performed in-memory and on the browser to avoid blocking network requests. 
* **Enhance application performance.** Run experiments and deliver personalization to your customers and users without compromising end-user experiences. 
* **Improve Google Site Quality Score.** With decisioning happening in-memory, improve the Google Site Quality score of your online business to make it more discoverable by consumers. 
* **Learn from real-time analytics.** Gain insights from your activity performance in real time via [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) reporting. A4T allows you to pivot your strategy at critical moments.

## Supported features

The Adobe Target JS SDK gives customers the flexibility to choose between performance and freshness of data for decisions. In other words, if delivering the most relevant and engaging personalized content via machine learning is most important to you, a live server call should be made. But when performance is more critical, an on-device and in-memory decision should be made. For on-device decisioning to work, refer to the list of features that are supported: 

* Activity types
* Audience targeting
* Allocation method

For more information, see [Supported features for on-device decisioning](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md).

## How does on-device decisioning work?

When you deploy and initialize at.js with on-device decisioning enabled, a [rule artifact](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md) that includes your on-device decisioning for A/B and XT activities, audiences, and assets, is downloaded from the closest Akamai CDN to your visitor and cached locally on your visitor's browser. When a request is made from at.js to retrieve an experience, the decision regarding which experience to return is made in-memory, based on the metadata encoded in the cached rule artifact.

## Decisioning method

With on-device decisioning, [!DNL Target] introduces a new setting called [!UICONTROL Decisioning Method]. The [!UICONTROL Decisioning Method] setting dictates how at.js delivers your experiences. [!UICONTROL Decisioning Method] has three values:

* [!UICONTROL Server-side only]
* [!UICONTROL On-device only]
* [!UICONTROL Hybrid]

### Server-side only

[!UICONTROL Server-side only] is the default decisioning method that is set out of the box when at.js 2.5.0+ is implemented and deployed on your web properties.

Using [!UICONTROL server-side only] as the default configuration means that all decisions are made on the [!DNL Target] edge network, which involves a blocking server call. This approach can introduce incremental latency, but it also provides significant benefits, such as giving you the ability to apply Target’s machine-learning capabilities that include [Recommendations](/help/c-recommendations/recommendations.md), [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP), and [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) activities. 

Furthermore, enhancing your personalized experiences by using Target’s user profile, which is persisted across sessions and channels, can provide powerful outcomes for your business. 

Lastly, [!UICONTROL server-side only] lets you use the Adobe Experience Cloud and fine-tune audiences that can be targeted against through Audience Manager and Adobe Analytics segments. 

The following diagram illustrates the interaction between your visitor, the browser, at.js 2.5.0+, and the Adobe Target Edge network. This flow diagram captures new visitors and returning visitors.

![Server-side only flow diagram](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

The following list corresponds to the numbers in the diagram:

|Step|Description|
| --- | --- |
|1|The [!DNL Experience Cloud Visitor ID] is retrieved from the [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en).|
|2|The at.js library loads synchronously and hides the document body.<br>   The at.js library can also be loaded asynchronously with an optional pre-hiding snippet implemented on the page.|
|3|The at.js library hides the body to prevent flickering.|
|4|A page-load request is made that includes all configured parameters, such as (ECID, Customer ID, Custom Parameters, User Profile, and so forth.)|
|5|Profile scripts execute and then feed into the Profile Store.<br>The Profile Store requests qualified audiences from the Audience Library (for example, audiences shared from [!DNL Adobe Analytics], [!DNL Adobe Audience Manager], and so forth.).<br>Customer attributes are sent to the Profile Store in a batch process.|
|6|The Profile Store is used for audience qualification and bucketing to filter activities.|
|7|The resulting content is selected after the experience is determined from live [!DNL Target] activities.|
|8|The at.js library hides the corresponding elements on the page that are associated with the experience that must be rendered.|
|9|The at.js library displays the body so that the rest of the page can be loaded for your visitor to view.|
|10|The at.js library manipulates the DOM to render the experience from the Target Edge Network.|
|11|The experience renders for the visitor.|
|12|The entire web page loads.|
|13|[!DNL Analytics] data is sent to Data Collection servers.| 
|14|Targeted data is matched to [!DNL Analytics] data via the SDID and is processed into the [!DNL Analytics] reporting storage. [!DNL Analytics] data can then be viewed in both [!DNL Analytics] and [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) reports.|

### On-device only

[!UICONTROL On-Device only] is the decisioning method that must be set in at.js 2.5.0+ when on-device decisioning should be used only throughout your web pages. 

On-device decisioning can deliver your experiences and personalization activities at blazing fast speed because the decisions are made from a cached rules artifact that contains all of your activities that qualify for on-device decisioning. 

To learn more about which activities qualify for on-device decisioning, see [Supported features in on-device decisioning](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md). 

This decisioning method should be used only if performance is highly critical across all the pages that require decisions from [!DNL Target]. Furthermore, keep in mind that when this decisioning method is selected, your [!DNL Target] activities that do not qualify for on-device decisioning will not be delivered or executed. The at.js library 2.5.0+ is configured to only look for the cached rules artifact to make decisions.  

The following diagram illustrates the interaction between your visitor, the browser, at.js 2.5.0+, and the Akamai CDN. The Akamai CDN caches the rules artifact for the visitor's first visit. For the first page visit for a new visitor, the JSON rules artifact must be downloaded from the Akamai CDN to be cached locally on the visitor's browser. After the JSON rules artifact is downloaded, the decision is made immediately without a blocking network call. The following flow diagram captures new visitors.

![On-device only flow diagram](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

The following list corresponds to the numbers in the diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers qualify all of your activities that are eligible for on-device decisioning, generate the JSON rules artifact, and propagates it to the Akamai CDN. Your activities are continuously monitored for updates to output a new JSON rules artifact to be propagated to the Akamai CDN.

|Step|Description|
| --- | --- |
|1|The [!DNL Experience Cloud Visitor ID] is retrieved from the [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html).|
|2|The at.js library loads synchronously and hides the document body.<br>The at.js library can also be loaded asynchronously with an optional pre-hiding snippet implemented on the page.|
|3|The at.js library hides the body to prevent flickering.|
|4|The at.js library makes a request to retrieve the JSON rule artifact from the nearest Akamai CDN to the visitor.|
|5|The Akamai CDN responds with the JSON rule artifact.|
|6|The JSON rule artifact is cached locally on the visitor's browser.|
|7|The at.js library interprets the JSON rule artifact and executes the decision to retrieve the experience and hides the tested elements.|
|8|The at.js library displays the body so that the rest of the page can be loaded for your visitor to view.|
|9|The at.js library manipulates the DOM to render the experience from the cached JSON rule artifact.|
|10|The experience renders for the visitor.|
|11|The entire web page loads.| 
|12|[!DNL Analytics] data is sent to Data Collection servers. Targeted data is matched to [!DNL Analytics] data via the SDID and is processed into the [!DNL Analytics] reporting storage. [!DNL Analytics] data can then be viewed in both [!DNL Analytics] and [!DNL Target] via Analytics for Target (A4T) reports.|

The following diagram illustrates the interaction between your visitor, the browser, at.js 2.5.0+, and the cached JSON rule artifact for the visitor's subsequent page hit or returning visit. Because the JSON rules artifact is already cached and available on the browser, the decision is made immediately without a blocking network call. This flow diagram captures subsequent page navigation or returning visitors.

![On-device only flow diagram for subsequent page navigation and repeat visits](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

The following list corresponds to the numbers in the diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers qualify all of your activities that are eligible for on-device decisioning, generate the JSON rules artifact, and propagates it to the Akamai CDN. Your activities are continuously monitored for updates to output a new JSON rules artifact to be propagated to the Akamai CDN.

|Step|Description|
| --- | --- |
|1|The [!DNL Experience Cloud Visitor ID] is retrieved from the [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html).|
|2|The at.js library loads synchronously and hides the document body.<br>The at.js library can also be loaded asynchronously with an optional pre-hiding snippet implemented on the page.|
|3|The at.js library hides the body to prevent flickering.|
|4|The at.js library interprets the JSON rule artifact and executes the decision in memory to retrieve the experience.|
|5|The tested elements are hidden.|
|6|The at.js library displays the body so that the rest of the page can be loaded for your visitor to view.|
|7|The at.js library manipulates the DOM to render the experience from the cached JSON rule artifact.|
|8|The experience renders for the visitor.|
|9|The entire web page loads.|
|10|[!DNL Analytics] data is sent to Data Collection servers. Targeted data is matched to [!DNL Analytics] data via the SDID and is processed into the [!DNL Analytics] reporting storage. [!DNL Analytics] data can then be viewed in both [!DNL Analytics] and [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) reports.|

### Hybrid

[!UICONTROL Hybrid] is the decisioning method that must be set in at.js 2.5.0+ when both on-device decisioning and activities that require a network call to the Adobe Target Edge network must be executed. 

When you are managing both on-device decisioning activities and server-side activities, it can be a bit complicated and tedious when thinking about how to deploy and provision [!DNL Target] on your pages. With hybrid as the decisioning method, [!DNL Target] knows when it must make a server call to the Adobe Target Edge network for activities that require server-side execution, and also when to only execute on-device decisions. 

The JSON rules artifact includes metadata to inform at.js whether an mbox has a server-side activity running or an on-device decisioning activity. This decisioning method ensures that activities you intend to be delivered quickly are done through on-device decisioning and for activities that require more powerful ML-driven personalization, those activities are done via the Adobe Target Edge network.

The following diagram illustrates the interaction between your visitor, the browser, at.js 2.5.0+, the Akamai CDN, and the Adobe Target Edge Network for a new visitor visiting your page for the first time. The takeaway from this diagram is that the JSON rules artifact is downloaded asynchronously while the decisions are made through the Adobe Target Edge network. 

This approach ensures that the size of the artifact, which can include many activities, doesn’t negatively influence the latency of the decision. Downloading the JSON rules artifact synchronously and making the decision thereafter can also have adverse effects to latency and can be inconsistent. Therefore, the hybrid decisioning method is a best practice recommendation to always make a server-side call for the decision for a new visitor, and as the JSON rules artifact is cached in parallel. For any subsequent page visits and return visits, the decisions are made from the cache and in-memory through the JSON rules artifact.

![Hybrid flow diagram for a first-time visitor](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

The following list corresponds to the numbers in the diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers qualify all of your activities that are eligible for on-device decisioning, generate the JSON rules artifact, and propagates it to the Akamai CDN. Your activities are continuously monitored for updates to output a new JSON rules artifact to be propagated to the Akamai CDN.

|Step|Description|
| --- | --- |
|1|The [!DNL Experience Cloud Visitor ID] is retrieved from the [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html).|
|2|The at.js library loads synchronously and hides the document body.<br>The at.js library can also be loaded asynchronously with an optional pre-hiding snippet implemented on the page.|
|3|The at.js library hides the body to prevent flickering.|
|4|A page-load request is made to the Adobe Target Edge Network, including all configured parameters such as (ECID, Customer ID, Custom Parameters, User Profile, and so forth.)| 
|5|In parallel, at.js makes a request to retrieve the JSON rule artifact from the nearest Akamai CDN to the visitor.|
|6|(Adobe Target Edge Network) Profile scripts execute and then feed into the Profile Store. The Profile Store requests qualified audiences from the Audience Library (for example, audiences shared from [!DNL Adobe Analytics], [!DNL Adobe Audience Manager], and so forth.).|
|7|The Akamai CDN responds with the JSON rule artifact.|
|8|The Profile Store is used for audience qualification and bucketing to filter activities.|
|9|The resulting content is selected after the experience is determined from live [!DNL Target] activities.|
|10|The at.js library hides the corresponding elements on the page that are associated with the experience that must be rendered.|
|11|The at.js library displays the body so that the rest of the page can be loaded for your visitor to view.|
|12|The at.js library manipulates the DOM to render the experience from the Target Edge Network.|
|13|The experience renders for the visitor.|
|14|The entire web page loads.|
|15|[!DNL Analytics] data is sent to Data Collection servers. Targeted data is matched to [!DNL Analytics] data via the SDID and is processed into the [!DNL Analytics] reporting storage. [!DNL Analytics] data can then be viewed in both [!DNL Analytics] and [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) reports.|

The following diagram illustrates the interaction between your visitor, the browser, at.js 2.5.0+, and the cached JSON rules artifact for a subsequent page navigation or a return visit. In this diagram, focus only on the use case that an on-device decision is made for the subsequent page navigation or return visit. Keep in mind that depending on which activities are live for certain pages, a server-side call can be made to execute server-side decisions.

![Hybrid flow diagram for subsequent page navigation and repeat visits](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

The following list corresponds to the numbers in the diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers qualify all of your activities that are eligible for on-device decisioning, generate the JSON rules artifact, and propagates it to the Akamai CDN. Your activities are continuously monitored for updates to output a new JSON rules artifact to be propagated to the Akamai CDN.

|Step|Description|
| --- | --- |
|1|The [!DNL Experience Cloud Visitor ID] is retrieved from the [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html).|
|2|The at.js library loads synchronously and hides the document body.<br>The at.js library can also be loaded asynchronously with an optional pre-hiding snippet implemented on the page.|
|3|The at.js library hides the body to prevent flickering.|
|4|A request is made to retrieve an experience.|
|5|The at.js library confirms that the JSON rule artifact has already been cached and executes the decision in memory to retrieve the experience.| 
|6|The tested elements are hidden.|
|7|The at.js library displays the body so that the rest of the page can be loaded for your visitor to view.|
|8|The at.js library manipulates the DOM to render the experience from the cached JSON rule artifact.| 
|9|The experience renders for the visitor.|
|10|The entire web page loads.|
|11|[!DNL Analytics] data is sent to Data Collection servers. Targeted data is matched to [!DNL Analytics] data via the SDID and is processed into the [!DNL Analytics] reporting storage. [!DNL Analytics] data can then be viewed in both [!DNL Analytics] and [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) reports.|

## How do I enable on-device decisioning?

On-device decisioning is available for all [!DNL Target] customers who use At.js 2.5.0+. 

To enable on-device decisioning:

>[!NOTE]
>
>You must have the [!UICONTROL Admin] or [!UICONTROL Approver] [user role](/help/administrating-target/c-user-management/user-management.md) to enable or disable the On-Device Decisioning toggle.

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Account details]**.
1. Under **[!UICONTROL Account Details]**, slide the **[!UICONTROL On-Device Decisioning]** toggle to the "on" position.

   ![On-device decisioning toggle](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   The "[!UICONTROL Include all existing on-device decisioning qualified activities in the artifact]" option displays if you enable on-device decisioning.
1. (Conditional) Slide the toggle to the "on" position if you want all your live Target activities that qualify for on-device decisioning to be automatically included in the artifact.

   Leaving this toggle off means you must re-create and activate any on-device decisioning activities for them to be included in the generated rules artifact. In other words, any activity in live state before turning on the [!UICONTROL On-Device Decisioning] toggle are not included in the rules artifact.

After enabling the [!UICONTROL On-Device Decisioning] toggle, [!DNL Target] begins generating and propagating [rule artifacts](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md) for your client.

>[!IMPORTANT]
>
>Make sure you enable the toggle before you initialize the Adobe Target SDK to use on-device decisioning. The rule artifacts first need to generate and propagate to the Akamai CDNs for on-device decisioning to work. Propagation can take five to ten minutes for the first rule artifact to generate and propagate to the Akamai CDN.

## How do I configure at.js 2.5.0+ to use on-device decisioning?

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Account details]**.
1. Under **[!UICONTROL Implementation Methods]** > **[!UICONTROL Main Implementation Method]**, click **[!UICONTROL Edit]** next to your at.js version (must be at.js 2.5.0 or later).
 
   ![Edit Main Implementation Method settings](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >Before changing these default settings, consult with Client Care so you don't affect your current implementation.

1. Select the desired decisioning method:

   * [!UICONTROL Server-side only]
   * [!UICONTROL On-device only]
   * [!UICONTROL Hybrid]

   ![Edit at.js settings panel](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### Global settings

You can configure a default [!UICONTROL Decisioning Method] for all of [!DNL Target] decisions. The various decisioning methods are [!UICONTROL Server-side only], [!UICONTROL On-device only], and [!UICONTROL Hybrid]. The decisioning method that is selected in the Target UI is configured in `window.targetGlobalSettings` under the `decisioningMethod` field. Learn more about the `decisioningMethod` in [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

```javascript
<head> 
    <script type="text/javascript">

        window.targetGlobalSettings = { 
            clientCode: "yourClientCodeHere", 
            imsOrgId: "imsOrgId@AdobeOrg", 
            decisioningMethod: "on-device"

        }; 
    </script>

    <script type="text/javascript" src="at.js"></script> 
</head>
```

### Customized setting

If you set the `decisioningMethod` in `window.targetGlobalSettings`, but would like to override the `decisioningMethod` for each Adobe Target decision according to your use case, you can do this procedure by specifying `decisioningMethod` in At.js2.5.0+’s [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) call.

```javascript
adobe.target.getOffers({ 

  decisioningMethod:"on-device", 
  request: { 
    execute: { 
      mboxes: [ 
        { 
          index: 0, 
          name: "homepage" 
        } 
      ] 
    } 
 } 
});
```

>[!NOTE]
>
>In order to use “on-device” or “hybrid” as a decisioning method in the getOffers() call, ensure that the global setting has `decisioningMethod` as “on-device” or “hybrid.” The at.js library 2.5.0+ must know whether to download and cache the JSON rules artifact immediately after loading on the page. If the decisioning method for the global setting is set to “server-side”, and “on-device” or “hybrid” decisioning method is passed into the getOffers() call, at.js 2.5.0+ would not have the JSON rule artifact cached to execute your on-device decisions.

### Artifact Cache TTL

[!DNL Target] represents your activities that qualify for on-device decisioning as an artifact that consists of metadata, rules, and conditions. This artifact is cached on the Akamai CDN. During the first-time visit of your user, the user's browser downloads and caches the artifact that represents your on-device decisioning activities. 

On subsequent visits to your site, the browser automatically checks whether it must download a newer version of the artifact. This check adds latency. The Artifact Cache TTL defines the number of minutes you don't want the browser to check for an updated artifact since the last successful download. The longer the time frame, the better the performance. The shorter the time frame, the better the data freshness, but at the cost of added latency.

## How do I know that an activity is on-device decisioning eligible?

After you create an activity that is on-device decisioning eligible, a label that reads [!UICONTROL On-Device Decisioning Eligible], is visible in the activity's [!UICONTROL Overview] page. 

![On-Device Decisioning Eligible label on the activity's Overview page.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

This label does not mean that the activity will always be delivered via on-device decisioning. Only when at.js 2.5.0+ is configured to use on-device decisioning will this activity be executed on-device. If at.js 2.5.0+ is not configured to use on-device, then this activity will still be delivered via a server call that is made from at.js.

You can filter for all activities that are on-device decisioning eligible on the [!UICONTROL Activities] page via the [!UICONTROL On-Device Decisioning Eligible] filter.

![On-Device Decisioning Eligible filter on Activities page.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>After creating and activating an activity that is on-device decisioning eligible, it can take five to ten minutes before it is included in the rules artifact that is generated and propagated to the Akamai CDN point of presences.

## Summary of steps to ensure my on-device decisioning activities are delivered via At.js 2.5.0+?

1. Access the Adobe Target UI and navigate to **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!DNL Account Details]** to enable the **[!UICONTROL On-Device Decisioning]** toggle. 
1. Enable the **"[!UICONTROL Include all existing on-device decisioning qualified activities in the artifact]"** toggle. 

   The first JSON rules artifact generation can take up to 10 minutes. 

1. Create and activate an [activity type that is supported by on-device decisioning](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md), and verify that it is on-device decisioning eligible. 
1. Set the **[!UICONTROL Decisioning Method]** to either **[!UICONTROL “Hybrid”]** or **[!UICONTROL “On-device only”]** through the at.js settings UI. 
1. Download and deploy At.js 2.5.0+ to your pages.
