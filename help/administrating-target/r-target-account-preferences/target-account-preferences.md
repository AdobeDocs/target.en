---
description: Set your account preferences to configure Target Standard or Target Premium to work correctly with your account.
keywords: account preferences;preferences;site details;custom mbox name;Experience Cloud solution used for reporting;Show estimated lift in revenue;css selectors;use element classes;Default Visual Experience Composer URL;Enable Enhanced Experience Composer;Generate Experience Snapshots;mobile viewport configuration;Industry Vertical;Filter Incompatible Criteria
seo-description: Set your account preferences to configure Adobe Target Standard or Target Premium to work correctly with your account.
seo-title: Preferences
solution: Target
subtopic: Getting Started
title: Preferences
topic: Standard
uuid: ed3904c8-533b-4b9c-a3a1-079c61b1bf2a
---

# Preferences{#preferences}

Set your account preferences to configure [!DNL Target Standard] or [!DNL Target Premium] to work correctly with your account.

To set your account preferences, click **[!UICONTROL Setup]** > **[!UICONTROL Preferences]**, configure your preferences as desired, then click **[!UICONTROL Submit]**.

The following illustration shows the available settings on the [!UICONTROL Account Preferences] page.

![Preferences page](/help/administrating-target/r-target-account-preferences/assets/target-account-preferences.png)

>[!NOTE]
>
>Some of these preferences are available only if you have [Target Premium](/help/c-intro/intro.md#premium).

## Site Details {#section_04A3340FC29B46978DB77058259F4EE0}

Specify how your site has been configured.

### Custom Global Mbox

Select the optional custom mbox name you are using to deliver [!DNL Target] activities. This global mbox must be empty, meaning it has no default content. Save this setting only after the updated [!DNL at.js] or [!DNL mbox.js] file is installed on your site.

>[!CAUTION]
>
>Configuring this setting incorrectly might result in an outage for existing activities.

## Results and Reporting {#section_47C887AABD704A96BCD1C00BEABF4BCE}

Set options that determine what data is used for your results and reports.

| Option | Description |
|--- |--- |
|Experience Cloud solution used for reporting|Select the reporting source for your activities, either [!DNL Target] or Adobe Analytics. You can also choose to select your reporting source per activity. Consider the following information as you choose your reporting source:<ul><li>[!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], and [!UICONTROL Automated Personalization] (AP) activity creation, activation, and deactivation are allowed irrespective of the reporting source selected. These activity types are not supported when you choose [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Even if you specify Analytics as your reporting source, [!DNL Target] is used as the reporting source for these activity types.</li><li>If the reporting source is set to Analytics here, you are not allowed to activate an activity that uses [!DNL Target] as the reporting source (the reporting source is specified as Target per activity). You must change the reporting source to Analytics in your activity or change the reporting engine to Select Per Activity in Setup > Preferences.</li><li>If the reporting source is set to [!DNL Target] here, you are not allowed to activate an activity that uses Analytics as the reporting source. You must change the reporting source to [!DNL Target] in your activity or change the reporting source to Select Per Activity in Setup > Preferences.</li><li>If the reporting source is set to Select Per Activity here, you can create, activate, and deactivate activities that are supported by the selected reporting source. For a matrix of supported activities, see [Adobe Analytics as the reporting source for Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).</li><li>When you switch from A/B Manual to [!UICONTROL Auto-Allocate] or [!UICONTROL Auto-Target], all metrics and reporting audiences are lost if the reporting source of the A/B Manual activity is not supported in [!UICONTROL Auto-Allocate] or [!UICONTROL Auto-Target] activities.</li></ul>|
|Show estimated lift in revenue|You can also choose to show the estimated lift in revenue if you enter a monetary value for your goal. [!DNL Target] can estimate the revenue lift you would attain if all users view the winning experience. The estimated lift feature is disabled by default.<br>Only Experience Cloud Admin users can enable or disable this feature. If estimated lift is disabled, the corresponding fields do not appear in the interface. Disabling the feature does not result in a loss of data, including the data used for your estimates. The estimates are based on data that is collected whether or not the feature is enabled.<br>For detailed information, see [Estimating Lift in Revenue](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).|
|Enable fine-grained priorities|Allow numerical entries for priority ranging from 0-999.<br>Depending on your settings, the UI and options for  Priority  vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999.<br>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.|

## CSS Selectors {#section_8155EDBF449E4198863235F94D1EA872}

Specify how [!DNL Target] generates CSS selectors.

These options help [!DNL Target] understand your site's structure to generate better CSS selectors for content delivery. By default, [!DNL Target] generates selectors based on element IDs on the page. If your site uses few IDs, or duplicates IDs on the same page, then using classes might be a better option.

You can choose one or both of the following options:

| Option | Description |
|--- |--- |
|Use element IDs|Deselect this option if the same ID is used for multiple elements or if element ID might change on page load.|
|Use element classes|By default, [!DNL Target] only uses element IDs. However, if your page is designed to use classes to identify elements, such as a page built with [!DNL Adobe Experience Manager], you should also select [!UICONTROL Use element classes].<br>**Note**: Although everything has been done to assure accuracy, be aware that using classes can result in errors. If you do not select either option, accuracy is also affected. The order of accuracy is IDs > classes > neither option. Always be sure to test your page to make sure the selectors are correct.<br>You can override this setting per activity (click the [!UICONTROL Settings] gear icon, then select [!UICONTROL CSS Selectors]). This is especially useful if you have multiple sites that are configured differently.<br>**Note**: Overriding the setting per activity is not available in [!UICONTROL Automated Personalization] and [!UICONROL Multivariate Testing] activities.  See [Element Selectors Used in the Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/vec-selectors.md) for additional information about selectors.|

## Visual Experience Composer {#section_CD9BDD372CF54E678F88E8BA95757A5A}

| Option | Description |
|--- |--- |
|Default Visual Experience Composer URL|Set the default URL used by the [!UICONTROL Visual Experience Composer]. This is the default page, such as your home page, used whenever you set up an experience for each new activity. If you do not set a default URL, you must enter a URL for each activity when you create it.|
|Enable Enhanced Experience Composer|Allows editing on iFrame-busting sites and sites with mixed content. Some sites may not be compatible with the enhanced version. Uncheck this option to revert to the original Experience Composer. Activity delivery on sites is not affected by this choice.<br>For more information, see [Troubleshooting the Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).<br>**Note**: You can also enable the Enhanced Experience Composer at the activity level.|
|Load Mixed Content|Enable mixed content while opening a website using the Enhanced Experience Composer. Enabling this option avoids extra overhead of loading static resources via Target proxy servers.|
|Generate Experience Snapshots|Enabling experience snapshots generates thumbnails for your experiences in the activity workflow diagram. Disabling snapshots might result in faster performance for some users.|

## Mobile Viewport Configuration {#section_42176D062BCE4A28ADBB784CC4BEF84D}

You can add devices to use when previewing experiences. Each device has an associated audience.

| Option | Description |
|--- |--- |
|![Premium badge](/help/assets/premium.png) Add New|Click [!UICONTROL Add New], specify a descriptive name for the mobile viewport, specify the width and height, select the desired operating system, then click [!UICONTROL Save].  For information about how to add a mobile viewport, see [Mobile Viewport Configuration](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md).|

## Training video: Account Preferences (7:33)

This video includes information about account preferences.

* Describe the account settings available in [!DNL Target Standard]

>[!VIDEO](https://video.tv.adobe.com/v/17379)