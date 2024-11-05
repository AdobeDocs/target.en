---
keywords: redirect offer;create redirect offer;add html offer;Pass all URL parameters in redirect
description: Learn how to create redirect offers to seamlessly guide browsers to new pages.
title: How Do I Create Redirect Offers?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
hide: yes
hidefromtoc: yes
exl-id: 751a8d97-2e35-4527-99f3-d7a42c104fcb
---
# Create redirect offers

Learn how to create redirect offers to seamlessly guide browsers to new pages. 

>[!NOTE]
>
>This article contains information about updates to the [!DNL Target] user interface that is currently part of a Beta program. The [!DNL Adobe Target] team often enables new features for select customers for testing and feedback purposes. After the testing period completes, these features are enabled for all customers in future [!DNL Target] releases and announced in [release notes](/help/main/r-release-notes/release-notes.md).

You might have two completely different pages to test instead of just changing pieces of content within a page. In this case, your A/B test compares page A vs. page B. Set up an [!UICONTROL A/B Test] activity with two experiences: one pointing to the default page A, and the other redirecting to page B. The offer is configured to redirect the visitor to a different page.

>[!NOTE]
>
> * Redirect offers can be created on the [!UICONTROL Offers] > [!UICONTROL Code Offers] page or in the [Forms-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md). You cannot create or apply redirect offers in the [!UICONTROL Visual Experience Composer] (VEC). Content is injected in the [!DNL Target] request locations, so these locations are most likely not appropriate for a global [!DNL Target] request.
>
>* You cannot use redirect offers in AJAX mboxes (`mboxUpdate`).
>
>* For redirect offers in activities using [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), your implementation must meet certain minimum requirements. In addition, there is important information that you need to know. See [Redirect Offers - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* For information about setting up an experience that redirects, see [Redirect to a URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

The redirect offer executes JavaScript code to redirect the browser. It uses the `window.location.replace();` method, so the page the visitor is redirected from is not stored in the browser history. This process allows visitors to use the back button in their browsers.

>[!NOTE]
>
>If you want to pass the referrer value of the landing page, use an HTML offer rather than a redirect offer.

## Create a redirect offer from the [!UICONTROL Code Offers] page

1. Click **[!UICONTROL Offers]**, then select the **[!UICONTROL Code Offers]** tab.
1. Click **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Provide a descriptive name for the offer.

   A descriptive name helps you and others quickly find the offer in the [!UICONTROL Assets] library.

1. (Conditional) If you have a [Target Premium account](/help/main/c-intro/intro.md#premium), select the desired [workspace](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Specify the URL for the unique content or destination that you want to redirect to. This URL must be an absolute URL.

   >[!NOTE]
   >
   >Redirect offers result in an infinite loop if the redirect URL also qualifies the user for the same activity. Ensure that the user does not re-qualify for the activity after being redirected.

1. Select the desired options to customize your redirect offer:

   * **[!UICONTROL Include all URL parameters]:** Enable this option if you want all the URL parameters present on the previous page to be propagated to the redirected page.

      For example, you want to redirect people directly from a men's page to a men's shirts category page. You also want the dynamic parameters in the URL to be passed because this method is how you track if people reached your site via email, banner ad, search ad, or organically. By enabling this option, your redirect offer on page `https://www.mycompany.com/mens.html?emailId=123` automatically becomes `https://www.mycompany.com/mensShirts.html?emailId=123` when all you entered in the URL box was `https://www.mycompany.com/mensShirts.html`. 

   * **[!UICONTROL Pass mbox session ID]:** Required to redirect to a different domain. Slide the toggle to enable this option if you want the `sessionId` to be automatically included in the redirect. This option is required only when you are testing clicks from an email or clicks from one domain to another. The `sessionId` matches the visitor's cookie so the visitor can continue to be tracked and the proper content is shown.

      If you use the 1st- & 3rd-party cookie setup, you do not need to pass the mbox session ID when crossing domains. It is persistent on the 3rd-party cookie, so it is not necessary in the URL.

1. Click **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Ask your implementation consultant before launching these tests.

## Create a redirect offer using the [!UICONTROL Form-Based Experience Composer]

1. While creating an activity using the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md), select the location to display the **[!UICONTROL Content]** section.
1. Click the **[!UICONTROL Content]** drop-down list, click the **[!UICONTROL List]** icon ( ![List](/help/main/assets/icons/MoreSmallList.svg) ), then click **[!UICONTROL Change Redirect Offer]**.
1. Click **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Provide a descriptive name for the offer.

   A descriptive name helps you and others quickly find the offer in the [!UICONTROL Assets] library.

1. Specify the URL for the unique content or destination that you want to redirect to. This URL must be an absolute URL.

   >[!NOTE]
   >
   >Redirect offers result in an infinite loop if the redirect URL also qualifies the user for the same activity. Ensure that the user does not re-qualify for the activity after being redirected.

1. Select the desired options to customize your redirect offer:

   * **[!UICONTROL Include all URL parameters]:** Slide the toggle to enable this option if you want all the URL parameters present on the previous page to be propagated to the redirected page.

      For example, you want to redirect people directly from a men's page to a men's shirts category page. You also want the dynamic parameters in the URL to be passed because this method is how you track if people reached your site via email, banner ad, search ad, or organically. By enabling this option, your redirect offer on page `https://www.mycompany.com/mens.html?emailId=123` automatically becomes `https://www.mycompany.com/mensShirts.html?emailId=123` when all you entered in the URL box was `https://www.mycompany.com/mensShirts.html`. 

   * **[!UICONTROL Pass mbox session ID]:** Required to redirect to a different domain. Slide the toggle to enable this option if you want the `sessionId` to be automatically included in the redirect. This option is required only when you are testing clicks from an email or clicks from one domain to another. The `sessionId` matches the visitor's cookie so the visitor can continue to be tracked and the proper content is shown.

      If you use the 1st- & 3rd-party cookie setup, you do not need to pass the mbox session ID when crossing domains. It is persistent on the 3rd-party cookie, so it is not necessary in the URL.

1. Click **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Ask your implementation consultant before launching these tests.

## Use redirect offers in activities

Apply redirect offers using the [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md). You cannot currently apply redirect offers using the [!UICONTROL Visual Experience Composer] (VEC).

The [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is a non-visual experience and offer creation interface that's useful in creating experiences for use in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP), and [!UICONTROL Recommendations] activities when the [!UICONTROL Visual Experience Composer] is not available or practical for use. For example, you might use the [!UICONTROL Form-Based Experience Composer] to create experiences that use redirect offers.

1. Create or edit an activity in the [!UICONTROL Form-Based Experience Composer].

   See [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) for detailed step-by-step instructions.

1. Specify the desired location and add any audience refinements as necessary.

1. Click the **[!UICONTROL Content]** drop-down list, click the **[!UICONTROL List]** icon ( ![List](/help/main/assets/icons/MoreSmallList.svg) ), then click **[!UICONTROL Change Redirect Offer]**.
1. Select the desired redirect offer from the [!UICONTROL Select Redirect Offer] dialog box, then click **[!UICONTROL Add]**.
1. Finish configuring the activity.
