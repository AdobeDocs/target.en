---
keywords: qa;server side;server-side;preview;preview links
description: Learn how to use Adobe [!DNL Target] QA URLs with server-side delivery to perform easy end-to-end activity QA with preview links that never change, optional audience targeting, and QA reporting that stays segmented from live activity data.
title: Use Can I Perform Activity QA with Server-Side Delivery?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
TQID: 'https://experienceleague.adobe.com/zZJmFqpXtAigTiEWMZhRqXBJqvG3ANLussSPE3-NoDA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Use Activity QA with server-side delivery {#qa-server-side}

>[!BEGINSHADEBOX]

**On this page:** Learn how to pass Activity QA parameters in a server-side [!DNL Adobe Target] call, so that you can test activities when `pageUrl` is not available.

>[!ENDSHADEBOX]

The standard implementation of Activity QA supports passing `qa_mode` parameters via `pageUrl` parameters. This approach is convenient for standard/ajax [!DNL Target] calls. However, it is not suitable for server-to-server calls, such as a Mobile SDK implementation, where `pageUrl` is not available. In these cases, pass the QA parameters in the request itself, which keeps the same preview links, optional audience targeting, and QA reporting that is segmented from live activity data.

The following code sample shows Activity QA in a server-side call:

```json
{
  "mbox" : "orderConfirmPage",
  "clientSideAnalyticsLogging": true,
  "clicked" : true,
  "tntId" : "12121212.17_01",
  "order" : {
    ...
  },
  "profileParameters" : {
    ...
  },
  "mboxParameters" : {
    ...
  },
  "requestLocation" : {
    ...
  },
  "qaMode" : {
    "token" : "<encrypted token string>",
    "bypassEntryAudience" : true,
    "listedActivitiesOnly" : true,
    "evaluateAsTrueAudienceIds" : [audienceId1, audienceId2...],
    "evaluateAsFalseAudienceIds" : [audienceId3, audienceId4...],
    "previewIndexes" : [
       {
         "activityIndex" : 1,
         "experienceIndex" : 1
       }
     ],
  },
  "mboxTrace" : true
}
```

The following table describes the parameters of a server-side request:

| Parameter | Type | Default value | Description |
|--- |--- |--- |--- |
|token|Encrypted token|None. It cannot be empty.|An encrypted entity that contains the list of activity IDs that are allowed to be executed in Activity QA.<br>Validation rules: The token must be an encrypted token belonging to the client specified in the [!DNL Target] request. All activities specified in the token must belong to the client.|
|bypassEntryAudience|Boolean|False|Specifies whether entry step targets for QA activities are evaluated or are considered as matching.|
|listedActivitiesOnly|Boolean|False|Specifies whether QA activities are executed in isolation or are evaluated as active activities for the current environment.|
|evaluateAsTrueAudienceIds|List of IDs|Empty list|List of audience IDs that are always evaluated as true in the scope of the [!DNL Target] request.|
|evaluateAsFalseAudienceIds|List of IDs|Empty list|List of audience IDs that are always evaluated as false in the scope of the [!DNL Target] request.|
|activityIndex|Integer|Null. It cannot be empty.|Activity index in the encrypted token. If `activityIndex` is null or out of the boundaries of the activities in the token, it is ignored. The index starts with 1.<br>Validation rules: At least one activity index is required, and it must reference an activity specified in the token.|
|experienceIndex|Integer|Null|When specified, selects an experience by index in the activity definition. If not specified or out of boundaries, it falls back to the experience selector strategy of the activity. The index starts with 1.<br>Validation rules: The value can be null, or it must reference an experience in the activity.|
