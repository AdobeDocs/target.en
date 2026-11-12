---
keywords: mvt;multivariate test;multivariate test create;multivariate test creating;mvt create;mvt creating;mvt how;multivariate test how
description: Learn how to use the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] to create a [!UICONTROL Multivariate Test] (MVT).
title: How Do I Create a [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
TQID: 'https://experienceleague.adobe.com/gxrnY43A7OWsiW48Rlq1Orp7ZxBswdAPZEAbRQrCDZA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Create a Multivariate Test {#create-mvt}

>[!BEGINSHADEBOX]

**On this page:** Learn how to create a **[!UICONTROL Multivariate Test]** (MVT) in the **[!UICONTROL Visual Experience Composer]** (VEC). You create the activity, build and review the experiences, set targeting, then configure goals and settings.

>[!ENDSHADEBOX]

The **[!UICONTROL Visual Experience Composer]** (VEC) in [!DNL Adobe Target] makes it easy to create a **[!UICONTROL Multivariate Test]** and to modify portions of the page within [!DNL Target].

The [!DNL Target] point-and-click editor enables you to pick any location and add multiple offers.

The **[!UICONTROL Multivariate Test]** (MVT) takes a page-first report. In other words, the test runs on a specific URL, with the experiences you design for that page.

Follow the steps below to create a **[!UICONTROL Multivariate Test]** (MVT):

1. [Create the activity](#create-activity)
1. [Build and review the experiences](#build-experiences)
1. [Set targeting](#set-targeting)
1. [Configure goals and settings](#configure-goals-and-settings)

## Create the activity {#create-activity}

Choose the activity type and delivery type, specify the page to test, and name the activity.

1. Click **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   For more information about the various activity types available in [!DNL Target] and their differences, see [Activities](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). See [Target Activity types](/help/main/c-activities/target-activities-guide.md) to help you decide which activity type best suites your needs.

   ![](../../assets/create-mvt-1.png)

1. Choose the delivery type: **[!UICONTROL Web]**, **[!UICONTROL Mobile]**, **[!UICONTROL Email]**, or **[!UICONTROL Other/API]**.

1. (Conditional) If you are a [Target Premium](/help/main/c-intro/intro.md#premium) customer, [choose a workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specify the URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#ab-activity-url) for the page that you want to test. Use a complete URL, including HTTP or HTTPS at the beginning.

1. Then, click **[!UICONTROL Create]**. The **[!UICONTROL Visual Experience Composer]** opens.

1. To name the activity, click the **[!UICONTROL Edit]** icon ( ![Edit icon](/help/main/assets/icons/Edit.svg) ) and specify a descriptive name for the activity, and then click **[!UICONTROL Save]**.

   {{activity-name-rules}}

   ![](../../assets/create-mvt-2.png)

## Build and review the experiences {#build-experiences}

Add offers to each location, preview the resulting experiences, and check that your test plan is feasible.

1. [Create the offers in each location](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   You can add the following kinds of offers:

   * HTML
   * Image
   * Text

1. Click **[!UICONTROL Preview]** to [preview your experiences](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. Click the **[!UICONTROL Show Experiences]** icon ( ![Show Experiences icon](/help/main/assets/icons/WebPages.svg) ) to display the list of all experiences in the left frame, then click a specific experience in the list to view that experience.

1. [Use the Traffic Estimator](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) to test the feasibility of your test plan.

### Exclude experiences (optional) {#exclude-experiences}

You might choose to exclude an experience that shows conflicting variations or an experience that is not aesthetically balanced.

1. Click the **[!UICONTROL Manage Content]** icon ( ![Manage Experiences icon](/help/main/assets/icons/Experience.svg) ) to display the **[!UICONTROL Manage Experiences]** dialog box.

1. To exclude one experience, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallList.svg) ) next to that experience, then click **[!UICONTROL Exclude]**.

1. To exclude multiple experiences, select the check boxes for the desired experiences, then click **[!UICONTROL Exclude]**.

## Set targeting {#set-targeting}

Choose which visitors enter the test, and review the test summary.

1. Click **[!UICONTROL Next]** to access the **[!UICONTROL Targeting]** page.

   The flow diagram leads you through the steps of assigning an audience and its traffic percentage, selecting the traffic allocation method, and specifying the traffic allocation for each experience in the activity.

1. (Conditional) Click the **[!UICONTROL All Visitors]** control to select another audience for the activity.

   The **[!UICONTROL All Visitors]** audience is set as the default. If you select another audience, its name displays in the leftmost control. For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.

   +++ Steps to select a different audience

   The right frame displays, which lets you add or delete an audience and assign the visitor percentage for the activity.

   1. To change the audience, click the **[!UICONTROL Replace]** icon ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) in the right frame.
   1. In the **[!UICONTROL Add Audience]** dialog box, [select the desired audience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), then click **[!UICONTROL Assign Audience]**.

      To create an audience that combines several audiences, click **[!UICONTROL Combine Audiences]**. For details, see [Combine multiple audiences](/help/main/c-target/combining-multiple-audiences.md).

      To create a new audience that is not already in the **[!UICONTROL Audience Library]**, click **[!UICONTROL Create Audience]**. In the [create-audience workflow](/help/main/c-target/c-audiences/audiences.md), choose one of the following options:

      * **[!UICONTROL Audience Library]**: Create an on-demand audience that is saved to the **[!UICONTROL Audience Library]** and can be reused in other activities.
      * **[!UICONTROL This activity only]**: Create an [activity-specific audience](/help/main/c-target/creating-activity-only-audience.md) that is not saved to the **[!UICONTROL Audience Library]** and can be used in the current activity only.

   1. Click **[!UICONTROL Visitor Percentage]** in the right frame, then choose the percentage of qualifying visitors that you want to enter the activity.

   +++

1. [Review the test summary](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) and make any desired changes, then click **[!UICONTROL Next]**.

## Configure goals and settings {#configure-goals-and-settings}

On the **[!UICONTROL Goals & Settings]** page, you tell [!DNL Target] how to measure the test. The available settings depend on whether you use [!DNL Target] or [!DNL Analytics] as the reporting source.

1. Review the sections of the page and set what you need. See [What you set on the Goals & Settings page](#goals-settings-overview).


   |Section|What you set|
   |---|---|
   |**[!UICONTROL Activity Settings]**|An optional objective, the **[!UICONTROL Priority]** (used when several activities share a location and an audience), and the **[!UICONTROL Duration]** (start and end dates).|
   |**[!UICONTROL Reporting Settings]**|The reporting source, the goal metric (for example, a **[!UICONTROL Conversion]** metric), additional metrics, and audiences for reporting. Advanced settings for the goal metric are also available here.|
   |**[!UICONTROL Other Metadata]**|Notes about the activity that are useful for you or for other team members.|

1. Click **[!UICONTROL Save and Close]** to create the activity.

For details about every option, see [Goals and settings](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#ab-goals-and-settings).

## Training video: Creating Multivariate Tests (9:25) ![Tutorial badge](/help/main/assets/tutorial.png)

This video demonstrates how to plan and create a multivariate test using the [!DNL Target] three-step guided workflow.

* Define and design a multivariate test
* Create a multivariate test

>[!VIDEO](https://video.tv.adobe.com/v/17395)
