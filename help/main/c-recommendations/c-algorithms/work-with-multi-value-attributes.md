---
keywords: multi-value;attributes;recommendations;multi value;multivalue;multi-value
description: Learn how to work with a multi-value field in [!DNL Target Recommendations] using special multi-value operators.
title: Work with multi-value attributes
feature: Recommendations
exl-id: 82018a9a-0983-458c-9387-3602dab4409b
TQID: 'https://experienceleague.adobe.com/FrjVxvYfGh2o-qomXRbVh6WS6f65Mja41gBMhejEPlE'
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
# Work with multi-value attributes {#multi-value-attributes}

>[!BEGINSHADEBOX]

**On this page:** Learn how to send multi-value data to [!DNL Adobe Target Recommendations] and how to use it in inclusion rules with the multi-value operators.

>[!ENDSHADEBOX]

A multi-value field holds several values for the same item or visitor. For example:

* Movies offered to users: a given movie has multiple actors.
* Tickets sold for concerts: a given user has multiple favorite bands.
* Clothing sold: a shirt is available in multiple sizes.

To handle recommendations in these scenarios, multi-value data can be passed to [!DNL Target Recommendations] and used with special multi-value operators.

## Send multi-value data {#send}

To allow [!DNL Recommendations] to identify multi-value data, it should be sent as a JSON array.

For a multi-value parameter in JavaScript (`targetPageParams`), see [Implementing multi-value attributes](/help/main/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) in *Custom entity attributes*.

In a CSV file, a multi-value entity attribute is sent as a JSON array in the cell of the attribute, as in the following sample.

+++ Sample CSV file with a multi-value attribute

```
## RECSRecommendations Upload File,,,,,,,,,,,,,,,,,,,
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines.,,,,,,,,,,,,,,,,,,,
## RECS,,,,,,,,,,,,,,,,,,,
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left.,,,,,,,,,,,,,,,,,,,
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'.,,,,,,,,,,,,,,,,,,,
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations.,,,,,,,,,,,,,,,,,,,
## RECSentity.id ,entity.name,entity. categoryId ,entity. message ,entity.thumbnailUrl ,entity.value ,entity.pageUrl ,entity.inventory ,entity.margin ,entity.custom1 ,entity.custom2 ,entity.custom3 ,entity.custom4,entity.custom5,entity.custom6,entity.custom7,entity.custom8,entity.custom9,entity.custom10,
1,Sample Product 1,category1,Save 10%,http://sample.store/products/images/product1_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=1,1000,48,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
2,Sample Product 2,category1,Save 10%,http://sample.store/products/images/product2_th.jpg,369,http://sample.store/products/product_detail.jsp?productId=2,1000,52,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
3,Sample Product 3,category1,Save 10%,http://sample.store/products/images/product3_th.jpg,479,http://sample.store/products/product_detail.jsp?productId=3,1000,78,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
4,Sample Product 4,category1,Save 10%,http://sample.store/products/images/product4_th.jpg,409,http://sample.store/products/product_detail.jsp?productId=4,1000,66,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
5,Sample Product 5,category1,Save 10%,http://sample.store/products/images/product5_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=5,1000,45,a,"[ ""v1"", ""v2"" ]",,,,,,,,, 
```

+++

When an entity attribute, profile attribute, or mbox parameter is provided as multi-value in this format, [!DNL Recommendations] automatically infers that the field is multi-value.

## Use multi-value attributes in inclusion rules {#multi-value-inclusion-rules}

The following operators are available for use with multi-value entity, profile, and mbox attributes:

* **[!UICONTROL is contained in list]**
* **[!UICONTROL is not contained in list]**

>[!NOTE]
>
>Support for dynamic matching to multi-value attributes is currently available only in criteria that use a profile attribute matching or parameter (mbox) attribute matching rule that compares a single value on the left side to a multi-value on the right side. Multi-value attributes are not currently supported in promotions, entity attribute matching, or for lists on the left side of inclusion rules.

### Example: Exclude recently watched items

To prevent any movies in the last ten watched movies of the user from being recommended, first write a profile script called `user.lastWatchedMovies` that tracks the last ten viewed movies as a JSON array. The items can then be excluded with the following inclusion rule:

```
Profile Attribute Matching
id - is not contained in list - user.lastWatchedMovies
```

JSON API representation of the inclusion rule:

```
{
    "attribute": "id",
    "operation": "isNotContainedInList",
    "source": {
        "name": "user.lastWatchedMovies",
        "type": "PROFILE"
    }
} 
```

### Example: Recommend items from the user's favorites

To recommend concert tickets only when the band playing is one of the favorite bands of the user, two items are required: a profile variable called `profile.favoriteBands` that contains the favorite bands of the user, and an attribute `entity.artistPerforming` in the catalog that contains the artist performing in the concert. The following inclusion rule can then be used:

```
Profile Attribute Matching
artistPerforming - is contained in list - profile.favoriteBands
```

JSON API representation of the inclusion rule:

```
{
    "attribute": "artistPerforming",
    "operation": "isContainedInList",
    "source": {
        "name": "profile.favoriteBands",
        "type": "PROFILE"
    }
}
```

### Example: API creation of criteria recommending items from a user's favorites

Criteria that use multi-value filtering rules can be created through the [!DNL Adobe Target] APIs, like all criteria. The following example API call creates a criteria where the entity attribute `id` is contained in the mbox parameter list `favorites`:

```
curl -X POST \
  https://<serverhost>/api/recs/<client>/criteria/item \
  -H 'Accept: application/vnd.adobe.target.v1+json' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: <from API client>' \
  -H 'X-Target-user-email: <email address>' \
  -H 'cache-control: no-cache' \
  -d '{
    "name": "viewed criteria",
    "criteriaTitle": "test title",
    "type": "VIEWED_CF",
    "key": "CURRENT",
    "daysCount": "TWO_WEEKS",
    "aggregation": "NONE",
    "backupDisabled": false,
    "partialDesignAllowed": true,
    "configuration": {
        "inclusionRules": [
            {
                "attribute": "id",
                "operation": "isContainedInList",
                "source": {
                    "name": "mbox.favorites",
                    "type": "MBOX"
                }
            }
        ]
    }
}'
```

This call is paired with JavaScript on the page that passes in the content of the favorites:

```
<!-- pass in the value of mbox parameter "favorites" as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
