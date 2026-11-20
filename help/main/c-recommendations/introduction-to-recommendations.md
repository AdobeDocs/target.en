---
keywords: Recommendations;intro;introduction;webinar;demo
description: Learn about Recommendations activities in Adobe [!DNL Target] that automatically display content that might interest your customers based on previous user activity or other algorithms.
title: What Are Recommendations Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: bc4d9a46-ea21-4687-b8a0-7f2e1dc33ebf
TQID: 'https://experienceleague.adobe.com/6jmXI9CsdCnyyQrQXKzq5WF8OQPQSCbE2Zb8AnpUvks'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
---
# Introduction to Recommendations {#introduction-to-recommendations}

>[!BEGINSHADEBOX]

**On this page:** Learn how [!DNL Recommendations] activities in [!DNL Adobe Target] display relevant products or content to visitors, and how to plan and build a [!DNL Recommendations] implementation and activity.

>[!ENDSHADEBOX]

This page is based on the *Introduction to Recommendations* webinar. A [!DNL Recommendations] activity automatically displays products or content that might interest customers by optimizing real-time suggestions based on previous visits. The page also describes how to build a [!DNL Recommendations] activity in the [!DNL Target] UI.

## Introduction

Customers increasingly expect recommendations and use them as a starting point to explore other available options. Nearly everyone has bought a product that they first saw in a recommendation, whether in a store or on a digital property.

![Recommendation showing accessories that are commonly purchased with a new phone, including charging stations, cases, and headphones.](/help/main/c-recommendations/assets/intro-1.png)

The way people consume media and content is increasingly driven by personalized recommendations, and digital-first brands such as Netflix, Spotify, and YouTube start the customer experience with recommendations. As more alternatives are available than ever, it is critical to identify the most relevant content for a customer at the point of interaction.

Marketers use [!DNL Adobe Target] to drive personalized experiences across a wide variety of industries, customer types, and channels. The following table lists a few examples of how customers use [!DNL Target] to deliver personalized recommendations.

| Use case | Example |
|---|---|
| Publishing | Web publishers use [!DNL Target Recommendations] to recommend articles to site visitors and drive increased engagement. |
| Video tutorials | [!DNL Adobe Creative Cloud] uses [!DNL Target] to recommend video tutorials to Photoshop users in the Photoshop application. |
| Gaming | Gaming companies use [!DNL Target] to recommend games and content to users on their consoles. |
| B2B sales | Business-to-business companies use [!DNL Target] to recommend videos, whitepapers, and blog posts to B2B prospects, deliver downloads, and provide help to existing customers. |
| Travel | A German travel booker uses [!DNL Target] to recommend hotels and more to travelers. For details, see the [Adobe Summit session](https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608){target=_blank}. |
| Retail | A leading B2B retailer uses [!DNL Target] to recommend top categories and products to return visitors in the browser and in its mobile app. |

## Elements of great recommendations

Great recommendations are relevant and personalized. Three elements drive relevance and personalization:

* **Marketer controls** to drive the relevance of the recommended items. Marketers know which attributes of their products or content a recommendations model should consider. For example, on a video site, users might be interested in movies from the same director, but probably not in movies from the same studio. [!DNL Target] provides controls to enhance algorithms with this domain knowledge.
* **Sophisticated models** to make sense of millions of catalog items and interaction events. [!DNL Target] has machine learning capabilities built over a decade of experience and handles billions of recommendations per year.
* **User context** to ensure that recommendations are timely and relevant. For example, recommendations must not include the video that someone just watched or the shirt that someone just added to their cart. The [!DNL Target] user profile can be used in recommendations to ensure personalization.

## Implement [!DNL Target] Recommendations

Start with a strategy that defines the following points:

* **Items to recommend**: Products, videos, or content.
* **Locations for recommendations**: The channels (web, mobile, in-store, a kiosk, and so forth), the parts of the customer journey, and the pages of your site that contain recommendations.
* **Success measurement**: How to determine whether recommendations are successful, for example, by comparing an experience without recommendations to an experience with recommendations, or by comparing two different types of recommendations. Some metrics, such as the impact on Customer Lifetime Value, are difficult to measure directly, so a more concrete metric is often easier to use, such as revenue per visit, average order value, or number of clicks. In some cases, the goal is to minimize a metric, for example, the number of support calls.

After the strategy is defined, the implementation of [!DNL Target Recommendations] involves three broad steps:

![Illustration showing the three steps of a recommendations implementation: teach Target about your content or products, capture user behavior, and get recommendations with the right context.](assets/intro-6.png)

### Teach [!DNL Target] about your content or products

When you start with [!DNL Recommendations], you pass information about every item that you want to recommend.

![Illustration showing how to teach Target about your content or products: feeds in CSV or Google Feed format, the data layer with Target, the API, and the Analytics integration.](assets/intro-7.png)

