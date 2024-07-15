---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;static;static filter
description: Learn how to manually enter one or more static values to filter using inclusion rules in Adobe [!DNL Target] Recommendations.
title: How Do I Filter By Static Values In Recommendations Activities?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
hide: yes
hidefromtoc: yes
---
# [!UICONTROL Static Filter]

Manually enter one or more static values to filter using inclusion rules in [!DNL Adobe Target Recommendations].

For example, only recommend content with a Motion Picture Association (MPA) rating of "G" or "PG."

You can create as many inclusion rules as necessary. The inclusion rules are joined with an AND operator. All rules must be met to include an item in a recommendation.

>[!NOTE]
>
>If you are familiar with how inclusion rules were configured prior to the Target 17.6.1 release (June 2017), you'll notice that some of the options and operators have changed. Only those operators applicable to the selected option display and some operators were renamed ("matches" is now "equals") to be more consistent and intuitive. All existing exclusion rules created prior to this release were automatically migrated into the new structure. No restructuring is necessary on your part.

## Recommend content rated G or PG

To create an inclusion rule with static values to recommend content with an MPA rating of "G" or "PG" only (exclude "R" and "NC17" content), you could create the following filtering rules "movie-rating equals any of g-rated" and "movie-rating equals any of pg-rated".
