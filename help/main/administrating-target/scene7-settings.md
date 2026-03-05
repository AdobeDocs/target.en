---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: Learn how to integrate Adobe [!DNL Target] with Adobe Dynamic Media Classic (formerly Scene7) to provide Digital Asset Management (DAM) in the Content Library.
title: How Do I Configure the Dynamic Media Classic (Scene7) Integration?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
TQID: https://experienceleague.adobe.com/LKbjwlGIxrgaU-2i6Ddn1wi-VjsSmpQPAxYkFHRNOYQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: da3860b0-d637-47df-bef0-273751180266
    internal-label: Digital asset management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Dynamic Media Classic (formerly Scene7) configuration

[!DNL Adobe Target] can be integrated with [!DNL Adobe Dynamic Media Classic] (formerly [!DNL Scene7]) to provide Digital Asset Management (DAM) in the [!UICONTROL Content Library].

{{permissions-update}}

>[!NOTE]
>
>Integrating [!DNL Target] with [!DNL Dynamic Media Classic] enables delivery of assets (as part of activities) uploaded to the [!DNL Adobe Experience Cloud] assets folder. This integration does not enable access to all assets uploaded in [!DNL Dynamic Media Classic] for delivery in [!DNL Target] activities.

If you already have a [!DNL Dynamic Media] account, you can supply your existing credentials. If you do not have an account, you can request a restricted-use [!DNL Dynamic Media Classic] account at no additional charge from your [!DNL Adobe] representative. This account can be used for purposes restricted for use in [!DNL Target] only. This service is made available to customers for workflows needing image-swap functionality.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

If this setting is not configured, the [!UICONTROL Swap Image offer] option within the activity creation workflow is not available. After this setting is configured, the option to swap/change image offers is available in both the [Visual Experience Composer (VEC) and in the Form-Based Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). You can then leverage image offers with images that have been uploaded from the [!DNL Adobe Experience Cloud] for use in [!DNL Target] activities.

If you want to reference a public image URL directly in an offer or custom code during activity creation, you should deploy the image to your own web servers and use your own URL in the code. There is no way to obtain the published URL of an image uploaded into the [!DNL Experience Cloud] to consume directly or outside of targeting workflows using [!DNL Target]. This functionality is not allowed, as per contract.

Note that the storage URL and the final publish URLs of images from [!DNL Dynamic Media] are different and one must *NOT* create offers using the storage link of images as delivery will not work in such cases. You must use the image offers capability as explained in our help documentation.

To integrate with [!DNL Dynamic Media Classic] ([!DNL Scene7]), you need to specify the following information. 

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.

1. Specify the following [!DNL Dynamic Media Classic] account information:

   **Region:** The region for your [!DNL Dynamic Media] account: North America, Europe, or Asia.

   **Adhoc folder:** The location for content that resides outside the target folder and are manually uploaded to [!DNL Dynamic Media].

   **Email address:** The email address used to log in to [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Password:** The password used to log in to [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Click **[!UICONTROL Submit]**.