The simplest and most frequently used method is to send a CSV file on a daily or weekly basis from a product information management system or from a content management system. Other options are to pass information on the data layer from your page by using the [!DNL Adobe Target] JavaScript library, to use the APIs to pass information directly from your source system, or to use the [!DNL Adobe Analytics] integration if you are already passing catalog data to [!DNL Analytics]. You can use multiple options together, for example, passing most data daily via a CSV file and passing inventory updates more frequently via an API. The IT department is usually involved in setting up this step.

Whichever method you choose, include metadata about each item in three categories:

* **Data that you want to display to the user receiving the recommendation.** For example, the name of the movie and a thumbnail image URL.
* **Data that is useful for applying marketing and merchandising controls.** For example, the rating of the movie so that you do not recommend NC-17 movies.
* **Data that is useful for determining the similarity of items to other items.** For example, the genre of the movie or the actors that are in the movie.

### Capture user behavior

![Illustration showing how to capture user behavior: views and clicks lead to purchases, conversions, downloads, subscriptions, and plays, tracked with Target, Analytics, or the API.](assets/intro-9.png)

Add tags or use your existing [!DNL Analytics] implementation so that [!DNL Target] is aware of the items that your users view and purchase. If purchasing is not relevant to your context, track a different type of conversion event, for example, downloading a PDF, completing a survey, subscribing to a newsletter, or watching a video.

If you already use [!DNL Target] to run A/B Test activities on your site, you might have already completed this step. If you already use [!DNL Adobe Analytics] to report on site visits and conversion behavior, you can use [!DNL Analytics] as your behavioral data source. Otherwise, the simplest option is to set this up with a tag manager such as tags in [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html){target=_blank}. Offline or in-app interactions can also be sent to [!DNL Target] via the real-time API.

### Get recommendations with the right context

![Illustration showing how to get recommendations with the right context: the current product viewed, current product category, user favorite category, user favorite brand, and user loyalty tier are passed to Target.](assets/intro-10.png)

Besides user behavior in aggregate, [!DNL Target] needs the specific context where recommendations are shown, which includes information about the page and information from the user profile. [!DNL Target] uses this information to filter items and improve the personalization of recommendations.

## Build your first Recommendations activity

A [!DNL Recommendations] activity combines an audience, criteria, and a design. [!DNL Target] includes 14 built-in audiences, 42 built-in criteria, and 10 built-in design templates. You can customize each of these items or add your own.

![Illustration showing the parts that make a good recommendations activity: the audience (who should see these recommendations), the criteria (what items should be recommended), and the design (how the recommended items are displayed).](assets/intro-11.png)

[!DNL Target] uses the concept of the criteria card, which is like a recipe for personalization. Choosing or creating the right criteria is important to achieve the intended personalization results. A criteria card works like a funnel that takes you from your entire catalog to your final set of recommendations.

![Illustration of the criteria funnel: catalog contents, static filters (collections and exclusions), algorithm (recommendation key and logic), online business rules (dynamic filtering and attribute weighting), and final recommendations, next to an example criteria card.](assets/intro-14.png)

The following sections describe the parts of this funnel and how they work in [!DNL Target].

### Static filters (collections and exclusions)

Static filters are broadly applicable rules related to catalog attributes that you do not expect to change frequently, so you can use them in multiple recommendations.

![Illustration of static filters. Content: include all movies and exclude movies rated NC-17 from recommendations. Products: include all products available in the United States and exclude products from a regional private label.](assets/intro-16.png)

### Algorithm (recommendation key and logic)

The next step is to choose a recommendation key and logic, which are the basis for your recommendation. The recommendation key is what you are "looking up" to choose the recommendation.

![Illustration of the algorithm step. Recommendation key: currently viewed item, currently viewed category, last purchased item, or custom attribute. Recommendation logic: items with similar attributes, most viewed items in category, customers who bought this item also bought these items, or custom algorithm.](assets/intro-17.png)

[!DNL Target] includes a portfolio of algorithms.

![Illustration of the portfolio of algorithms: popularity-based (Most Viewed, Top Sellers), content-based (Content Similarity), item-based collaborative filtering (Viewed/Viewed, Viewed/Bought, Bought/Bought, where bought can be any conversion), personalized (Recently Viewed, Site Affinity, Profile-Enhanced Collab. Filtering), and bring your own (custom algorithms).](assets/intro-15.png)

### Online business rules

The last step is applying online business rules, which enhance your algorithms with domain knowledge and current context, based on what the visitor is doing on your digital property.

![Illustration of online business rules. Content: exclude previously watched movies, show movies from the same director, and boost movies with the same genre. Products: exclude out of stock products, show items with a price from $5 to $500, and boost items from the same brand.](/help/main/c-recommendations/assets/intro-18.png)
