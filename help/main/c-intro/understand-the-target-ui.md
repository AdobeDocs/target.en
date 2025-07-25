---
keywords: target user interface;user interface;ui;announcements;events;notifications
description: Familiarize yourself with the user interface and find links to more in-depth information to help you get the most out of [!DNL Target].
title: How Do I Use the [!DNL Target] UI?
feature: Overview
exl-id: ce4c72b2-b635-406b-9830-650816445a64
---
# Understand the [!DNL Target] UI

The user interface is arranged in a logical and user-friendly format to help you get the most out of [!DNL Adobe Target]. The following brief overview helps you get familiarized with [!DNL Target] and provides links for more in-depth information and step-by-step instructions.

{{updated-ui}}

## [!DNL Target] UI header

The header at the top of the [!DNL Target] UI contains tabs and options to help you navigate the different capabilities of the solution. You can also switch organizations and [!DNL Adobe Experience Cloud] solutions, provide feedback if you are part of a Beta program, access AI Assistant, get help and notifications, manage your [!DNL Adobe] profile, and log out of [!DNL Target].

![Target header](/help/main/c-intro/assets/target-header.png)

The tabs along the left side let you access the various capabilities of [!DNL Target], which is discussed later. Let's start by discussing the options on the right side before discussing the tabs.

### [!UICONTROL Organization]

An *organization* is the entity that enables an administrator to configure groups and users, and to control single sign-on in the [!DNL Adobe Experience Cloud]. The organization functions like a log-in company that spans all the [!DNL Experience Cloud] products and solutions. Most often, an organization is your company name. However, a company can have many organizations.

Select the desired organization from the [!UICONTROL Organization] drop-down list if your company has multiple organizations:

![Organization drop-down list](/help/main/c-intro/assets/organizations.png)

### [!UICONTROL Beta Feedback]

(Conditional) If you are part of an official [!DNL Target] Beta program, you might see the [!UICONTROL Beta Feedback] icon. 

![Beta Feedback icon](/help/main/c-intro/assets/beta-feedback.png)

Provide a description for your feedback, include applicable files or screenshots, and any additional details, as necessary, then click **[!UICONTROL Submit]**.

### [!DNL AI Assistant]

(Conditional) If you have been granted the rights to use [!DNL AI Assistant] by your organization, click the [!DNL AI Assistant] icon.

For more information, see [Adobe Experience Platform AI Assistant overview](/help/main/c-intro/ai-assistant.md).

### Help

Clicking the [!UICONTROL Help] icon ( ![Help icon](/help/main/assets/icons/HelpOutline.svg) ) lets you access information, videos, blogs, and more to help you use [!DNL Target] more effectively. You can create a support ticket, find support telephone numbers, ask questions via Twitter, or provide feedback about [!DNL Target] to let us know how the [!DNL Target] team is doing.

![Help](/help/main/c-intro/assets/help.png)

### Requests, notifications, and announcements {#notifications-announcements}

The [!UICONTROL Requests], [!UICONTROL Notifications], and [!UICONTROL Announcements] panels help keep you up to date about all things [!DNL Adobe Target]. Proactive notifications help keep you abreast of the status of [!DNL Adobe Experience Cloud] solutions and [!DNL Target] events. Proactive announcements alert you to outage events and maintenance events.

Click the [!UICONTROL Notifications] icon ( ![Notifications icon](/help/main/assets/icons/Bell.svg) ) from the header to view notifications:

The panel contains tabs for [!UICONTROL Requests], [!UICONTROL Notifications], and [!UICONTROL Announcements].

![Notifications](assets/notifications.png)

The following sections contain information about each tab, and how to configure notifications and announcements:

#### [!UICONTROL Requests]

Receive important information about [!DNL Adobe] products and solutions, your collaboration with fellow users, and other relevant updates in the [!UICONTROL Requests] panel.

When someone sends you a request to approve an object or to grant access to an object, that request displays in the [!UICONTROL Requests] panel.

#### Notifications {#notifications}

[!DNL Target] event notifications include the following:

* **Activities**: Notifications for all activity types when an activity is approved or deactivated, either manually or when it reaches its start or end date. The notification includes the name of the activity with a link to the activity's overview page.

  Notifications are configurable and are received, by default, by product admins, publishers, and approvers in the activity's workspace for [!DNL Target Premium] accounts. For [!DNL Target Standard] accounts, notifications are received by all publishers and approvers.

  Notifications are formatted like the following samples:

  * `Activity {target.activity.name} has been activated`
  
  * `Activity {target.activity.name} has been deactivated`

* **Profile scripts**: Notifications when a profile script is activated or deactivated, either manually or by [!DNL Target].

  Notifications are configurable and are received, by default, by product admins and approvers for both [!DNL Target Premium] and [!DNL Target Standard] accounts.

  Notifications are formatted like the following samples:

  * `Profile Script {target.profileScript.name} has been activated`
  * `Profile Script {target.profileScript.name} has been deactivated`

* **Recommendations feeds**: Notifications when a [!DNL Recommendations] feed is activated or deactivated, either manually or by [!DNL Target]. Notifications are also sent when a [!DNL Recommendations] feed fails.

  Notifications are configurable and are received, by default, by product admins and approvers for [!DNL Target Premium] accounts. [!DNL Recommendations] is a [!DNL Target Premium] feature and is not available in [!DNL Target Standard].

  Notifications are formatted like the following samples:

  * `Feed  {target.feed.name} has been activated`
  * `Feed {target.feed.name} has been deactivated`
  * `Feed {target.feed.name} has failed`
  * `Feed {target.feed.name} has failed to import from source`

