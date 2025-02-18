---
keywords: optimization;personalization;adobe journey optimizer;ajo;use cases;scenarios;add content;hide content;add components;hide components
description: Learn how to add or hide components on your web page using [!DNL Adobe Journey Optimizer].
title: Add Or Hide Components To Your Web Page in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
feature: Integrations
hide: yes
hidefromtoc: yes
exl-id: 8c4fba88-908e-4742-ac4b-bdf7f4c882db
---
# Add or hide components to your web page

This use case helps you unlock the secrets to effective A/B testing content changes in [!DNL Adobe Journey Optimizer].

This use case demonstrates how to perform familiar tasks, such as A/B testing with an [A/B Test activity](/help/main/c-activities/t-test-ab/test-ab.md), using [!DNL Journey Optimizer] instead of [!DNL Adobe Target].

This use case is designed to demonstrate how to perform familiar tasks you might have performed using [!DNL Adobe Target], A/B testing using an [A/B Test activity](/help/main/c-activities/t-test-ab/test-ab.md), but using [!DNL Journey Optimizer].

## Benefits and value

* **Enhance user engagement**: Capture users' attention with an optimized page design that highlights relevant information, such as promotions.
* **Improve discoverability**: Strategically place new components or content on web or mobile apps to streamline actions and enhance navigation.
* **Increase additional touchpoints**: Effectively guide users towards conversion events and goals to accelerate business impact.

## Possible scenarios

* A financial services company plans to add a new tile on its homepage for quick access to the loan calculator, reducing search time and boosting loan applications.

* An apparel company increased conversions by adding a new call-to-action button on its web page.

## Steps

>[!NOTE]
>
>The instructions in this section highlight the necessary steps to change an image and to use profile attributes to personalize text messages. For more information about available options in the [!DNL Journey Optimizer] web designer, see [Work with the web designer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in the *Journey Optimizer documentation*. 
>
>The video at the bottom of the page is especially helpful.

Perform the following steps to add components or to hide components on your web page:

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

   ![Yoga landing page on the LUMA web site](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. To add a hide an element, click **[!UICONTROL Edit Web Page]** in the right rail.

1. Click the element you want to hide, then click the [!UICONTROL Hide] button in the right rail.

   The right rail displays option that you can perform on the selected element. These options vary, depending on the selected element.

   ![Hide element button](/help/main/c-integrating-target-with-mac/ajo/assets/hide-element.png)

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
>[Work with the web designer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in the *Journey Optimizer documentation*
>[Create a campaign](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Journey Optimizer Tutorials*
