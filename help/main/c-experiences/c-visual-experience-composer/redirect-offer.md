---
keywords: redirect;redirect url;send to different page
description: Learn how to use the Redirect to URL option in Adobe [!DNL Target] when you want to send the visitor to a different page rather than showing content on the same page.
title: Can I Redirect a Page to a Different URL?
feature: Visual Experience Composer (VEC)
exl-id: bd448482-0079-4689-aa24-65ecbb31b8ae
TQID: 'https://experienceleague.adobe.com/8Bh5z7SRWw3QqKQMHZck01GKVBtMufwLbw9JxLsSACU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Redirect to a URL {#redirect-to-url}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use the **[!UICONTROL Redirect to URL]** option to send visitors to a different page instead of showing content on the same page.

>[!ENDSHADEBOX]

The **[!UICONTROL Redirect to URL]** option in [!DNL Adobe Target] sends a visitor to a different page instead of showing content on the same page. It suits the comparison of two completely different pages, as opposed to changes to pieces of content within one page. An A/B test then compares page A with page B: one experience points to the default page A, and the other redirects to page B.

A redirect offer runs JavaScript code that redirects the browser. The code uses the `window.location.replace();` method, so the page that the visitor is redirected from is not stored in the browser history. The visitor can therefore still use the back button of the browser.

## Create a redirect offer {#create-redirect-offer}

The experience that redirects defines the page to which visitors are sent and, optionally, the conditions of the redirect.

1. Create an experience.

1. From the **[!UICONTROL Experiences]** frame, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallList.svg) ) for the experience that redirects.

1. Click **[!UICONTROL Redirect to URL]**.

    ![More Actions icon](assets/redirect_1.png)
  
1. In the **[!UICONTROL Redirect to URL]** dialog box, enter the URL of page B.

    ![More Actions icon](assets/redirect_2.png)

1. (Optional) Select the option to include the current query parameters.

   When this option is selected, everything after the `?` in the URL of the visitor is appended to the redirect URL at the time of the redirect.

## Limitations

Redirect offers have the following limitations:

* **A4T:** a redirect offer in an activity that uses A4T requires an implementation that meets certain minimum requirements, and other important information applies. See [Redirect offers - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
* **Form-Based Experience Composer:** do not use a redirect offer in mboxes that are part of the page. Use a redirect offer only from a script tag that is part of the HTML `<head>`, and always use auto-create and set the redirect offer for the global mbox.

>[!NOTE]
>
>To pass the referrer value of the landing page, use an HTML offer instead of a redirect offer.

## Known issues

Redirect activities in at.js implementations might cause the preview URL to enter a loop, with the offer delivered repeatedly. Use [QA Mode](/help/main/c-activities/c-activity-qa/activity-qa.md) to preview and test the activity instead. This issue does not affect the actual delivery of the offer. (TGT-23019) 
