---
keywords: multi-page;journey testing;multipage activity
description: Learn how to create a multipage activity in Adobe [!DNL Target] lets you create a story over multiple pages, with a design that is specific to each page.
title: How Do I Create a Multipage Activity?
feature: Visual Experience Composer (VEC)
exl-id: d000cc73-4729-4ce0-ab30-756dd3ca8545
TQID: 'https://experienceleague.adobe.com/ZFqgbNp-sLF-ahG-uXKvWY0XPcxO0oZScGkpNX8hDHY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
    internal-label: Mobile experience
---
# Multipage activity {#multipage-activity}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use a multipage activity to create a story over multiple pages, with a design that is specific to each page.

>[!ENDSHADEBOX]

A multipage activity in [!DNL Adobe Target] creates a story over multiple pages, with a design that is specific to each page.

For example, an offer for free shipping with purchases above a certain amount can be tested. The offer can appear on the landing page, a category page, and certain product pages, with a different size and in a different location on each page type. A prominent offer can be displayed on the home page, then reinforced with smaller offers on other relevant pages.

A multipage activity can also define different layouts for desktop and non-responsive mobile sites. If the site has a separate mobile site such as [!DNL m.mysite.com] instead of [!DNL `www.mysite.com`], create a multipage activity, add [!DNL m.mysite.com] as separate pages, then apply mobile editing to make appropriate changes on the desktop version and the mobile version in the same experience. For responsive mobile sites, use [mobile experience editing](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

>[!NOTE]
>
>Multipage activities are designed for activities where the same offer has a different appearance on multiple pages. If the offer appears the same on all pages, a [template test](/help/main/c-experiences/c-visual-experience-composer/temtest.md#similar-pages) is more efficient.

Template rules can be specified for each page in the multipage test. For example, a multipage test can run across the home page and all category pages by applying template rules to the category page in the multipage test. See [Include the same experience on similar pages](/help/main/c-experiences/c-visual-experience-composer/temtest.md#similar-pages).

## Add pages to an activity {#add-pages}

Each page added to the activity can have its own design of the offer.

1. Click the **[!UICONTROL Configure]** icon ( ![Configure icon](/help/main/assets/icons/Setting.svg) ).

1. Click **[!UICONTROL Add Additional Pages]**.

   A **[!UICONTROL Pages]** pane displays on the left of the screen.

    ![Configure icon](assets/vec_edit_4.png)

1. Specify the pages and set the default page.

   Click **[!UICONTROL Add Page]** ( ![Add icon](/help/main/assets/icons/Add.svg) ) to add an additional page, specify the page name and URL, then click **[!UICONTROL Save]**.

1. Use the [!UICONTROL Visual Experience Composer] to design the way the offer looks on each page. 
