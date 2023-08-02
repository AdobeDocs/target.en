---
keywords: activities list;activities;activity;activity types;edit activity;activity actions;activity attribute;activity list filter;activity limitations;personalize;personalization
description: Learn how activities in Adobe [!DNL Target] let you personalize content to specific audiences and test page designs
title: How Can I Personalize Content and Test Page Designs with Target?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
---
# Activities

Activities in [!DNL Adobe Target] let you personalize content to specific audiences and test page designs.

For example, you might design an activity that tests two different landing pages, one that highlights information about women's summer shoes, and another landing page that highlights more general summer apparel. The activity determines the conditions that control when each of these landing pages appears, and the metrics that determine which page is more successful. The activity is configured to start and end when specific conditions are met, such as between specific dates, or to start when the activity is approved and to end when it is deactivated.

When designing an activity, you should plan carefully. Determine when the activity will start and how long it will last. Then, list your offers and assign a target audience to each one.

## Activities list {#section_DE8E2DB30D534962A931EF8BB48240F5}

The [!UICONTROL Activities] list is the default view when you open [!DNL Target]. You can create new activities from this page and manage existing activities.

You can also display the [!UICONTROL Activities] list by clicking the [!UICONTROL Activities] tab at the top of the [!DNL Target] UI.

![Activities list](/help/main/c-activities/assets/activities-list-new.png)

The [!UICONTROL Activities] list provides an overview of all activities and lets you perform various actions:

