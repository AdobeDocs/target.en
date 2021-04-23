---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Find Adobe [!DNL Target] APIs, including the Admin, Delivery, Reporting, and Profile APIs.
title: Where Can I Find [!DNL Target] API and SDK Documentation?
feature: APIs/SDKs
role: Developer
exl-id: 2a0232cc-9a6a-42f4-afb6-4b3e2b13939c
---
# Adobe [!DNL Target] API overview
 
[!DNL Adobe Target] APIs can be grouped according to type: Admin, Delivery, Reporting, and Profile APIs.
 
|API type|What it enables you to do|Download link|Other helpful links|
| --- | --- | --- |--- |
|Admin|Create, modify, and delete activities, audiences, offers, and other objects (including [!DNL Recommendations] entities, criteria, designs, and so on. The [!DNL Recommendations] APIs are a type of admin API.)|<UL><li>[Target Admin API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul>|[Use Recommendations APIs](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Adobe Target Tutorials*|
|Delivery|Retrieve optimized and personalized content from [!DNL Target] for delivery to an end user.|[Target Delivery API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection)||
|Reporting|Export activity results and other reporting results.|Reporting APIs are included within the [Target Admin API Postman collection](https://developers.adobetarget.com/api/#admin-postman-collection).||
|Profile|Retrieve and modify user profiles stored in Adobe Target.|[Target Profile API Postman Collection](https://developers.adobetarget.com/api/#profiles)||

>[!NOTE]
>
>There are important distinctions between [!DNL Target] Admin APIs (including the [!DNL Recommendations] APIs) and [!DNL Target] Delivery APIs:
>
>* Admin APIs let you configure various aspects of [!DNL Target] that you could also configure in the [!DNL Target] UI. Admin APIs require authentication.
>
>* Delivery APIs let you retrieve content. Delivery APIs do not require authentication.
>
>To use [!DNL Target] Admin APIs, you first need to configure authentication using Adobe I/O. For more information, see [Configure Authentication](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target Tutorials*.
