---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;search engine optimization;search engine optimization;seo;edge clusters, central clusters;at.js;mbox.js;
description: Learn how [!DNL Adobe Target] works, including information about JavaScript libraries (AEP Web SDK at.js), server-call usage strategies, usage, Adobe data centers, SEO testing, and bots.
title: How Does [!DNL Target] Work?
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
---
# How [!DNL Adobe Target] works

Learn how [!DNL Adobe Target] works, including details on the JavaScript libraries ([!DNL Adobe Experience Platform Web SDK] and at.js). This article also covers the various activity types that you can create, [!DNL Target] usage-counting strategies, the [!DNL Target] Edge Network, SEO, and bot detection.

Key points include:

* **JavaScript Libraries**: Learn information about the [!DNL Target] JavaScript libraries: [!DNL Adobe Experience Platform Web SDK] and at.js.
* **Server-call usage strategies**: Understand how [!DNL Target] counts various server calls, including  endpoints, single mbox, batch mbox, execute, prefetch, and notification calls.
* **Edge Network**: Discover how [!DNL Target] interacts with the [!DNL Adobe Experience Platform Edge Network].
* **Protected user experience**: Learn how [!DNL Adobe] ensures the availability and performance of its targeting infrastructure.
* **SEO Guidelines**: Follow best practices for aligning [!DNL Target] activities with SEO guidelines.
* **Bot Traffic**: Learn how Target handles bot traffic to avoid skewing tests and personalization algorithms.

## [!DNL Adobe Target] JavaScript libraries {#libraries}

Target integrates with websites using the [!DNL Experience Platform Web SDK] or at.js:

* **[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}**: This client-side JavaScript library allows [!DNL Adobe Experience Cloud] customers to interact with various services through the [!DNL Experience Platform Edge Network]. [!DNL Adobe] recommends that new [!DNL Target] customers implement the [!DNL Experience Platform Web SDK].
* **[at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank}**: This implementation library for [!DNL Target] improves page-load times for web implementations and offers better options for single-page applications. Frequently updated with new capabilities, [!DNL Adobe] recommends all [at.js users update to the latest version](https://experienceleague-review.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

>[!NOTE]
>
>The mbox.js library is a legacy implementation for [!DNL Target] and is no longer supported after March 31, 2021. Upgrade to the [!UICONTROL Experience Platform Web SDK] (preferred) or the latest version of at.js.

Reference the [!UICONTROL Experience Platform Web SDK] or at.js on every page of your site. For example, add one of these libraries to your global header. Alternatively, use [tags in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home){target=_blank} to implement [!DNL Target].

The following resources contain detailed information to help you implement the [!DNL Experience Platform Web SDK] or at.js:

* [[!DNL Adobe Experience Platform Web SDK] extension](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html){target=_blank}
* [Implement [!DNL Target] using [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch){target=_blank}

Each time a visitor requests a page optimized for [!DNL Target], a real-time request is sent to the targeting system to determine the content to serve. This request is made and fulfilled every time a page loads, governed by marketer-controlled activities and experiences. Content is targeted to individual site visitors, maximizing response rates, acquisition rates, and revenue. Personalized content helps ensure that visitors respond, interact, or make purchases.

In [!DNL Target], each element on the page is part of a single experience, which can include multiple elements. 

The displayed content depends on the type of activity that you create:

### [!UICONTROL A/B Test]

In a basic A/B test, content is randomly chosen from the assigned experiences. You can set traffic allocation percentages for each experience. Initially, traffic may be unevenly distributed due to random splitting, but it equalizes as traffic increases. For example, with two experiences, the starting experience is chosen randomly. Low traffic can skew visitor percentages toward one experience, but this situation balances out with more traffic.

Specify percentage targets for each experience. A random number is generated to select the experience to display. While the resulting percentages might not exactly match the targets, higher traffic leads to a closer split to the target goals.

1. A customer requests a page from your server, which displays in their browser.
1. A first-party cookie is set in the customer's browser to store their behavior.
1. The page calls the targeting system.
1. Content is displayed based on the activity rules.

See [Create an A/B Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) for more information.

### [!UICONTROL Auto-Allocate]

[!UICONTROL Auto-Allocate] identifies the winning experience among two or more options. It then automatically reallocates more traffic to the winner, increasing conversions as the test continues to run and learn.

See [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) for more information.

### [!UICONTROL Auto-Target] (AT)

[!UICONTROL Auto-Target] leverages advanced machine learning to choose from multiple high-performing, marketer-defined experiences. [!UICONTROL Auto-Target] delivers the most tailored experience to each visitor based on individual customer profiles and the behavior of previous visitors with similar profiles. Use [!UICONTROL Auto-Target] to personalize content and drive conversions.

See [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) for more information.

### [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP) combines offers or messages and uses advanced machine learning to match different variations to each visitor. AP personalizes content based on individual customer profiles to drive lift.

See [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) for more information.

### [!UICONTROL Experience Targeting] (XT)

[!UICONTROL Experience Targeting] (XT) delivers content to specific audiences based on marketer-defined rules and criteria. Including geotargeting, XT is valuable for defining rules that target specific experiences or content to particular audiences. Multiple rules can be set in an activity to deliver different content variations to different audiences. When visitors view your site, XT evaluates them to determine if they meet the criteria. If they qualify, they enter the activity and see the experience designed for them. You can create experiences for multiple audiences within a single activity.

See [Experience Targeting](/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4) for more information.

### [!UICONTROL Multivariate Test] (MVT)

[!UICONTROL Multivariate Testing] (MVT) compares combinations of offers in page elements to determine which combination performs best for a specific audience. MVT helps identify which element most impacts the activity's success.

See [Multivariate Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499) for more information.

### [!UICONTROL Recommendations]

[!UICONTROL Recommendations] activities automatically display products or content that might interest customers based on their previous activity or other algorithms. Recommendations help direct customers to relevant items that they might not otherwise discover.

See [Recommendations](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) for more information.

## How [!DNL Target] counts server-call usage {#usage}

[!DNL Target] counts only server calls that provide value to customers. The following table shows how [!DNL Target] counts endpoints, single mbox, batch mbox calls, execute, prefetch, and notification calls.

The following information helps you understand the counting strategy used for [!DNL Target] server calls, as shown in the table below:

* **Count Once**: Counts once per API call
* **Count the Number of mboxes**: Counts the number of mboxes under the array in the payload of a single API call
* **Ignore**: Is not counted at all
* **Count the Number of Views (Once)**: Counts the number of views under the array in the payload. In a typical implementation, a view notification has only one view under the notifications array, making this equivalent to counting once in most implementations

|Endpoint|Fetch type|Options|Counting strategy|
|--- |--- |--- |-- |
|`rest//v1/mbox`|Single|[!UICONTROL execute]|Count once|
|`rest/v2/batchmbox`|Batch|[!UICONTROL execute]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch]|Ignore|
||Batch|[!UICONTROL notifications]|Count the number of mboxes|
|`/ubox/[raw\|image\|page]`|Single|[!UICONTROL execute]|Count once|
|`rest/v1/delivery`<p>`/rest/v1/target-upstream`|Single|[!UICONTROL execute] > [!UICONTROL pageLoad]|Count once|
||Single|[!UICONTROL prefetch] > [!UICONTROL pageLoad]|Ignore|
||Single|[!UICONTROL prefetch] > [!UICONTROL views]|Ignore|
||Batch|[!UICONTROL execute] > [!UICONTROL mboxes]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch] > [!UICONTROL mboxes]|Ignore|
||Batch|[!UICONTROL notifications] > [!UICONTROL views]|Count the number of views (once)|
||Batch|[!UICONTROL notifications] > [!UICONTROL pageLoad]|Count once|
||Batch|[!UICONTROL notifications] > type ([!UICONTROL conversions])|Count once|
||Batch|[!UICONTROL notifications] > [!UICONTROL mboxes]|Count the number of mboxes|

## The edge network {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

An 'Edge' is a geographically distributed serving architecture that ensures optimal response times for visitors requesting content, regardless of their location.

To improve response times, [!DNL Target] Edges host only activity logic, cached profiles, and offer information.

Activity and content databases, [!DNL Analytics] data, APIs, and marketer user interfaces are housed in [!DNL Adobe] Central Clusters. Updates are sent to the [!DNL Target] Edges, which are automatically synced with the Central Clusters to continually update cached activity data. All 1:1 modeling is also stored on each edge, allowing complex requests to be processed locally.