You can mark individual notifications as read by hovering over the desired notification and then clicking the [!UICONTROL Mark as Read] ( ![Mark as Read icon](/help/main/assets/icons/CheckmarkCircle.svg) ) icon. You can mark all notifications as read or view all notifications by clicking [!UICONTROL Mark as Read] or [!UICONTROL View All] at the bottom of the panel.

You can also set a reminder to be notified again by hovering over a notification, clicking the [!UICONTROL Snooze] ( ![Snooze icon](/help/main/assets/icons/Clock.svg) ) icon. You can then select when you want to be notified: 5 minutes, 15 minutes, one hour, or tomorrow.

#### Announcements

Proactive announcements alert you to outage events and maintenance events.

More in-depth information can be found on the [Adobe Status](https://status.adobe.com/) page.

### Configure notifications and announcements

To edit your notifications preferences:

1. Click the [!UICONTROL Edit Preferences] ( ![Edit Preferences icon](/help/main/assets/icons/Setting.svg) ) icon, then click **[!UICONTROL Notifications]** in the left rail.
1. Under **[!UICONTROL Target]**, select how you want to be notified:

   * [!UICONTROL In-app]
   * [!UICONTROL Email]
   * [!DNL Slack]

1. Select the categories that you want to be considered high priority.

   >[!NOTE]
   >
   >"[!UICONTROL New releases]" and "[!UICONTROL Updates on content]" are the only notification categories that apply to [!DNL Target]. The other categories apply to other [!DNL Adobe] solutions.

1. Select the notifications for which you would like to see alerts display in your browser. 

   These alerts appear in the top-right corner of your browser for a few seconds. You can choose to see high-priority categories, all categories, or to hide all notification pop-ups. You can also configure if you want the notifications to remain visible until you dismiss them or you can configure the notification duration.

1. Select the frequency at which you want to receive notification emails:

   * [!UICONTROL Don't send emails]
   * [!UICONTROL Instant notifications]
   * [!UICONTROL Daily digest]
   * [!UICONTROL Weekly digest]

1. Configure Slack notifications for a workspace. 

### Apps switcher

The Apps switcher lets you quickly access the [!DNL Adobe Experience Cloud] solutions that you have access to.

![Apps switcher](/help/main/c-intro/assets/apps.png)

### Profile

Click your profile avatar to edit your [!DNL Adobe Experience Cloud] preferences or to sign out of [!DNL Target]. You can also access or edit your [!DNL Adobe] profile.

![Profile avatar](/help/main/c-intro/assets/change-language.png)

Now, let's discuss the tabs along the left side of the [!DNL Target] header.

## Activities

The **[!UICONTROL Activities]** list is the default view when you open [!DNL Target]. You can create activities from this page and manage existing activities.

See [Activities](/help/main/c-activities/activities.md) for in-depth information about the activity types available in [!DNL Target] and to learn more about the [!UICONTROL Activity] list's user interface.

## Audiences

Click the **[!UICONTROL Audiences]** tab to display the [!UICONTROL Audiences] list where you can create audiences and manage existing audiences.

An audience is a group of similar activity entrants who see a targeted activity. An audience is a group of people with the same characteristics, such as a new visitor, a returning visitor, or returning visitors from the Midwest. The [!UICONTROL Audience] feature allows you to target different content and experiences to specific audiences to optimize your digital marketing by displaying the right messages to the right people at the right time. If a visitor is identified as part of a target audience, [!DNL Target] determines which experience to display, based on criteria defined during activity creation.

See [Create audiences](/help/main/c-target/c-audiences/create-audience.md) for in-depth information about the audience types in [!DNL Target] and to learn more about the [!UICONTROL Audience] list's user interface.

## Offers

Click the **[!UICONTROL Offers]** tab to display the [!UICONTROL Offers] list where you can create experiences and offers and manage existing experiences and offers.

An experience can be an offer, image, text, button, video, combination of these various elements on a page, an entire web page, or a set of pages that perhaps form a purchase funnel or some other logical sequence of pages. It can also be the response of a voice assistant, a customer service script, or even a personalized flavor from a drink machine. You test or personalize experiences in [!DNL Target] activities.

See [Offers](/help/main/c-experiences/c-manage-content/manage-content.md) for in-depth information about the offer types in [!DNL Target] and to learn more about the [!UICONTROL Offer] list's user interface.

## Recommendations

Click the **[!UICONTROL Recommendations]** tab to access [!DNL Target Recommendations].

>[!NOTE]
>
>[!UICONTROL Recommendations] activities are available as part of the [!DNL Target Premium] solution. [!UICONTROL Recommendations] activities are not available in [!DNL Target Standard] without a [!DNL Target Premium] license. For more information, see [Target Premium](/help/main/c-intro/intro.md#premium) in *Introduction to Target*.

[!UICONTROL Recommendations] activities automatically display products or content that might interest your customers based on previous user activity or other algorithms. Recommendations help direct customers to relevant items that they might otherwise not know about.

See [Recommendations](/help/main/c-recommendations/recommendations.md) for in-depth information about [!UICONTROL Recommendations] in [!DNL Target] and to learn more about the [!UICONTROL Recommendations] user interface.

## Administration

Click the **[!UICONTROL Administration]** tab to access the [!UICONTROL Administration] pages.

The [!UICONTROL Administration] pages let you administer [!DNL Target], including configuration settings for the [!UICONTROL Visual Experience Composer] (VEC), reporting, [!DNL Scene7] configuration, implementation, hosts, environments, response tokens, users, and recommendations.

See [Administer Target overview](/help/main/administrating-target/administrating-target.md) for in-depth information and to learn more about the user interface.

## Visual Experience Composer (VEC)

In addition to the [!DNL Target] UI, you should familiarize yourself with the VEC UI. For more information, see [[!DNL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md). 
