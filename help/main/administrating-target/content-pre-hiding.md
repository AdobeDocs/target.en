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

With content pre-hiding you can manage flicker by hiding only the parts of the page your activities personalize during page loading, so your customers see less flicker and less empty screen time.

Here is how content pre-hiding works, from the account default through your page implementation and per-activity choices.

1. Enable content pre-hiding for your account to set the global default. It is off by default. [Learn more](#content-pre-hiding-enable-account)

1. Add the Content pre-hiding library to the `<head>` of all the pages where you run personalization activities.

1. [!DNL Target] builds a rule set from live [!UICONTROL Visual Experience Composer] and [!UICONTROL Enhanced Experience Composer] activities. The rule set lists selectors and regions that delivery may change. 

    Note that [!UICONTROL Form-Based Composer] activities are not supported.

1. The library fetches that rule set from the Adobe CDN and pre-hides matching elements only while personalized content is still loading.

1. In **[!UICONTROL Goals & Settings]**, you can disable **[!UICONTROL Content pre-hiding]** for individual activities, but only if it is enabled at the account level. [Learn more](#content-pre-hiding-activity)

## Enable content pre-hiding for your instance {#content-pre-hiding-enable-account}

>[!IMPORTANT]
>
>To enable content pre-hiding for the instance, you must be an **Administrator**.

Content pre-hiding is off for your instance until you enable it. Use **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** to turn on the feature, set defaults, and access the download for your implementation team.

1. In [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. From the **[!UICONTROL Content pre-hiding]** menu, enable Content pre-hiding option.

    ![](assets/content-pre-hiding-1.png)

1. If needed, update the **[!UICONTROL Pre-hiding timeout]** in seconds.

1. Click **[!UICONTROL Save]**. This will apply flicker management settings to your instance.

1. Once enabled, click **[!UICONTROL Download]**, then add the file to the page `<head>` so it loads before [!DNL at.js] or the [!DNL Web SDK].

    ![](assets/content-pre-hiding-2.png)

Your instance now uses the saved content pre-hiding and timeout settings as the default for activities that opt in.

## Enable content pre-hiding for your activity {#content-pre-hiding-activity}

With pre-hiding enabled for your instance, choose whether each activity uses it in **[!UICONTROL Goals & Settings]**. Activities for which you enable pre-hiding are included in the targeted behavior when they are live.

[!DNL Target] then builds a lightweight rule set from live activities authored in the [!UICONTROL Visual Experience Composer] (VEC) and the [!UICONTROL Form-Based Composer], describing the selectors and areas that delivery can change.

When you create or edit an activity:

1. Access the activity you want to enable the pre-hiding option.

1. Access the **[!UICONTROL Edit activity]** drop-down and select **[!UICONTROL Edit Goals & Settings]**.

    ![](assets/content-pre-hiding-3.png)

1. From the **[!UICONTROL Content pre-hiding]** menu, toggle on the **[!UICONTROL Enable content pre-hiding]** option to opt this activity in or out of pre-hiding.

    ![](assets/content-pre-hiding-4.png)

1. Once done, click **[!UICONTROL Save & Close]**.

After you save and as activities go live or are deactivated, the rule set is updated so pre-hiding stays aligned with what is actually delivering, without edits to your page code for each launch.

On the visitor side, the library retrieves that rule set from the Adobe CDN on each page load and pre-hides matching elements only when needed until personalized content is ready.