Each Edge Cluster contains all necessary information to respond to visitor content requests and track analytics data. Visitor requests are routed to the nearest Edge Cluster.

For more information, see the [Adobe Target Security Overview](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf) white paper.

[!DNL Target] is hosted on Adobe-owned and Adobe-leased data centers worldwide.

Central Cluster locations house both data collection and data processing centers. Edge Cluster locations contain only data collection centers. Each report suite is assigned to a specific data processing center.

Customer site activity data is collected by the nearest of seven Edge Clusters. This data is then directed to a pre-determined Central Cluster destination (Oregon, Dublin, or Singapore) for processing. Visitor profile data is stored on the Edge Cluster closest to the site visitor. Edge Cluster locations include the Central Cluster locations, as well as Virginia, Mumbai, Sydney, and Tokyo.

Instead of processing all targeting requests from a single location, requests are handled by the Edge Cluster nearest to the visitor. This approach mitigates the impact of network and Internet travel time.

![Map showing the different types of Target servers](/help/main/c-intro/assets/target-servers.png)

[!DNL Target] Central Clusters, hosted on Amazon Web Services (AWS), include:

* Oregon, USA
* Dublin, Ireland
* Republic of Singapore

[!DNL Target] Edge Clusters, hosted on AWS, include:

* Mumbai, India
* Tokyo, Japan
* Virginia, USA
* Oregon, USA
* Sydney, Australia
* Dublin, Ireland
* Republic of Singapore

The [!DNL Target Recommendations] service is hosted in an [!DNL Adobe] data center in Oregon.

>[!IMPORTANT]
>
>[!DNL Target] currently lacks an Edge Cluster in China, limiting visitor performance for [!DNL Target] customers in the region. The firewall and absence of Edge Clusters can affect site experiences, causing slow rendering and page load times. Additionally, marketers can experience latency when using the [!DNL Target] authoring UI.

You can allowlist [!DNL Target] Edge Clusters, if desired. For more information, see [allowlist Target edge nodes](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/allowlist-edges){target=_blank}.

## Protected user experience {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

[!DNL Adobe] ensures the availability and performance of its targeting infrastructure is as reliable as possible. However, communication breakdowns between a visitor's browser and [!DNL Adobe] servers can interrupt content delivery.

To safeguard against service interruptions and connectivity issues, all locations are set up to include default content (defined by the client). This default content is displayed if the visitor's browser cannot connect to [!DNL Target].

No changes are made to the page if the visitor's browser cannot connect within a defined timeout period (default: 15 seconds). If this timeout threshold is reached, default location content is displayed.

[!DNL Adobe] protects the user experience by optimizing and safeguarding performance.

* [!DNL Adobe] ensures performance benchmarks based on industry standards, guaranteed by the [!UICONTROL Adobe Service Level Agreement]. 
* The Edge Network ensures timely data delivery. 
* [!UICONTROL Adobe] employs a multi-tiered approach to secure its applications, providing the highest level of availability and reliability for customers.
* [!DNL Target] Consulting offers implementation assistance and ongoing product support.

## Search Engine Optimization (SEO) friendly testing {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] aligns with search engine guidelines for testing. [!DNL Google] encourages user testing and states that A/B and [!UICONTROL Multivariate Testing] do not harm organic search engine rankings if certain guidelines are followed.

[!DNL Adobe Target] aligns with search engine guidelines for testing.

For more information, see the following Google resources:

