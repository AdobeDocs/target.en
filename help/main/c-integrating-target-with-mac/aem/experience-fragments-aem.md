---
keywords: experience;json;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
description: Learn how to use [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] in [!DNL Adobe Target] activities.
title: How Do I Use [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments]?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
---
# AEM [!UICONTROL Experience Fragments]

Use [!UICONTROL Experience Fragments] (XFs) created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization and personalization.

## Considerations

Consider the following as you work with AEM [!UICONTROL Experience Fragments] in [!DNL Target]:

* This feature requires that you are an [!DNL Adobe Experience Manager] (AEM) customer. For more information, see [Requirements](#section_AE6F0971E1574B3AA324003599B96E5A) below.
* [!UICONTROL Experience Fragments] and [!UICONTROL Content Fragments] are available for the following activity types: 

  * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
  * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
  * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
  * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
  * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)
  
* [!UICONTROL Experience Fragments] and [!UICONTROL Content Fragments] are not available for the following activity types:
  
  * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
  * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* You can consume [!UICONTROL Experience Fragments] in [!DNL Target] activities using the [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) and the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

To learn more about AEM [!UICONTROL Experience Fragments] and [!UICONTROL Content Fragments], see [AEM [!UICONTROL Experience Fragments] and Content Fragments overview](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requirements {#requirements}

You must be provisioned with the [!UICONTROL Experience Fragments] functionality within [!DNL Target]. In addition, you must be using [!DNL AEM] as a Cloud Service or [!DNL AEM] 6.4 (or later). Your account representative can help ensure that you meet the requirements to use this feature:

* [!DNL Adobe Experience Manager ] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4 
* [!DNL Adobe Target Standard] or [!DNL Adobe Target Premium] account 

[!DNL Adobe Experience Manager] 6.3 and 6.4 have reached end-of-life and are no longer supported (except for customers who purchased extended support).

Contact [Adobe Target Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to enable the integration and to provide you with authentication details.

## Creating and configuring [!UICONTROL Experience Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

To use [!DNL AEM] [!UICONTROL Experience Fragments] in [!DNL Target], you must perform the following steps:

### Step 1: Integrate [!DNL AEM] with [!DNL Target]

For more information, see:

* **AEM as a Cloud Service**: [Integrating with Adobe Target](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target){target=_blank} in the *Experience Manager as a Cloud Service* guide. 
* **Adobe Developer**: [Integration with Adobe Target using Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-target-ims-adobe-io.html){target=_blank} in the *Administering User Guide* documentation.
* **[!DNL AEM] 6.5**: [Opting into Adobe Analytics and Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=en){target=_blank} in the *Adobe Experience Manager 6.5* documentation.
* **[!DNL AEM] 6.4**: [Opting into Adobe Analytics and Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html){target=_blank} in the *Adobe Experience Manager 6.4* documentation.

### Step 2: Create the Experience Fragment

[!UICONTROL Experience Fragments] are created in [!DNL AEM]. For more information, see:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=en){target=_blank} in the *Experience Manager as a Cloud Service* guide.
* **[!DNL AEM] 6.5**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=en){target=_blank} in the *Adobe Experience Manager 6.5* documentation.
* **[!DNL AEM] 6.4**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=en){target=_blank} in the *Adobe Experience Manager 6.4* documentation.

### Step 3: Configure [!DNL AEM] to share the [!UICONTROL Experience Fragment] with [!DNL Target]

1. From within [!DNL AEM], select the desired [!UICONTROL Experience Fragment] or its containing folder, then click **[!UICONTROL Properties]**.
2. Click the **[!UICONTROL Cloud Services]** tab, then from the **[!UICONTROL Cloud Service Configuration]** drop-down list, select **[!UICONTROL Adobe Target]**.

   The previous step assumes that someone in your organization has created the [!DNL Adobe Target] configuration.

3. Click **[!UICONTROL Save & Close]**.

### Step 4: Publish the [!UICONTROL Experience Fragment] and export it into [!DNL Target]

Depending on your [!DNL AEM] version, see the following links for step-by-step instructions:

* **AEM as a Cloud Service**: [Exporting [!UICONTROL Experience Fragments] to Adobe Target](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target?lang=en){target=_blank} in the *Experience Manager as a Cloud Service* guide. 
* **[!DNL AEM] 6.5**: [Exporting an Experience Fragment to Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=en){target=_blank} in the *Adobe Experience Manager 6.5* documentation. 
* **[!DNL AEM] 6.4**: [Exporting an Experience Fragment to Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html){target=_blank} in the *Adobe Experience Manager 6.4* documentation.

## Using [!UICONTROL Experience Fragments] in [!DNL Target] activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

After performing the preceding tasks, the [!UICONTROL Experience Fragment] displays on the [!UICONTROL Offers] page in [!DNL Target].

[!DNL Target] currently looks for [!UICONTROL Experience Fragments] to import every ten minutes. The imported [!UICONTROL Experience Fragment] should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.

The [!UICONTROL Experience Fragment] is imported into [!DNL Target] as an HTML or JSON offer. The [!UICONTROL Experience Fragment] "primary" version remains in [!DNL AEM]. You cannot edit the [!UICONTROL Experience Fragment] in [!DNL Target].

You can filter and search by [!UICONTROL HTML XFs] and [!UICONTROL JSON XFs] to help you distinguish between [!UICONTROL Experience Fragment] types that are exported to [!DNL Target].

