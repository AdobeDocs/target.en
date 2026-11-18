---
keywords: debug mbox;troubleshoot mbox;mbox issues;flicker;mboxDebug;mboxTrace;token;debugger;priority;activity priority;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst  purchase mbox;top selling;top seller
description: Find suggestions to help remedy issues if your page does not display the expected content. Learn how to debug content delivery in Adobe Target.
title: How Can I Troubleshoot Content Delivery?
feature: Activities
exl-id: 887b7956-1d61-439a-8339-c150deb9a378
TQID: 'https://experienceleague.adobe.com/nkaoqcuoqMm67AnEjSg6dCnFDy-jvlwvD1a6YeXTkwk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Troubleshoot content delivery {#content-trouble}

>[!BEGINSHADEBOX]

**On this page:** Learn how to debug content delivery in [!DNL Adobe Target] when your page does not display the expected content.

>[!ENDSHADEBOX]

When a page does not display the expected content, the cause can be an error in the activity code, a missing or misplaced [!DNL Target] request, or a conflict with another activity. Check your activity or campaign code carefully, because a typo or other error can prevent the expected content from displaying. Then use mboxTrace, mboxDebug, or the Adobe Experience Cloud Debugger to examine the [!DNL Target] request.

**mboxDebug** is especially useful when you set up [!DNL Target] on your page, to make sure that the [!DNL Target] request fires and that the cookie is set. However, it does not go into the detail that is useful when debugging content delivery. If your activity does not appear on your page or undesired content appears, use mboxTrace to examine and debug the page in detail.

## Debugging tools {#debugging-tools}

### Retrieve the authorization token {#section_BED130298E794D1FA229DB7C3358BA54}

mboxTrace and mboxDebug can expose campaign data and profile data to external parties, so an authorization token is required. The authorization token can be retrieved in the [!DNL Target] UI. The token is valid for six hours.

You must have one of the following user permissions to generate an authentication token:

