---
keywords: recommendations;frequently asked questions;faq
description: Frequently asked questions (FAQs) and their answers about [!DNL Target Recommendations] designs.
title: Design FAQ
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
TQID: 'https://experienceleague.adobe.com/xRu0XEnc8wX8PZngba7CO67mFdja7HALL-1OSnhAmuY'
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
# Design FAQ {#design-faq}

>[!BEGINSHADEBOX]

**On this page:** Find answers to frequently asked questions about [!DNL Adobe Target] [!DNL Recommendations] designs.

>[!ENDSHADEBOX]

* +++ How can the price of a recommended item display both digits to the right of the decimal point?

  By default, numeric values (such as `entity.value`) returned in designs do not display any trailing zeroes after the decimal point. For example, if an item costs $35.00, `entity.value` is equal to 35 and only 35 is displayed on the page, not $35.00.

  Two options are available to address this issue:

  * Velocity scripting or JavaScript can apply formatting to the returned value.

  * The price of the item can be passed into two separate entity attributes. The first, `entity.value`, can be used for numeric comparisons (such as price comparison rules). The second should be a custom attribute, such as `entity.displayValue`, that stores the value of the entity as a string to allow for proper rendering.

  For example,

  `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

  +++

* +++ Why is the category not displayed in the design when $entity1.categoryId is used?

  The category ID cannot be displayed in a design. Multiple categories can be stored, so the system does not know which category to display.

  +++

* +++ How can a design be changed to get an instant update?

  Altering the design that is currently in use takes a while to update. To change the design instantly, create a new design, select it in the activity, and save the recommendation.

  +++

* +++ How can key information, such as the category of the key product, be displayed in a design?

  The `$key` parameters capture most of the information of the key product for display within the design. For example, to display the thumbnail of the key product, use `$key.thumbnailURL`.

  +++

* +++ Which version of Velocity is used?

  Version 1.7, with no additional tools or libraries added. Basic Velocity functionality is available.

  +++

* +++ How can an existing entity value be replaced with a blank, for example when the entity.message of an item must be cleared at the end of a promotion?

  Sending a JavaScript non-breaking space appears to do this. The developers send `\u00A0` as the value, for example `entity.message=\u00A0`. Using that value as the default when no value is present, instead of a null, can also be considered.

  +++

* +++ Can a profile script be used in a [!DNL Recommendations] design?

  Yes. To use a profile script in a [!DNL Recommendations] design, wrap the name in `\${...}`. For example, if the profile script is named `user.basket`, refer to it as `\${user.basket}` in the design. The backslash implies that the profile script is not rendered by Velocity, so no operations can be performed on the profile script in a Velocity template. The value is printed directly on the page.

  +++
