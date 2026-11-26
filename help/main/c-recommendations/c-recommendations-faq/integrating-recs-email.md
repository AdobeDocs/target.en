---
keywords: email;ESP;email service provider;rawbox;delivery API;download-only template;email template;batch processing;build-time email
description: Learn how to integrate email with Adobe [!DNL Target Recommendations], including using the [!DNL Target] Delivery API, rawbox templates, and down-load only templates.
title: How Do I Integrate Recommendations with Email?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
TQID: 'https://experienceleague.adobe.com/ZyeOl6ysM03a0mMiNgHuicOLPfgpXnrdqXJE1gHRRvE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Integrate [!DNL Recommendations] with email {#integrate-recs-email}

>[!BEGINSHADEBOX]

**On this page:** Learn about the methods to integrate [!DNL Target Recommendations] with an Email Service Provider (ESP) for send-time personalization of recommendations in email.

>[!ENDSHADEBOX]

[!DNL Adobe Target] supports send-time personalization of recommendations in email. Open-time personalization of recommendations is not supported.

Three methods are available to integrate [!DNL Target Recommendations] with an ESP. The capabilities of the ESP determine which method to use, and the account manager or consultant can help choose the best option.

|Method|Details|
| --- | --- |
|[Method 1: [!DNL Adobe Target Delivery API]](#delivery-api) (Preferred)|Use the [!DNL Adobe Target Delivery API] to make per-customer, per-email requests for recommendations.|
|[Method 2: [!DNL Adobe Rawbox API]](#rawbox)|Use the [!DNL Adobe Target Rawbox API] to make per-customer, per-email requests for recommendations.|
|[Method 3: [!DNL Recommendations Download API]](#download-api)|Use the [!DNL Recommendations Download API] to request bulk recommendations for a list of products or categories in CSV format.|

Methods 1 and 2 require the ESP to make calls to an external API on a per-customer, per-email basis, and to wait for the content to be returned. Not all ESPs support these methods, so the ESP must be contacted to determine whether it is compatible with this integration pattern.

Method 3 requires the ESP to join a list of recommendations by product ID or category ID to the list of emails. This join can be based on an attribute such as the last viewed product, the last purchased product, or the most viewed category of the customer. The ESP must have access to this data in its customer profile to perform the join, so the ESP must be contacted to determine whether it has access to this data and is compatible with this integration pattern.

>[!IMPORTANT]
>
>The following capacity guidelines apply to the Delivery API and rawbox email template methods (methods 1 and 2):
>
>* Requests should be rate-limited to the lower of 1,000 requests per second or 25 times the peak daily traffic.
>* Traffic should be ramped in steps of 200 requests per second each minute.
>
>To use higher rate limits, contact the account manager.

## Method 1: Use the Delivery API (Preferred) {#delivery-api}

The Delivery API is a POST request that works with build-time email. This option is the preferred method for build-time email.

Most email clients do not allow POST requests, so this API is not recommended for open-time use cases. Some email clients, such as Gmail or Outlook, can cache the content or block the image, and require the recipient to proactively allow the image to render.

Default content cannot be returned with the Delivery API.

The following code is a sample API delivery request, where `clientcode` is the [!DNL Target] client code:

```javascript
curl -X POST \ 
  'https://clientcode.tt.omtrdc.net/rest/v1/mbox/?client=clientcode' \ 
  -H 'authorization: Bearer 3423614b-4843-4664-83c4-c6c3f6c8869b' \ 
  -H 'cache-control: no-cache' \ 
  -H 'content-type: application/json' \ 
  -d '{ 
  "mbox" : "email-mbox", 
  "tntId" : "111499796294071-449025.28_44", 
  "requestLocation" : { 
    "host" : "prod" 
  }, 
   "profileParameters" : { 
   }, 
  "mboxParameters" : { 
    "at_property": "b468a242-64a4-32a0-ca0c-890bddd78789", 
    "entity.id": "article-123", 
    "entity.event.detailsOnly" : "true" 
  } 
  "contentAsJson":  true 
}'
```

>[!NOTE]
>
>Provide a unique value for both `sessionId` and one of `tntId` or `thirdPartyId` for each email recipient (for each API call). Without unique values for these fields, the API response can slow or fail because of the many events generated within a single profile.

For more information, see the [Delivery API documentation](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/overview.html){target=_blank}.

## Method 2: Use a rawbox email template {#rawbox}

A rawbox is similar to an mbox request, but for non-web environments, such as email service providers (ESPs). The [!DNL Adobe Experience Platform Web SDK] and [!DNL at.js] are not available for rawbox requests, so the requests must be created manually. The following examples explain how to work with rawbox requests in email.

This approach allows tracking the performance of recommendations in emails, testing them in the normal way with a recommendation, and continuing the tracking on the site.

>[!NOTE]
>
>When using a rawbox and [!DNL Target], see the important security notice under [Create allowlists that specify hosts that are authorized to send mbox calls to [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist).

1. Set up a [!DNL Recommendations] activity in [!DNL Target], with the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) option.

1. For the location, select the name of the mbox that is used in the rawbox request coming from the ESP.

1. Select a design with the look and feel wanted for the email.

At email build time, the ESP makes a call to the [!DNL Target] servers for each rawbox in each email being generated. The ESP must have a way to include the returned HTML in the email when it is sent.

The email system must be able to handle the following scenarios.

### A valid response is received, but no recommendations are present

* The response is the value set in the `mboxDefault` parameter. See the description of this parameter in the table of required parameters.
* The email provider should have a default HTML block of recommendations to use in this case.

### The [!DNL Target] server times out and returns without data

* The [!DNL Target] server returns the following content:

  `//ERROR: application server timeout`

* The email application should search for that text and must be able to handle the error. The email provider has multiple options for handling this case:

  * Try another server call immediately (recommended, perhaps with an attempt counter).
  * Discard that particular email and continue to the next one.
  * Queue that particular email and rerun the failed emails as a batch at the end of the initial run.

### Sample request URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Required parameters {#reqparams}

>[!NOTE]
>
>To use [!DNL Recommendations] in email, the rawbox call must usually include either the `entity.id` or the `entity.categoryId`, or both, depending on the type of recommendation criteria. The sample call above includes both.

| Parameter | Value | Description | Validation |
|--- |--- |--- |--- |
|`client_code`|*client_code*|The client code used in [!DNL Recommendations]. The Adobe consultant can provide this value.||
|`mbox`|*mboxName*|The mbox name that is used for targeting.|Same validation as for all mbox calls.<br>250 character limit.<br>Cannot contain any of the following characters: `', ", %22, %27, <, >, %3C, %3E`|
|`mboxXDomain`|disabled|Prevents the response from setting a cookie in non-web environments.||
|`entity.id`<br>(Required for certain types of criteria: view/view, view/bought, bought/bought)|*entity_id*|The productId that the recommendation is based on, such as an abandoned product in the cart, or a previous purchase.<br>If required by the criteria, the rawbox call must include the `entity.id`.||
|`entity.event.detailsOnly`|true|If `entity.id` is passed, passing this parameter is highly recommended, to prevent the request from incrementing the number of tallied page views for an item, so as not to skew product view-based algorithms.||
|`entity.categoryId`<br>(Required for certain types of criteria: most viewed by category and top sellers by category)|*category_id*|The category that the recommendation is based on, such as top sellers in a category.<br>If required by the criteria, the rawbox call must include the `entity.categoryId`.||
|`mboxDefault`|*`https://www.default.com`*|If the `mboxNoRedirect` parameter is not present, `mboxDefault` should be an absolute URL that returns default content if no recommendation is available. This URL can be an image or other static content.<br>If the `mboxNoRedirect` parameter is present, `mboxDefault` can be any text that indicates there are no recommendations, for example `no_content`.<br>The email provider must handle the case where this value is returned, and insert default HTML into the email.<br>See the security best practice below the tables.||
|`mboxHost`|*mbox_host*|The domain that is added to the default environment (host group) when the call fires.||
|`mboxPC`|Empty|(Required for recommendations that use a visitor's profile.)<br>If no "thirdPartyId" was provided, a new tntId is generated and returned as part of the response. Otherwise, the value remains empty.<br>See the note on unique values below the tables.|1 < Length < 128<br>Cannot contain more than a single "." (dot).<br>The only dot allowed is for the profile location suffix.|

### Optional parameters

| Parameter | Value | Description | Validation |
|--- |--- |--- |--- |
|`mboxPC`<br>(Optional)|*mboxPCId*|The [!DNL Target] visitor ID. Use this value to track a user full-circle back to the site across multiple visits, or when using a user profile parameter.<br>This value must be the actual [!DNL Adobe Target] PCID of the user, which is exported from the website to the CRM. The email provider retrieves this ID from the CRM or data warehouse, and uses it as the value of this parameter.<br>The `mboxPC` value is also useful for tracking visitor site behavior across multiple visits for metrics tracking, when a recommendation is part of an A/B activity.<br>See the note on unique values below the tables.|1 < Length < 128<br>Cannot contain more than a single "." (dot).<br>The only dot allowed is for the profile location suffix.|
|`mboxNoRedirect`<br>(Optional)|1|By default, the caller is redirected when no deliverable content is found. Use this parameter to disable the default behavior.||
|`mbox3rdPartyId`|*xxx*|Use this option to specify a custom visitor ID for profile targeting.||

For `mboxSession` and `mboxPC`, provide a unique value for each email recipient (for each API call). Without unique values for these fields, the API response can slow or fail because of the large number of events generated within a single profile.

As a security best practice for `mboxDefault`, use authorized hosts to allowlist the default redirect URL domains. If the domain used in the `mboxDefault` URL is not allowlisted, a risk of an Open Redirect Vulnerability can be exposed. Authorized hosts avoid the unauthorized use of Redirector links or `mboxDefault` by third parties. [!DNL Target] uses hosts to allowlist the domains to which redirects are allowed. For more information, see the security notice at the beginning of this section.

### Potential [!DNL Target] server responses

| Response | Description |
|--- |--- |
|//ERROR:|Generated by the load balancer when it cannot return content.|
|Success|The `mboxNoRedirect` parameter is set to 'true' and the server does not return any recommendations (there is no match for the mbox, or the server cache is not initialized).|
|bad request|The `mbox` parameter is missing.<ul><li>Either `mboxDefault` or the `mboxNoRedirect` parameter is not specified.</li><li>The `mboxTrace` request parameter is specified but `mboxNoRedirect` is not.</li><li>The `mboxTarget` parameter is not specified when mbox names end with the `-clicked` suffix.</li></ul>|
|`Cannot redirect to default content, please specify mboxDefault parameter`|`mboxDefault` is not specified when no match for the request exists and the `mboxNoRedirect` parameter is not specified.|
|`Invalid mbox name:= MBOX_NAME`|The `mbox` parameter contains invalid characters.|
|`Mbox name [MBOX_NAME] is too long`|The `mbox` parameter is longer than 250 characters.|

## Method 3: Use the Recommendations Download API {#download-api}

Set up a recommendation as usual, but choose **download only** in the presentation section instead of a template and mbox combination. Then provide the ESP with the ID of the recommendation that was created. The ESP accesses the recommendation data through the API. This data shows which items should be recommended for a particular category or key item, such as items in an abandoned cart. The ESP stores this data, connects it with its own look and feel, displays information about each item, and delivers it in the emails.

With this option, the recommendations server cannot directly track the performance of a recommendation or split traffic across multiple algorithm and template combinations. Also, the recommendations are not tied to a visitor profile.

For more information about the download API, see [Legacy APIs > Download](/help/main/assets/adobe-recommendations-classic.pdf). 
