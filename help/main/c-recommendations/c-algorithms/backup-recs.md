---
keywords: recommendation;backup;back up
description: Learn how to use backup recommendations in Adobe [!DNL Target Recommendations].
title: Use a backup recommendation
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
TQID: 'https://experienceleague.adobe.com/TziWJoAuEdCqa7uMTpX0O0InnlnjtbPXP-0wzQ-FCM0'
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Use a backup recommendation {#backup-recommendations}

>[!BEGINSHADEBOX]

**On this page:** Learn how backup recommendations fill the remaining slots of a design in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

When a recommendation does not have enough recommended items to fill the design, the backup recommendation feature in [!DNL Adobe Target] displays the results of the backup algorithm instead of default content. Without a backup recommendation, the system displays default content to the user.

>[!NOTE]
>
>For more information, including a matrix that explains the results of using the **[!UICONTROL Partial Design Rendering]** and **[!UICONTROL Show Backup Content]** options together or separately, see the [Backup Content section of Create criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

The backup recommendation feature always uses the top-viewed items on the site to fill any remaining slots after the data of the algorithm is used. For example, a design is configured to show five recommended items, but the algorithm has enough data to fill only two of the five slots. The backup recommendation feature then fills the other three slots with top-viewed items.

Backup recommendations are randomly chosen from the top 500 most-viewed products across the entire site. The data time period for backup recommendations is one week.

The 500 most-viewed results are ordered sequentially and then split into buckets of 20. The buckets are served in order, but the results inside each bucket are randomized and returned to the page, so users who refresh the page are presented with new, randomized results. If the result set from the union of the collection and the filtering rules is smaller than 20, items are randomly selected from the collection.

This bucketing process means that backup recommendations are displayed in the following order:

1. The 20 most-viewed items, randomized.
1. The next 20 most-viewed items, randomized.
1. The next 20 most-viewed items, randomized, and so forth.

Without bucketing, the 499th most-viewed item could be shown, followed by the 200th most-viewed item, followed by the 380th most-viewed item, and so on. Bucketing ensures that the most-viewed items are recommended first.

If items are grouped into collections, the backup recommendations generated for each criteria also use the collection, so only items in the collection are included in the backup recommendation. Any item that is excluded by global exclusion rules is not served as a backup recommendation. Duplicates are removed from batches of recommendations.

Backup recommendations are enabled by default and fill the extra slots in a design with a random selection of the most popular items on the site.

The use of backup recommendations is usually part of the discussion with the implementation team during the initial setup. To change the backup recommendation setting after implementation, contact the account manager.

When **[!UICONTROL Partial Design Rendering]** (see [Backup Content](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) is not enabled and the design cannot be filled, backup recommendations (when enabled) or default content are displayed instead.
