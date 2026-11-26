---
keywords: Recommendations
description: Explore common scenarios that show how changes made to your page in the Visual Experience Composer (VEC) affect Adobe Target's ability to display an experience.
title: What Are Some Common Page Modification Scenarios?
feature: Visual Experience Composer (VEC)
exl-id: 7a05fbf9-3427-436e-a54f-4f1dd16d885a
TQID: 'https://experienceleague.adobe.com/BI2SnUU5ilCf0auld15q1rpCrnLoPEwbe1fZO6G1quc'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Page modification scenarios {#vec-scenarios}

>[!BEGINSHADEBOX]

**On this page:** Learn how changes made to a page outside of [!DNL Target] affect the ability of [!DNL Target] to display an experience, through seven scenarios with examples.

>[!ENDSHADEBOX]

The [!DNL Target] selector determines where an experience displays. When a page is modified outside of [!DNL Target], the changes might affect the ability of [!DNL Target] to find that location and display the experience.

The selector always works with a unique class, which is not equivalent to an ID. When no class is assigned to the element, the selector counts the previous siblings that have the same tag name.

>[!NOTE]
>
>The scenarios use list items as examples, but the concepts apply to any element.

The following table summarizes the scenarios. In every scenario, the selector is `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`.

|Scenario|Action applied|Reason|
|---|---|---|
|Insert an element with a different class name before the selected element|Yes|`li.women-section:eq(0)` is not affected|
|Insert an element with the same class name as the selected element|No|A new element takes the first position, which breaks the selector|
|Insert an element after the selected element|Yes|The new element is added at the same position relative to the parent element|
|Remove the element immediately preceding the selected element|Yes|The class of the selected item is not altered|
|Remove the element immediately following the selected element|Yes|The class of the selected item is not altered|
|Remove the selected element|Yes|The element is removed successfully|
|Rename the class of the selected element|No|`class` is not found|

## Insert an element with a different class name before the selected element

A new element is inserted as a sibling of the element in the [!DNL Target] selector. If the first class on the element was added by JavaScript, delivery fails and the action is not applied.

**Inserted element:**

```html
<li class="kids-section">Kids</li>
```

**Selected element:**

`<li class="women-section">Women</li>`

**Selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** The selector works as expected, because `li.women-section:eq(0)` is not affected.

**Before:**

```html
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul>
</div>
```

**After:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

## Insert an element with the same class name as the selected element

A list is inserted while an item of a list is selected.

**Inserted element:**

```html
<ul class="nav">
   <li class="item"> Sale </li>
   <li class="item"> Offers </li>
</ul>
```

**Selected element:**

`<li class="women-section">Women</li>`

**Selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** The selector does not work. `ul.nav:eq(0)` now points to a dynamically added element, which is not available, so the action is not applied. Adding a similar list item with the same class, dynamically or manually, after the activity is created puts a new element in the first position, which breaks the selector.

**Before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

**After (attempted):**

```html
<div id="wrap">
     <ul class="nav">
        <li class="item"> Sale</li>
        <li> class="item"> Offers</li>
     </ul>
     <ul class="nav">
       <li class="men-section"> Men</li>
       <li class="women-section">Women</li>
    </ul>
</div>
```

## Insert an element after the selected element

A list is inserted after the selected list item.

**Inserted element:**

```html
<ul class="nav">
   <li class="men-section"> Men Clothes</li>
   <li class="women-section"> Women Clothes</li>
</ul>
```

**Selected element:**

`<li class="women-section">Women Shoes</li>`

**Selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** Inserting a list after the list that ends with the selected item works as expected. The new element is added at the same position as the selected element relative to the parent element.

**Before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>       <li class="women-section">Women Shoes</li>
    </ul>
</div>
```

**After:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>
        <li class="women-section">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## Remove the element immediately preceding the selected element

The list item before the selected element is deleted.

**Removed element:**

```html
<li class="men-section"> Men </li>
```

**Selected element:**

`<li class="women-section">Women</li>`

**Selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** The element is removed successfully, because the class of the selected item is not altered.

**Before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**After:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Remove the element immediately following the selected element

The list item after the selected element is deleted.

**Removed element:**

```html
<li class="kids-section">Kids</li>
```

**Selected element:**

`<li class="women-section">Women</li>`

**Selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** The element is removed successfully, because the class of the selected item is not altered and the removed element has a unique class within its parent subtree.

**Before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Kids</li>
    </ul>
</div>
```

**After:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Remove the selected element

The selected list item is deleted.

**Removed element:**

```html
<li class="women-section">Women</li>
```

**Selected element:**

`<li class="women-section">Women</li>`

**Selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** The element is removed successfully.

**Before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**After:**

```html
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## Rename the class of the selected element

The class of the selected list item is changed.

**Changed element:**

```html
<li class="women-section">Women</li>
```

**Selected element:**

`<li class="women-section">Women</li>`

**Selector:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Result:** The class cannot be renamed, because `class` is not found.

**Before:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**After (attempted):**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```
