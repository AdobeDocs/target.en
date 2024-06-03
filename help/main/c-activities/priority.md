---
keywords: settings;priority
description: Learn how [!DNL Adobe Target] determines which activity (or activities) to deliver to a page differently depending on which [!DNL Target] interface and which activity creation function you're using.
title: How Does [!DNL Target] Assign Priority to Different Activities?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
---
# Priority

[!DNL Adobe Target] determines which activity (or activities) to deliver to a page differently depending on which [!DNL Target] interface and which activity creation function ([[!UICONTROL Visual Experience Composer (VEC)]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) or [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md)) you're using.

## [!UICONTROL Visual Experience Composer] only or [!UICONTROL Form-Based Experience Composer] using a global [!DNL Target] request only {#section_4A0A317DFED345649B58B0CB5B410C8B}

If your company uses the VEC exclusively, content from multiple activities can be returned for the same call. Activities are delivered using the following decision flow:

1. The [!DNL Target] server call comes to [!DNL Target] with information about the URL. 
1. [!DNL Target] pulls every activity running on that URL. 
1. [!DNL Target] attempts to match the visitor into activities.

   If the visitor is already in an [!UICONTROL A/B Test] or [!UICONTROL Multivariate Test] activity, they match into that activity until they convert. If they were previously in an [!UICONTROL Experience Targeting] activity, they must match into it again. If they meet the audience rules, then the visitor falls into those activities and into specific experiences. 

1. Content for all the activities and experiences the visitor matches is returned to the page. 
1. If the content for each activity references different [CSS selectors](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337), then all content is displayed.

   If there is an overlap or a duplicated CSS selector, then the activity content with the highest priority is displayed. The results from all activities that run on the page are counted and reflected in the reports.

   >[!IMPORTANT]
   >
   >[!DNL Target] returns the content for all activities on the page, beginning with the lowest-priority content, which is then overwritten by each activity, from lowest to highest priority. Usually, this results in the highest-priority content being displayed. However, if a lower-priority activity alters the structure of the DOM for the page, it is possible that the higher-priority activity does not recognize the page structure, so the lower-priority content is displayed. The results from all activities that run on the page are counted and reflected in the reports.

1. If multiple activities share priority level, there are two tiebreakers:

    * If only one activity has audience targeting, that activity is displayed. 
    * If all or none has targeting, then the activity that was approved first is displayed.

## [!UICONTROL Form-Based Experience Composer] and [!UICONTROL Visual Experience Composer] {#section_4620253E1CE942DD830724C7822B175F}

If your company uses the [!UICONTROL Form-Based Experience Composer] *and* the VEC, content from multiple [!UICONTROL Form-Based Experience Composer] and VEC activities can deliver. Previously, only one activity from the form-based workflow could deliver. There is no longer a limit to the number of form-based activities that can deliver. 

Activity delivery is determined using the following decision flow:

1. [!DNL Target] server call comes to [!DNL Target] with information about the [!DNL Target] request and URL. 
1. [!DNL Target] pulls every activity running in that [!DNL Target] request. 
1. [!DNL Target] attempts to match the visitor into activities.

   If the visitor is already in an [!UICONTROL A/B Test] or [!UICONTROL Multivariate Test] activity, they match into that test until they convert. If they were previously in an [!UICONTROL Experience Targeting] activity, they must match into it again. If they meet the audience rules, then the visitor falls into those activities and into specific experiences. 

1. If a form-based activity is the highest priority, then that activity content is returned along with all matching activity content from VEC activities. 
1. If a VEC activity is the highest priority, then content from all matching VEC activities is returned, but no form-based activity content is returned.

   The results from all activities that run on the page are counted and reflected in the reports.

**Example**

If you have two activities, one targeting the branded search keyword "Nike" and the second targeting the non-branded keyword "sneakers", the priorities of both activities are checked. If the Nike activity has a higher priority, that content is displayed. If the sneakers activity has the higher priority, its content is displayed.

If both targeted activities have the same priority, the activity that was most recently viewed is displayed. If the visitor is new to the page, the activity that was activated most recently is displayed.

## [!UICONTROL Form-Based Experience Composer] with non-global [!DNL Target] requests {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

If your company uses [!DNL Target] requests other than the global [!DNL Target] request in the form-based composer, content from only one activity can be returned per call. Activity delivery is determined using the following decision flow:

1. The [!DNL Target] server call comes to [!DNL Target] with information about the [!DNL Target] request and URL. 
1. [!DNL Target] pulls every activity running in that [!DNL Target] request. 
1. [!DNL Target] attempts to match the visitor into the highest-priority activity.

   If the visitor is already in an [!UICONTROL A/B Test] or [!UICONTROL Multivariate Test] activity, they match into that activity until they convert. If they were previously in an [!UICONTROL Experience Targeting] activity, they must match into it again. If they meet the audience rules, then the visitor falls into those activities and into specific experiences. 

1. If multiple activities share priority level, there are two tiebreakers:

    * If only one activity has audience targeting, that activity is displayed. 
    * If all or none has targeting, then the activity that was approved first is displayed.

## Examples {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Depending on your settings, the priority values vary. You can use the legacy settings of [!UICONTROL Low], [!UICONTROL Medium], or [!UICONTROL High], or you can enable fine-grained priorities from 0 to 999. For more information, see [Activity settings](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

Response: offer1

**Two activities use only offers created in the [!UICONTROL Visual Experience Composer] for different selectors**

* Activity 1: target-global-mbox, selector1, visualExpCompOffer1, priority low 
* Activity 2: target-global-mbox, selector2, visualExpCompOffer2, priority high

Response: visualExpCompOffer1, visualExpCompOffer2

**Two activities use only offers created in the [!UICONTROL Visual Experience Composer] for same selector**

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