* [Website testing and Google Search](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) 
* [Experiments and Cloaking](https://support.google.com/analytics/answer/12979939?hl)


Guidelines were presented in a [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) post. Although the post dates back to 2012, it remains [!DNL Google]'s most recent statement on the matter, and the guidelines are still relevant.

* **No cloaking**: Cloaking involves showing one set of content to users and a different set to search engine bots by specifically identifying bots and feeding them different content.

  [!DNL Target] is configured to treat search engine bots the same as any user. Consequently, bots can be included in activities if they are randomly selected and "see" the test variations.

* **Use rel="canonical"**: Sometimes an A/B test requires different URLs for variations. In these cases, all variations should include a rel="canonical" tag referencing the original (control) URL. For example, if [!DNL Adobe] is testing its home page with different URLs for each variation, the following canonical tag for the home page should be placed in the `<head>` tag of each variation:

  `<link rel="canonical" href="https://www.adobe.com" />`

* **Use 302 (temporary) redirects**: When separate URLs are used for variation pages in a test, [!DNL Google] recommends using a 302 redirect to direct traffic to the test variations. The 302 redirect informs search engines that the redirect is temporary and active only while the test is running.

  A 302 redirect is a server-side redirect, while [!DNL Target] and most optimization providers use client-side capabilities. Therefore, [!DNL Target] is not fully compliant with [!DNL Google]'s recommendations for redirects. However, this impacts only a small fraction of tests. The standard approach for running tests through [!DNL Target] involves changing content within a single URL, eliminating the need for redirects. In cases where multiple URLs are required for test variations, [!DNL Target] uses the JavaScript `window.location` command, which does not specify whether the redirect is a 301 or 302.

  [!DNL Adobe] is actively seeking solutions to fully comply with search engine guidelines. For clients needing separate URLs for testing, [!DNL Adobe] believes that correctly implementing canonical tags mitigate associated risks.

* **Run experiments only as long as necessary**: [!DNL Adobe] defines "as long as necessary" as the time required to reach statistical significance. [!DNL Target] offers best practices and the [!DNL Adobe Target] [Sample Size Calculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) to determine when your test has reached this point. [!DNL Adobe] recommends incorporating the hardcoded implementation of winning tests into your testing workflow and allocating the appropriate resources.

  Using [!DNL Target] to "publish" winning tests is not recommended as a permanent solution. If the winning test is published for 100% of users all the time, this approach can be used temporarily while hard-coding the winning test.

  Consider what your test has changed. Minor updates, such as button colors, do not impact organic rankings. However, text changes should be hardcoded.

  Also, consider the accessibility of the page you're testing. If the page is not accessible to search engines and was never intended to rank in organic search, these considerations do not apply. An example is a dedicated landing page for an email campaign.

Google states that following these guidelines "should result in your tests having little or no impact on your site in search results."

In addition to these guidelines, Google also provides one more guideline in the documentation to their Content Experiments tool:

* "Your variation pages should maintain the spirit of the content on your original pages. Those variations shouldn't change the meaning of or your user's general perception of that original content."

Google states as an example that "if a site's original page is loaded with keywords that don't relate to the combinations being shown to users, we may remove that site from our index."

[!UICONTROL Adobe] feels that it would be difficult to unintentionally change the meaning of the original content within test variations. However, [!UICONTROL Adobe] recommends being aware of the keyword themes on a page and maintaining those themes. Changes to page content, especially adding or deleting relevant keywords, can result in ranking changes for the URL in organic search. [!DNL Adobe] recommends that you engage with your SEO partner as part of your testing protocol.

## Bots {#bots}

[!DNL Target] uses the [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) metric "isRobot" to detect known bots based on the User Agent String passed in the Request Header. 

>[!NOTE]
>
> For [!DNL Server-Side] requests, the value passed in the [Request's "Context" node](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) is given precedence over the User Agent String for bot detection.

Traffic identified as bot-generated is still served content. Bots are treated like regular users to ensure that [!DNL Target] aligns with SEO guidelines. However, bot traffic can skew A/B tests or personalization algorithms if treated like normal users. Therefore, known bot traffic in your [!DNL Target] activity is treated differently. Removing bot traffic provides a more accurate measurement of user activity.

For known bot traffic, [!DNL Target] does not:

* Create or retrieve a visitor profile
* Log profile attributes or execute profile scripts
* Look up [!DNL Adobe Audience Manager] (AAM) segments (if applicable)
* Use bot traffic in modeling or serving personalized content for [!UICONTROL Recommendations], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization], or [!UICONTROL Auto-Allocate] activities
* Log an activity visit for reporting
* Log data to be sent to the [!DNL Adobe Experience Cloud] platform

For known bot traffic, when using [!UICONTROL Analytics for Target] (A4T), [!DNL Target] does not:

* Send events to [!DNL Analytics]

For known bot traffic when using `client_side` logging, [!DNL Target] does not return:

* `tnta payload`
