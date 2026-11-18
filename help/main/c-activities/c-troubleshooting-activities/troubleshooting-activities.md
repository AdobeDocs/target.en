---
keywords: troubleshoot target;troubleshooting target;default content;test not live;activity not live;targeting not working;previous experience displays;cannot create activities;cannot create activities;create activities;page structure changed;page structure modified;error message;error delete profile script;ajax not working
description: Find troubleshooting suggestions should your Adobe [!DNL Target] activity not appear on your site.
title: How Can I Troubleshoot Activities?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
TQID: 'https://experienceleague.adobe.com/L-011t7q6c3aICs0ZrM01m9pZByH86FKGiLG1A7Rl2s'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Get started with troubleshooting activities {#troubleshooting-activities}

>[!BEGINSHADEBOX]

**On this page:** Find solutions to common problems when an [!DNL Adobe Target] activity does not appear on your site or does not behave as expected.

>[!ENDSHADEBOX]

Several causes can prevent an [!DNL Adobe Target] activity from appearing on your site. Use the following problems and suggested solutions to identify the cause and apply the fix.

>[!NOTE]
>
>In addition to the following troubleshooting information, see [Troubleshoot Target](/help/main/r-troubleshooting-target/troubleshooting-target.md) for links to additional troubleshooting topics, FAQs, and other useful information about troubleshooting activities and other features in [!DNL Adobe Target].

## The activity does not display as expected {#not-displayed}

+++ You are seeing default content

Make sure that your activity is complete and has been activated.

+++

</br>

+++ Activity is not live

**Validate:** On the **[!UICONTROL Overview]** tab, check whether the activity is marked inactive or draft.

**Options:**

* Activate the activity.
* Use preview links to display the inactive activity.

+++

</br>

+++ You do not qualify for the audience-targeting conditions

**Validate:** Review the targeting conditions on the **[!UICONTROL Overview]** page.

**Options:**

* Qualify for the audience, then try again.
* Use preview links to bypass the targeting conditions.

+++

</br>

+++ The page does not qualify for the page-targeting conditions

**Validate:** On the **[!UICONTROL Overview]** page, determine whether the page falls outside of the targeting conditions.

**Options:**

* Go to the **[!UICONTROL Visual Experience Composer]**, then click URL > Advanced > current page.

+++

</br>

+++ A previous experience displays rather than the new experience

**Validate:** Try one of the following options, then attempt to view the experience again.

**Options:**

* Clear the cache and cookies, then try again.
* Try a different browser.
* Use private or incognito mode.

+++

</br>

+++ The structure of the page changed since setting up the activity

**Validate:** Go to the **[!UICONTROL Visual Experience Composer]** for the existing activity and look for a warning message that indicates that the selectors (or structure) changed.

**Options:**

* Rebuild the activity.

For more information about how page modifications affect the ability of [!DNL Target] to display content, see [Page Modification Scenarios](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md).

+++

</br>

+++ The structure of the page is modified during page load (at run time)

**Validate:** Ask your developer.

**Note:** For [!DNL Target] to recognize where the activity changes must be applied, avoid dynamically inserting an element with the same class or dynamically modifying the class of any siblings.

**Options:**

* Update the page code to uniquely identify each element that is tested, by using an ID.
* Stop dynamically modifying the class or the siblings as described above.

For more information about how page modifications affect the ability of [!DNL Target] to display content, see [Page Modification Scenarios](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md).

+++

</br>

+++ Other activities are running on the same page

**Validate:** Use the **[!UICONTROL Collisions]** tab to see whether other activities are running.

**Note:** The **[!UICONTROL Collisions]** tab does not work with the Template Testing module.

**Options:**

* Increase the priority of this activity.
* Decrease the priority of the other activities.
* Deactivate the other activities.

+++

## Users, API, and the UI {#users-api-ui}

+++ I created an activity using the [!DNL Target] UI and I cannot update it via API

Activities created using the [!DNL Target] UI should be updated via the [!DNL Target] UI. Activities created via API should be updated via API. For example, if you create an activity using the API, but later edit the activity via the [!DNL Target] UI, not all changes are updated. All changes are stored on the backend and can be updated by making another API call.

As a best practice, update the activity by using the same method (UI or API) that was used to create it.

+++

</br>

+++ You were recently added to [!DNL Target] but cannot create activities

**Validate:** Click **[!UICONTROL Create Activity]**. If the option is not available, you most likely have not been given sufficient rights to create an activity.

**Options:**

After you are added as a user in [!DNL Target], you need the **[!UICONTROL Approver]** role to create activities.

* Ask the administrator of your account to make you an approver.
* If you are the administrator, give yourself the **[!UICONTROL Approver]** role from **[!UICONTROL Administration]** > **[!UICONTROL Users]** in [!DNL Target]. See [Assign yourself the Approver role](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

+++

</br>

+++ You activated an activity using the [!DNL Target] API, but the activity shows a status of [!UICONTROL Inactive] in the [!DNL Target] UI

When you perform certain actions, such as activating an activity outside of the UI by using the [!DNL Target] API, the update can take up to ten minutes to propagate to the UI.

+++

</br>

+++ An error message appears when you delete a profile script

**Validate:** Deleting a profile script from [!DNL Target] displays the error message "Failed to delete profile script."

**Options:**

Do one of the following:

* Delete the profile script again. The success message appears.
* Wait about 10 minutes for the [!DNL Target] importer to run. The importer updates the profile script list.

+++

## Calls and conversion {#calls-and-conversion}

+++ Some ajax [!DNL Target] calls are not working

**Note:** Multiple ajax [!DNL Target] calls with the same name but different parameters do not work on the same page. Only the first call is made.

+++

</br>

+++ After activity conversion, the visitor is not in any experience

In rare cases, if the conversion metric of the activity that qualifies a visitor for an experience is sent in the same request as the activity qualification, the visitor might not be in any experience after the request is sent. In this situation, the visitor sees default content and the experience ID captured via tokens is -1. [!DNL Adobe] does not recommend sending activity qualification and conversion in the same [!DNL Target] request.

If you want to send both metrics in the same request, you can use **[!UICONTROL Advanced Settings]** to specify that the visitor stays in the same experience after conversion.

+++
