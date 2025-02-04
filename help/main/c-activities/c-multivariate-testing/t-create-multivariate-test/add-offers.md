---
keywords: mvt;multivariate test;offers;combinations
description: Learn how to use the [!UICONTROL Visual Experience Composer] (VEC) in Adobe [!DNL Target] to create the offers you want to include in your [!UICONTROL Multivariate Test] (MVT).
title: How Do I Create Combinations in a [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
---
# Create combinations

Use the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] to create the offers you want to include in your [!UICONTROL Multivariate Test] (MVT).

For more information about using the VEC to create and edit offers, see [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>You can click **[!UICONTROL Expand Selection]** when selecting objects on the page to select the parent element in addition to the originally selected element. When you select any parent element, all children of that element are automatically selected. You can expand the selection multiple times.
>
>You can also use the [DOM path](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) to navigate elements.

## Image Offers {#section_A48333211DB149ED926AE467D0032914}

Test multiple images offers within a location to determine which image is most successful.

1. Click an image on your page, and then select **[!UICONTROL Change Image Offer]**.

1. From the [!UICONTROL Image Offer] dialog box, select all images that you want to include in the test, then click **[!UICONTROL Add]**.

Each image becomes a separate experience in that location.

## HTML Offers {#section_DF016101AFA9412C9B99862C23DE77B1}

Test multiple HTML offers within a location to determine which offer is most successful.

1. Click an HTML offer on your page, then click **[!UICONTROL Change HTML Offer]**.

1. Click **[!UICONTROL Create Offer]**, click **[!UICONTROL HTML Offer]**, name the offer, type or paste the code for the HTML offer, then click **[!UICONTROL Create]**.

   Repeat for any additional HTML offers you want to include. 

1. Click **[!UICONTROL Save]**.

Each HTML offer becomes a separate experience in that location.

## Best Practices {#section_2E98C23D2F1A460FA732A31799CE6291}

* Don't include more locations than necessary for the test. Every experience you include in the test significantly increases the amount of traffic and time required to achieve acceptable results. For example, if you have page elements with three offers each, there are nine possible combinations (3x3). Three elements, where two contain three possible offers and one has two offers, provide 18 options (3x3x2). The numbers increase substantially with each additional element and offer. 
* When creating multivariate tests, you can exclude more than 10 percent of experiences from the test, provided you acknowledge the warning that you must then use offline reporting for analysis. 
* Take advantage of the preview features to avoid undesirable combinations of content. For example, you might have two images that offer different discounts on the same item or service. Showing both of these images on the same page is illogical and is likely to create confusion. 
* Use the [Traffic Estimator](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) to make sure that your test is designed for the amount of traffic your page receives. Make sure that the Traffic Estimator gives your test configuration the green light so you can get the results you desire. 
* You must have at least three elements to test. If you have fewer, run a series of A/B tests. 
* Each element's alternatives should be significantly different from each other. 
* Although not required, it is good practice for each element to have the same number of alternatives.
