---
keywords: activity url;url;different url
description: Discover how to set the [!UICONTROL Activity URL] to define test pages and to ensure accurate test design.
title: What Is the Activity URL In an A/B Activity?
feature: A/B Tests
hide: yes
hidefromtoc: yes
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
---
# Activity URL

The activity URL determines the page that is used in the test and that opens when the test is designed using [!DNL Adobe Target].

When prompted during activity creation, specify the activity URL. Type the complete URL (including `https://`), then click **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] does not differentiate between URL protocols ( [!DNL https] and [!DNL http]). As a result, [!DNL `http://www.adobe.com`] and [!DNL `https://www.adobe.com`] both match.

## Specify a different URL

By default, the [!UICONTROL Visual Experience Composer] opens the page that is specified in your [Visual Experience Composer settings](/help/main/administrating-target/visual-experience-composer-set-up.md). You can specify a different page during activity creation.

1. (Conditional) To display a different page after the [!UICONTROL Visual Experience Composer] opens, on the **[!UICONTROL Experiences]** page, click  **[!UICONTROL Configure]** at the top of the page, then select **[!UICONTROL Page Delivery]**. 

1. Specify the URL in the **[!UICONTROL URL]** field.

1. (Conditional) Click **[!UICONTROL Add Rule]** to add more pages or sections to the activity.

   Additional rules can be based on any of the following:

   * URL 
   * Domain 
   * Path 
   * Hash (#) Fragment 
   * Query 
   * mbox Parameter
   * Custom

   Additional rules can be joined to the activity URL with AND or OR. All rules you add are evaluated against each other with AND.

1. Click **[!UICONTROL Save]** when you have finished.

<!-- If you entered a URL for a site that does not include the [!DNL Target]s JavaScript code, you cannot select page elements.

By default, the [!UICONTROL Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL Render using JavaScript]** if you want to be able to alter those elements using the [!UICONTROL Visual Experience Composer].-->

>[!NOTE]
>
>If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.
