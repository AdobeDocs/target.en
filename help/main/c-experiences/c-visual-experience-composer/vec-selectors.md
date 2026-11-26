---
keywords: Experience Targeting;Landing Page Test
description: An element selector is a CSS expression that can identify one or more elements. Learn how to use element selectors in the Adobe [!DNL Target] Visual Experience Composer (VEC).
title: Can I Use Element Selectors in the Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: f4ddb30a-f599-4fe5-861c-2deeeb9a70dd
TQID: 'https://experienceleague.adobe.com/sqvUyLFddt7HPHH62jwpOZmwTIMSg-hyLIUr8w-x7vg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Element selectors used in the [!UICONTROL Visual Experience Composer] {#vec-selectors}

>[!BEGINSHADEBOX]

**On this page:** Learn how element selectors work in the [!UICONTROL Visual Experience Composer] (VEC), how to choose which selectors are used, and how [!DNL Target] generates a selector for an element.

>[!ENDSHADEBOX]

An element selector is a CSS expression that can identify one or more elements. Basic information about CSS selectors is available in the [Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) document on the *[!DNL Mozilla Developer Network]* (MDN).

Whether to use element classes or element IDs is set in the account preferences. Click **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**, then choose the preferred CSS selectors:

* **[!UICONTROL Use element IDs]**: Disable if the same ID is used for multiple elements, or if element IDs might change on page load.
* **[!UICONTROL Use element classes]**: Disable if element classes on a page might change.
* **[!UICONTROL Use preferred selectors]**: Enable to use unique selectors in the VEC to identify key areas of the website.

>[!NOTE]
>
>Element classes are available as selectors in **[!UICONTROL A/B Test]**, **[!UICONTROL Automated Personalization]**, and **[!UICONTROL Multivariate Test]** activities.

For information about when to use CSS selectors and when to use unique IDs, see [Visual Experience Composer best practices and limitations](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#vec-best-practices).

## How [!DNL Target] generates a selector for an element {#generate-selector}

[!DNL Target] uses a simple algorithm to create a selector. The generation logic is as follows:

1. If an element has an ID, for example `id="container"`, the selector for the element is `#container`.

   For example:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- Selector is computed for this element -->
       <ul class="navigation">
         <li class="item active"> Home </li>
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   
   ```

1. If an element contains a class attribute, [!DNL Target] attempts to use the first class of any classes present on the element.

   [!DNL Target] attempts to parse the parent element until it finds the `<HTML>` element or an element with an ID. Whenever an element contains an ID and the selector is computed on its descendant child, the ID of this element contributes to the selector.

   For example:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li class="item active"> Home </li> <!-- Selector is computed for this element -->
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   ```

   In this example, the selector is `#container` > `ul.navigation:eq(0)` > `li.item:eq(0)` (" > " indicates the immediate child).

   `eq` gives the index of the element that has "tagName=UL" and the first class `navigation`. Therefore, `index` is 0. See the [Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) article in MDN for more information.

1. If an element does not contain a class, [!DNL Target] uses `tagName` for the element and traverses up the parent element until either the `<HTML>` element or an element with an ID is found.

   For example:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li> Home </li>
         <li> Men </li>
         <li class="active"> Women </li>
         <li> Kids </li><!-- Selector is computed for this element -->
       </ul>
     </div>
   </div>
   ```

   The selector is `#container` > `ul.navigation:eq(0)` > `li:nth-of-type(4)`.

In this process:

* Any CSS selector can be used, as long as it uniquely identifies an element in the DOM.
* The approach above is the one used by [!DNL Target]. [!DNL Target] does not mandate this approach. Any selector can be added, as long as it uniquely identifies the element.
* Any attribute can be used in the selector. This article uses only a class name as an example.
