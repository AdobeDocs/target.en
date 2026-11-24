---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Learn how to filter dynamically in Adobe [!DNL Target] Recommendations by comparing items (entities) against a value in the request (API or mbox).
title: Parameter matching
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
TQID: 'https://experienceleague.adobe.com/GTli-O1p4Gm2Fg9J-L0ukQ8dSw2t-da8OatFLP8Ks9g'
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
---
# Parameter matching {#parameter-matching}

>[!BEGINSHADEBOX]

**On this page:** Learn how to filter recommendations dynamically in [!DNL Adobe Target Recommendations] by comparing items (entities) against a value in the request (API or mbox).

>[!ENDSHADEBOX]

**[!UICONTROL Parameter Matching]** recommends only the content that matches the page parameters or the parameters of the visitor, such as device dimensions or geo-location. For example, only content that matches the "industry" page parameter can be recommended. The process for creating and using inclusion rules for criteria and promotions is similar, as are the use cases and examples. For more information, see [Use dynamic and static inclusion rules](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

Other examples include:

* Mbox parameters for screen width and height can be used to target mobile visitors and recommend only mobile devices and accessories.
* A recommendations rule can return only the top-selling mobile phones that match or exceed the screen height of the mobile device that the visitor uses to view the page.
* Regional geo-location parameters can be used to return recommendations for tools during the winter. Snow blowers and other snow abatement tools can be recommended for visitors in areas where it snows but not for visitors in areas where it does not snow.

## Parameter matching examples

[!DNL Recommendations] can match parameter values sent in the [!DNL Target] call. In the following example, [!DNL Target] detects that a visitor is using a mobile device, based on the screen height and width parameters sent in the [!DNL Target] call, and recommends only items that are mobile devices.

Consider the following example [!DNL Target] call:

![Target call](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

On the page that a visitor is viewing, mobile device products are displayed.

![Mobile device products](/help/main/c-recommendations/c-algorithms/assets/phones.png)
