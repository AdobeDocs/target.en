---
keywords: Multivariate Tests;activity url
description: Learn how to specify the activity URL that determines the page that is used in the test and that opens when the [!UICONTROL Multivariate Test] activity is designed using [!DNL Adobe Target].
title: What Is the Activity URL In a [!UICONTROL Multivariate Test] (MVT) Activity?
feature: Multivariate Tests
hide: yes
hidefromtoc: yes
---
# Activity URL

The activity URL determines the page that is used in the [!UICONTROL Multivariate Test] (MVT), and that opens when the test is designed in [!DNL Adobe Target].

1. When prompted during [activity creation](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specify the activity URL. Type the complete URL (including `https://`), then click **[!UICONTROL Create]**.

   >[!NOTE]
   >
   >[!DNL Target] does not differentiate between URL protocols ( [!DNL https] and [!DNL http]). As a result, [!DNL `https://www.adobe.com`] and [!DNL `http://www.adobe.com`] both match.

   By default, the [!UICONTROL Visual Experience Composer] (VEC) opens the page that is specified in your [Visual Experience Composer settings](/help/main/administrating-target/visual-experience-composer-set-up.md). You can specify a different page during activity creation.

1. (Conditional) To display a different page after the VEC opens, click the **[!UICONTROL Configure]** icon, then select **[!UICONTROL Page Delivery]**, then specify the URL.

1. (Conditional) Click **[!UICONTROL Add Rule]** to add more pages or sections to the activity.

   Additional rules can be based on any of the following:

   * [!UICONTROL  URL] 
   * [!UICONTROL Domain] 
   * [!UICONTROL Path] 
   * [!UICONTROL Hash (#) Fragment] 
   * [!UICONTROL Query] 
   * [!UICONTROL Custom]

   Additional rules can be joined to the activity URL with AND or OR. All rules that you add are evaluated against each other with AND.

   Click **[!UICONTROL Save]** when you have finished.

>[!NOTE]
>
>If you entered a URL for a site that does not include the [!DNL Target] JavaScript code, you cannot select page elements.
>
>By default, the VEC does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL Render using JavaScript]** if you want to be able to alter those elements using the [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.
