---
keywords: optimization;personalization;adobe journey optimizer;ajo;use cases;scenarios;content change/ab test;profile attribute;change image;swap image
description: Unlock the Secrets to Effective A/B Testing Content Changes in Adobe Journey Optimizer
title: Content changes through A/B testing in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
feature: Integrations
hide: yes
hidefromtoc: yes
---
# Content changes through A/B testing in [!DNL Adobe Journey Optimizer]

This use case helps you unlock the secrets to effective A/B testing content changes in [!DNL Adobe Journey Optimizer].

## Scenario

An apparel company increased conversions by testing various images and personalizing campaign landing pages with users' first names from their profile attributes.

## Benefits and value

* **Optimize content effectiveness**: Discover which content variations and elements resonate most with your customers, leading to higher engagement and conversions.
* **Data-driven decisions**: Leverage data to make informed decisions across your content strategy, ensuring maximum impact.
* **Personalized user experience**: Tailor content to meet the unique preferences and needs of all your audience segments.

## Step-by-step instructions

Perform the following steps to optimize a web page by testing various images and personalizing messages with users' first names:

1. In [!DNL Adobe Journey Optimizer], click **Campaigns** in the left rail to display the [!UICONTROL Campaigns] page.

   ![Adobe Journey Optimizer landing page with Campaigns tab highlighted.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Click **[!UICONTROL Create Campaign]** in the upper right corner of the [!UICONTROL Campaigns] page.

1. Select **[!UICONTROL Scheduled - Marketing]** (the default), then click **Create** to display the [!UICONTROL Campaign] details page.

   ![Campaign details page in Adobe Journey Optimizer](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. Provide a descriptive name and optional description for the campaign.

1. (Conditional) Click **[!UICONTROL Select Audience]** and choose the desired audiences.

   For this use case, we chose to activate the campaign for all visitors (the default).

1. Choose **[!UICONTROL Web]** from the **[!UICONTROL Action]** drop-down list, then select or create a new web configuration.

   A web configuration, or channel surface, is a configuration that has been defined by a System Administrator. The web configuration contains all the technical parameters for sending the message, such as header parameter, subdomain, mobile apps, and so forth.

   For more information, see [Set up channel surfaces](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in the *Journey Optimizer documentation*.

1. Click **[!UICONTROL Edit Content]** to open your web site in the [!DNL Journey Optimizer] web designer.

   ![Yoga landing page on the LUMA web site](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Click **[!UICONTROL Edit Web Page]** in the right rail.

   ![Edit Content page on the Yoga landing page](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. To change the hero image, click the image that you want to change, then click the **[!UICONTROL Choose Image]** button.

   ![Choose image button](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Browse to and select the desired image, then click **[!UICONTROL Use This Image]**.

   ![New hero image on Yoga page](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. To personalize the message with users' first names using profile attributes, click the text that you want to personalize, then click **[!UICONTROL Add Personalization]** to display the [!UICONTROL Add Personalization] page.

   ![Add Personalization button.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

1. Search for and select the "first name" profile attribute, adjust the text as desired, then click **[!UICONTROL Save]**.

   ![Add profile attribute for name](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   For more information, see [Get started with the personalization editor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in the *Journey Optimizer documentation*.

1. Click the back arrow in the upper left corner to return to the web designer.

   ![Back arrow](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Click **[!UICONTROL Review to Activate]**, ensure that everything looks as expected, then click **Activate**.

>[!MORELIKETHIS]
>
>[Edit web content](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} in the *Journey Optimizer documentation*
>[How-to video](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/web-spa#video){target=_blank} in the *Journey Optimizer documentation*
>[Create a campaign](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Journey Optimizer Tutorials*

