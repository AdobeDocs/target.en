---
keywords: ajo;adobe journey optimizer;adobe journey optimizer target integration;recommendations;target recommendations;integration
description: Integrate [!DNL Adobe Target Recommendations] with [!DNL Adobe Journey Optimizer].
title: How do I use [!DNL Target Recommendations] in customer journeys using [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
hide: yes
hidefromtoc: yes
---
# Integrate [!DNL Adobe Target Recommendations] and [!DNL Adobe Journey Optimizer]

This article explains use cases and information to help you set up the integration between [!DNL Adobe Target Recommendations] and [!DNL Adobe Journey Optimizer] to help you deliver connected, contextual, and personalized experiences to your customers.

This integration helps you drive more conversions and see the impact of email messages containing personalized recommendations.

## Prerequisites 

To use the [!DNL Target Recommendations] and [!DNL Adobe Journey Optimizer] integration, you need the following:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) implemented using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

  This feature is not available with a [!DNL Target Standard] license or when implementing [!DNL Target] with at.js or other [!DNL Target] SDKs.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Sample use cases

These are just a few possible use cases for integrating [!DNL Target Recommendations] with [!DNL Adobe Journey Optimizer]: 

* **[!DNL Adobe Journey Optimizer] sends a personalized email after cart abandonment**: This use case is based on a customer visiting a website, placing items in the shopping cart, and then leaving the site without completing the purchase process. 

  Suppose, for example, that a visitor visits a clothing company's website and places two winter coats and a sweatshirt in the shopping cart. The visitor then gets distracted and leaves the website or is unsure of the purchases and closes the browser or app. 

  After a specified period, perhaps a few hours or a day, a custom action in [!DNL Adobe Journey Optimizer] makes a call to [!DNL Target Recommendations] to determine the contents of the abandoned shopping cart using a [cart-based recommendations](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) algorithm. [!DNL Adobe Journey Optimizer] then sends this visitor a personalized email as a reminder that the purchasing process was not completed, along with images and links to the abandoned items.

* **[!DNL Adobe Journey Optimizer] sends a bulk email after site visits to remind visitors which items were viewed**: This use case is based on visitors visiting a website, viewing various items, and then leaving the site or app without placing items in the shopping cart.

  After a specified period, a custom action in [!DNL Adobe Journey Optimizer] makes a call to [!DNL Target Recommendations] to determine which items each visitor viewed, using each visitor's [!DNL Adobe Experience Cloud Identifier] (EDID), the visitor's [!DNL Target] profile, and a [user-based](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) algorithm. [!DNL Adobe Journey Optimizer] then sends each member of the qualified audience a personalized email with images and links to each visitor's viewed items to get the visitor to return and make a purchase.
  
  In this scenario, the [!UICONTROL Experience Cloud Visitor ID] (ECID) and the contents of each visitor's [!DNL Target] profile is used to generate the recommendation based on the recently viewed algorithm. 
  
  Suppose, for example, a visitor visits a retail website and views several watches. This visitor's [!DNL Target] profile is updated with a list of the viewed watches. Using the ECID and the visitor's [!DNL Target] profile, [!DNL Target] sends the recommendation to [!DNL Adobe Journey Optimizer]. [!DNL Adobe Journey Optimizer] then sends an email containing images and links to the watches that this visitor viewed, using the recently viewed algorithm. Another visitor receives a personalized email containing images and links to the items this visitor viewed. Each email message is personalized for each visitor.

* **[!DNL Adobe Journey Optimizer] sends a bulk email to qualified visitors after site visit to suggest popular items**: This use case is based on a visitor visiting a website, but not viewing any particular items. The email is sent in bulk to all those that qualify for a particular audience, for example:
  
  Suppose that the visitor does not view any particular watches. Perhaps the visitor simply clicked around the site and viewed category pages or blog entries. As a result, the [!DNL Target] profile doesn't have specific information about recently viewed items. In this situation, [!DNL Target Recommendations] can use a [backup recommendation](/help/main/c-recommendations/c-algorithms/backup-recs.md) so that [!DNL Adobe Journey Optimizer] can send an email with images and links to popular items on the website to get the visitor to return and possibly make a purchase.


