---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: Learn how to filter dynamically in [!DNL Target Recommendations] by comparing items (entities) against a value in the user's profile.
title: Profile attribute matching
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
TQID: 'https://experienceleague.adobe.com/Gm91Mww5ylvNjUcmzp6KwxIG6LTibvI44LnW67KFzqk'
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
# Profile attribute matching {#profile-attribute-matching}

>[!BEGINSHADEBOX]

**On this page:** Learn how to filter recommendations dynamically in [!DNL Adobe Target Recommendations] by comparing items (entities) against a value in the profile of the visitor.

>[!ENDSHADEBOX]

Use **[!UICONTROL Profile Attribute Matching]** to show recommendations that match a value stored in the profile of the visitor, such as size or favorite brand. The process for creating and using inclusion rules for criteria and promotions is similar, as are the use cases and examples. For more information, see [Use dynamic and static inclusion rules](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

The following scenarios show how **[!UICONTROL Profile Attribute Matching]** can be used:

* A company that sells eyeglasses stores the favorite frame color of a visitor as "walnut." For that visitor, recommendations are set up to return only eyeglass frames that match "walnut" in color.
* A profile parameter can be defined for the clothing size (for example, Small, Medium, or Large) of a visitor as the visitor navigates the website of the company. A recommendation can be set up to match that profile parameter and return only the products in the preferred clothing size of the visitor.

## Profile attribute matching examples

**[!UICONTROL Profile Attribute Matching]** recommends only the items that match an attribute from the profile of the visitor, as in the following examples.

### Recommending items from the user's favorite brand

The **[!UICONTROL Profile Attribute Matching]** option can create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. With such a rule, if a visitor is looking at running shorts from a particular brand, only the recommendations that match the favorite brand of that visitor (the value stored in `profile.favoritebrand` in the profile of the visitor) are displayed.

![Favorite brand](/help/main/c-recommendations/c-algorithms/assets/favorite-brand-new.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Matching jobs to job seekers

To match jobs to job seekers, only the jobs that are in the same city as the job seeker are recommended. Inclusion rules can match the location of a job seeker from the profile of the visitor to a job listing, as in the following example:

![User's city](/help/main/c-recommendations/c-algorithms/assets/city-new.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Recommending items based on size

The following example shows how profile attribute matching affects recommendations on a website that sells electric fans.

When a visitor clicks various images of fans on this website, each page sets the value of the `entity.size` parameter based on whether the size of the fan in the image is small or large. A profile script tracks and counts the number of times the value of `entity.size` is set to small versus large.

If the visitor then returns to the Home Page, filtered recommendations are displayed based on whether more small fans or large fans were clicked.

Recommendations based on viewing more small fans on the website:

![small fans recommendations](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations based on viewing more large fans on the website:

![large fans recommendations](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
