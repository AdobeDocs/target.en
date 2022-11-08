---
keywords: troubleshoot target;troubleshooting target;default content;test not live;activity not live;targeting not working;previous experience displays;cannot create activities;can't create activities;create activities;page structure changed;page structure modified;error message;error delete profile script;ajax not working
description: Find troubleshooting suggestions should your Adobe [!DNL Target] activity not appear on your site.
title: How Can I Troubleshoot Activities?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
---
# Troubleshoot activities

If your [!DNL Adobe Target] activity does not appear on your site, these troubleshooting suggestions should help you find your solution.

>[!NOTE]
>
>In addition to the following troubleshooting information, see [Troubleshooting Target](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) for links to additional troubleshooting topics, FAQs, and other useful information about troubleshooting activities and other features in [!DNL Adobe Target].

The following sections contain problems that you might encounter with suggested solutions.

## I created an activity using the [!DNL Target] UI and I cannot update it via API.

Activities created using the [!DNL Target] UI should be updated via the [!DNL Target] UI. Activities created via API should be updated via API. If you originally create an activity using the API, for example, but then later edit the activity via the [!DNL Target] UI, not all changes are updated. All changes are stored on the backend and can be updated by making another API call.

As best practice, try updating the activity using the same method (UI or API) that was used to originally create the activity.

## You are seeing default content.

Make sure that your activity is complete and has been activated.

## Activity is not live.

**Validate:** Go to [!UICONTROL Overview] tab and see if test is marked inactive or draft.

**Options:**

* Activate test.  
* Use Preview Links to display inactive test.

## You don't qualify for the audience-targeting conditions.

**Validate:** Review targeting conditions on overview page.

**Options:**

* Qualify and try again.
* Use Preview Links to bypass targeting conditions.

## The page doesn't qualify for the page-targeting conditions.

**Validate:** On the [!UICONTROL Overview] page, determine if the page falls outside of the targeting conditions.

**Options:**

* Go to the [!UICONTROL Visual Experience Composer], click URL > Advanced >current page.

## A previous experience displays rather than the new experience.

**Validate:** Try one of the options below and attempt to view the experience again.

**Options:**

* Clear cache and cookies, then try again.
* Try a different browser.
* Use Private/Incognito mode.

## You were recently added to [!DNL Target] but cannot create activities.

**Validate:** Click [!UICONTROL Create Activity]. If the option is not available, you most likely have not been given sufficient rights to create an activity.

**Options:**

After you are added as a user in [!DNL Target], you need to have the [!UICONTROL Approver] role in order to create activities.

* Ask the Admin of your account to make you an approver.
* If you are the Admin, give yourself the [!UICONTROL Approver] role from **[!UICONTROL Administration]** > **[!UICONTROL Users]** in [!DNL Target]. 

  See [Assign Yourself the Approver Role](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## The structure of the page changed since setting up activity.

**Validate:** Go to the [!UICONTROL Visual Experience Composer] for the existing activity. Look for warning message indicating that the selectors (or structure) has changed.

**Options:**

* Rebuild the activity.

For more information about how page modifications affect [!DNL Target]'s ability to display, see [Page Modification Scenarios](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## The structure of the page is modified during page load (at run time).

**Validate:** Ask developer.

**Note:** In order for [!DNL Target] to recognize where activity changes should be applied, avoid dynamically inserting an element with the same class or dynamically modifying the class of any siblings.

**Options:**

* Update page code to uniquely identify each element that is tested (using an id).
* Stop dynamically modifying the class or siblings as described above.

For more information about how page modifications affect [!DNL Target]'s ability to display, see [Page Modification Scenarios](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Other activities are running on the same page.

**Validate:** Use the [!UICONTROL Collisions] tab to see if other activities are running.

**Note:** The [!UICONTROL Collisions] tab does not work with the Template Testing module.

**Options:**

* Increase the priority of this activity.
* Decrease the priority of other activities.
* Deactivate other activities.

## An error message appears when you delete a profile script.

**Validate:** Deleting a profile script from [!DNL Target] displays the error message, "Failed to delete profile script."

**Options:**

Do one of the following:

* Delete the profile script again. The success message appears.
* Wait about 10 minutes for the [!DNL Target] importer to run. The importer updates the profile script list.

## Some ajax [!DNL Target] calls are not working.

**Note:** Multiple ajax [!DNL Target] calls with the same name but different parameters does not work on the same page. Only the first call is made.

## You activated an activity using the [!DNL Target] API, but the activity shows a status of [!UICONTROL Inactive] in the [!DNL Target] UI.

When you perform certain actions, such as activating an activity outside of the UI using the [!DNL Target] API, the update can take up to ten minutes to propagate to the UI.

## After activity conversion, the visitor is not in any experience. 

If the activity's conversion metric to qualify for an experience is sent in the same [!DNL Target] request as activity qualification, the visitor might not be in any experience after the request is sent. In this situation, the visitor sees default content. [!DNL Adobe] recommends not sending activity conversion and qualification in the same request. 

If you want to send both settings in the same request, you can use [!UICONTROL Advanced Settings] to specify that the visitor stays in the same experience after conversion. 
