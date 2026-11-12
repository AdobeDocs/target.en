---
keywords: activity url;url;different url
description: Discover how to set the [!UICONTROL Activity URL] in an A/B, Experience Targeting, or Multivariate Test activity to define test pages and to ensure accurate test design.
title: What Is the Activity URL in an A/B, Experience Targeting, or Multivariate Test Activity?
feature: A/B Tests
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
reason: republish
TQID: 'https://experienceleague.adobe.com/arQWsSfBKYtrayq9AI8ejU1T-Uor-oL5j2Sp2JKKXZE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Activity URL {#ab-activity-url}

>[!BEGINSHADEBOX]

**On this page:** Learn how to specify the activity URL of an A/B, Experience Targeting (XT), or Multivariate Test (MVT) activity, how to display a different page, and how to add rules for more pages or sections.

>[!ENDSHADEBOX]

The [!UICONTROL Activity URL] determines the page that is used in the activity. This is the page that opens in the [!UICONTROL Visual Experience Composer] (VEC) or in the [!UICONTROL Form-Based Experience Composer] when the activity is designed in [!DNL Adobe Target].

## Specify the activity URL {#specify-url}

When prompted during activity creation, specify the activity URL. Type the complete URL (including `https://`), then click **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] does not differentiate between URL protocols ([!DNL https] and [!DNL http]). As a result, [!DNL `http://www.adobe.com`] and [!DNL `https://www.adobe.com`] both match.

If you specify a URL for a site that does not include the [!DNL Target] [at.js JavaScript library or [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank}, you cannot select page elements.

## Display a different page {#different-page}

By default, the VEC or the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) opens the page that is specified in your [Visual Experience Composer settings](/help/main/administrating-target/visual-experience-composer-set-up.md). You can specify a different page during activity creation.

To display a different page after the VEC opens:

1. On the **[!UICONTROL Experiences]** page, click **[!UICONTROL Configure]** at the top of the page, then select **[!UICONTROL Page Delivery]**.

1. Specify the URL in the **[!UICONTROL URL]** field.

1. Click **[!UICONTROL Save]** when you have finished.

By default, the VEC does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL Render using JavaScript]** if you want to be able to alter those elements using the VEC.

>[!NOTE]
>
>If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.

## Add rules for more pages or sections {#add-rules}

To add more pages or sections to the activity, click **[!UICONTROL Add Rule]** in the **[!UICONTROL Page Delivery]** settings, then click **[!UICONTROL Save]** when you have finished.

Additional rules can be based on any of the following:

* URL
* Domain
* Path
* Hash (#) Fragment
* Query
* mbox Parameter
* Custom

Additional rules can be joined to the activity URL with AND or OR. All rules you add are evaluated against each other with AND.
