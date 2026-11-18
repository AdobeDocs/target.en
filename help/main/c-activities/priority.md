---
keywords: settings;priority
description: Learn how [!DNL Adobe Target] determines which activity (or activities) to deliver to a page differently depending on which [!DNL Target] interface and which activity creation function you are using.
title: How Does [!DNL Target] Assign Priority to Different Activities?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
TQID: 'https://experienceleague.adobe.com/KSkJ1CDkd4hgwnLQ1RKn8l8r2MDIO-6flcHcdN0c0oQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Priority {#priority}

>[!BEGINSHADEBOX]

**On this page:** Learn how [!DNL Adobe Target] decides which activities to deliver to a page, depending on the experience composer and the type of [!DNL Target] request in use.

>[!ENDSHADEBOX]

[!DNL Adobe Target] determines which activity (or activities) to deliver to a page differently depending on which [!DNL Target] interface and which activity creation function ([**[!UICONTROL Visual Experience Composer (VEC)]**](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) or [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md)) you are using. The following table summarizes the three cases, which are detailed in the sections below.

| Scenario | Activities that can deliver | Content returned |
|---|---|---|
| **[!UICONTROL Visual Experience Composer]** only, or **[!UICONTROL Form-Based Experience Composer]** with a global [!DNL Target] request only | Multiple | Content of all matching activities. If selectors overlap, the content of the highest-priority activity is displayed. |
| **[!UICONTROL Form-Based Experience Composer]** and **[!UICONTROL Visual Experience Composer]** | Multiple | If a form-based activity has the highest priority, its content and the content of all matching VEC activities. If a VEC activity has the highest priority, the content of all matching VEC activities only. |
| **[!UICONTROL Form-Based Experience Composer]** with non-global [!DNL Target] requests | One per call | Content of the highest-priority matching activity. |

## VEC, or [!UICONTROL Form-Based Experience Composer] with a global request {#section_4A0A317DFED345649B58B0CB5B410C8B}

If your company uses the VEC exclusively, content from multiple activities can be returned for the same call. Activities are delivered using the following decision flow:

1. The [!DNL Target] server call reaches [!DNL Target]. The call carries information about the URL of the page that is requested.
1. [!DNL Target] pulls every activity that is running on that URL. These activities are the candidates for delivery.
1. [!DNL Target] attempts to match the visitor into the candidate activities.

   {{visitor-matching}}

1. Content for all the activities and experiences that the visitor matches is returned to the page, so content from several activities can be delivered for the same call.
1. [!DNL Target] compares the [CSS selectors](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) that the content of each activity references. If the activities reference different selectors, all content is displayed.
1. If a selector overlaps or is duplicated, the content of the highest-priority activity is displayed.

   >[!IMPORTANT]
   >
   >[!DNL Target] returns the content for all activities on the page, beginning with the lowest-priority content, which is then overwritten by each activity, from lowest to highest priority. Usually, this results in the highest-priority content being displayed. However, if a lower-priority activity alters the structure of the DOM for the page, the higher-priority activity might not recognize the page structure, so the lower-priority content is displayed.

1. If multiple activities share a priority level, a tiebreaker applies. If only one of the activities has audience targeting, that activity is displayed. If all or none of the activities have targeting, the activity that was approved first is displayed.
1. The results from all activities that run on the page are counted and reflected in the reports.

## [!UICONTROL Form-Based Experience Composer] and VEC {#section_4620253E1CE942DD830724C7822B175F}

If your company uses the [!UICONTROL Form-Based Experience Composer] *and* the VEC, content from multiple [!UICONTROL Form-Based Experience Composer] and VEC activities can be delivered. Previously, only one activity from the form-based workflow could deliver. There is no longer a limit to the number of form-based activities that can deliver.

Activity delivery is determined using the following decision flow:

1. The [!DNL Target] server call reaches [!DNL Target]. The call carries information about the [!DNL Target] request and the URL.
1. [!DNL Target] pulls every activity that is running in that [!DNL Target] request. These activities are the candidates for delivery.
1. [!DNL Target] attempts to match the visitor into the candidate activities.

   {{visitor-matching}}

1. [!DNL Target] checks which of the matching activities has the highest priority, and whether that activity was created in the [!UICONTROL Form-Based Experience Composer] or in the VEC.
1. If a form-based activity has the highest priority, its content is returned along with the content of all matching VEC activities.
1. If a VEC activity has the highest priority, the content of all matching VEC activities is returned, but no form-based activity content is returned.
1. The results from all activities that run on the page are counted and reflected in the reports.

**Example**

Two activities exist: one targets the branded search keyword "Nike" and the other targets the non-branded keyword "sneakers". The priorities of both activities are checked. If the Nike activity has a higher priority, its content is displayed. If the sneakers activity has the higher priority, its content is displayed.

If both targeted activities have the same priority, the activity that was most recently viewed is displayed. If the visitor is new to the page, the activity that was activated most recently is displayed.

## [!UICONTROL Form-Based Experience Composer] with non-global requests {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

If your company uses [!DNL Target] requests other than the global [!DNL Target] request in the form-based composer, content from only one activity can be returned per call. Activity delivery is determined using the following decision flow:

1. The [!DNL Target] server call reaches [!DNL Target]. The call carries information about the [!DNL Target] request and the URL.
1. [!DNL Target] pulls every activity that is running in that [!DNL Target] request. These activities are the candidates for delivery.
1. [!DNL Target] attempts to match the visitor into the highest-priority candidate activity.

   {{visitor-matching}}

1. If multiple activities share a priority level, a tiebreaker applies. If only one of the activities has audience targeting, that activity is displayed. If all or none of the activities have targeting, the activity that was approved first is displayed.
1. Content from that single activity is returned to the page.

## Examples {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Depending on your settings, the priority values vary. You can use the legacy settings of **[!UICONTROL Low]**, **[!UICONTROL Medium]**, or **[!UICONTROL High]**, or you can enable fine-grained priorities from 0 to 999. For more information, see [Activity settings](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC).

**Two activities use only offers created in the [!UICONTROL Visual Experience Composer] for different selectors**

* Activity 1: target-global-mbox, selector1, visualExpCompOffer1, priority low
* Activity 2: target-global-mbox, selector2, visualExpCompOffer2, priority high

Response: visualExpCompOffer1, visualExpCompOffer2

**Two activities use only offers created in the [!UICONTROL Visual Experience Composer] for the same selector**

* Activity 1: target-global-mbox, selector1, visualExpCompOffer1, priority low
* Activity 2: target-global-mbox, selector1, visualExpCompOffer2, priority high

Response: visualExpCompOffer1, visualExpCompOffer2

## Training video: Activity Settings (3:02)

This video includes information about activity settings.

* Enter an objective for your activity
* Set the priority level of your activities
* Schedule activity start and end times
* Add audiences for reporting to create report filters
* Enter notes for your activities

>[!VIDEO](https://video.tv.adobe.com/v/17381)
