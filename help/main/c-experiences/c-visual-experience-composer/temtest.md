---
keywords: template testing;template;same experience on similar pages;template test
description: Learn how to use the Adobe [!DNL Target] Visual Experience Composer (VEC) to include the same experience on multiple pages that are similarly structured or contain the same template elements.
title: Can I Include the Same Experience on Similar Pages?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
TQID: 'https://experienceleague.adobe.com/zk7U6g7gk7XkpWsEFQbwuCm7xbpIb1lCaZefxjn-39g'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: ef98a6e0-f26c-4870-9bd4-e6b72e9cc699
    internal-label: Experiences and offers
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
---
# Include the same experience on similar pages {#similar-pages}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use page delivery rules in the [!UICONTROL Visual Experience Composer] (VEC) to include the same experience on pages that have a similar structure.

>[!ENDSHADEBOX]

A page template in [!DNL Adobe Target] provides structure to pages. When pages contain similar elements, variations in those similarly structured page elements can be tested across multiple pages or across an entire domain.

To work correctly, this feature must be used on pages that have a similar structure or contain template elements that are structured the same on all pages.

>[!IMPORTANT]
>
>Using this feature to change elements across dissimilar pages likely causes unexpected results.

This feature can be used, for example, to do one of the following:

* Test a global navigation bar by rearranging or removing elements
* Remove an item from all product pages that use a particular page template
* Add a banner to all product pages
* Change the layout of the article template

## Specify the pages for an experience {#specify-pages}

The pages where an experience appears are specified with page delivery rules. The rules can include specific pages, or apply the change across the site or domain.

1. Create or edit an activity as described in [Activities](/help/main/c-activities/activities.md).

1. In the [!UICONTROL Visual Experience Composer] (VEC), click the **[!UICONTROL Configure]** icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ), then select **[!UICONTROL Page Delivery]**.

    ![Activities](assets/vec_edit_1.png)

1. Click **[!UICONTROL Add Rule]**, then specify the criteria for the pages to add the experience to.

1. Specify the page range: **[!UICONTROL URL]**, **[!UICONTROL Domain]**, **[!UICONTROL Path]**, **[!UICONTROL Hash (#) Fragment]** (the part of a URL that follows the # symbol), **[!UICONTROL Query]**, or **[!UICONTROL Custom]**.

   For more information about how [!DNL Target] evaluates URLs, see [Targets and audiences FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).

    ![Activities](assets/vec_edit_2.png)

1. Choose an operator. The operator specifies how the items after the operator relate to the page range.

1. Type the strings that define where the experience is added, such as the domain or the strings contained in the page name.

   For example, if **[!UICONTROL Domain]** and **[!UICONTROL Is (case sensitive)]** are selected, type the domain where the experience is added to all pages.

   Multiple items can be included. Multiple items use OR logic, meaning that any single item in the list makes the condition true.

1. (Optional) Click **[!UICONTROL Add Rule]** and repeat steps 3 to 6 to enter additional criteria.

   Multiple criteria are joined with AND logic. [!DNL Target] adds the experience to all pages that match the specified criteria.

>[!IMPORTANT]
>
>[!DNL Target] cannot check the pages to make sure they appear as expected, so it is always an important practice when using this feature to test the affected pages before making them public.

## Use cases {#use-cases}

Template rules can be used on a site in different ways, as the following use case shows.

### Render the same activity across the entire domain {#entire-domain}

Template rules can render the same activity across the entire domain, for example:

* To include a global header or footer
* To include a global banner (for example, COVID-19 announcements)
* To include a global free-shipping promo

1. Create or edit an activity as described in [Activities](/help/main/c-activities/activities.md).

1. To specify the domain where the experience appears, in the [!UICONTROL Visual Experience Composer] click the **[!UICONTROL Configure]** icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ), then select **[!UICONTROL Page Delivery]**.

1. Click **[!UICONTROL Add Rule]** > **[!UICONTROL Domain]**.

1. From the **[!UICONTROL Choose evaluator]** drop-down, select **[!UICONTROL Contains]**, then specify the domain.

    ![Activities](assets/vec_edit_3.png)
