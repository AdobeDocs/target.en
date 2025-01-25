---
keywords: Experience Targeting;xt;activity url;url
description: Learn how to specify the [!UICONTROL Activity URL] that determines the page that is used in the test and that opens when the [!UICONTROL Experience Targeting] activity is designed using [!DNL Adobe Target].
title: What Is the [!UICONTROL Activity URL] In an [!UICONTROL Experience Targeting] (XT) Activity?
feature: Experience Targeting
hide: yes
hidefromtoc: yes
exl-id: 9926e4e0-728d-4375-b639-d26f067ed854
---
# Activity URL in [!UICONTROL Experience Targeting] (XT) activities

The [!UICONTROL Activity URL] determines the page that is used in an [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activity. This is the page that opens in the [!UICONTROL Visual Experience Composer] (VEC) or [!UICONTROL Form-Based Experience Composer] when the activity is designed.

1. When prompted while [creating an XT activity](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), specify the activity URL. Type the complete URL (including `https://`), then click **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >[!DNL Target] does not differentiate between URL protocols ( [!DNL https] and [!DNL http]). As a result, [!DNL `https://www.adobe.com`] and [!DNL `http://www.adobe.com`] both match.
   >
   >By default, the VEC or [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) opens the page that is specified in your [Visual Experience Composer settings](/help/main/administrating-target/visual-experience-composer-set-up.md). You can specify a different page during activity creation.
   >
   >If you specify a URL for a site that does not include a [[!DNL Target] at.js JavaScript library or [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank}, you cannot select page elements.

1. (Conditional) To display a different page after the VEC opens, click **[!UICONTROL Configure]**, select **[!UICONTROL Page Delivery]**, then specify the URL in the [!UICONTROL URL] field.

   >[!NOTE]
   >
   >If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.

1. (Conditional) Click **[!UICONTROL Add Rule]** to add more pages or sections to the activity.

   Additional rules can be based on any of the following:

   * URL 
   * Domain 
   * Path 
   * Hash (#) Fragment 
   * Query 
   * mbox Parameter

   Additional rules can be joined to the Activity URL with AND or OR. All rules you add are evaluated against each other with AND.

1. Click **[!UICONTROL Save]** when you have finished.
