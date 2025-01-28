---
keywords: Recommendations;Settings;name;objective;priority;duration;reporting settings;other metadata
description: Learn how to configure the settings used to describe and control a Recommendations activity in Adobe Target.
title: How Do I Configure Recommendations Activity Settings?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
---
# Recommendations Activity settings

Information about the settings you can use to describe and control a [!UICONTROL Recommendations] activity in [!DNL Adobe Target].

The following sections describe the available settings for a [!UICONTROL Recommendations] activity.

## Name

Click the More Actions icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallListVert.svg) ), then click **[!UICONTROL Rename]** to provide a descriptive name that will help you and your team identify the activity.

The following characters are not allowed in an activity name:

`/`
`?`
`#`
`:`
`=`
`+`
`-`
`@`

If you specify a [!UICONTROL Recommendations] activity name that already exists for another activity in [!UICONTROL Recommendations Classic], the new activity is resynced with a new name. The new name is the original name appended with a timestamp to make it unique. This new name is displayed in both [!DNL Target Standard/Premium] and [!UICONTROL Recommendations Classic].

## Objective

(Optional) Describe the goal of the activity.

## Priority

Adjust the slider to determine the priority level.

The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.

## Duration

Set the duration of the activity.

The activity can start when activated, or you can set a specific date and time. Likewise, the activity can either end when it is deactivated or you can set a date and time. The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is set to the time zone configured in your browser. To use a different time zone, set your browser to another time zone and restart the browser.

## Reporting Settings

* **Reporting Source:** Specify which solution data is collected from:

  * [!DNL Adobe Target]
  * [!DNL Adobe Analytics]
  * [!DNL Adobe Customer Journey Analytics]

  If a reporting solution is specified in your [account settings](/help/main/administrating-target/reporting.md), the specified solution is used and this setting is not visible.

  You cannot change your reporting source after the activity goes live to keep reports consistent.

  **[!DNL Adobe Analytics]**: See [[!DNL Adobe Analytics] as the reporting source for [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) to learn about the differences between the reporting solutions and the advantages of each.

  When selecting [!DNL Analytics] as the reporting source for [!DNL Target] (A4T), you select an [!DNL Analytics] report suite to receive [!DNL Target] activity data. To do this, first choose from any of the [!DNL Analytics] companies your account is tied to, and then select the appropriate report suite for the activity. Only report suites that are provisioned to connect to [!DNL Target] are available for selection. If you don't see the report suite that you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again. If the report suite is still missing from the list, contact [Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  [!DNL Analytics for Target] (A4T) requires a tracking server to report results correctly. A default tracking server displays in the [!UICONTROL Tracking Server] field. If you use more than one tracking server, ensure you include the correct tracking server in this field. See [Using an Analytics Tracking Server](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) for more information.

  **[!DNL Adobe Customer Journey Analytics]**: See [[!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) for more information about the integration between [!DNL Adobe Customer Journey Analytics] and [!DNL Target].
  
* **Goal Metric:** Select the success metric that determines whether the activity is successful.
* **Additional Metrics:** Configure additional success metrics to be used in your reports.
* **Audiences for Reporting:** Define audiences that can be used when filtering your reports.

## Other Metadata

Enter notes about your activity.

## Training video: Activity Settings (3:02) ![Tutorial badge](/help/main/assets/tutorial.png)

This video includes information about activity settings.

* Enter an objective for your activity 
* Set the priority level of your activities 
* Schedule activity start and end times 
* Add audiences for reporting to create report filters 
* Enter notes for your activities

>[!VIDEO](https://video.tv.adobe.com/v/17381)
