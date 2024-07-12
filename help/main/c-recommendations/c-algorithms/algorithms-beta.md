---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Learn how to use criteria in Adobe [!DNL Target] [!DNL Recommendations].
title: How Do I Use Criteria in [!DNL Target] Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
hide: yes
hidefromtoc: yes
---
# [!UICONTROL Criteria]

[!UICONTROL Criteria] in [!DNL Adobe Target] [!DNL Recommendations] are rules that determine which products or content to recommend based on a predetermined set of visitor behaviors. Criteria can be based on popular trends, a visitor's current and past behaviors, or similar products and content. You can test multiple recommendation types against each other by adding multiple criteria.

The following sections explain more about the criteria keys and the recommendation logic that you can use for each key. Click the links for more detailed information.

## Industry Vertical {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

While creating a criteria, you select an industry vertical based on the goals of your recommendations activity.

| Industry Vertical | Goal |
|--- |--- |
|[!UICONTROL Retail/Ecommerce]|Conversion resulting in purchase|
|[!UICONTROL Lead Generation/B2B/Financial Services]|Conversion with no purchase|
|[!UICONTROL Media/Publishing]|Engagement|

Other criteria options change based on the industry vertical you select. You can set your default industry vertical on the **[!UICONTROL Administration] > [!UICONTROL Recommendations]** page or you can specify the industry vertical for each criteria.

## Algorithm Type {#section_885B3BB1B43048A88A8926F6B76FC482}

The algorithm type that you select determines the available algorithms.

![Criteria page](assets/criteria-page-new.png)

The following table explains the various algorithm types and their accompanying algorithms.

|Algorithm type|When to use|Available algorithms|
| --- | --- | --- |
|[!UICONTROL Cart-Based]|Make recommendations based on the user's cart contents.|<ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul>For more information, see [Cart-Based](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Base the recommendation on a recommendation key*.|
|[!UICONTROL Popularity-Based]|Make recommendations based on the overall popularity of an item across your site or based on the popularity of items within a user's favorite or most-viewed category, brand, genre, and so forth.|<ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul>|
|[!UICONTROL Item-Based]|Make recommendations based on finding similar items to an item that the user is currently viewing or has recently viewed.|<ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul>|
|[!UICONTROL User-Based]|Make recommendations based on the user's behavior.|<ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul>|
|[!UICONTROL Custom Criteria]|Make recommendations based on a custom file that you upload.|<ul><li>Custom Algorithm</li></ul>|

For more information about each algorithm, see [Base the recommendation on a recommendation key](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Using a custom recommendation key {#custom-key}

You can also base recommendations on the value of a custom profile attribute.

>[!NOTE]
>
>Custom profile parameters can be passed to [!DNL Target] through JavaScript, API, or integrations. For more information about custom profile attributes, see [Visitor profiles](/help/main/c-target/c-visitor-profile/visitor-profile.md).

For example, suppose that you want to display recommended movies based on the movie that a user most recently added to the queue.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Fill in the information in the [Basic Information section](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. In the [Recommended Algorithm](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo) section, select **[!UICONTROL Item Based]** from the **[!UICONTROL Algorithm Type]** list.

1. Select **[!UICONTROL People Who Viewed This, Viewed That]** from the **[!UICONTROL Algorithm]** list.

1. Select your custom profile attribute from the **[!UICONTROL Recommendation Key]** list (for example, [!UICONTROL Last Show Added to Watchlist]).

## Viewing criteria information {#section_7162DE58E4594FD688A4D7FDB829FD8B}

You can view criteria details by clicking the desired criteria in the [!UICONTROL Name] column.

![Criteria Card hover](/help/main/c-recommendations/c-algorithms/assets/criteria-hover.png)

The **[!UICONTROL Algorithm Info]** tab lets you view general information about the selected criteria, including its [!UICONTROL Name], [!UICONTROL Description], [!UICONTROL Industry Vertical], [!UICONTROL Page Types], [!UICONTROL Recommendation Key], [!UICONTROL Recommendation Logic], [!UICONTROL Algorithm ID], and Last Modified information (date and who modified the algorithm).

The **[!UICONTROL Algorithm Usage]** section lets you view a list of activities that reference the selected criteria.

>[!NOTE]
>
>The [!UICONTROL Algorithm Usage] feature is currently supported for [!DNL Recommendations] activities only. This feature is not currently supported for [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Experience Targeting] (XT) activities that include [recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).