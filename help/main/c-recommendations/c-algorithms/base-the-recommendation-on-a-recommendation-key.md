---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Learn how to use recommendations based on keys that use visitor behavior context to show relevant results in [!UICONTROL Recommendations] activities.
title: How Do I Base the [!UICONTROL Recommendation] on a [!UICONTROL Recommendation Key]?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
TQID: 'https://experienceleague.adobe.com/1gI3rMMf9s5ogc4BvBz4fMUqxed1Nqad0XoaR8SlU58'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
    internal-label: Integrations
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Base the recommendation on a recommendation key {#base-on-recommendation-key}

>[!BEGINSHADEBOX]

**On this page:** Learn about the algorithm types, algorithms, and recommendation keys available for basing recommendations in [!DNL Adobe Target Recommendations] activities.

>[!ENDSHADEBOX]

Algorithm-based recommendations use the context of visitor behavior to show relevant results in [!DNL Adobe Target] [!DNL Recommendations] activities. Each algorithm type offers its own set of algorithms. For a summary of the algorithm types and their algorithms, see [Get started with Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md#section_885B3BB1B43048A88A8926F6B76FC482).

Each criteria is defined in its own tab. Traffic is split evenly across the criteria tests: with two criteria, traffic is divided equally between them, and with two criteria and two designs, traffic is split evenly between the four combinations. A percentage of site visitors can also be set to see the default content, for comparison. In that case, the specified percentage of visitors sees the default content, and the rest are split between the criteria and design combinations.

For more information about creating criteria and defining its algorithm types and algorithms, see [Create criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

Different algorithms suit different types of pages. The following sections describe each algorithm type and its algorithms.

## Cart-Based {#cart-based}

The **[!UICONTROL Cart-Based]** algorithm type recommends items based on the contents of the visitor's current cart. The recommendation keys are supplied as comma-separated values in the [mbox parameter `cartIds`](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}. Only the first 10 values are considered.

Cart-based recommendation logic is similar to the "**[!UICONTROL Recommended For You]**" user-based algorithm and to the "**[!UICONTROL People Who Viewed This, Bought That]**" and "**[!UICONTROL People Who Bought This, Bought That]**" item-based algorithms.

[!DNL Target] uses collaborative filtering techniques to determine similarities for each item in the visitor's cart, then combines the behavioral similarities of all the items into a merged list.

Marketers can choose whether [!DNL Target] looks at visitor behavior within a single session or across multiple sessions:

* **[!UICONTROL Single Session]**: Based on what other visitors did within a single session.

  A single session suits products that strongly "go with" each other based on a usage, occasion, or event. For example, a visitor who is buying a printer might also need ink and paper, and a visitor who is buying peanut butter might also need bread and jelly.

* **[!UICONTROL Across Sessions]**: Based on what other visitors did across multiple sessions.

  Multiple sessions suit products that strongly "go with" each other based on visitor preference or taste. For example, a visitor who likes Star Wars might also like Indiana Jones, even if the visitor does not necessarily want to watch both movies in the same sitting. Similarly, a visitor who likes the board game "Codenames" might also like the board game "Avalon," even if the visitor cannot play both games simultaneously.

[!DNL Target] makes recommendations for each visitor based on the items in their current cart, regardless of whether visitor behavior is considered within a single session or across multiple sessions.

The following algorithms are available with the **[!UICONTROL Cart-Based]** algorithm type:

| Algorithm | How it works | When to use | Recommendation keys |
| --- | --- | --- | --- |
| **[!UICONTROL People Who Viewed These, Also Viewed]** | Recommends items that are most often viewed in the same session that the specified item is viewed. Returns other products people viewed after viewing this one. The specified product is not included in the results set. | Create additional conversion opportunities by recommending items that other visitors who viewed an item also viewed. For example, visitors who view road bikes on the site might also look at bike helmets, cycling kits, locks, and so forth, so a recommendation can suggest other products that help increase revenue. | **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |
| **[!UICONTROL People Who Viewed These, Also Bought]** | Recommends items that are most often purchased in the same session that the specified item is viewed. Returns other products people purchased after viewing this one. The specified product is not included in the results set. | Increase cross-selling opportunities by displaying a recommendation on a product page, for example, that displays items that other visitors who viewed the item purchased. If the visitor is viewing a fishing pole, the recommendation could show additional items other visitors purchased, such as tackle boxes, waders, and fishing lures. As visitors browse the site, they receive additional purchasing recommendations. | **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |
| **[!UICONTROL People Who Bought These, Also Bought]** | Recommends items that are most often purchased by customers at the same time as the specified item. Returns other products people purchased after buying this one. The specified product is not included in the results set. | Increase cross-selling opportunities by displaying a recommendation on a shopping cart summary page, for example, that displays items that other buyers also purchased. If the visitor is purchasing a suit, the recommendation could display additional items other visitors purchased along with the suit, such as ties, dress shoes, and cufflinks. As visitors review their purchases, they receive additional recommendations. | **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |

## [!UICONTROL Popularity-Based]

The **[!UICONTROL Popularity-Based]** algorithm type recommends items based on their overall popularity across the site, or on their popularity within the favorite or most-viewed category, brand, genre, and so forth of the user.

The following algorithms are available with the **[!UICONTROL Popularity-Based]** algorithm type:

| Algorithm | How it works | When to use | Recommendation keys |
| --- | --- | --- | --- |
| **[!UICONTROL Most Viewed Across the Site]** | The recommendation is determined by the item that has been viewed most often, based on recency/frequency criteria. See [Most Viewed Across the Site scoring](#most-viewed). | General pages, such as home or landing pages and offsite ads. | |
| **[!UICONTROL Most Viewed by Category]** | The recommendation is determined by the category that has received the most activity, using the same method as for the most viewed item, except that categories are scored instead of products. See [Most Viewed by Category scoring](#most-viewed-category). | General pages, such as home or landing pages and offsite ads. | **[!UICONTROL Current Category]**, **[!UICONTROL Favorite Category]** |
| **[!UICONTROL Most Viewed by Item Attribute]** | Recommends items or media similar to the most-viewed items or media on the site. The item attribute to base the recommendation on is selected, for example, "Name" or "Brand". Then the profile attributes stored in the visitor's profile to match are selected, for example "Favorite Brand," "Last Item Added to Cart," or "Most Viewed Show." | | |
| **[!UICONTROL Most Viewed by Profile Attribute]** | Recommends the most viewed items grouped by a visitor profile attribute rather than by item information, as **[!UICONTROL Most Viewed by Category]** and **[!UICONTROL Most Viewed by Item Attribute]** do. [!DNL Target] keeps a separate ranked list per attribute value and, at delivery time, shows each visitor the list matching their own stored value. See [Profile attribute algorithms](#profile-attribute-algorithms). | | |
| **[!UICONTROL Top Sellers Across the Site]** | Displays the items that are included in the most completed orders from across the site. Multiple units of the same item in a single order are counted as one order. | Create recommendations for top-selling items on the site to increase conversion and revenue. This logic is suited for first-time visitors to the site. | |
| **[!UICONTROL Top Sellers by Category]** | Displays the items that are included in the most completed orders by category. Multiple units of the same item in a single order are counted as one order. | Create recommendations for top-selling items on the site based on category to increase conversion and revenue. This logic is suited for first-time visitors to the site. | **[!UICONTROL Current Category]**, **[!UICONTROL Favorite Category]** |
| **[!UICONTROL Top Sellers by Item Attribute]** | Recommends items or media similar to the most-purchased items or media on the site. The item attribute to base the recommendation on is selected, for example, "Name" or "Brand". Then the profile attributes stored in the visitor's profile to match are selected, for example "Favorite Brand," "Last Item Added to Cart," or "Most Viewed Show." | | |
| **[!UICONTROL Top Sellers by Profile Attribute]** | Recommends the top-selling items grouped by a visitor profile attribute rather than by item information, as **[!UICONTROL Top Sellers by Category]** and **[!UICONTROL Top Sellers by Item Attribute]** do. [!DNL Target] keeps a separate top-sellers list per attribute value and, at delivery time, shows each visitor the list matching their own stored value. See [Profile attribute algorithms](#profile-attribute-algorithms). | | |
| **[!UICONTROL Top by Analytics Metric]** | Displays the "Top x" where *x* is an arbitrary [!DNL Analytics] metric. When using behavioral data from mboxes, **[!UICONTROL Top Sold]** or **[!UICONTROL Top Viewed]** can be used (x = "Sold" or x = "Viewed"). When using behavioral data from [!DNL Adobe Analytics], x = "Cart Adds" or some other [!DNL Analytics] metric can be used. | | |

### [!UICONTROL Most Viewed Across the Site] scoring {#most-viewed}

The recommendation is the item that has been viewed most often, determined by recency/frequency criteria as follows:

* 10 points for first product view
* 5 points for every subsequent view
* At the end of a session, divide all values by 2

For example, viewing surfboard A then surfboard B in one session results in A: 10, B: 5. When the session ends, the result is A: 5, B: 2.5. If the same items are viewed in the next session, the values change to A: 15, B: 7.5.

### [!UICONTROL Most Viewed by Category] scoring {#most-viewed-category}

The recommendation is the category that has received the most activity. It uses the same method as "most viewed item", except that categories are scored instead of products, with recency/frequency criteria as follows:

* 10 points for first category view
* 5 points for every subsequent view

With each visit, the score of every non-current category that has been viewed before is decremented by 1.

For example, viewing category A then category B in one session results in A: 9, B: 10. If the same items are viewed in the next session, the values change to A: 20, B: 9.

### Profile attribute algorithms {#profile-attribute-algorithms}

>[!CONTEXTUALHELP]
>id="target_recommendations_profile_attribute"
>title="Profile Attribute"
>abstract="You can create a Profile attribute using Profile Scripts. Once a Profile Script is created and activated, its corresponding Profile attribute can be used with this algorithm."

**[!UICONTROL Most Viewed by Profile Attribute]** and **[!UICONTROL Top Sellers by Profile Attribute]** depend on a profile script to populate the attribute. The script name must begin with the `recsAttribute` prefix so [!DNL Target] stores it as `user.recsAttribute<Name>`. A script can be written for any visitor characteristic that is relevant to the use case. For more information about setting profile attributes with profile scripts, see [Profile parameters](https://experienceleague.adobe.com/en/docs/target/using/audiences/visitor-profiles/profile-parameters).

For example, the following script, named `recsAttributeRegion`, bases recommendations on the region of the visitor:

```
var region = mbox.param('userRegion');
if (region) return region;
```

Similarly, the following script, named `recsAttributeLoyaltyTier`, bases recommendations on the loyalty tier of the visitor:

```
var tier = mbox.param('visitorLoyaltyTier');
if (tier) return tier;
```

After the script is created and activated, the corresponding **[!UICONTROL Region]** or **[!UICONTROL Loyalty Tier]** entry becomes available in the profile attribute drop-down of the create criteria window. The `recsAttribute` prefix itself is not shown in the drop-down.

## [!UICONTROL Item-Based]

The **[!UICONTROL Item-Based]** algorithm type recommends items that are similar to an item that the user is currently viewing or has recently viewed.

The following algorithms are available with the **[!UICONTROL Item-Based]** algorithm type:

| Algorithm | How it works | When to use | Recommendation keys |
| --- | --- | --- | --- |
| **[!UICONTROL People Who Viewed This, Viewed That]** | Recommends items that are most often viewed in the same session that the specified item is viewed. Returns other products people viewed after viewing this one. The specified product is not included in the results set. | Create additional conversion opportunities by recommending items that other visitors who viewed an item also viewed. For example, visitors who view road bikes on the site might also look at bike helmets, cycling kits, locks, and so forth, so a recommendation can suggest other products that help increase revenue. | **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |
| **[!UICONTROL People Who Viewed This, Bought That]** | Recommends items that are most often purchased in the same session that the specified item is viewed. Returns other products people purchased after viewing this one. The specified product is not included in the results set. | Increase cross-selling opportunities by displaying a recommendation on a product page, for example, that displays items that other visitors who viewed the item purchased. If the visitor is viewing a fishing pole, the recommendation could show additional items other visitors purchased, such as tackle boxes, waders, and fishing lures. As visitors browse the site, they receive additional purchasing recommendations. | **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |
| **[!UICONTROL People Who Bought This, Bought That]** | Recommends items that are most often purchased by customers at the same time as the specified item. Returns other products people purchased after buying this one. The specified product is not included in the results set. | Increase cross-selling opportunities by displaying a recommendation on a shopping cart summary page, for example, that displays items that other buyers also purchased. If the visitor is purchasing a suit, the recommendation could display additional items other visitors purchased along with the suit, such as ties, dress shoes, and cufflinks. As visitors review their purchases, they receive additional recommendations. | **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |
| **[!UICONTROL Items with Similar Attributes]** | Recommends items or media similar to items or media based on current page activity or past visitor behavior. If **[!UICONTROL Items with Similar Attributes]** or **[!UICONTROL Media with Similar Attributes]** is selected, content similarity rules can be set. For more information, see [Content Similarity](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity). | Content similarity is effective for new items, which are not likely to show up in recommendations using **[!UICONTROL People Who Viewed This]**, **[!UICONTROL Viewed That]**, and other logic based on past behavior. It can also generate recommendations for new visitors, who have no past purchases or other historical data. | **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |

## [!UICONTROL User-Based]

The **[!UICONTROL User-Based]** algorithm type recommends items based on the user's behavior.

The following algorithms are available with the **[!UICONTROL User-Based]** algorithm type:

| Algorithm | How it works | When to use | Recommendation keys |
| --- | --- | --- | --- |
| **[!UICONTROL Recently Viewed Items]** | Uses the visitor's history (spanning sessions) to present the last *x* items the visitor has viewed, based on the number of slots in the design. See [Recently Viewed Items details](#recently-viewed). | General pages, such as home or landing pages and offsite ads. | |
| **[!UICONTROL Recommended for You]** | Recommends items based on each visitor's browsing, viewing, and purchasing history. Both views and purchases are used to determine the recommended items. The list of recommendations is weighted towards the visitor's most recent activity, is updated in session, and becomes more personalized as the user browses the site. | Deliver personalized content and experiences to both new and returning visitors. The specified recommendation key (for example, **[!UICONTROL Current Item]**) is used to apply any inclusion rule filters selected, for example, to exclude items that do not meet certain criteria (products out of stock, articles published more than 30 days ago, movies rated R, and so forth), or to limit included items to a single category or to the current category. | Filtering keys: **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]** |

### [!UICONTROL Recently Viewed Items] details {#recently-viewed}

The **[!UICONTROL Recently Viewed Items]** algorithm returns results specific to a given [environment](/help/main/administrating-target/hosts.md). If two sites belong to different environments and a visitor switches between the two sites, each site shows only recently viewed items from the appropriate site. If two sites are in the same environment and a visitor switches between the two sites, the visitor sees the same recently viewed items for both sites.

The **[!UICONTROL Recently Viewed Items]** criteria cannot be used for backup recommendations.

**[!UICONTROL Recently Viewed Items]** or **[!UICONTROL Recently Viewed Media]** can be filtered so that only items with a particular attribute are displayed.

* **[!UICONTROL Recently Viewed]** criteria are configurable, like other criteria in recommendations.
* [Collections](/help/main/c-recommendations/c-products/collections.md), [exclusions](/help/main/c-recommendations/c-products/exclusions.md), and [inclusions](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (including the special rules for Price and Inventory) can be used in the same way as with any other criteria.

One use case is a multinational company with multiple businesses, where a visitor might view items across multiple digital properties. Recently viewed items can then be limited to the property where they were viewed, so they do not display on the site of another property.

>[!NOTE]
>
>**[!UICONTROL Recently Viewed Items]** respects both the global exclusions settings and the selected collection setting for the activity. If an item is excluded by a global exclusion, or is not contained in the selected collection, it is not displayed. Therefore, when using a **[!UICONTROL Recently Viewed Items]** criteria, the "All Collections" setting should generally be used.

## Custom Criteria {#custom}

The **[!UICONTROL Custom Criteria]** algorithm type recommends items based on an uploaded custom file.

The recommendation is determined by an item that is stored in a visitor's profile, using either user.*x* or profile.*x* attributes. When this option is selected, the `entity.id` value must be present in the profile attribute. When recommendations are based on custom attributes, the custom attribute must be selected first, and then the recommendation type.

Real-time filtering can be applied to the output of the custom criteria. For example, the recommended items can be limited to those from the favorite category or brand of a visitor. This combines offline calculations with real-time filtering, so [!DNL Target] can add personalization to offline calculated recommendations or custom-curated lists. The data science and research of the organization are then combined with the delivery, run-time filtering, A/B testing, targeting, reporting, and integrations of Adobe.

Inclusion rules on **[!UICONTROL Custom Criteria]** turn otherwise static recommendations into dynamic recommendations based on the interests of the visitor.

* Custom criteria are configurable, like other criteria in recommendations.
* [Collections](/help/main/c-recommendations/c-products/collections.md), [exclusions](/help/main/c-recommendations/c-products/exclusions.md), and [inclusions](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (including the special rules for Price and Inventory) can be used in the same way as with any other criteria.

Possible use cases include:

* Recommend movies from a custom-curated list, but only if the visitor has not already watched them.
* Run an offline algorithm and use the results to power the recommendations, while ensuring that out-of-stock items are never recommended.
* Include only items that are from this visitor's favorite category.

## Recommendation keys {#keys}

The following recommendation keys are available from the **[!UICONTROL Recommendation Key]** drop-down list:

| Key | How it is determined | What to pass | Use on | Do not use on | Algorithms |
| --- | --- | --- | --- | --- | --- |
| **[!UICONTROL Current Item]** | The item the visitor is currently viewing. Recommendations display other items that might interest visitors who are interested in the specified item. | The `entity.id` value must be passed as a parameter in the display mbox. | Single-item pages, such as product pages. | Null search results pages. | **[!UICONTROL Items with Similar Attributes]**, **[!UICONTROL People Who Viewed This, Viewed That]**, **[!UICONTROL People Who Viewed This, Bought That]**, **[!UICONTROL People Who Bought This, Bought That]** |
| **[!UICONTROL Last Purchased Item]** | The last item that was purchased by each unique visitor. | Nothing. This is captured automatically. | Home page, My Account page, offsite ads. | Product pages or pages relevant to purchases. | **[!UICONTROL Items with Similar Attributes]**, **[!UICONTROL People Who Viewed This, Viewed That]**, **[!UICONTROL People Who Viewed This, Bought That]**, **[!UICONTROL People Who Bought This, Bought That]** |
| **[!UICONTROL Last Viewed Item]** | The last item that was viewed by each unique visitor. | Nothing. This is captured automatically. | Home page, My Account page, offsite ads. | Product pages or pages relevant to purchases. | **[!UICONTROL Items with Similar Attributes]**, **[!UICONTROL People Who Viewed This, Viewed That]**, **[!UICONTROL People Who Viewed This, Bought That]**, **[!UICONTROL People Who Bought This, Bought That]** |
| **[!UICONTROL Most Viewed Item]** | The items or media that are viewed most often on the site. This logic displays recommendations based on the most-viewed items to increase conversions for other items. For example, a media site could display recommendations on its home page for its most-viewed videos to encourage visitors to watch additional videos. | | | | **[!UICONTROL Items with Similar Attributes]**, **[!UICONTROL People Who Viewed This, Viewed That]**, **[!UICONTROL People Who Viewed This, Bought That]**, **[!UICONTROL People Who Bought This, Bought That]** |
| **[!UICONTROL Current Category]** | The product category that the visitor is currently viewing. Recommendations display items in the specified product category. | The `entity.categoryId` value must be passed as a parameter to the display mbox. | Single-category pages. | Null search results pages. | **[!UICONTROL Top Sellers]**, **[!UICONTROL Most Viewed]** |
| **[!UICONTROL Favorite Category]** | The visitor's favorite product category. Recommendations display items in the specified product category. | The `entity.categoryId` value must be passed as a parameter to the display mbox. | Single-category pages. | Null search results pages. | **[!UICONTROL Top Sellers]**, **[!UICONTROL Most Viewed]** |

### Custom recommendation key

Recommendations can be based on the value of a custom profile attribute. For example, recommended movies can be displayed based on the movie that a visitor most recently added to the queue.

1. Select the custom profile attribute from the **[!UICONTROL Recommendation Key]** drop-down list (for example, "**[!UICONTROL Last Show Added to Watchlist]**").

1. Select the **[!UICONTROL Recommendation Logic]** (for example, "**[!UICONTROL People Who Viewed This, Viewed That]**").

If the custom profile attribute does not directly match a single entity ID, specify how [!DNL Recommendations] matches an entity. For example, to display the top-selling items of the favorite brand of a visitor:

1. Select the custom profile attribute from the **[!UICONTROL Recommendation Key]** drop-down list (for example, "Favorite Brand").

1. Select the **[!UICONTROL Recommendation Logic]** to use with this key (for example, "**[!UICONTROL Top Sellers]**").

   The **[!UICONTROL Group By Unique Value Of]** option displays.

1. Select the entity attribute that matches the chosen key. In this case "**[!UICONTROL Favorite Brand]**" matches `entity.brand`.

   [!DNL Recommendations] now produces a "**[!UICONTROL Top Sellers]**" list for each brand and shows the visitor the appropriate "**[!UICONTROL Top Sellers]**" list based on the value stored in the visitor's **[!UICONTROL Favorite Brand]** profile attribute.

### [!UICONTROL Site Affinity] {#site-affinity}

Recommends items based on the certainty of a relationship between items. This criteria can be configured to set how much data is required before a recommendation is displayed, using the **[!UICONTROL Inclusion Rules]** slider. For example, when very strong is selected, the products with the strongest certainty of a match are recommended.

For example, if a very strong affinity is set and the design includes five items, three of which meet the strength of connection threshold, the two items that do not meet the minimum strength requirements are not displayed in the recommendations and are replaced by the defined backup items. The items with the strongest affinity display first.

As another example, an online retailer can recommend items in subsequent visits that a visitor has shown interest in during past sessions. Activity for each visitor's session is captured to calculate an affinity based on a recency and frequency model. As the visitor returns to the site, site affinity is used to display recommendations based on past actions on the site.

A weak site affinity might give the best results for customers with diverse product collections and diverse site behaviors.

This logic can be used with the following recommendation keys: **[!UICONTROL Current Item]**, **[!UICONTROL Last Purchased Item]**, **[!UICONTROL Last Viewed Item]**, **[!UICONTROL Most Viewed Item]**.
