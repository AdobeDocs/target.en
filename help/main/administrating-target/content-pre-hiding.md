---
keywords: flicker,pre-hide,prehiding,personalization,implementation,anti-flicker,VEC,visual experience composer
description: Learn how content pre-hiding reduces flicker by hiding only the regions that active Adobe Target personalization will change, using an account-level setting, a lightweight page library, and per-activity controls.
title: Content pre-hiding for personalized experiences
feature: Administration & Configuration
role: Admin
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Beta features in [!DNL Adobe Target]."
---
# Content pre-hiding for personalized experiences

>[!AVAILABILITY]
>
>Content pre-hiding for personalized content is available as a **beta** capability.

When a visitor loads a page, default content can appear briefly and then be replaced by personalized content from [!DNL Adobe Target]. That visible switch is often called **flicker**, and it is a common experience issue for personalization programs.

**Content pre-hiding** uses a small library in the page `<head>` and a rule list [!DNL Target] keeps for your organization. It hides only the regions your live activities will change until delivery finishes, instead of hiding the whole `<body>`. Visitors see less flicker and less of a blank full-page wait.


## Configure content pre-hiding

1. [Turn on content pre-hiding](#content-pre-hiding-enable-account) for the account (off by default) to set the global default. For more information about accessing [!UICONTROL Administration] settings, see [Permissions required for editing [!UICONTROL Administration] settings](/help/main/administrating-target/start-target.md#admin-permissions).
1. [Add the Content pre-hiding library](#content-pre-hiding-add-library) in the document head before the personalization libraries run. You typically add this script once. You do not need to change it for each new activity.
1. Target [builds a rule set](#content-pre-hiding-rule-set) from live VEC and Form-Based Composer activities. The rule set describes the selectors and areas that delivery can change.
1. [The library loads the rule set from the Adobe CDN and pre-hides matching elements when needed](#content-pre-hiding-library-cdn).
1. [Turn content pre-hiding on or off per activity in Goals & Settings](#content-pre-hiding-per-activity). This overrides the account default without changing the global setting.

### Enable content pre-hiding for your instance {#content-pre-hiding-enable-account}

Content pre-hiding is off for your instance until you enable it. Use **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** to turn on the feature, set defaults, and access the download for your implementation team.

1. In [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. From the **[!UICONTROL Content pre-hiding]** menu, enable Content pre-hiding option.

    ![](assets/content-pre-hiding-1.png)

1. If needed, update the **[!UICONTROL Pre-hiding timeout]** in seconds.

1. Click **[!UICONTROL Save]**. This will apply flicker management settings to your instance.

1. Once enabled, click **[!UICONTROL Download prehide.min.js]**, then add the file to the document `<head>` so it loads before [!DNL at.js] or the [!DNL Web SDK].

    ![](assets/content-pre-hiding-2.png)

Your instance now uses the saved content pre-hiding and timeout settings as the default for activities that opt in.

### Enable content pre-hiding for your activity {#content-pre-hiding-activity}

[!DNL Target] builds a lightweight rule set from live activities authored in the [!UICONTROL Visual Experience Composer] (VEC) and the [!UICONTROL Form-Based Composer], describing the selectors and areas that delivery can change.

As activities go live or are deactivated, the rule set is updated so pre-hiding stays aligned with what is actually delivering, without edits to your page code for each launch.

The library retrieves that rule set from the Adobe CDN and pre-hides matching elements only when needed.

When you create or edit an activity:

1. Go to the **[!UICONTROL Goals & Settings]** step.
1. Use the **[!UICONTROL Content pre-hiding]** option to opt this activity in or out of pre-hiding.

This setting affects only the current activity. It does not change the account default configured under **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

## See also

* [Implementation](/help/main/administrating-target/implementation.md)
* [Implement [!DNL Target]](/help/main/c-implementing-target/implementing-target.md)
* [Troubleshoot activity content](/help/main/c-activities/c-troubleshooting-activities/content-trouble.md)
