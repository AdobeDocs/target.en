---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: Connect Adobe Target to Adobe Dynamic Media Classic (Scene7) so authors can use image offers and swap images from Experience Cloud assets in activities.
landing-page-description: Configure Scene7 Configuration in Administration to enable image offers, Content Library DAM workflows, and swap-image actions in the VEC and Form-Based Experience Composer.
short-description: Configure Scene7 Configuration in Administration to enable image offers, Content Library DAM workflows, and swap-image actions in the VEC and Form-Based Experience Composer.
title: How Do I Configure the Dynamic Media Classic (Scene7) Integration?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
TQID: https://experienceleague.adobe.com/LKbjwlGIxrgaU-2i6Ddn1wi-VjsSmpQPAxYkFHRNOYQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: da3860b0-d637-47df-bef0-273751180266
    internal-label: Digital asset management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Configure Dynamic Media Classic (Scene7)

Use the **[!UICONTROL Scene7 Configuration]** tab under **[!UICONTROL Administration]** to connect [!DNL Adobe Target] to [!DNL Adobe Dynamic Media Classic] (formerly [!DNL Scene7]). The integration brings Digital Asset Management (DAM) into the [!UICONTROL Content Library] and enables image-swap workflows in activities.

For how this tab fits with other administration tasks, see [How Do I Administer Target?](/help/main/administrating-target/administrating-target.md). To locate **[!UICONTROL Administration]** in the interface, see [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md).

**Overview**

1. [What the integration enables](#what-it-enables): Image offers, swap images, and eligible assets.
1. [Account and credentials](#account-and-credentials): Existing [!DNL Dynamic Media] accounts and supported account types.
1. [Usage guidelines](#usage-guidelines): URLs, delivery, and what is not supported.
1. [Configure Scene7 in Target](#configure-scene7): Sign-in and region settings.

{{permissions-update}}

## What the integration enables {#what-it-enables}

When **[!UICONTROL Scene7 Configuration]** is set up, authors can use images uploaded to the [!DNL Adobe Experience Cloud] assets folder in [!DNL Target] activities. The **[!UICONTROL Swap Image offer]** option appears in the activity workflow, including in the [Visual Experience Composer and Form-Based Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). For swap behavior in the VEC, see [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

If this setting is not configured, **[!UICONTROL Swap Image offer]** is not available during activity creation.

The integration delivers assets that are part of activities from the Experience Cloud assets folder. It does **not** expose every asset in [!DNL Dynamic Media Classic] for use in [!DNL Target] activities.

After configuration, manage image offers in the [!UICONTROL Offers] library. See [Manage content](/help/main/c-experiences/c-manage-content/manage-content.md).

## Account and credentials {#account-and-credentials}

If you already have a [!DNL Dynamic Media] account, enter those credentials on the **[!UICONTROL Scene7 Configuration]** page.

Adobe no longer provisions restricted-use, no-charge [!DNL Dynamic Media Classic] accounts for new [!DNL Target] customers or new users. If your organization already has sign-in credentials for this integration, they continue to work. For account questions, contact your [!DNL Adobe] representative.

## Usage guidelines {#usage-guidelines}

Keep the following constraints in mind when you use images with this integration:

* **Image offers, not storage URLs.** [!DNL Dynamic Media] storage URLs and published delivery URLs are different. Do not build offers from storage links; delivery fails. Use [image offers](/help/main/c-experiences/c-manage-content/manage-content.md) and swap-image workflows instead.
* **Public URLs in custom code.** To reference a public image URL directly in an offer or custom code, host the image on your own web servers and use that URL. You cannot obtain a published URL for an Experience Cloud–uploaded image for use outside [!DNL Target] targeting workflows; that use is not permitted under contract.
* **Eligible assets.** Only assets uploaded to the Experience Cloud assets folder (and workflows supported by this integration) are in scope—not the full [!DNL Dynamic Media Classic] catalog.

## Configure Scene7 in Target {#configure-scene7}

Use the following steps to connect [!DNL Dynamic Media Classic] ([!DNL Scene7]):

1. Click **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.
1. Enter your [!DNL Dynamic Media Classic] account information:

   | Field | Description |
   | --- | --- |
   | **Region** | Region for your [!DNL Dynamic Media] account: North America, Europe, or Asia. |
   | **Adhoc folder** | Location for content outside the Target folder that you manually upload to [!DNL Dynamic Media]. |
   | **Email address** | Email address used to sign in to [!DNL Dynamic Media Classic] ([!DNL Scene7]). |
   | **Password** | Password used to sign in to [!DNL Dynamic Media Classic] ([!DNL Scene7]). |

   ![Scene7 Configuration fields](/help/main/administrating-target/assets/scene7-1.png)

1. Click **[!UICONTROL Submit]**.