* At least **[!UICONTROL Editor]** permission (or **[!UICONTROL Approver]**)

  For more information for [!DNL Target Standard] customers, see [Specify roles and Permissions](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Users*. For more information for [!DNL Target Premium] customers, see [Configure enterprise permissions](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

* Admin role on the workspace/product profile level

  Workspaces are available to [!DNL Target Premium] customers only. For more information, see [Configure enterprise permissions](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

* Admin Rights (Sysadmin permission) on the [!DNL Adobe Target] product level

To retrieve the authorization token:

1. Access **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
1. From the Debugger Tools section, click **[!UICONTROL Generate New Authentication Token]**.

   ![Generate New Authentication Token](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

1. Add the generated token as a parameter to your URL to enable one of the advanced debugging tools.

   ![Authorization token](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/auth-token.png)

### mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace enables you to receive trace information attached to [!DNL Target] responses. Trace information reflects the outcome of a [!DNL Target] call (for example, a conversion or an impression) and any additional data that may help in determining why this particular outcome happened, such as a set of available branches among which the selection was made in a campaign. Use this information to debug content delivery.

The following parameters are available:

| mboxTrace Options | Outcome |
|--- |--- |
|`?mboxTrace=console`|Prints into console log as objects.<br>For at.js, instead of popping a new browser window or outputting to the console as was in  mbox.js (now deprecated), you need to inspect the Network request and look under Preview (Chrome) or Response (Firefox).|
|`?mboxTrace=json`|Prints into console log as a literal JSON string|
|`?mboxTrace=window`|Prints into a popup window as a JSON string|
|`?mboxTrace=disable`|Turns off tracing session mode|

**Example mboxTrace call**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

The output displays detailed information about your content. mboxTrace shows details about your campaign or activity and profile. It also provides a snapshot of the profile before execution, and a snapshot of what changed after execution. It also shows which campaigns or activities were evaluated for each location.

Some of the information includes matched and unmatched segment and target IDs:

* **SegmentId**: The IDs of segments, either from the reusable segments library or anonymous ones created for the particular campaign.
* **TargetId**: The IDs of targets, either from the target expression library or anonymous targets for any segments from campaign.
* **Unmatched**: The request did not qualify in this call for those segments or targets.
* **Matched**: The request qualified for the specified segments or targets.

**Using mboxTrace on recommendations pages**: Adding mboxTrace as a query parameter on pages with recommendations replaces the Recommendations design on the page with an mboxTrace details window, which displays in-depth information about your recommendations, including:

* Recommendations returned vs. recommendations requested
* The key used, and if it is generating recommendations
* Criteria-generated recommendations vs. backup recommendations
* Criteria configuration
* Exclusions and inclusions applied
* Collection rules

You do not need to include `=console`, `=json`, or `=window` in the query parameter. When you are done with the mboxTrace details, add `=disable` and press **[!UICONTROL Enter]** to return to the normal display mode.

The normal functioning and appearance of your site is not affected by mboxTrace. Visitors see your regular Recommendations design.

### mboxDebug {#mboxdebug}

To use mboxDebug, append an mboxDebug parameter to the end of your URL. The following table contains information about [!DNL Target] response-related URL parameters.

Note that some mboxDebug parameters are available with or without authentication.

| URL Parameters | Purpose |
|--- |--- |
|`mboxDebug=1`|Debugger<br>Adding this parameter to any URL with Target requests defined opens a pop-up window with valuable debugging details. Cookie information, PCid and Session ID values are written out, and all of the URLs are visible. Click on a Target request URL to show the response for that [!DNL Target] request. More details are available in [mbox_debug.pdf](/help/main/assets/mbox_debug.pdf).|
|`mboxDisable=1`|Disable mboxes on the page|
|`mboxOverride.browserIp=<Insert IP address>`|Test geotargeting<br>Test geotargeting with this URL parameter. Type an IP address as the value for this attribute, and the [!DNL Target] geotargeting evaluates that IP address to match against any geotargeting or segmentation set in a campaign.|

>[!NOTE]
>
>Ensure that the URL fragment is after query string parameters. Anything after the first `#` is a fragment identifier and causes debugging parameters not to function correctly.

### Adobe Experience Cloud Debugger {#section_A2798ED3A431409690A4BE08A1BFCF17}

The Adobe Experience Cloud Debugger helps you understand your [!DNL Target] implementation. You can view your library configuration, verify that your custom parameters are passed correctly, turn on console logging, and disable all [!DNL Target] requests. After you authenticate into the Experience Cloud, you can use mboxTrace to inspect your activity and audience qualifications as well as your visitor profile.

For more information, see the [training videos](#training-videos) at the end of this page and [Debug at.js using the Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/target-debugging-atjs.html){target=_blank}.

## Common problems {#common-problems}

+++ Top sellers are not appearing in Recommendations

The *`SiteCatalyst: purchase`* call cannot be used for Purchase algorithm traffic data. Use the *`orderConfirmPage`* call instead.

+++

</br>

+++ Form-based activities collide with Target Classic activities

Form-based activities created with [!DNL Target Standard/Premium] might collide with activities created in the [!DNL Target Classic] UI that have the same priority and use the same [!DNL Target] request. For more information, see [Activity priority](/help/main/c-activities/priority.md).

+++

</br>

+++ The [!DNL Target] cookie does not get set

If your site has a sub domain, such as [!DNL us.domain.com], but you need the [!DNL Target] cookie set on [!DNL domain.com] (instead of [!DNL us.domain.com]), you must override the `cookieDomain` setting. For more information, see [targetGlobalSettings()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}.

+++

</br>

+++ Content flickers or is not shown when an element is also part of Adobe Experience Manager personalization

If a DOM element is part of Adobe Experience Manager (AEM) personalization targeting and a [!DNL Target] activity, [!DNL Target] content might flicker or not be shown.

To remedy this situation, you can disable AEM personalization on pages on which [!DNL Target] is running.

+++

</br>

+++ Redirect and remote offers fail to deliver because of an invalid URL

If the redirect or remote offer uses an invalid URL, it might fail to be delivered.

* For redirect offers, the [!DNL Target] response can contain `/* invalid redirect offer URL */`.
* For remote offers, the [!DNL Target] response can contain `/* invalid remote offer URL */`.

You can check the [!DNL Target] response in the browser or by using mboxTrace. See [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66) for more information on valid URLs.

+++

</br>

+++ [!DNL Target] requests are not firing on my site

at.js does not fire [!DNL Target] requests if you are using an invalid doctype. at.js requires the HTML 5 doctype.

+++

## Activities with query string parameters in the URL {#query-strings}

The **[!UICONTROL Activity URL]** determines the page that qualifies visitors for the activity and renders the activity experiences to users. When prompted during activity creation, typing the complete URL does not always ensure that the content is delivered on that site page, especially with URLs that contain query string parameters.

By default, the [!UICONTROL Visual Experience Composer] (VEC) opens the page that is specified in your [Visual Experience Composer settings](/help/main/administrating-target/visual-experience-composer-set-up.md). You can also specify a different page during activity creation.

To display a different page after the VEC opens, click the **[!UICONTROL Configure gear icon]** > select **[!UICONTROL Page Delivery]** > then specify the desired URL in the **[!UICONTROL Activity URL]** field.

![Configure Page Delivery settings UI](assets/configure-page-delivery.png)

When the URL contains query string parameters, the page might not qualify for the activity or display the personalized content. Regardless of your targeted audience, you can include template rules in addition to the base URL to define your query parameters.

The following options can be used to include additional template rules:

* **Option 1:** Replicate the URL and keep it in the template rule with the "contains" option

  +++ View the template rule setup

  This option ensures that this URL qualifies for the activity, but be aware that there are corner cases attached to it that can influence your reporting data with additional records to URLs that contains the base URL.

  In this scenario, the URL is `https://shopping.mycart.com?type=Summers%20Offers` and additional template rules "contains" the same URL, separated by an OR operator:

  ![Replicate URL in template rules](assets/option1.png)

  +++

* **Option 2:** Restrict the URL "contains" condition with only the query string

  +++ View the template rule setup

  The corner case discussed in the previous option is applied in this option, but here the conditional setup is limited to the query string only.

  In this scenario, the URL is `https://shopping.mycart.com?type=Summers%20Offers` and additional template rules "contains" only the query string, separated by an OR operator:

  ![Template rule contains only the query string](assets/option2.png)

  +++

* **Option 3:** Instead of targeting the complete URL, leverage a specific part of the URL

  +++ View the template rule setup

  In this scenario, the URL is `https://shopping.mycart.com?type=Summers%20Offers` and additional template rules specify a **[!UICONTROL Query]** with **[!UICONTROL type]** > **[!UICONTROL is (case sensitive)]** > type=Summers%20Offers, separated by an OR operator:

  ![Template rule leveraging a specific part of the URL](assets/option3.png)

  +++

## Escaping double quotes in profile attribute values {#escape}

When you send values containing double quotes in a [!DNL Target] profile attribute, you must double escape them as shown below.

```
adobe.target.trackEvent({
    "mbox": "data-collection",
    "params":    {
        "profile.tagLine": "Escape \\\"Double Quotes\\\" like this."
    }
});
```

## Training videos {#training-videos}

The following videos contain more information about the concepts discussed in this article.

### Add the Extension ![Tutorial badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/)

### Basic Adobe Target Debugging ![Tutorial badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/)

### Mbox Trace ![Tutorial badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/)
