---
keywords: experience;json;aem;adobe experience manager;export to adobe target;content fragments;fragments;CF
description: Learn how to use [!DNL Adobe Experience Manager] Content Fragments in [!DNL Adobe Target] activities.
title: How Do I Use [!DNL Adobe Experience Manager] (AEM) Content Fragments?
feature: Integrations
---
# AEM Content Fragments

Use Content Fragments (CFs) created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization.

>[!NOTE]
>
>Consider the following as you work with AEM Content Fragments in [!DNL Target]:
> 
>* This feature requires that you are an [!DNL Adobe Experience Manager] (AEM) customer. For more information, see [Requirements](#section_AE6F0971E1574B3AA324003599B96E5A) below.
>* This feature is available for the following activity types: [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] (AP), and [!UICONTROL Experience Targeting] (XT). This feature is not available in [!UICONTROL Multivariate Test] (MVT) and [!UICONTROL Recommendations] activities.
>
>* You can consume Content Fragments in [!DNL Target] activities using the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) only.

To learn more about AEM Content Fragments and Experience Fragments, see [AEM Experience Fragments and Content Fragments overview](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requirements {#requirements}

You must be provisioned with the Content Fragments functionality within [!DNL Target]. In addition, you must be using [!DNL AEM] as a Cloud Service. Your account representative can help ensure that you meet the requirements to use this feature:

* [!DNL Adobe Experience Manager] as a Cloud Service 

Contact [Adobe Target Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to enable the integration and to provide you with authentication details.

## Creating and configuring experience fragments in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

In order to use [!DNL AEM] Experience Fragments in [!DNL Target], you must perform the following steps:

### Step 1: Integrate [!DNL AEM] with [!DNL Target]

For more information, see:

* **AEM as a Cloud Service**: Integrating with Adobe Target link in the *Experience Manager as a Cloud Service* guide. 

### Step 2: Create the Content Fragment

Content Fragments are created in [!DNL AEM]. For more information, see:

* **AEM as a Cloud Service**: Content Fragments link in the *Experience Manager as a Cloud Service* guide.

### Step 3: Configure [!DNL AEM] to share the Content Fragment with [!DNL Target]

1. From within [!DNL AEM], select the desired Content Fragment or its containing folder, then click **[!UICONTROL Properties]**.
2. Click the **[!UICONTROL Cloud Services]** tab, then from the **[!UICONTROL Cloud Service Configuration]** drop-down list, select **[!UICONTROL Adobe Target]**.

   >[!NOTE]
   >
   >The previous step assumes that someone in your organization has created the [!DNL Adobe Target] configuration.

3. Click **[!UICONTROL Save & Close]**.

### Step 4: Publish the Content Fragment and export it into [!DNL Target]

See the following links for step-by-step instructions:

* **AEM as a Cloud Service**: Exporting Content Fragments to Adobe Target link in the *Experience Manager as a Cloud Service* guide. 

## Using Content Fragments in [!DNL Target] activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

After performing the preceding tasks, the Content Fragment displays on the [!UICONTROL Offers] page in [!DNL Target].

>[!NOTE]
>
>* [!DNL Target] currently looks for Content Fragments to import every ten minutes. The imported Content Fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
>
>* The Content Fragment is imported into [!DNL Target] as a JSON offer. That Content Fragment "primary" version remains in [!DNL AEM]. You cannot edit the Content Fragment in [!DNL Target].

You can filter and search by [!UICONTROL HTML XFs] and [!UICONTROL JSON XFs] to help you distinguish between Content and Experience Fragment types that are exported to [!DNL Target].

![Filter by Experience Fragment types: HTML or JSON in the Target UI](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

You can hover over a Content Fragment in the list, then click the [!UICONTROL View] icon ![View icon](assets/icon_info.png) to see additional information about the Content Fragment, including its [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path], and last modifications information. Click the [!UICONTROL Offer Usage] tab to see the activities that reference this offer.

![Experience Fragment information pop-up](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

You can consume Content Fragments in [!DNL Target] activities using the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) only. You *cannot* consume Content Fragments in [!DNL Target] activities using the [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC). Content Fragments are exported as JSON in [!DNL Target] and cannot be used in activities created using the VEC.

>[!NOTE]
>
>To fully use the [!DNL Target] AI and ML functionality, you can select [Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) or [Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) while creating an A/B Test.
>
>Content Fragments are not supported in [!DNL Recommendations] activities. However, to use Content Fragments for recommendations you can create an [!UICONTROL A/B Test] activity (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) or an [!UICONTROL Experience Targeting] (XT) activity and [include recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md). 

**To consume Content Fragments using the Form-based Experience Composer:**

1. In [!DNL Target], while creating or editing an experience in the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), select the location on the page where you want to insert [!DNL AEM] content, then select **[!UICONTROL Change Content Fragment]** to display the [!UICONTROL Choose a Content Fragment] list.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   The [!UICONTROL Content Fragment] list displays the content created in [!DNL AEM] that is now natively available from within [!DNL Target]. 

1. Select the desired Content Fragment, then click **[!UICONTROL Save]**. 
1. Finish configuring the activity.

## Considerations {#considerations}

* [!DNL Target] currently looks for Content Fragments to import every ten minutes. The imported Content Fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
* The Content Fragment is imported into [!DNL Target] as a JSON offer. The Content Fragment "primary" version remains in [!DNL AEM]. You cannot edit the Content Fragment in [!DNL Target].
* You cannot create Content Fragments using [!DNL Adobe I/O]. Create Content Fragments using AEM, as explained above.
* If you update your Content Fragment in AEM, the Content Fragment must be published and exported to [!DNL Target] again so [!DNL Target] can use the latest changes.