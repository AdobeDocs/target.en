---
keywords: experience;json;aem;adobe experience manager;export to adobe target;content fragments;fragments;CF
description: Learn how to use [!DNL Adobe Experience Manager] Content Fragments in [!DNL Adobe Target] activities.
title: How Do I Use [!DNL Adobe Experience Manager] (AEM) Content Fragments?
feature: Integrations
---
# AEM [!UICONTROL Content Fragments]

Use [!UICONTROL Content Fragments] (CFs) created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization.

>[!NOTE]
>
>Consider the following as you work with AEM [!UICONTROL Content Fragments] in [!DNL Target]:
> 
>* This feature requires that you are an [!DNL Adobe Experience Manager] (AEM) customer. For more information, see [Requirements](#section_AE6F0971E1574B3AA324003599B96E5A) below.
>
>* This feature is available for the following activity types: [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] (AP), and [!UICONTROL Experience Targeting] (XT). This feature is not available in [!UICONTROL Multivariate Test] (MVT) and [!UICONTROL Recommendations] activities.
>
>* You can consume [!UICONTROL Content Fragments] in [!DNL Target] activities using the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) only. You cannot consume [!UICONTROL Content Fragments] using the [!UICONTROL Visual Experience Composer] (VEC).

To learn more about AEM [!UICONTROL Content Fragments] and [!UICONTROL Experience Fragments], see [AEM Experience Fragments and Content Fragments overview](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requirements {#requirements}

You must be provisioned with the [!UICONTROL Content Fragments] functionality within [!DNL Target]. In addition, you must be using [!DNL AEM] as a Cloud Service. Your account representative can help ensure that you meet the requirements to use this feature:

Contact [Adobe Target Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to enable the integration and to provide you with authentication details.

## Configuring and working with [!UICONTROL Content Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

In order to export [!UICONTROL Content Fragments] to use in [!DNL Target] activities, you must perform some preliminary steps in AEM. For more information, see *Exporting Content Fragments to Adobe Target* in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}.

For information about designing, creating, curating, and publishing [!UICONTROL Content Fragments], see [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments.html){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}.

## Using [!UICONTROL Content Fragments] in [!DNL Target] activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

After performing the preceding tasks, the [!UICONTROL Content Fragment] displays on the [!UICONTROL Offers] page in [!DNL Target].

[!DNL Target] currently looks for [!UICONTROL Content Fragments] to import every ten minutes. The imported [!UICONTROL Content Fragment] should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.

The [!UICONTROL Content Fragment] is imported into [!DNL Target] as a JSON offer. That [!UICONTROL Content Fragment] "primary" version remains in [!DNL AEM]. You cannot edit the [!UICONTROL Content Fragment] in [!DNL Target].

You can filter and search by [!UICONTROL HTML XFs], [!UICONTROL JSON XFs] and [!UICONTROL Content Fragments] to help you distinguish between different offers types that are exported to [!DNL Target].

![Filter by Content Fragment types: HTML or JSON in the Target UI](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

You can hover over a [!UICONTROL Content Fragment] in the list, then click the [!UICONTROL View] icon ![Info icon](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) to see additional information about the [!UICONTROL Content Fragment], including its [!UICONTROL AEM path] and [!UICONTROL AEM deep link]. Click the [!UICONTROL Offer Usage] tab to see the activities that reference this offer.

![Content Fragment information pop-up](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

You can consume [!UICONTROL Content Fragments] in [!DNL Target] activities using the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) only. You *cannot* consume [!UICONTROL Content Fragments] in [!DNL Target] activities using the [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC). [!UICONTROL Content Fragments] are exported as JSON in [!DNL Target] and cannot be used in activities created using the VEC.

>[!TIP]
>
>Use Artificial Intelligence, Machine Learning, and recommendations with [!UICONTROL Content Fragments]:
>
>* To fully use the [!DNL Target] AI and ML functionality, you can select [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) or [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) while creating an A/B Test.
>
>* [!UICONTROL Content Fragments] are not supported in [!DNL Recommendations] activities. However, to use [!UICONTROL Content Fragments] for recommendations you can create an [!UICONTROL A/B Test] activity (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) or an [!UICONTROL Experience Targeting] (XT) activity and [include recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md). 

**To consume [!UICONTROL Content Fragments] using the [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target], while creating or editing an experience in the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), select the location on the page where you want to insert [!DNL AEM] content, then select **[!UICONTROL Change Content Fragment]** to display the [!UICONTROL Choose a Content Fragment] list.

   ![content_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   The [!UICONTROL Content Fragment] list displays the content created in [!DNL AEM] that is now natively available from within [!DNL Target]. 

1. Select the desired [!UICONTROL Content Fragment], then click **[!UICONTROL Save]**. 
1. Finish configuring the activity.

## Considerations {#considerations}

* [!DNL Target] currently looks for [!UICONTROL Content Fragments] to import every ten minutes. The imported [!UICONTROL Content Fragment] should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
* The [!UICONTROL Content Fragment] is imported into [!DNL Target] as a JSON offer. The [!UICONTROL Content Fragment] "primary" version remains in [!DNL AEM]. You cannot edit the [!UICONTROL Content Fragment] in [!DNL Target].
* You cannot create [!UICONTROL Content Fragments] using [!DNL Adobe I/O]. Create [!UICONTROL Content Fragments] using AEM, as explained above.
* If you update your [!UICONTROL Content Fragment] in AEM, the [!UICONTROL Content Fragment] must be published and exported to [!DNL Target] again so [!DNL Target] can use the latest changes.