| Element | Description |
|--- |--- |
|Left-navigation rail|Switch between your saved or live activities and failed or [draft activities](/help/main/c-activities/edit-activity.md).|
|Search box|Quickly find an activity or narrow the activities displayed in the [!UICONTROL Activity] list. You can search by [!UICONTROL Name], [!UICONTROL URL], or [!UICONTROL ID].|
|[!UICONTROL Create Activity]|Create a new activity. For more information about creating the various activity types, see: <ul><li>[Create an A/B Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Create an Auto-Allocate activity](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Create an Auto-Target activity](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Create an Automated Personalization activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Create an Experience Targeting activity](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Create a Multivariate Test](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Create a Recommendations activity](/help/main/c-recommendations/recommendations.md)</li></ul>For more information about each type, see [Activity types](#types) below.|
|Create mobile preview link|Use [mobile preview links](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html) to perform easy end-to-end QA for mobile app activities. Click the **More options** icon (three vertical ellipsis), select the **Create Mobile Preview Link**, then choose the activities you want to test on mobile.|
|Customize Table<P>![Customize Table icon](/help/main/c-activities/assets/icon-customize-table.png)|Change the columns displayed in the [!UICONTROL Activity] list by clicking the **[!UICONTROL Customize Table]** icon on the upper right side of the table, then selecting or deselecting the desired columns. The changes are applied to your account and remain active even after you log out of [!DNL Target].|
|[!UICONTROL Show filters] icon<P>![Show Filters icon](/help/main/c-activities/assets/show-filters-icon.png)|Access filters by clicking the **[!UICONTROL Show Filters]** icon near the top of the list. For more information, see [Apply filters to the Activities list](#filters) below.|
|Bulk operations checkboxes|Perform bulk operations on selected activities.<P>For a list of actions that are available (depending on your permissions and the activity status), see [Perform quick actions](#quick-actions) below.|
|[!UICONTROL Type]|The activity type. The [!UICONTROL Type] column lets you quickly identify each activity by type. <ul><li>AB-M: manual [!UICONTROL A/B Test]</li><li>AB-AA: [!UICONTROL Auto-Allocate]</li><li>AB-AT: [!UICONTROL Auto-Target]</li><li>AP: [!UICONTROL Automated Personalization]</li><li>XT: [!UICONTROL Experience Targeting]</li><li>MVT: [!UICONTROL Multivariate Test]</li><li>REC: [!UICONTROL Recommendations]</li></ul>For more information about each type, see [Activity types](#types) below.|
|Name|The name of the activity. Click an activity name to display that activity's [!UICONTROL Overview] page. <P>Click the **[!UICONTROL Quick Info]** icon next to each activity name to view more information about that activity in a pop-up card.<p>Click the **[!UICONTROL More actions]** icon (three horizontal ellipsis) next to each activity name to open a menu that lets you to perform quick actions on an activity. The following actions are available (depending on your permissions and the activity status): [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete], and [!UICONTROL Archive]. For more information about each action, see [Perform quick actions](#quick-actions) below.<P>Click the table header to sort the list in ascending or descending order by name.|
|Status|The status of the activity can be one of the following:<ul><li>**Live**: The activity is currently running.</li><li>**Draft**: The activity setup has started but the activity is not yet ready to run.</li><li>**Scheduled**: The activity is ready to be activated when the specified start date and time arrives.</li><li>**Inactive**: The activity has been paused or deactivated.</li><li>**Syncing**: The activity has been saved and is being synced to the [!DNL Target] delivery network.</li><li>**Ended**: The specified end date and time of the activity has reached and the activity is no longer being served.</li><li>**Archived**: The activity has been archived. You can activate an archived activity to use it again.</li></ul>**Note**: When you perform certain actions, such as activating an activity outside of the [!DNL Target] UI using API methods, the update can take up to ten minutes to propagate to the UI.<P>Click the table header to sort the list in ascending or descending order by date.|
|Last Updated|The date when the activity was last updated, and by whom.|
|[!UICONTROL Priority]|The priority of the activity.<P>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.<P>Depending on your [settings](/help/main/administrating-target/reporting.md), the [!DNL Target] UI and options for [!UICONTROL Priority] vary. You can use the legacy settings of Low, Medium, or High, or you can enable fine-grained priorities from 0 to 999.|
|Property|Shows the [property](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) for the activity.|
|[!UICONTROL Estimated Lift in Revenue]|Shows the predicted increase in revenue if 100% of the audience sees the winning experience.<P>Calculated using the following formula:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>This number is rounded to one decimal place, maximum, if the condensed form has only a single digit before the decimal. For example: $1.6M, $60K, $900, $8.5K, $205K<P>This column shows "---" for activities that do not have enough data to call a winner show or do not have a cost estimate.<P>See [Estimating Lift in Revenue](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) for more information.|
|Source|Shows where the activity was created: Adobe Target, [Adobe Target API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html), or [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/)|
|Location|The URL for the activity identifies where the activity is displayed. This helps you quickly identify an activity, and determine whether a particular page already has a test running on it.<P>If a test runs on multiple URLs, a link shows how many more URLs are used. Click the link to view the complete list of URLs for that activity.<P>You can search based on URL. Use the drop-down list next to search box and select [!UICONTROL URL].|
|Author|The name of the person who created the activity.|
|Decisioning Method|The decisioning method used in each activity: [Server-Side](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html) or [Client-Side](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html).|

## Activity types {#types}

[!DNL Target] includes several activity types. The following table provides an overview of each activity type with links to help you learn more. To help you better choose the best activity type for your purposes, we have also created the [Adobe Target Activities Guide](/help/main/c-activities/target-activities-guide.md).

| Activity Type | Description |
|--- |--- |
|[A/B Test](/help/main/c-activities/t-test-ab/test-ab.md)|A/B testing compares two or more versions of your website content to see which version best improves your conversions during a pre-specified test period.<br>**Note:** You can now include [recommendations inside A/B Test activities](/help/main/c-recommendations/recommendations-as-an-offer.md). This functionality requires that you have a [Target Premium license](/help/main/c-intro/intro.md#premium).|
|[Auto-Allocate](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)|[!UICONTROL Auto-Allocate], a type of A/B test, identifies a winner among two or more experiences and automatically reallocates more traffic to the winner to increase conversions while the test continues to run and learn.<br>**Note:** You can now include [recommendations inside Auto-Allocate activities](/help/main/c-recommendations/recommendations-as-an-offer.md). This functionality requires that you have a [Target Premium license](/help/main/c-intro/intro.md#premium).|
|[Auto-Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<br>![Target Premium](/help/main/assets/premium.png)|Auto-Target, a type of A/B test, uses advanced machine learning to identify multiple high performing marketer-defined experiences, and serves the most tailored experience to each visitor based on their individual customer profile and the behavior of previous visitors with similar profiles, in order to personalize content and drive conversions.<br>**Note:** You can now include [recommendations inside Auto-Target activities](/help/main/c-recommendations/recommendations-as-an-offer.md). This functionality requires that you have a [Target Premium license](/help/main/c-intro/intro.md#premium).|
|[Multivariate Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)|[!UICONTROL Multivariate Testing] (MVT) compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience, and identifies which element most impacts the activity's success.|
|[Experience Targeting](/help/main/c-activities/t-experience-target/experience-target.md)|[!UICONTROL Experience Targeting] (XT) delivers content to a specific audience based on a set of marketer-defined rules and criteria.<br>**Note:** You can now include [recommendations inside Experience Targeting activities](/help/main/c-recommendations/recommendations-as-an-offer.md). This functionality requires that you have a [Target Premium license](/help/main/c-intro/intro.md#premium).|
|[Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br>![Target Premium](/help/main/assets/premium.png)|[!UICONTROL Automated Personalization] (AP) combines offers or messages, and uses advanced machine learning to match different variations to each visitor based on their individual customer profile, in order to personalize content and drive conversions.|
|[Recommendations](/help/main/c-recommendations/recommendations.md)<br>![Target Premium](/help/main/assets/premium.png)|A recommendation determines how a product is suggested to a website visitor, depending on that visitor's activities on the site.<br>For example, you might want to encourage people who purchase a backpack to consider buying hiking shoes and trekking poles. You could create a recommendation that shows items that are often purchased together, using the "People who bought this also bought that" algorithm. Or, you might want to encourage visitors to spend more time on your media site by recommending similar videos to the video they are watching, using the "People who viewed this viewed that" algorithm.<br>**Note:** You can now include recommendations inside A/B Test (including [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target]) and [!UICONTROL Experience Targeting] (XT) activities. See [Recommendations as an offer](/help/main/c-recommendations/recommendations-as-an-offer.md).|

## Apply filters to the Activities list {#filter}

Access filters by clicking the **[!UICONTROL Show Filters]** icon near the top of the list. The menu lets you filter activities by the following attributes:

* **Type**: Filter by [activity type](#types).
* **Status**: Filter by activity status. For more information about each status, see the "Status" row below.
* **Reporting Source**: Filter by reporting source.

  * [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md): Display activities that use [!UICONTROL Analytics for Target] (A4T) as the reporting source.
  * [Target](/help/main/c-reports/reports.md): Display activities that use [!DNL Target] as the reporting source.

* **Experience Composer**: Filter by which experience composer was used during activity creation:
  * [Visual](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): Displays activities that were created using the [!UICONTROL Visual Experience Composer] (VEC).
  * [Form Based](/help/main/c-experiences/form-experience-composer.md): Display activities that were created using the [!UICONTROL Form-Based Experience Composer].

* **Metrics Type**: Filter by which [success metric](/help/main/c-activities/r-success-metrics/success-metrics.md) was chosen during activity creation.
  * Conversion
  * Revenue
  * Engagement

* **Decisioning Method**: Filter by the decisioning method used in each activity.
  * [Server-Side](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html): Display activities that use server-side decisioning.
  * [Client-Side](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): Display activities that use client-side decisioning.

* **Activity Source**: Filter by activity source in which the activity was created.
  * Adobe Target
  * [Adobe Target API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html)
  * [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html)
  * [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html)
  * [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/)

* **Property**: Filter by the [property](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) in which the activity was created.

## Perform quick actions {#quick-actions}

Click the **[!UICONTROL More actions]** icon (three horizontal ellipsis) next to each activity name to open a menu that lets you to perform quick actions on an activity.

The following actions are available (depending on your permissions and the activity status):

|Action|Description|
| --- | --- |
|Edit|Change the activity. Any activity can be edited.<br>For more information about the various ways you can edit activities, see [Edit an activity or save as draft](/help/main/c-activities/edit-activity.md).|
|Deactivate|Stop a live or scheduled activity. A deactivated campaign can be reactivated or archived<br>If you deactivate or archive an activity and then later reactivate it, a visitor will continue being a part of that activity after the reactivation if they were in it before it was deactivated or archived. Any conversion metrics recorded during the time between the two events won't be attributed to that activity.|
|Activate|Start an inactive or ready activity.|
|Archive|Send the activity to the archive. By default, archived activities no longer appear in the Activities list. Change the filter for the activities list to include archived activities to see them. You can activate an archived activity to use it again.<br>If you deactivate or archive an activity and then later reactivate it, a visitor will continue being a part of that activity after the reactivation if they were in it before it was deactivated or archived. Any conversion metrics recorded during the time between the two events won't be attributed to that activity.|
|Copy|Copy an activity. Any activity can be copied. Copying an activity creates a new activity with the same name, appended with "Copy." For example, a test called "Browser Offers" is copied to "Browser Offers Copy."<br>Visual offers are copied with the activity. You can safely edit the offers in the copy without impacting the original activity. The only exception is saved offers and images in the Content/Assets folder.|
|Delete|Delete a draft or activity.<BR>**NOTE**: Deleted activities cannot be recovered. Unless you are absolutely sure that you'll never need this activity again, use the [!UICONTROL Archive] action. You can then reactivate the activity if necessary.|

Note the following details about the Activity list:

* Archived and ended activities do not appear in the [!UICONTROL Activities] list. To view these activities, filter them using the advanced filter settings on left rail. 
* As soon as an activity originally created in [!DNL Target Classic] is deactivated or deleted, it is deleted from [!DNL Target Standard/Premium]. Deleted activities originally created in [!DNL Target Classic] are not sent to the [!UICONTROL Archive] folder in [!DNL Target Standard/Premium]. The archived folder functionality applies only to activities created in [!DNL Target Standard/Premium]. 
* All activity types other than [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate], and [!UICONTROL Auto-Target] give you the choice to use either [!DNL Target] or [!DNL Adobe Analytics] as the data source. [!UICONTROL AP], [!UICONTROL Auto-Allocate], and [!UICONTROL Auto-Target] *always* use [!DNL Target] data. 
* Activities are available to several channels:

    * Web and mobile sites 
    * Internet-connected screens and devices, including kiosks and ATMs 
    * Email and other acquisition channels or partner sites 
    * Mobile apps 
    * Anywhere else you can deliver tagged content

## Limitations {#section_049D4684403A4E07B998067EB8E9BE56}

Each Target activity has the following content limitations:

| Item | Limit |
|--- |--- |
|Unique selectors|300 if a selector is repeated in a different experience, it is counted once. However, if it is repeated in the same experience, it is counted again.|
|Offers in each experience|350|
|Click track selectors in metrics|50|
|Mboxes in metrics|50|
|Audiences and locations|50 Audiences and locations (mbox) combination should not be more than 50.|

The activity cannot be saved if you exceed any of these limits.

Increasing the numbers of these items in your activity also increases the length of time it takes to synchronize the activity across Target.

For additional limits of the Visual Experience Composer, see [Visual Experience Composer Limitations](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Attributes imported into [!DNL Target] for activities updated outside of [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

If activities created in [!DNL Target] are updated from outside of [!DNL Target] (for example, via Adobe I/O), the following activity attributes are imported back into [!DNL Target]:

`thirdpartyId`

`startDate`

`endDate`

`status`

`priority`

`marketingCloudMetadata(remoteModifiedBy)`

This import job will run when the activities page is opened, with a maximum delay of ten minutes. (KB-1526) 

## Training videos {#section_BE80D13A2E81460C885F902010E1AD87}

The following videos contain more information about the concepts discussed in this article.

### Activity Types (9:03) ![Overview badge](/help/main/assets/overview.png)

This video explains the activity types available in [!DNL Target Standard/Premium].

* Describe the types of activities included in [!DNL Adobe Target] 
* Select the appropriate activity type to achieve your goals 
* Describe the three-step guided workflow that applies to all activity types 

>[!VIDEO](https://video.tv.adobe.com/v/17386)