![Filter by Experience Fragment types: HTML or JSON in the Target UI](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

You can hover over an [!UICONTROL Experience Fragment] in the list, then click the [!UICONTROL View] icon ![Info icon](/help/main/assets/icons/InfoOutline.svg) to see additional information about the [!UICONTROL Experience Fragment], including its [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path], and last modifications information. Click [!UICONTROL [!UICONTROL View Full Details]] to see the activities that reference this offer.

![Experience Fragment information pop-up](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

You can consume [!UICONTROL Experience Fragments] in [!DNL Target] activities using the [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) and the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

>[!TIP]
>
>Use Artificial Intelligence, Machine Learning, and recommendations with [!UICONTROL Experience Fragments]:
>
>* To fully use the [!DNL Target] AI and ML functionality, you can select [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) or [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) while creating an  activity.
>
>* [!UICONTROL Experience Fragments] are not supported in [!DNL Recommendations] activities. However, to use [!UICONTROL Experience Fragments] for recommendations you can create an [!UICONTROL A/B Test] activity (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) or an [!UICONTROL Experience Targeting] (XT) activity and [include recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md). 

**To consume [!UICONTROL Experience Fragments] using the VEC:**

1. In [!DNL Target], while creating or editing an experience in the [Visual Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), click the location on the page where you want to insert [!DNL AEM] content, then click **[!UICONTROL Replace Content]** > **[!UICONTROL Experience Fragment]** to display the [!UICONTROL Experience Fragment] dialog box.

   The [!UICONTROL Experience Fragment] list displays the content created in [!DNL AEM] that is now natively available from within [!DNL Target].

   >[!NOTE]
   >
   >The [!UICONTROL Swap with Experience Fragment] option is not available for images. If you want to use this option with an image, click the container element that contains the desired image.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Select the desired [!UICONTROL Experience Fragment], then click **[!UICONTROL Add]**. 
1. Finish configuring the activity.

   For more information about configuring the various activity types, see the following topics:

    * **A/B Test:** [Create an A/B Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) 
    * **Auto-Allocate:** [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 
    * **Auto-Target:** [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
    * **Automated Personalization (AP):** [Creating an Automated Personalization Activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) 
    * **Experience Targeting (XT):** [Create an Experience Targeting Activity](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
    * **Recommendations in an A/B Test or XT activity:** [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md)   

   [!UICONTROL Experience Fragments] exported as JSON in [!DNL Target] cannot be used in activities created using the VEC; only HTML [!UICONTROL Experience Fragments] are supported in VEC-based activities. If you want to use JSON [!UICONTROL Experience Fragments], use them in activities created using the [Form-based experience composer](/help/main/c-experiences/form-experience-composer.md).

**To consume [!UICONTROL Experience Fragments] using the [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target], while creating or editing an experience in the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), select the location on the page where you want to insert [!DNL AEM] content, click the **[!UICONTROL More Details]** icon ( ![More Details icon](/help/main/assets/icons/MoreSmall.svg) ), then select **[!UICONTROL Change Experience Fragment]** to display the [!UICONTROL Change Experience Fragment] dialog box.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   The [!UICONTROL Experience Fragment] list displays the content created in [!DNL AEM] that is now natively available from within [!DNL Target]. 

1. Select the desired [!UICONTROL Experience Fragment], then click **[!UICONTROL Add]**. 
1. Finish configuring the activity.

## Additional information

* [!DNL Target] currently looks for [!UICONTROL Experience Fragments] to import every ten minutes. The imported [!UICONTROL Experience Fragment] should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
* The [!UICONTROL Experience Fragment] is imported into [!DNL Target] as an HTML or JSON offer. The [!UICONTROL Experience Fragment] "primary" version remains in [!DNL AEM]. You cannot edit the [!UICONTROL Experience Fragment] in [!DNL Target].
* You cannot create [!UICONTROL Experience Fragments] using [!DNL Adobe Developer]. Create [!UICONTROL Experience Fragments] using AEM, as explained above.
* If you update your [!UICONTROL Experience Fragment] in AEM, the [!UICONTROL Experience Fragment] must be published and exported to [!DNL Target] again so [!DNL Target] can use the latest changes.

## Removing clientlibs and extraneous HTML from [!UICONTROL Experience Fragments] exported to [!UICONTROL Target]

When using [!UICONTROL Experience Fragment] offers with [!DNL Target] on a page delivered by AEM, the targeted page already contains the necessary Client Libraries. Note also that extraneous HTML elements in the offer are also not necessary.

Sometimes entire HTML pages wrap the [!UICONTROL Experience Fragment] and cause problems. Ensure that the [!UICONTROL Experience Fragment] is a small piece of HTML and not a full HTML page with HTML, HEAD, BODY, and so forth.

For more information, see the following blog post: [AEM 6.5: Removing clientlibs from [!UICONTROL Experience Fragments] exported to Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Training video: Using AEM [!UICONTROL Experience Fragments] with [!DNL Adobe Target]

The following video shows you how to set up and use [!UICONTROL Experience Fragments]: 

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>The [!DNL AEM] deeplink feature discussed at 4:54 has been removed.

For more detailed information, see [Using [!UICONTROL Experience Fragments] with Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) on the *AEM Sites Videos and Tutorials* page.
