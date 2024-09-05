---
keywords: optimization;personalization;adobe journey optimizer;ajo;use cases;scenarios;content change/ab test;profile attribute;change image;swap image
description: Unlock the Secrets to Effective A/B Testing Content Changes in Adobe Journey Optimizer
title: Content changes through A/B testing in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
feature: Integrations
hide: yes
hidefromtoc: yes
exl-id: e5aed7cd-7701-4133-ac7c-98e528c8a763
---
# Content changes through A/B testing in [!DNL Adobe Journey Optimizer]

This use case helps you unlock the secrets to effective A/B testing content changes in [!DNL Adobe Journey Optimizer].

This use case demonstrates how to perform familiar tasks, such as A/B testing with an [A/B Test activity](/help/main/c-activities/t-test-ab/test-ab.md), using [!DNL Journey Optimizer] instead of [!DNL Adobe Target].

This use case is designed to demonstrate how to perform familiar tasks you might have performed using [!DNL Adobe Target], A/B testing using an [A/B Test activity](/help/main/c-activities/t-test-ab/test-ab.md), but using [!DNL Journey Optimizer].

## Benefits and value

* **Optimize content effectiveness**: Discover which content variations and elements resonate most with your customers, leading to higher engagement and conversions.
* **Data-driven decisions**: Leverage data to make informed decisions across your content strategy, ensuring maximum impact.
* **Personalized user experience**: Tailor content to meet the unique preferences and needs of all your audience segments.

## Possible scenarios

* An apparel company increased conversions by testing various images and personalizing campaign landing pages with users' first names in the call-to-action text.

* An e-commerce company found that its gold loyalty members had higher conversion rates by testing various product descriptions and images on a campaign landing page, leading to increased sales.

## Steps

>[!NOTE]
>
>The instructions in this section highlight the necessary steps to change an image and to use profile attributes to personalize text messages. For more information about available options in the [!DNL Journey Optimizer] web designer, see [Edit web content](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} in the *Journey Optimizer documentation*. 
>
>The video at the bottom of the page is especially helpful.

Perform the following steps to optimize a web page by testing various images and personalizing messages with users' first names using a profile script:

1. In [!DNL Adobe Journey Optimizer], click **Campaigns** in the left rail to display the [!UICONTROL Campaigns] page.

   ![Adobe Journey Optimizer landing page with Campaigns tab highlighted.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Click **[!UICONTROL Create Campaign]** in the upper right corner of the [!UICONTROL Campaigns] page.

1. Select **[!UICONTROL Scheduled - Marketing]** (the default), then click **Create** to display the [!UICONTROL Campaign] details page.

   ![Campaign details page in Adobe Journey Optimizer](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. In the **[!UICONTROL Properties]** section, provide a descriptive name and optional description for the campaign.

1. (Conditional) In the **[!UICONTROL Audience]** section, click **[!UICONTROL Select Audience]** and choose the desired audience.

   For this use case, you can activate the campaign for [!UICONTROL All Visitors] (the default).

1. In the **[!UICONTROL Action]** section, choose **[!UICONTROL Web]** from the **[!UICONTROL Action]** drop-down list, then select or create a new web configuration.

   A web configuration, or channel surface, is a configuration defined by a system administrator. The web configuration contains all the technical parameters for sending the message, such as header parameter, subdomain, mobile apps, and so forth.

   For more information, see [Set up channel surfaces](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in the *Journey Optimizer documentation*.

1. In the **[!UICONTROL Action]** section, click **[!UICONTROL Edit Content]** to open your web site in the [!DNL Journey Optimizer] web designer.

   Two or more experiments are needed for A/B testing. You can use your existing home page as the first experiment. Subsequent steps explain how to set up a second experiment.

   ![Yoga landing page on the LUMA web site](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. To create an experiment to determine which content performs better, click **[!UICONTROL Create Experiment]**.

   Content experiments let you vary the message content, subject, or sender to define multiple treatments and to determine the best combination for your audiences. For more information, see [Create a content experiment](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} in the *Journey Optimizer documentation*.

1. Select a success metric and click action.

   Click the Help icons for more information and links to relevant articles.

1. Click **[!UICONTROL Add Treatment]**, then click **[!UICONTROL Create]**.

   For this use case, you can leave the distribution at 50% for each experiment.

1. On the [!UICONTROL Campaign] details page, under **[!UICONTROL Action]**, click **[!UICONTROL Edit Content]**.

1. Click Web under Treatment B

   For this use case, keep [!UICONTROL Treatment A] unchanged to use the original experience as the first experience in the A/B test.

1. Click **[!UICONTROL Edit Web Page]** in the right rail.

   ![Edit Content page on the Yoga landing page](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. To change the hero image, click the image that you want to change, then click the **[!UICONTROL Choose Image]** button.

   ![Choose image button](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Browse to and select the desired image, then click **[!UICONTROL Use This Image]**.

   ![New hero image on Yoga page](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. To personalize the message with users' first names using profile attributes, click the text that you want to personalize, then click **[!UICONTROL Add Personalization]** to display the [!UICONTROL Add Personalization] page.

   ![Add Personalization button.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   For more information about profile attributes, see [Get started with the personalization editor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in the *Journey Optimizer documentation*.

1. Search for and click the plus sign to add the "first name" profile attribute, adjust the text as desired, then click **[!UICONTROL Save]**.

   ![Add profile attribute for name](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   For more information, see [Get started with the personalization editor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in the *Journey Optimizer documentation*.

1. Click the back arrow in the upper left corner to return to the web designer.

   ![Back arrow](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Click **[!UICONTROL Review to Activate]**, ensure that everything looks as expected, then click **Activate**.

## View reports

Click the [!UICONTROL Reports] button, then click the desired reporting period:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

For more information, see [Get started with new Reporting interface](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} in the *Journey Optimizer documentation*.

>[!MORELIKETHIS]
>
>[Edit web content](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} in the *Journey Optimizer documentation*
>[How-to video](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content#video){target=_blank} in the *Journey Optimizer documentation*
>[Create a campaign](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Journey Optimizer Tutorials*
