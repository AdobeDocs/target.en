---
keywords: custom design;velocity;decimal;comma;customize design
description: Learn how to use the open-source [!DNL Velocity] design language to customize recommendation designs in [!DNL Target] Recommendations.
title: Customize a design using Velocity
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 035d7988-80d8-4080-bb0d-1d0e9f8856d1
TQID: 'https://experienceleague.adobe.com/cccBRfwqqn-eL2hraSDAoJHPYSCkcA9tVne3OWDXxEU'
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
# Customize a design using [!DNL Velocity] {#customize-design}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use the open-source [!DNL Velocity] design language to customize recommendation designs in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

## [!DNL Velocity] overview {#velocity-overview}

Information about [!DNL Velocity] can be found at [https://velocity.apache.org](https://velocity.apache.org).

All [!DNL Velocity] logic, syntax, and so on can be used for a recommendation design. This means that *for* loops, *if* statements, and other code can be created with [!DNL Velocity] instead of JavaScript.

Entity attributes sent to [!DNL Recommendations] in the `productPage` mbox or the CSV upload can be displayed in a design, with the exception of "multi-value" attributes. Any type of attribute can be sent; however, [!DNL Target] does not pass attributes of type "multi-value" as an array over which a design can iterate (for example `entityN.categoriesList`).

These values are referenced with the following syntax:

```
$entityN.variable
```

Entity attribute names must follow [!DNL Velocity] shorthand notation, which consists of a leading *$* character, followed by a [!DNL Velocity] Template Language (VTL) Identifier. The VTL Identifier must start with an alphabetic character (a-z or A-Z).

[!DNL Velocity] entity attribute names are restricted to the following types of characters:

* Alphabetic (a-z, A-Z)
* Numeric (0-9)
* Hyphen ( - )
* Underscore ( _ )

The following attributes are available as [!DNL Velocity] arrays. As such, they can be iterated over or referenced through an index.

* `entities`
* `entityN.categoriesList`

For example:

```
#foreach ($category in $entity1.categoriesList) 
<br/>$category 
#end
```

Or

```
#if ($entities[0].categoriesList.size() >= 3 ) 
$entities[0].categoriesList[2] 
#end
```

For more information about [!DNL Velocity] variables (attributes), see [Velocity documentation](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

If a profile script is used in a design, the $ preceding the script name must be escaped with a `\` (backslash). For example:

`\${user.script_name}`

>[!NOTE]
>
>The maximum number of entities that can be referenced in a design, either hard-coded or through loops, is 99. The design script can contain up to 65,000 characters.

A design that displays something similar to the following illustration:

![Example of a 4 x 1 design titled "Other fun activities", with four items that each show a photo, a name, a price, a rating, and a distance](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

can use the following code:

```
<table style="border:1px solid #CCCCCC;"> 
<tr> 
<td colspan="3" style="font-size: 130%; border-bottom:1px solid  
#CCCCCC;"> You May Also Like... </td> 
</tr> 
<tr> 
<td style="border-right:1px solid #CCCCCC;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity1.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity1.id</a></div> 
By $entity1.message <a href="?x14=brand;q14=$entity1.message"> 
(More)</a><br/> 
sku: $entity1.prodId<br/> Price: $$entity1.value 
<br/><br/> 
</div> 
</td> 
<td style="border-right:1px solid #CCCCCC; padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;">  
<div class="search_title"><a href="$entity2.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity2.id</a></div> 
By $entity2.message <a href="?x14=brand;q14=$entity2.message"> 
(More)</a><br/> 
sku: $entity2.prodId<br/> 
Price: $$entity2.value 
<br/><br/> 
</div> 
</td> 
<td style="padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity3.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity3.id</a></div> 
By $entity3.message <a href="?x14=brand;q14=$entity3.message"> 
(More)</a><br/> 
sku: $entity3.prodId<br/> Price: $$entity3.value 
<br/><br/> 
</div> 
</td> 
</tr>  
</table>
```

>[!NOTE]
>
>To add text after the value of an attribute, before a tag that indicates that the attribute name has finished, use formal notation to enclose the name of the attribute. For example: `${entity1.thumbnailUrl}.gif`.

`algorithm.name` and `algorithm.dayCount` can also be used as entity attributes in designs, so one design can be used to test multiple criteria, and the criteria name can be dynamically displayed in the design. This shows the visitor that the visitor is looking at "top sellers" or "people who viewed this bought that". The `dayCount` (the number of days of data used in the criteria, for example "top sellers over the last 2 days") can also be displayed.

## Working with numbers in [!DNL Velocity] designs {#numbers}

By default, [!DNL Velocity] designs treat all entity attributes as string values. An entity attribute might need to be treated as a numeric value to perform a math operation or to compare it to another numerical value. To treat an entity attribute as a numeric value, follow these steps:

1. Declare a dummy variable and initialize it to an arbitrary integer or double value.
1. Ensure that the entity attribute to use is not blank (required for the design parser of [!DNL Target Recommendations] to validate and save the design).
1. Pass the entity attribute into the `parseInt` or `parseDouble` method on the dummy variable created in step 1 to turn the string into an integer or double value.
1. Perform the math operation or comparison on the new numeric value.

### Example: Calculating a discount price

To reduce the displayed price of an item by $0.99 to apply a discount, the following approach can be used:

```
#set( $double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

### Example: Choosing the number of stars to display based on an item's rating

To display an appropriate number of stars based on the numerical average customer rating of an item, the following approach can be used:

```
#set( $double = 0.1 )

#if( $entity1.get('rating') != '' )
    #set( $rating = $double.parseDouble($entity1.get('rating')) )
    #if( $rating >= 4.5 )
        <img src="5_stars.jpg">
    #elseif( $rating >= 3.5 )
        <img src="4_stars.jpg">
    #elseif( $rating >= 2.5 )
        <img src="3_stars.jpg">
    #elseif( $rating >= 1.5 )
        <img src="2_stars.jpg">
    #else
        <img src="1_star.jpg">
    #end
#else
    <img src="no_rating_default.jpg">
#end
```

### Example: Calculating the time in hours and minutes based on an item's length in minutes

To display the length of a movie in hours and minutes when the length is stored in minutes, the following approach can be used:

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## Displaying a key item with recommended products {#key-item}

A design can show the key item alongside the other recommended products. For example, the current item can be shown for reference next to the recommendations.

To do this, create a column in the design that uses the `$key` attribute that the recommendation is based on, instead of the `$entity` attribute. For example, the code for the key column might look like this:

```
<div class="at-table-column"> 
   <a href="$key.pageURL"> 
      <img src=$key.thumbnailUrl" class="at-thumbnail"/> 
      <br/><h3>$key.name</h3> 
      <br/><p class="at-light">$key.message</p> 
      <br/><p class="at-light">$key.value</p> 
   </a> 
</div>
```

The result is a design like the following, where one column shows the key item.

![Design with four columns, where the first column shows the key item marked as the current product](/help/main/c-recommendations/c-design-overview/assets/rec_key.png)

When a [!DNL Recommendations] activity is created, if the key item is taken from the profile of the visitor, such as "last purchased item," [!DNL Target] displays a random product in the **[!UICONTROL Visual Experience Composer]** (VEC). This is because a profile is not available while the activity is designed. When visitors view the page, they see the expected key item.

## Performing replacements in a string value {#replacements}

A design can replace values within a string. For example, the decimal point delimiter used in the United States can be replaced with the comma delimiter used in Europe and other countries.

The following code shows a single line in a conditional sale pricing example:

```
<span class="price">$entity1.value.replace(".", ",") &euro;</span><br>
```

The following code is a complete conditional example of a sale price:

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") &euro;</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") &euro;<br> #else 
    <span class="price">$entity1.value.replace(".", ",") &euro;</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
</div>
```

## Customizing the design size and checking for blank values {#default}

A [!DNL Velocity] script can control the dynamic sizing of the entity display. The following design accommodates a 1-to-many result to avoid creating empty HTML elements when not enough matching entities are returned from [!DNL Recommendations]. This script is best for scenarios when backup recommendations would not make sense and **[!UICONTROL Partial Design Rendering]** is enabled.

The following HTML snippet replaces the existing HTML portion in the 4x2 default design (the CSS is not included here, for the sake of brevity):

* If a fifth entity exists, the script inserts a closing div and opens a new row with `<div class="at-table-row">`.
* With 4x2, the maximum number of results shown is eight, but this can be customized for smaller or larger lists by modifying `$count <=8`.
* The logic does not balance the entities on multiple rows. For example, if there are five or six entities to display, it does not dynamically become three on top and two on the bottom (or three on top and three on the bottom). The top row displays four items before starting a second row.

```
<div class="at-table">
  <div class="at-table-row">
    #set($count=1) 
    #foreach($e in $entities)  
        #if($e.id != "" && $count < $entities.size() && $count <=8) 
            #if($count==5) 
                </div>
                <div class="at-table-row">
            #end
            <div class="at-table-column">
                <a href="$e.pageUrl"><img src="$e.thumbnailUrl" class="at-thumbnail" />
                    <br/>
                    <h3>$e.name</h3>
                    <br/>
                    <p class="at-light">$e.message</p>
                    <br/>
                    <p class="at-light">$$e.value</p>
                </a>
            </div>
            #set($count = $count + 1) 
        #end 
    #end
  </div>
</div>
```
