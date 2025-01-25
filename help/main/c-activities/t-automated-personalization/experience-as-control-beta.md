---
keywords: experience;control;automated personalization;auto-target
description: Learn how to select an experience to be used as a control while creating an [!UICONTROL Automated Personalization] (AP) or [!UICONTROL Auto-Target] activity in [!DNL Adobe Target].
title: How Can I Use a Specific Experience as Control in an [!UICONTROL Automated Personalization] Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
hide: yes
hidefromtoc: yes
exl-id: baf939d8-1f6d-4586-8323-69f818a5ef1a
---
# Select the control for your [!UICONTROL Automated Personalization] or [!UICONTROL Auto-Target] activity

You can select a randomly served experience or a specific experience to be used as a control while creating an [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activity.

This feature lets you route the control traffic to the relevant experiences, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against control traffic to that control.

The options for setting a control in [!UICONTROL Automated Personalization] and [!UICONTROL Auto-Target] activities are a little different from other activity types. In a manual [!UICONTROL A/B Test], you can change what reporting shows as your control, and lift is calculated based on the conversion rate of that control experience. You can make this change easily because traffic is served randomly to each of the experiences you included in your activity, no matter what the control is initially set to. In other words, selecting the control doesn't impact how traffic is served. In [!UICONTROL Automated Personalization] and [!UICONTROL Auto-Target] activities, your decision on what to choose as the control does impact how the visitor traffic is served. As a result, you must think more carefully about your decision.

There are two options available for your control in your [!UICONTROL Automated Personalization] and [!UICONTROL Auto-Target] activities:

* **Randomly served**: For a random control, the control percentage of traffic randomly serves all experiences in the activity, without considering that visitor's profile. You can think of the control as helping answer the question, "If I just randomly serve an experience (or offer) to visitors and don't consider their profiles, what is the conversion rate for that experience (or offer)?" The control is like an [!UICONTROL A/B Test] within your AI activity. Having this information of the non-personalized conversion rate for each experience or offer can be helpful to understand when analyzing your activity results.

* **Specific experience**: A specific experience control lets you compare your traffic served by [!DNL Target] personalization models to a specific marketer-defined experience (for example, your default homepage). With this option, the control percentage of traffic randomly serves traffic for only that one experience.

## Specify a specific experience as control

1. While creating or editing an [[!UICONTROL Automated Personalization] activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) or [[!UICONTROL Auto-Target] activity](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configure the experiences as desired.
1. On the [!UICONTROL Targeting] page (step 2 of the three-part guided workflow), select the desired experience as the control.
1. Specify the desired traffic allocation for the control experience and the other experiences.

   For a specific experience control, 10% to 30% is advised.

1. Continue with the [!UICONTROL Goals & Settings] page.

## Known limitations and considerations

Keep the following points in mind when using a specific experience as a control:

* Changing the control experience in an already live activity isn't advised. The latest control experience selected is named in reporting (even if older reports are based on another experience).
* Deleting the control experience isn't advised.
* Adding many new offers or experiences to a live activity with a specific experience as the control is not advised.
* In [!UICONTROL Automated Personalization] activities, including targeting on the control experience that could further constrain who can see that experience isn't advised.
* In [!UICONTROL Automated Personalization] activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. Lift and confidence information is available at the overall "targeted" versus "control" traffic level for the [!UICONTROL Automated Personalization] activity. Lift and confidence information is available if "random" is selected as the control. This difference is because comparing a specific experience's conversion rate to an offer's conversion rate isn't logical due to the difference in units. The information available in an [!UICONTROL Auto-Target] activity is the same, no matter what type of control is selected.
* Because all control traffic goes to a single experience or set of offers when you select the experience as control (compared to random, where the control traffic amount is split over the number of experiences or offers in your activity), you generally do not need as much traffic to flow to the control. 10% is a good place to start.
* If you do one of the following to a live activity with a specific experience as a control, the control is automatically reset to randomly served experiences (instead of the previously selected specific experience):

  * Delete an experience
  * Remove a location or offer ([!UICONTROL Automated Personalization] only)
  * Exclude an experience manually, via removing duplicate offers or via an exclusion group ([!UICONTROL Automated Personalization] only)
