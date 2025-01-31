---
keywords: template testing;template;same experience on similar pages;template test
description: Learn how to use the Adobe [!DNL Target] Visual Experience Composer (VEC) to include the same experience on multiple pages that are similarly structured or contain the same template elements.
title: Can I Include the Same Experience on Similar Pages?
feature: Experiences and Offers
hide: yes
hidefromtoc: yes
---
# Include the same experience on similar pages

Use a page template in [!DNL Adobe Target] to provide structure to your pages, or if your pages contain similar elements, to test variations in similarly structured page elements or across your entire domain.

To work correctly, this feature must be used on pages that have a similar structure or contain template elements that are structured the same on all pages.

>[!IMPORTANT]
>
>Using this feature to change elements across dissimilar pages likely causes unexpected results.

For example, you might use this feature to do one of the following:

* Test a global navigation bar by rearranging or removing elements 
* Remove an item from all product pages that use a particular page template 
* Add a banner to all product pages 
* Change the layout of the article template

You can specify pages that include the change elements, or apply the change across your site or domain. 

1. Create or edit an activity as described in [Activities](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. To specify the pages where the experience appears, in the [!UICONTROL Visual Experience Composer] (VEC) click the [!UICONTROL Configure] icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ), then select **[!UICONTROL Page Delivery]**.

1. Click **[!UICONTROL Add Rule]**, then specify the criteria for the pages you want to add the experience to.

1. Specify the page range. The page range can be one of the following:

    * [!UICONTROL URL] (For more information about how [!DNL Target] evaluates URLs, see [Targets and audiences FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
    * [!UICONTROL Domain]
    * [!UICONTROL Path]
    * [!UICONTROL Hash (#) Fragment] (target the part of a URL that follows the # symbol.) 
    * [!UICONTROL Query]
    * [!UICONTROL Custom]

1. Choose an operator.

   The operator specifies how the items after the operator relate to the page range. Available operators include:

    * [!UICONTROL Contains]
    * [!UICONTROL Does not contain]
    * [!UICONTROL Is (case sensitive)]
    * [!UICONTROL Is not]
    * [!UICONTROL Starts with]
    * [!UICONTROL Ends with]

1. Type the strings that define where the experience is added, such as the domain or the strings contained in the page name.

   For example, if you select **[!UICONTROL Domain]** and **[!UICONTROL Is (case sensitive)]**, type the domain where you want the experience added to all pages.

   You can include multiple items.

   >[!IMPORTANT]
   >
   >Multiple items use OR logic, meaning that any single item in the list makes the condition true.

1. If desired, enter additional criteria by clicking **[!UICONTROL Add Rule]** and repeating the procedure in the previous steps.

   Multiple criteria are joined with AND logic. [!DNL Target] adds the experience to all pages that match the specified criteria.

>[!IMPORTANT]
>
> [!DNL Target] cannot check the pages to make sure they appear as expected, so it is always an important practice when using this feature to test affected pages before making them public.

## Use cases

Review the following use cases for ways to use template rules on your site:

### Render the same activity across the entire domain

You might consider using template rules to render the same activity across your entire domain for the following use cases:

* To include a global header or footer
* To include a global banner (for example, COVID-19 announcements)
* To include a global free-shipping promo

1. Create or edit an activity as described in [Activities](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. To specify the domain where the experience appears, in the [!UICONTROL Visual Experience Composer] click the [!UICONTROL Configure] icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ), then select **[!UICONTROL Page Delivery]**.

1. Click **[!UICONTROL Add Rule]** > **[!UICONTROL Domain]**.

1. From the **[!UICONTROL Choose evaluator]** drop-down, select **[!UICONTROL Contains]**, then specify the domain.
