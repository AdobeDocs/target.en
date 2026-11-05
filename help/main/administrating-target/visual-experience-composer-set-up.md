---
keywords: visual experience composer;vec;default url;enhanced experience composer;eec;mixed content;experience snapshots;mobile viewport;css;css selectors
description: Learn how to configure the Adobe [!DNL Target] Visual Experience Composer (VEC) by specifying its general settings, mobile viewport configuration, and CSS selectors.
title: How Do I Configure the Visual Experience Composer (VEC)?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
TQID: https://experienceleague.adobe.com/E1ck4-aG4txqaFLs3t3-8bN-BQIoY8stRASTRJfhZMY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: b1d5cd6a-4ed3-43f6-9a52-2721acea1129
    internal-label: Troubleshooting
  - id: c011fe9c-b94b-4a88-93d8-f2acece55112
    internal-label: Administration
  - id: fc9c2184-9102-403f-bd6c-0055021e4bea
    internal-label: Overview
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Configure the Visual Experience Composer (VEC)

Use the **[!UICONTROL Visual Experience Composer]** tab under **[!UICONTROL Administration]** to set account-wide defaults for the [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC). These settings apply whenever authors build or preview experiences in the VEC.

**Configuration overview**

1. [General settings](#general-settings): Default URL, Enhanced Experience Composer, mixed content, and experience snapshots.
1. [Mobile viewport configuration](#mobile-viewport-configuration): Preview devices for responsive experiences ([Target Premium](/help/main/c-intro/intro.md#premium) only).
1. [CSS selectors](#css): How Target generates selectors for content delivery.

To open the configuration page, click **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.

>[!NOTE]
>
>Settings on this page apply to the entire [!DNL Target] account.

## General settings {#general-settings}

On the **[!UICONTROL General Settings]** section, configure defaults used when you open the VEC.

![General Settings section](/help/main/administrating-target/assets/general-settings.png)

The following settings are available:

* **Default URL**

  Set the default URL used by the [!UICONTROL Visual Experience Composer]. This is the default page, such as your home page, used whenever you set up an experience for each new activity. If you do not set a default URL, you must enter a URL for each activity when you create it.

* **Enable Enhanced Experience Composer**

  Allows editing on iFrame-busting sites and sites with mixed content. Some sites might not be compatible with the enhanced version. Deselect this option to revert to the original [!UICONTROL Visual Experience Composer]. Activity delivery on sites is not affected by this choice.

  Note that the [!UICONTROL Enhanced Experience Composer] is not supported in [!DNL Safari]. 

  For more information, see [Troubleshooting the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

  You can also enable the [!UICONTROL Enhanced Experience Composer] at the activity level. See [Learn how to enable the Enhanced Experience Composer at the activity level](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md).

* **Load Mixed Content**

  Enable mixed content while opening a website using the [!UICONTROL Enhanced Experience Composer] (EEC). Enabling this option avoids the extra overhead of loading static resources via [!DNL Target] proxy servers.

  This option is helpful if, for example:

    * Your Content Security Policy (CSP) headers allow loading mixed content without the use of proxy servers with the EEC enabled.
    * Your HTTP website faces increased load time in the EEC, wherein JavaScript, images, and so forth take longer to load via proxy.

* **Generate experience snapshots in the activity flow diagram**

  Enabling experience snapshots generates thumbnails for your experiences in the activity workflow diagram. Disabling snapshots might result in faster performance for some users.

## Mobile viewport configuration {#mobile-viewport-configuration}

>[!NOTE]
>
>The **[!UICONTROL Mobile Viewport Configuration]** settings are a [Target Premium](/help/main/c-intro/intro.md#premium) feature.

Add devices to use when previewing experiences. Each device has an associated audience.

![Mobile Viewport Configuration section](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

Use the following steps to add a mobile viewport:

1. Click **[!UICONTROL Add]**.
1. Specify a descriptive name for the mobile viewport, specify the width and height, and select the desired operating system.
1. Click **[!UICONTROL Save]**.

For preview and audience details, see [Learn how to use mobile viewports for responsive experiences](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## CSS Selectors {#css}

Specify how [!DNL Target] generates CSS selectors.

![CSS Selectors section](/help/main/administrating-target/assets/css-selectors.png)

These options help [!DNL Target] understand your site's structure to generate better CSS selectors for content delivery. By default, [!DNL Target] generates selectors based on element IDs on the page. If your site uses few IDs, or duplicates IDs on the same page, then using classes might be a better option.

You can choose one or both of the following options:

* **Use element IDs**

  Deselect this option if the same ID is used for multiple elements or if element ID might change on page load.

* **Use element classes**

  By default, [!DNL Target] only uses element IDs. However, if your page is designed to use classes to identify elements, such as a page built with [!DNL Adobe Experience Manager], you should also select **[!UICONTROL Use element classes]**. Selector accuracy is generally highest when using IDs, lower when using classes, and lowest when neither option is selected. Test your page in the VEC to confirm that selectors are correct.

  You can override this setting per activity by clicking the **[!UICONTROL Settings]** gear icon and selecting **[!UICONTROL CSS Selectors]**, useful when sites in the same account are configured differently. Per-activity overrides are not available in **[!UICONTROL Automated Personalization]** or **[!UICONTROL Multivariate Testing]** activities. For selector behavior and troubleshooting, see [Element selectors used in the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Training video: Account Preferences (7:33) ![Overview badge](/help/main/assets/overview.png)

>[!BEGINSHADEBOX]

The [!DNL Target] **[!UICONTROL Administration]** menu UI (formerly **[!UICONTROL Setup]**) has been redesigned to provide improved performance, reduce the maintenance time required when releasing new features, and to improve the user experience across the product. The information in the following video is generally correct; however, options might be in slightly different locations. Updated videos will be posted soon.

>[!ENDSHADEBOX]

This video includes information about account preferences.

* Describe the account settings available in [!DNL Target Standard]

>[!VIDEO](https://video.tv.adobe.com/v/17379)
