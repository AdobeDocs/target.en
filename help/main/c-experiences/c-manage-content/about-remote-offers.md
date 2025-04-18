---
keywords: remote offer;cached content;dynamic content;url type
description: Discover how to leverage remote offers in [!DNL Target] to host external content from a CMS or other systems.
title: How Do I Create Remote Offers?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
---
# Create remote offers

Use remote offers to host content outside of [!DNL Adobe Target], allowing [!DNL Target] to reference and deliver this content to user websites. This content can reside in a content management system (CMS) or another system for ease of use or security reasons.

Remote offers can be created on the [!UICONTROL Offers] > [!UICONTROL Code Offers] page or in the [Forms-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md). You cannot create or apply remote offers in the [!UICONTROL Visual Experience Composer] (VEC). Content is injected in the [!DNL Target] request locations, so these locations are most likely not appropriate for a global [!DNL Target] request.

Some examples of remote offers include:

* Different versions of your cross-sells
* Dynamic shopping cart messages
* Forms
* Calculators
* Interest rate updates
* Emails
* Kiosks
* Voice assistants

## Best practices for using remote offers {#section_7718512D08E14121B6F6B8C38134F4BC}

Best practices for using remote offers in your activities:

* If your offer resides in the same domain as the [!DNL Target] requests, using the [!UICONTROL Cached] option lets you use relative URLs in describing your offer location.

  This means that when you move your activity from your staging servers to production, the content is automatically accessible without having to change the URL manually.

* If your test involves data dynamically generated by your server, the [!UICONTROL Dynamic] option might be the right choice. 
* If you plan to test only the appearance of your existing remote offer content, use the [!UICONTROL Visual Experience Composer] to change the look and feel of the content that is returned from the content management system. 
* Use the [Remote Offer Selection Matrix](#reference_B23BEDD29DDD47709A7651AFD27E776B) (below) to help you choose the offer best suited for your specific case. Consult your account representative if you have questions.

## Create a remote offer from the [!UICONTROL Code Offers] page

1. Click **[!UICONTROL Offers]**, then select the **[!UICONTROL Code Offers]** tab.

1. Click **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. In the [!UICONTROL Create Remote Offer] dialog, provide a descriptive name for the offer.

   A descriptive name helps you and others quickly find the offer in the [!UICONTROL Offers] library.

1. (Conditional) If you have a [Target Premium account](/help/main/c-intro/intro.md#premium), select the desired [workspace](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Specify the redirect URL type.

   See [Redirect URL Type: [!UICONTROL Onsite Cached] or [!UICONTROL Onsite Dynamic]](#url-type) below for more information.

1. Specify the absolute remote URL for the remote offer.

1. Click **[!UICONTROL Create]**.

## Create a remote offer using the [!UICONTROL Form-Based Experience Composer]

1. While creating an activity using the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md), select the location to display the **[!UICONTROL Content]** section.
1. Click the **[!UICONTROL Content]** drop-down list, click the **[!UICONTROL List]** icon ( ![List](/help/main/assets/icons/MoreSmallList.svg) ), then click **[!UICONTROL Change Remote Offer]**.

1. Click **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Provide a descriptive name for the offer.

   A descriptive name helps you and others quickly find the offer in the [!UICONTROL Assets] library.

1. (Conditional) If you have a [Target Premium account](/help/main/c-intro/intro.md#premium), select the desired [workspace](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Specify the redirect URL type.

   See [Redirect URL Type: [!UICONTROL Onsite Cached] or [!UICONTROL Onsite Dynamic]](#url-type) below for more information.

1. Specify the remote URL for the remote offer.

1. Click **[!UICONTROL Create]**.

## Redirect URL Type: [!UICONTROL Onsite Cached] or [!UICONTROL Onsite Dynamic] {#url-type}

The following information helps you understand the differences between the two options:

### [!UICONTROL Onsite Cached] URL

The content for a cached remote offer is served from [!DNL Target].

Every two hours, [!DNL Target] fetches the content at the remote URL and then stores the content inside [!DNL Target]. When visitors load a site with an experience that includes a remote offer, [!DNL Target] delivers the offer.

Cached remote offers provide enhanced security because somebody logged in to [!DNL Target] cannot change the content. To change the content, someone would need to log in to the content management or other system, and change the content there.

You can specify an absolute or relative URL for a cached remote offer.

### [!UICONTROL Onsite Dynamic] URL

A dynamic remote offer is served from the content management or other system rather than from [!DNL Target].

You might not want the content periodically cached and then delivered by [!DNL Target] whenever visitors load a site with an experience that includes a remote offer. Instead, you want to call the system that is hosting the content, possibly pass in specific information so that the returned offer can be dynamic (or different) for each user. For example, if a user logs in to a website for a credit card that includes an experience with a dynamic remote offer, you could pass parameters into the URL for the user's account information. Then the website could provide user-specific information, such as account balance.

You can click **[!UICONTROL Add Parameter]** to add one or more [!DNL Target] requests or request parameters.

## Use remote offers in activities

Apply remote offers using the [!UICONTROL Form-Based Experience Composer]. You cannot currently apply remote offers using the [!UICONTROL Visual Experience Composer] (VEC).

The [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is a non-visual experience and offer creation interface that's useful in creating experiences for use in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP), and [!UICONTROL Recommendations] activities when the [!UICONTROL Visual Experience Composer] is not available or practical for use. For example, you might use the [!UICONTROL Form-Based Experience Composer] to create experiences that use remote offers.

1. Create or edit an activity in the [!UICONTROL Form-Based Experience Composer].

   See [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) for detailed step-by-step instructions.

1. Specify the desired location and add any audience refinements as necessary.

1. Click the **[!UICONTROL Content]** drop-down list, click the **[!UICONTROL List]** icon ( ![List](/help/main/assets/icons/MoreSmallList.svg) ), then click **[!UICONTROL Change Remote Offer]**.

1. Select the desired remote offer from the [!UICONTROL Change Remote Offer] dialog box, then click **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Finish configuring the activity.

## How dynamic remote offers work {#concept_CC2A969420B34364A9FA78C1CE251818}

Dynamic remote offers use your dynamic page technology to pass values to the offer.

The offer is executed after you render the page. An invisible iFrame gathers the data, copies it out of the frame, and inserts in on the page, loading your passed values.

![remote_offer_howitworks_2 image](assets/remote_offer_howitworks_2.jpeg)

1. The visitor's browser requests a page from your server.

2. Browser renders page, including mboxes.

3. `mboxCreate` call includes parameters necessary to render dynamic content.

4. [!DNL Target] returns a URL with the location of dynamic content and its parameters. Sets an iFrame in the mbox area.

5. The browser requests the URL and renders in page.

## Remote offer selection matrix {#reference_B23BEDD29DDD47709A7651AFD27E776B}

The remote offer selection matrix helps you decide which type of remote offer to choose: [!UICONTROL Onsite Cached] or [!UICONTROL Onsite Dynamic].

| Feature | Onsite Cached | Onsite Dynamic |
|--- |--- |--- |
|Updates each time a visitor makes a request|No|Yes|
|Content updates|Cached every two hours|Updated immediately upon each request|
|Load time|Faster|Slower due to request processing|
|Can see JavaScript on page|Yes|No, but can pass via URL|
|Offers can include JavaScript|Yes|Yes|
|Offer URL|Absolute or Relative|Relative|
|Requesting computer|Adobe servers|The visitor's computer, which carries the visitor's cookies|
