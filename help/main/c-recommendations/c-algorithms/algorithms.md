---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Learn how to use criteria in Adobe [!DNL Target] [!DNL Recommendations].
title: How Do I Use Criteria in [!DNL Target] Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
TQID: 'https://experienceleague.adobe.com/Wo7I3piBQ7zwYF7kqRphDeWjcBCpyvIvTkwKK0t0f9U'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
    internal-label: Integrations
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Get started with [!UICONTROL Criteria] {#get-started-criteria}

>[!BEGINSHADEBOX]

**On this page:** Learn how criteria work in [!DNL Adobe Target Recommendations] and which industry vertical, algorithm type, and recommendation key options are available.

>[!ENDSHADEBOX]

**[!UICONTROL Criteria]** in [!DNL Adobe Target] [!DNL Recommendations] are rules that determine which products or content to recommend based on a predetermined set of visitor behaviors. Criteria can be based on popular trends, a visitor's current and past behaviors, or similar products and content. Multiple criteria can be added to an activity to test multiple recommendation types against each other.

The industry vertical and the algorithm type that are selected determine the options that are available when criteria are created.

## Industry Vertical {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

When criteria are created, an industry vertical is selected based on the goals of the recommendations activity.

| Industry Vertical | Goal |
|--- |--- |
|**[!UICONTROL Retail/Ecommerce]**|Conversion resulting in purchase|
|**[!UICONTROL Lead Generation/B2B/Financial Services]**|Conversion with no purchase|
|**[!UICONTROL Media/Publishing]**|Engagement|

Other criteria options change based on the selected industry vertical. The default industry vertical can be set on the **[!UICONTROL Administration]** > **[!UICONTROL Recommendations]** page, or the industry vertical can be specified for each criteria.

## Algorithm Type {#section_885B3BB1B43048A88A8926F6B76FC482}

The algorithm type that is selected determines the available algorithms. The following table explains the algorithm types and their accompanying algorithms.

|Algorithm type|When to use|Available algorithms|
| --- | --- | --- |
|**[!UICONTROL Cart-Based]**|Make recommendations based on the user's cart contents.|<ul><li>**[!UICONTROL People Who Viewed These, Also Viewed]**</li><li>**[!UICONTROL People Who Viewed These, Also Bought]**</li><li>**[!UICONTROL People Who Bought These, Also Bought]**</li></ul>For more information, see [Cart-Based](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Base the recommendation on a recommendation key*.|
|**[!UICONTROL Popularity-Based]**|Make recommendations based on the overall popularity of an item across the site, or on the popularity of items within the favorite or most-viewed category, brand, genre, and so forth of the user.|<ul><li>**[!UICONTROL Most Viewed Across the Site]**</li><li>**[!UICONTROL Most Viewed by Category]**</li><li>**[!UICONTROL Most Viewed by Item Attribute]**</li><li>**[!UICONTROL Most Viewed by Profile Attribute]**</li><li>**[!UICONTROL Top Sellers Across the Site]**</li><li>**[!UICONTROL Top Sellers by Category]**</li><li>**[!UICONTROL Top Sellers by Item Attribute]**</li><li>**[!UICONTROL Top Sellers by Profile Attribute]**</li><li>**[!UICONTROL Top by Analytics Metric]**</li></ul>|
|**[!UICONTROL Item-Based]**|Make recommendations based on items that are similar to an item that the user is currently viewing or has recently viewed.|<ul><li>**[!UICONTROL People Who Viewed This, Viewed That]**</li><li>**[!UICONTROL People Who Viewed This, Bought That]**</li><li>**[!UICONTROL People Who Bought This, Bought That]**</li><li>**[!UICONTROL Items with Similar Attributes]**</li></ul>|
|**[!UICONTROL User-Based]**|Make recommendations based on the user's behavior.|<ul><li>**[!UICONTROL Recently Viewed Items]**</li><li>**[!UICONTROL Recommended for You]**</li></ul>|
|**[!UICONTROL Custom Criteria]**|Make recommendations based on an uploaded custom file.|<ul><li>Custom Algorithm</li></ul>|

For more information about each algorithm, see [Base the recommendation on a recommendation key](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Use a custom recommendation key {#custom-key}

Recommendations can also be based on the value of a custom profile attribute. For example, recommended movies can be displayed based on the movie that a user most recently added to the queue.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

    ![Criteria page with the Create criteria menu open, showing Create Criteria and Create Criteria Sequence](../assets/criteria_1.png)

1. Fill in the information in the [Basic Information section](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. In the [Recommended Algorithm](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo) section, select **[!UICONTROL Item Based]** from the **[!UICONTROL Algorithm Type]** list.

1. Select **[!UICONTROL People Who Viewed This, Viewed That]** from the **[!UICONTROL Algorithm]** list.

1. Select the custom profile attribute from the **[!UICONTROL Recommendation Key]** list (for example, **[!UICONTROL Last Show Added to Watchlist]**).

   >[!NOTE]
   >
   >Custom profile parameters can be passed to [!DNL Target] through JavaScript, API, or integrations. For more information about custom profile attributes, see [Visitor profiles](/help/main/c-target/c-visitor-profile/visitor-profile.md).

    ![Create Criteria dialog box showing the Recommendations Algorithm section with the Algorithm Type, Algorithm, and Recommendation Key lists](../assets/criteria_2.png)

## View criteria information {#section_7162DE58E4594FD688A4D7FDB829FD8B}

The criteria details show how a criteria is configured and which activities use it.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** to display the list of criteria.

1. Click the desired criteria in the **[!UICONTROL Name]** column.

1. View general information about the selected criteria in the **[!UICONTROL Attributes]** and Details sections, including its **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL Industry Vertical]**, **[!UICONTROL Page Types]**, **[!UICONTROL Recommendation Key]**, **[!UICONTROL Recommendation Logic]**, **[!UICONTROL Algorithm ID]**, and Last Modified information (date and who modified the algorithm).

1. View the list of activities that reference the selected criteria in the **[!UICONTROL Usage]** section.

   >[!NOTE]
   >
   >The **[!UICONTROL Algorithm Usage]** feature is currently supported for [!DNL Recommendations] activities only. This feature is not currently supported for **[!UICONTROL A/B Test]**, **[!UICONTROL Auto-Allocate]**, **[!UICONTROL Auto-Target]**, and **[!UICONTROL Experience Targeting]** (XT) activities that include [recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).

    ![Criteria details with the Attributes and Details sections and the Usage section highlighted](../assets/criteria_3.png)
