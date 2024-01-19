---
keywords: ajo;adobe journey optimizer;adobe journey optimizer target integration;recommendations;target recommendations;integration
description: Use [!DNL Adobe Target Recommendations] with [!DNL Adobe Journey Optimizer].
title: How do I use [!DNL Target Recommendations] in customer journeys using [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
hide: yes
hidefromtoc: yes
---
# [!DNL Adobe Target Recommendations] and [!DNL Adobe Journey Optimizer] integration

This article explains use cases and information to help you set up the integration between [!DNL Adobe Target Recommendation] and [!DNL Adobe Journey Optimizer] to help you deliver connected, contextual, and personalized experiences to your customers.

## Prerequisites 

To use the [!DNL Target Recommendations] and [!DNL Adobe Journey Optimizer] integration, you need the following:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) implemented using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

  The feature is not available with a [!DNL Target Standard] license or when implementing [!DNL Target] with at.js or other [!DNL Target] SDKs.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Sample use cases

The following are just two possible use cases for integrating [!DNL Target Recommendations] with [!DNL Adobe Journey Optimizer]: 

* **[!DNL Customer Journey Optimizer] sends a personalized email after cart abandonment**: This use case is based on a customer visiting a website, placing items in the shopping cart, and then leaving the site without completing the purchase process. 

  Suppose, for example, that a visitor visits a clothing company's website and places two winter coats and a sweatshirt in the shopping cart. The visitor then gets distracted and leaves the website or is unsure of the purchases and closes the browser or app. 

  After a specified period of time, perhaps a few hours or a day, a custom action in [!DNL Adobe Journey Optimizer] makes a call to [!DNL Target Recommendations] to determine the contents of the abandoned shopping cart. [!DNL Adobe Journey Optimizer] then sends this visitor a personalized email as a reminder that the purchasing process was not completed, along with images and links to the abandoned items.

* **[!DNL Customer Journey Optimizer] sends an email after site visit using the user profile**: This use case is based on a customer visiting a website, viewing various items, and then leaving the site without placing items in the shopping cart.

  After a specified period of time, a custom action in [!DNL Adobe Journey Optimizer] makes a call to [!DNL Target Recommendations] to determine which items this visitor viewed using the visitor's [!DNL Adobe Experience Cloud Identifier] (EDID). [!DNL Adobe Journey Optimizer] then sends this visitor a personalized email as a reminder that the purchasing process was not completed, along with images and links to the abandoned items.

