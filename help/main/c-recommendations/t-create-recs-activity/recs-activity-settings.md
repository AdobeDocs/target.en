---
keywords: Recommendations;Settings;name;objective;priority;duration;reporting settings;other metadata
description: Learn how to configure the settings used to describe and control a Recommendations activity in Adobe Target.
title: How Do I Configure Recommendations Activity Settings?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
TQID: 'https://experienceleague.adobe.com/pfMAvl6MmLCtH3PZfOR4Ve-WFIc3e2iN2Bh-cIzjeC0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Recommendations activity settings {#recs-activity-settings}

>[!BEGINSHADEBOX]

**On this page:** Learn about the settings that describe and control a [!DNL Recommendations] activity in [!DNL Adobe Target].

>[!ENDSHADEBOX]

Activity settings identify a [!DNL Recommendations] activity, control when and where it displays, and define how its results are reported.

## Name

Click the More Actions icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallListVert.svg) ), then click **[!UICONTROL Rename]** to give the activity a descriptive name that helps identify it.

The following characters are not allowed in an activity name: `/`, `?`, `#`, `:`, `=`, `+`, `-`, and `@`.

If the name of a [!DNL Recommendations] activity already exists for another activity in [!UICONTROL Recommendations Classic], the new activity is resynced with a new name. The new name is the original name with a timestamp appended, to make it unique. It displays in both [!DNL Target Standard/Premium] and [!UICONTROL Recommendations Classic].

## Objective

(Optional) Describe the goal of the activity.

## Priority

Adjust the slider to set the priority level.

The priority is used when multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.

## Duration

Set the duration of the activity.

The activity can start when it is activated, or at a specific date and time. Likewise, it can end when it is deactivated, or at a specific date and time.

The time picker uses a 24-hour clock, with 00:00 being midnight. The time zone is the one configured in the browser. To use a different time zone, set the browser to that time zone and restart the browser.

## Reporting Settings

The following settings define how the results of the activity are reported.

* **[!UICONTROL Reporting Source]:** Specifies the solution that the data is collected from: [!DNL Adobe Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics].

  If a reporting solution is specified in the [account settings](/help/main/administrating-target/reporting.md), that solution is used and this setting is not visible. The reporting source cannot be changed after the activity goes live, to keep reports consistent.

  **[!DNL Adobe Analytics]**: See [[!DNL Adobe Analytics] as the reporting source for [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) for the differences between the reporting solutions and the advantages of each. For the selection of the [!DNL Analytics] report suite and the tracking server, see [Reporting Source](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source).

  **[!DNL Adobe Customer Journey Analytics]**: See [[!DNL Target] reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) for more information about the integration between [!DNL Adobe Customer Journey Analytics] and [!DNL Target].

* **[!UICONTROL Goal Metric]:** Selects the success metric that determines whether the activity is successful.
* **[!UICONTROL Additional Metrics]:** Configures additional success metrics for the reports.
* **[!UICONTROL Audiences for Reporting]:** Defines audiences that can be used to filter the reports.

## Other Metadata

Enter notes about the activity.

## Training video: Activity Settings (3:02) ![Tutorial badge](/help/main/assets/tutorial.png)

This video covers the following activity settings:

* Enter an objective for the activity.
* Set the priority level of the activity.
* Schedule the start and end times.
* Add audiences for reporting to create report filters.
* Enter notes for the activity.

>[!VIDEO](https://video.tv.adobe.com/v/17381) 
