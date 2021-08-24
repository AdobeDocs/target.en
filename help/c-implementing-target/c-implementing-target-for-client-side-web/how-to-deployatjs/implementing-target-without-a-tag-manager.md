---
keywords: implement target;implementation;implement at.js;tag manager;on-device decisioning;on device decisioning
description: Learn how to specify the settings (account details, implementation methods, etc.) to implement the Adobe [!DNL Target] at.js library without using a tag manager.
title: Can I Implement [!DNL Target] without a Tag Manager?
feature: Implement Server-side
role: Developer
exl-id: cb57f6b8-43cb-485d-a7ea-12db8170013f
---
# Implement [!DNL Target] without a tag manager

Information about implementing [!DNL Adobe Target] without using a tag manager or tags in [!DNL Adobe Experience Platform].

>[!NOTE]
>
>Tags in [Adobe Experience Platform](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is the preferred method for implementing [!DNL Target] and the at.js library. The following information is not applicable when using tags in [!DNL Adobe Experience Platform] to implement [!DNL Target].

To access the [!UICONTROL Implementation] page, click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

You can specify the following settings on this page:

* Account details
* Implementation methods
* Profile API
* Debugger tools
* Privacy

>[!NOTE]
>
>You can override settings in the at.js library, rather than configuring the settings in the [!DNL Target Standard/Premium] UI or by using REST APIs. For more information, see [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Account details

You can view the following account details. These settings cannot be changed.

| Setting | Description |
| --- | --- |
|[!UICONTROL Client Code]|The client code is a client-specific sequence of characters often required when using the [!DNL Target] APIs.|
|[!UICONTROL IMS Organization ID]|This ID ties your implementation to your [!DNL Adobe Experience Cloud] account.|
|[!UICONTROL On-Device Decisioning]|To enable on-device decisioning, slide the toggle to the "on" position.<br>On-device decisioning lets you cache your A/B and [!UICONTROL Experience Targeting] (XT) campaigns on your server and perform in-memory decisioning at near-zero latency. For more information, see [Introduction to on-device decisioning](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) in the *[!DNL Adobe Target] SDKs* guide.|
|[!UICONTROL Include all existing on-device decisioning qualified activities in the artifact.]|(Conditional) This option displays if you enable on-device decisioning.<br>Slide the toggle to the "on" position if you want all your live Target activities that qualify for on-device decisioning to be automatically included in the artifact.<br>Leaving this toggle off means you must re-create and activate any on-device decisioning activities in order for them to be included in the generated rules artifact.|

## Implementation methods

The following settings can be configured in the Implementation methods panel:

### Global settings

>[!NOTE]
>
>These settings are applied to all [!DNL Target] .js libraries. After performing changes in the Implementation methods section, you must download the library and update it in your implementation.

|Setting|Description|
| --- | --- |
|Page load enabled (Auto-create global mbox|Select whether to embed the global mbox call in the at.js file to automatically fire on each page load.|
|Global mbox|Select a name for the global mbox. By default, this name is  target-global-mbox.<br>Special characters, including ampersands (&), can be used in mbox names with at.js.|
|Timeout (seconds)|If [!DNL Target] does not respond with content within the defined period, the server call times out and default content is displayed. Additional calls continue to be attempted during the visitor's session. The default is 5 seconds.<br>The at.js library uses the timeout setting in `XMLHttpRequest`. The timeout starts when the request is fired and stops when [!DNL Target] gets a response from the server. For more information, see [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) on the Mozilla Developer Network.<br>If the specified timeout occurs before receiving the response, default content is shown and the visitor might be counted as a participant in an activity because all data collection happens on the [!DNL Target] edge. If the request reaches the [!DNL Target] edge, the visitor is counted.<br>Consider the following when configuring the timeout setting:<ul><li>If the value is too low, users might see default content most of the time, although the visitor could be counted as a participant in the activity.</li><li>If the value is too high, visitors might see blank regions on your web page or blank pages if you use body hiding for extended periods of time.</li></ul>To get a better understanding of mbox response times, look at the Network tab in your browser's Developer Tools. You can also use third-party web performance monitoring tools, such as Catchpoint.<br>**Note**: The [visitorApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) setting ensures that [!DNL Target] doesn't wait for the Visitor API response for too long. This setting and the Timeout setting for at.js described here do not affect each other.|
|Profile Lifetime|This setting determines how long visitor profiles are stored. By default, profiles are stored for two weeks. This setting can be increased up to 90 days.<br>To change the  Profile Lifetime  setting, contact [Client Care](https://helpx.adobe.com/contact/enterprise-support.ec.html).|

### Main implementation method

>[!IMPORTANT]
>
>The Target team supports both at.js 1.*x* and at.js 2.*x*. Upgrade to the most recent update of either major version of at.js to ensure that you are running a supported version.

To download the desired at.js version, click the appropriate **[!UICONTROL Download]** button.

To edit at.js settings, click **[!UICONTROL Edit]** next to the desired at.js version. 

>[!IMPORTANT]
>
>Before changing these default settings, please consult with [Client Care](/help/cmp-resources-and-contact-information.md) so you don't affect your current implementation.

In addition to the settings explained above, the following specific at.js settings are also available:

| Setting | Description |
|--- |--- |
|Custom Library Header|Add any custom JavaScript to include at the top of the library.|
|Custom Library Footer|Add any custom JavaScript to include at the bottom of the library.|

### Profile API

Enable or disable authentication for batch updates via API and generate a profile authentication token.

For more information, see [Profile API settings](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md).

### Debugger tools

Generate an authorization token to use advanced [!DNL Target] debugging tools. Click **[!UICONTROL Generate New Authentication Token]**.

![Generate New Authentication Token](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Privacy

These settings allow you to use [!DNL Target] in compliance with applicable data privacy laws.

Choose the desired setting from the Obfuscate Visitor IP address drop-down list:

* Last octet obfuscation
* Entire IP obfuscation
* None

For more information, see [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).

>[!NOTE]
>
>The Legacy Browser Support option was available in at.js version 0.9.3 and earlier. This option was removed in at.js version 0.9.4. For a list of browsers supported by at.js, see [Supported Browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).<br>Legacy browsers are older browsers that do not fully support CORS (Cross Origin Resource Sharing). These browsers include: Internet Explorer browsers earlier than version 11 and Safari versions 6 and below. If Legacy Browser Support was disabled, Target did not deliver content or count visitors in reports on these browsers. If this option was enabled, it is recommended to do quality assurance across older browsers to ensure a good customer experience.

## Download at.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Instructions to download the library using the [!DNL Target] interface or the Download API.

>[!NOTE]
>
>* [[!DNL Adobe Experience Platform]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is the preferred method for implementing [!DNL Target] and the at.js library. The following information is not applicable when using tags in [!DNL Adobe Experience Platform] to implement [!DNL Target].
>
>* The [!DNL Target] team supports both at.js 1.*x* and at.js 2.*x*. Please upgrade to the most recent update of either major version of at.js to ensure that you are running a supported version. For more information about what's in each version, see [at.js Version Details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

### Download at.js using the [!DNL Target] interface {#section_1F5EE401C2314338910FC57F9592894E}

To download [!DNL at.js] from the [!DNL Target] interface:

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**. 
1. From the [!UICONTROL Implementation methods] section, click the **[!UICONTROL Download]** button next to the desired at.js version.

### Download at.js using the [!DNL Target] Download API {#section_C0D9D2A9068144708D08526BA5CA10D0}

To download [!DNL at.js] using the API.

1. Get your client code.

   Your client code is available at the top of the **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** page of the [!DNL Target] interface. 

1. Get your admin number.

   Load this URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Replace `client code` with the client code from Step 1.

   The result of loading this URL should look similar to the following example:

   ```
   { 
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1" 
   }
   ```

   In this example, "6" is the admin number. 

1. Download [!DNL at.js].

   Load this URL with the following structure:

   ```
   https://admin<varname>admin number</varname>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code</varname>&version=<version number>
   ```

    * Replace `admin number` with your admin number. 
    * Replace `client code` with the client code from Step 1. 
    * Replace `version number` with the desired at.js version number (for example, 2.2).

    >[!IMPORTANT]
    >
    >The Target team maintains only two versions of [!DNL at.js]—the current version and the second-latest version. Please upgrade [!DNL at.js] as necessary to ensure that you are running a supported version. For more information about what's in each version, see [at.js Version Details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Loading this URL starts the download of your customized [!DNL at.js] file.

## at.js implementation {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js should be implemented in the `<head>` element of every page of your website. 

A typical implementation of Target not using a tag manager, such as tags in [[!DNL Adobe Experience Platform]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) looks like this:

```
<!doctype html> 
<html> 
<head> 
    <meta charset="utf-8"> 
    <title>Title of the Page</title> 
    <!--Preconnect and DNS-Prefetch to improve page load time--> 
    <link rel="preconnect" href="//<client code>.tt.omtrdc.net"> 
    <link rel="dns-prefetch" href="//<client code>.tt.omtrdc.net"> 
    <!--/Preconnect and DNS-Prefetch--> 
    <!--Data Layer to enable rich data collection and targeting--> 
    <script> 
        var digitalData = { 
            "page": { 
                "pageInfo": { 
                    "pageName": "Home" 
                } 
            } 
        }; 
    </script> 
    <!--/Data Layer--> 
    <!-- targetPageParams(), targetPageParamsAll(), Data Providers or targetGlobalSettings() functions to enrich the visitor profile or modify the library settings--> 
    <script> 
        targetPageParams = function() { 
            return { 
                "a": 1, 
                "b": 2, 
                "pageName": digitalData.page.pageInfo.pageName, 
                "profile": { 
                    "age": 26, 
                    "country": { 
                        "city": "San Francisco" 
                    } 
                } 
            }; 
        }; 
    </script> 
    <!--/targetPageParams()--> 
 
    <!--jQuery or other helper libraries should be implemented before at.js if you would like to use their methods in Target--> 
    <script src="jquery-3.3.1.min.js"></script> 
    <!--/jQuery--> 
    <!--Target's JavaScript SDK, at.js--> 
    <script src="at.js"></script> 
    <!--/at.js--> 
</head>
<body> 
    The default content of the page 
</body> 
</html>
```

Consider the following important notes:

* The HTML5 Doctype (for example, `<!doctype html>`) should be used. Unsupported or older doctypes could result in Target not being able to make a request. 
* Preconnect and Prefetch are options that might help your web pages load faster. If you use these configurations, ensure that you replace `<client code>` with your own client code, which you can obtain from the **[!UICONTROL Administration]** > **[!UICONTROL Implementation] page. 
* If you have a data layer, it is optimal to define as much of it as possible in the `<head>` of your pages before at.js loads. This placement provides the maximum ability to use this information in Target for personalization. 
* Special Target functions, such as `targetPageParams()`, `targetPageParamsAll()`, Data Providers, and `targetGlobalSettings()` should be defined after your data layer and before at.js loads. Alternatively, these functions could be saved in the [!UICONTROL Library Header] section of the [!UICONTROL Edit at.js Settings] page and saved as part of the at.js library itself. For more information on these functions, see [at.js functions](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md). 
* If you use JavaScript helper libraries, such as jQuery, include them before Target so you can use their syntax and methods when building Target experiences. 
* Include at.js in the `<head>` of your pages.

## Track conversions {#task_E85D2F64FEB84201A594F2288FABF053}

The Order Confirmation mbox records details about orders on your site and allows reporting based on revenue and orders. The Order Confirmation mbox can also drive recommendation algorithms, such as "People who bought product x also bought product y."

>[!NOTE]
>
>If users make purchases on your website, Adobe recommends implementing an Order Confirmation mbox even if you use Analytics for Target (A4T) for your reporting.

1. In your order details page, insert the mbox script following the model below.
1. Replace the WORDS IN CAPITAL LETTERS with either dynamic or static values from your catalog.

   >[!NOTE]
   >
   >Use comma delimiting to separate multiple product IDs.

   **Tip:** You can also pass order information in any mbox (it does not need to be named `orderConfirmPage`). You can also pass order information in multiple mboxes within the same campaign.

   ```
   <script type="text/javascript"> 
   adobe.target.trackEvent({ 
       "mbox": "orderConfirmPage", 
       "params":{  
           "orderId": "ORDER ID FROM YOUR ORDER PAGE",  
           "orderTotal": "ORDER TOTAL FROM YOUR ORDER PAGE",  
           "productPurchasedId": "PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3"  
       } 
   }); 
   </script> 
   ```

The Order Confirmation mbox uses the following parameters:

| Parameter | Description |
|--- |--- |
|orderId|Unique value to identify an order for conversion counting.<br>The `orderId` must be unique. Duplicate orders are ignored in reports.|
|orderTotal|Monetary value of the purchase.<br>Do not pass the currency symbol. Use a decimal point (not a comma) to indicate decimal values.|
|productPurchasedId  (Optional)|Comma-separated list of product IDs purchased in the order.<br>These product IDs display in the audit report to support additional reporting analysis.|
