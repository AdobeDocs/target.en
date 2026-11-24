---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;static;static filter
description: Learn how to manually enter one or more static values to filter using inclusion rules in Adobe [!DNL Target] Recommendations.
title: Static filter
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
TQID: 'https://experienceleague.adobe.com/-HTJO4YFi0-isyA-5LbVUaEPu7YX1WFgPy-OexMSXFY'
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
# Static filter {#static-filter}

>[!BEGINSHADEBOX]

**On this page:** Learn how to filter recommendations by manually entering one or more static values in inclusion rules in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

**[!UICONTROL Static Filter]** limits the items in a recommendation to the items that match static values that are entered manually. Any number of inclusion rules can be created. The inclusion rules are joined with an AND operator, so all rules must be met for an item to be included in a recommendation. For general information about inclusion rules, see [Use dynamic and static inclusion rules](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Recommend content rated G or PG

To recommend only content with a Motion Picture Association (MPA) rating of "G" or "PG" (exclude "R" and "NC17" content), create one filtering rule with the operator "movie-rating equals any of" and enter the values "g-rated" and "pg-rated".
