---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Learn how to filter dynamically in Adobe [!DNL Target] Recommendations by comparing items (entities) against a value in the request (API or mbox).
title: How Do I Filter by Parameter Matching In Recommendations Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
hide: yes
hidefromtoc: yes
exl-id: f77c321b-57b0-4610-b58f-3765ace2d6ad
---
# [!UICONTROL Parameter Matching]

Filter dynamically by comparing items (entities) against a value in the request (API or mbox).

For example, only recommend content that matches the "industry" page parameter or other parameters, such as device dimensions or geo-location, as in the following examples.

* Mbox parameters for screen width and height can be used to target mobile visitors and recommend only mobile devices and accessories.
* Create a recommendations rule that returns only the top-selling mobile phones that match or exceed the screen height of the mobile device the visitor is using the view the page.
* Regional geo-location parameters can be used to return recommendations for tools during the winter. Snow blowers and other snow abatement tools can be recommended for visitors in areas where it snows but not recommended for visitors in areas where it does not snow.

>[!NOTE]
>
>If the activity was created before October 31, 2016, its delivery fails if it uses the "Parameter Matching" filter. To work around this problem:
>
>* Create a new activity and add your criteria in it.
>* Use a criteria that does not contain the "Parameter Matching" filter.
>* Remove the "Parameter Matching" filter from your criteria.

## Parameter Matching examples

[!UICONTROL Parameter Matching] lets you recommend content that matches the page parameters or the visitor's parameters, such as device dimensions or geo-location, as in the the following example:

[!DNL Recommendations] can match parameter values sent in the [!DNL Target] call. In this instance, [!DNL Target] detects that a visitor is using a mobile device, based on the screen height and width parameters sent in the [!DNL Target] call, and recommends only items that are mobile devices.

Consider the following example Target call:

![Target call](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

On the page a visitor is viewing, he or she will see mobile device products.

![Mobile device products](/help/main/c-recommendations/c-algorithms/assets/phones.png)
