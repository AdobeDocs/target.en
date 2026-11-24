---
keywords: criteria;algorithm;industry vertical;page type;recommendation key;recommendation logic;logic;data range;lookback window;behavior data source;partial design;backup recommendations;inclusion rules;attribute weighting;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Learn how to create criteria that control the content of your [!DNL Recommendations] activities to show the recommendations that are most appropriate for your activity.
title: How Do I Create [!UICONTROL Criteria] in [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 3f4f59b2-6637-4c33-bf17-bff11bef7173
TQID: 'https://experienceleague.adobe.com/r9FWgHWw6NX1CmhqI-7MLoamNFDepeCq1bpiJ8eyISM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
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
---
# Create criteria {#create-criteria}

>[!BEGINSHADEBOX]

**On this page:** Learn how to create criteria in [!DNL Adobe Target Recommendations] and how to configure each section of a criteria.

>[!ENDSHADEBOX]

Criteria in [!DNL Adobe Target] [!DNL Recommendations] control the content of [!DNL Recommendations] activities. Criteria use the visitor's actions to determine which content or products to display, so creating suitable criteria shows the recommendations that are most appropriate for the activity.

## Access the Create New Criteria screen

There are multiple ways to reach the **[!UICONTROL Create New Criteria]** screen. Some screen options vary depending on how the screen is reached.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Criteria created here are automatically made available for all [!DNL Recommendations] activities.

    ![More Actions icon](../assets/criteria_create_1.png)

* When creating a [!DNL Recommendations] activity using the **[!UICONTROL Visual Experience Composer]** (VEC), the **[!UICONTROL Select Criteria]** screen displays immediately after an element on the page is selected and **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]**, or **[!UICONTROL Insert Recommendations After]** is clicked. Select an available criteria or click **[!UICONTROL Create Criteria]**. A new criteria can be saved for use with other [!DNL Recommendations] activities. For more information, see [Create a Recommendations activity](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

    ![More Actions icon](../assets/criteria_create_2.png)

* When editing a [!DNL Recommendations] activity, click in a **[!UICONTROL Recommendations Location]** box on the page, and select **[!UICONTROL Change Criteria]**. On the **[!UICONTROL Select Criteria]** screen, click **[!UICONTROL Create Criteria]**. The new criteria can be saved for use with other [!DNL Recommendations] activities.

## [!UICONTROL Basic Information] {#info}

The basic information identifies the criteria and categorizes it for reuse in other activities.

1. Type a **[!UICONTROL Criteria Name]**.

   This is the internal name used to describe the criteria. For example, a criteria can be named "Highest margin products" without that title displaying publicly. The public-facing title is set in the next step.

1. Type a public-facing **[!UICONTROL Display Title]** to appear on the page for any recommendations that use this criteria.

   For example, "People who viewed this viewed that" or "Similar products" can be displayed when this criteria is used to show recommendations.

1. Type a short **[!UICONTROL Description]** of the criteria.

   The description should help identify the criteria and might include information about its purpose.

1. Select an industry vertical based on the goals of the recommendations activity.

   | Industry Vertical | Goal |
   |--- |--- |
   |**[!UICONTROL Retail/Ecommerce]**|Conversion resulting in purchase|
   |**[!UICONTROL Lead Generation/B2B/Financial Services]**|Conversion with no purchase|
   |**[!UICONTROL Media/Publishing]**|Engagement|

   Other criteria options change based on the selected industry vertical.

    ![More Actions icon](../assets/criteria_create_3.png)

1. Select a **[!UICONTROL Page Type]**.

   Multiple page types can be selected. Together, the industry vertical and page types help categorize saved criteria, making it easier to reuse criteria for other [!DNL Recommendations] activities.

## [!UICONTROL Recommendations Algorithm] {#rec-algo}

The algorithm determines how the items for the recommendations are selected.

>[!CONTEXTUALHELP]
>id="target_recommendations_profile_attribute"
>title="Profile Attribute"
>abstract="You can create a Profile Attribute using Profile Scripts."

1. Select an **[!UICONTROL Algorithm Type]** and **[!UICONTROL Algorithm]**:

   ![Recommended Algorithm section](assets/recommended-algorithm.png)

   |Algorithm type|When to use / Available algorithms|
   | --- | --- |
   |**[!UICONTROL Cart-Based]**|Make recommendations based on the user's cart contents. <ul><li>**[!UICONTROL People Who Viewed These, Also Viewed]** </li><li>**[!UICONTROL People Who Viewed These, Also Bought]**</li><li>**[!UICONTROL People Who Bought These, Also Bought]**</li></ul>|
   |**[!UICONTROL Popularity-Based]**|Make recommendations based on the overall popularity of an item across your site or based on the popularity of items within a user's favorite or most-viewed category, brand, genre, and so forth. <ul><li>**[!UICONTROL Most Viewed Across the Site]**</li><li>**[!UICONTROL Most Viewed by Category]**</li><li>**[!UICONTROL Most Viewed by Item Attribute]**</li><li>**[!UICONTROL Most Viewed by Profile Attribute]**</li><li>**[!UICONTROL Top Sellers Across the Site]**</li><li>**[!UICONTROL Top Sellers by Category]**</li><li>**[!UICONTROL Top Sellers by Item Attribute]**</li><li>**[!UICONTROL Top Sellers by Profile Attribute]**</li><li>**[!UICONTROL Top by Analytics Metric]**</li></ul>|
   |**[!UICONTROL Item-Based]**|Make recommendations based on finding similar items to an item that the user is currently viewing or has recently viewed. <ul><li>**[!UICONTROL People Who Viewed This, Viewed That]**</li><li>**[!UICONTROL People Who Viewed This, Bought That]**</li><li>**[!UICONTROL People Who Bought This, Bought That]**</li><li>**[!UICONTROL Items with Similar Attributes]**</li></ul>|
   |**[!UICONTROL User-Based]**|Make recommendations based on the user's behavior.<ul><li>**[!UICONTROL Recently Viewed Items]**</li><li>**[!UICONTROL Recommended for You]**</li></ul>|
   |**[!UICONTROL Custom Criteria]**|Make recommendations based on a custom file you upload.<ul><li>Custom Algorithm</li></ul>|

   >[!NOTE]
   >
   >If you select **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]**, you have the option to set [content similarity rules](#similarity).

1. Configure the algorithm as required by selecting a **[!UICONTROL Recommendation Key]**, **[!UICONTROL Filtering Key]**, **[!UICONTROL Co-Occurrence Basis]**, **[!UICONTROL Analytics Metric]**, and/or **[!UICONTROL Item Attribute]** and **[!UICONTROL Profile Attribute to Match]**. The available configuration options vary depending on the selected algorithm.

   For more information about choosing a **[!UICONTROL Recommendation Key]**, see [Base the recommendation on a recommendation key](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. (Conditional) If you selected **[!UICONTROL Most Viewed by Profile Attribute]** or **[!UICONTROL Top Sellers by Profile Attribute]**, select a **[!UICONTROL Profile Attribute]** to group the interaction data by.

   Profile attributes come from a profile script that captures a visitor characteristic, such as region or country. The script name must carry the `recsAttribute` prefix, so it is stored as `user.recsAttribute<Name>`, for example, `user.recsAttributeRegion`. At delivery time, [!DNL Target] serves each visitor the ranked list that corresponds to their own value of that attribute.

## [!UICONTROL Backup Content] {#content}

**[!UICONTROL Backup Content]** rules determine what happens if the number of recommended items does not fill the [recommendations design](/help/main/c-recommendations/c-design-overview/design-overview.md). Criteria can return fewer recommendations than the design calls for. For example, if the design has slots for four items but the criteria causes only two items to be recommended, the remaining slots can be left empty, filled with backup recommendations, or no recommendations can be displayed.

1. (Optional) Enable **[!UICONTROL Partial Design Rendering]** option.

   As many slots as possible are filled, but the design template might include blank space for the remaining slots. If this option is disabled and there is not enough content to fill all available slots, recommendations are not served and default content is displayed instead.

   Enable this option to serve recommendations with blank slots. To fill the empty slots with similar or popular content from the site, use backup recommendations, as explained in the next step.

1. (Optional) Enable **[!UICONTROL Show Backup Content]** option.

   Fill any remaining empty slots in the design with a random selection of most-viewed products from across the site. Using backup recommendations ensures that the recommendation design fills all available slots. Consider a 4 x 1 design, as illustrated below:

   ![4 x 1 design](../assets/velocity_example.png)

   If the criteria causes only two items to be recommended and the **[!UICONTROL Partial Design Rendering]** option is enabled, the first two slots are filled and the remaining two slots stay empty. If the **[!UICONTROL Show Backup Content]** option is enabled, the first two slots are filled based on the specified criteria and the remaining two slots are filled based on the backup recommendations.

   +++ The following matrix shows the result for each combination of the **[!UICONTROL Partial Design Rendering]** and **[!UICONTROL Backup Content]** options

   | Partial Design Rendering | Backup Content | Result |
   |--- |--- |--- |
   |Disabled|Disabled|If fewer recommendations are returned than the design calls for, the recommendations design is replaced by default content and no recommendations are displayed.|
   |Enabled|Disabled|The design is rendered, but may include blank space if fewer recommendations are returned than the design calls for.|
   |Enabled|Enabled|Backup recommendations will fill available design "slots," fully rendering the design.<br>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is partially rendered.<br>If the criteria does not return any recommendations, and inclusion rules restrict backup recommendations to zero, the design is replaced with default content.|
   |Disabled|Enabled|Backup recommendations will fill available design "slots," fully rendering the design.<br>If applying inclusion rules to backup recommendations restricts the number of qualifying backup recommendations to the point that the design cannot be filled, the design is replaced by default content and no recommendations are displayed.|

   For more information, see [Use a backup recommendation](/help/main/c-recommendations/c-algorithms/backup-recs.md).
   +++

1. (Conditional) If you selected **[!UICONTROL Show Backup Content]** in the previous step, you can enable **[!UICONTROL Apply inclusion rules to backup recommendations]**.

   Inclusion rules determine which items are included in the recommendations. The options available depend on the industry vertical.

   For more details, see [Specify inclusion rules](#inclusion) below.

## [!UICONTROL Data Source] {#data-source}

The data source determines the behavioral data that the criteria uses and the time range of that data.

1. Select the desired **[!UICONTROL Behavioral Data Source]**: **[!UICONTROL Adobe Target]** or **[!UICONTROL Analytics]**.

   >[!NOTE]
   >
   >The **[!UICONTROL Behavioral Data Source]** section displays only if the implementation uses [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).

   ![Behavioral Data Source section](../assets/criteria_create_4.png)

   If you chose **[!UICONTROL Analytics]**, select the desired report suite.

   +++ Criteria availability when Analytics is the data source

   If the criteria uses [!DNL Adobe Analytics] as the behavioral data source, once created, the time for criteria availability depends on whether the selected report suite and lookback window has been used for any other criteria, as explained below:

   * **One-time report suite setup**: The first time a report suite is used with a given data range lookback window, [!DNL Target Recommendations] can take from two to seven days to fully download the behavioral data for the selected report suite from [!DNL Analytics]. This time frame is dependent on the [!DNL Analytics] system load.
   * **New or edited criteria using an already available report suite**: When creating a new criteria or editing an existing criteria, if the selected report suite has already been used with [!DNL Target Recommendations], with a data range equal to or lesser than the selected data range, then the data is immediately available and no one-time setup is required. In this case, or if an algorithm's settings are edited while not modifying the selected report suite or data range, the algorithm runs or re-runs within 12 hours.
   * **Ongoing algorithm runs**: Data flows from [!DNL Analytics] to [!DNL Target Recommendations] on a daily basis. For example, for the **[!UICONTROL Viewed Affinity]** recommendation, when a user views a product, a product-view tracking call is passed into [!DNL Analytics] close to real-time. The [!DNL Analytics] data is pushed to [!DNL Target] early the next day and [!DNL Target] runs the algorithm in less than 12 hours.

   For more information, see [Use Adobe Analytics with Target Recommendations](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

   +++



1. Set the **[!UICONTROL Lookback Window]** to determine the time range of available historical user behavior data to use when determining which recommendations to show. This option is available for all algorithms with the exception of **[!UICONTROL Items with Similar Attributes]** and **[!UICONTROL Custom Algorithms]**.

   If the site has a lot of traffic and behaviors change frequently, choose a shorter data window. A shorter window enables [!DNL Recommendations] to be more responsive to changes in the market and in the business. For example, a shorter window means that [!DNL Recommendations] detects changes in visitor behavior as visitors begin seasonal shopping, such as back-to-school shopping or Christmas, and recommends items appropriate to those shopping seasons.

   If the site does not have a lot of data, or visitor behavior does not change frequently, a longer window might be selected. However, for many sites, a shorter window results in higher-quality recommendations.

   +++ Available data ranges

   |Lookback Window option|Updated frequency (displayed on hover)|Supported algorithms|
   | --- | --- | --- |
   |Six hours|Algorithm runs every 3-6 hours|**[!UICONTROL Popularity-Based]** algorithms when the selected **[!UICONTROL Behavioral Data Source]** is [!DNL Adobe Target]|
   |One day|Algorithm runs every 12-24 hours|**[!UICONTROL Popularity-Based]** algorithms|
   |Two days|Algorithm runs every 12-24 hours|<ul><li>**[!UICONTROL Popularity-Based]** algorithms</li><li>**[!UICONTROL Item-Based]** algorithms</li><li>**[!UICONTROL User-Based]** algorithms</li><li>**[!UICONTROL Cart-Based]** algorithms</li></ul>|
   |One week|Algorithm runs every 24-48 hours|<ul><li>**[!UICONTROL Popularity-Based]** algorithms</li><li>**[!UICONTROL Item-Based]** algorithms</li><li>**[!UICONTROL User-Based]** algorithms</li><li>**[!UICONTROL Cart-Based]** algorithms</li></ul>|
   |Two weeks|Algorithm runs every 24-48 hours|<ul><li>**[!UICONTROL Popularity-Based]** algorithms</li><li>**[!UICONTROL Item-Based]** algorithms</li><li>All **[!UICONTROL User-Based]** algorithms</li><li>**[!UICONTROL Cart-Based]** algorithms</li></ul>|
   |One month (30 days)|Algorithm runs every 24-48 hours|<ul><li>**[!UICONTROL Popularity-Based]** algorithms</li><li>**[!UICONTROL Item-Based]** algorithms</li><li>**[!UICONTROL User-Based]** algorithms</li><li>**[!UICONTROL Cart-Based]** algorithms</li></ul>|
   |Two months (61 days)|Algorithm runs every 24-48 hours|<ul><li>**[!UICONTROL Popularity-Based]** algorithms</li><li>**[!UICONTROL Item-Based]** algorithms</li><li>**[!UICONTROL User-Based]** algorithms</li><li>**[!UICONTROL Cart-Based]** algorithms</li></ul>|

   +++

## Content Similarity {#similarity}

Use **[!UICONTROL Content Similarity]** rules to make recommendations based on item or media attributes.

![Behavioral Data Source section](../assets/criteria_create_5.png)

Content similarity compares item attribute keywords and makes recommendations based on how many keywords different items have in common. Recommendations based on content similarity do not require past data.

Content similarity is effective for new items, which are not likely to show up in recommendations using *People Who Viewed This, Also Viewed* and other logic based on past behavior. It can also generate recommendations for new visitors, who have no past purchases or other historical data.

When **[!UICONTROL Item-Based]**/ **[!UICONTROL Item with Similar Attributes]** is selected, rules can be created to increase or decrease the importance of specific item attributes in determining recommendations. For items such as books, the importance of attributes like *genre*, *author*, *series*, and so on can be boosted to recommend similar books.

Content similarity uses keywords to compare items, so some attributes, such as *message* or *description*, can introduce "noise" into the comparison. Rules can be created to ignore these attributes.

By default, all attributes are set to *Baseline*. A rule is needed only to change this setting.

>[!NOTE]
>
>The content similarity algorithm might use random sampling in computing similarity between items. As a result, similarity ratings between items might vary between algorithm runs.

## Inclusion Rules {#inclusion}

Inclusion rules narrow the items that display in the recommendations. They can be used while creating criteria or promotions. Inclusion rules are optional; however, setting these details gives more control over the items that appear in the recommendations. Each detail that is configured further narrows the display criteria.

For example, only women's shoes that have an inventory of more than 50 and a price between $25 and $45 can be displayed. Each attribute can also be weighted so that the items that are more important to the business are most likely to appear. As another example, job openings can be displayed only to visitors who visit the site from certain cities and who have the required college degrees.

Inclusion rule options vary by industry vertical. By default, inclusion rules are applied to backup recommendations. The inclusion rules are joined with an AND, so all rules must be met to include an item in a recommendation.

>[!IMPORTANT]
>
>Use inclusion rules cautiously. They are useful if, for example, the organization has rules that demand that one brand is not recommended while another brand is being shown. However, this feature has an opportunity cost: restricting items from showing when they would normally be shown by the activity criteria could lose a percentage of lift.

The following steps create a simple inclusion rule that displays only women's shoes that have an inventory of more than 50 and a price between $25 and $45:

1. (Conditional) Enable **[!UICONTROL Allow recently purchased items to be recommended]**.

   This setting is based on the `productPurchasedId`. The default behavior is to not recommend previously purchased items. In most cases, items that a customer has recently purchased should not be promoted. The setting is useful for items that people typically purchase only once, such as kayaks. For items that people come back to purchase again on a repeated basis, such as shampoo or other personal items, enable this option.

1. Set a price range for the products to recommend.

1. Set the minimum inventory amount for the products to recommend.

1. Configure the recommendation to display items only when they meet certain criteria.

   Items can be included only when one of the attributes in the list meets or does not match one or more specified conditions.

   The available evaluators depend on the value chosen in the first drop-down. Multiple items can be listed, and they are evaluated with OR. Multiple rules are combined with an AND.

   >[!NOTE]
   >
   >This option limits the items that are displayed in the recommendation. It does not affect which pages the recommendation is displayed on. To limit where the recommendation displays, select the pages in the experience composer.

For more information, see [Use dynamic and static inclusion rules](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Attribute Weighting {#weighting}

Multiple rules can be added to "nudge" the algorithm based on important information or metadata about the content catalog, so that certain items are more likely to be shown.

For example, a higher weighting can be applied to on-sale items so they appear more often in the recommendation. Non-sale items are not completely excluded, but they appear less often. Multiple weighted attributes can be applied to the same algorithm, and the weighted attributes can be tested on split traffic in the recommendation.

1. Choose a value.

   The value determines the type of item that is more likely to display, based on one of several available criteria.

1. Choose an evaluator.

1. Type the keyword to complete the rule attributes.

   For example, the complete rule might be "Category contains substring shoes."

1. Select the weight to assign to the rule.

   Options range from 0 to 100 in increments of 25.

1. Add additional rules if desired.

When finished, click **[!UICONTROL Create]**.

If you are creating a new **[!UICONTROL Recommendations]** activity or editing an existing one, the **[!UICONTROL Save criteria for later]** check box is selected by default. If you do not want to use the criteria in other activities, clear the check box before saving.
