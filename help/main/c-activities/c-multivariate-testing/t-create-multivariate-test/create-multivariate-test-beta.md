---
keywords: mvt;multivariate test;multivariate test create;multivariate test creating;mvt create;mvt creating;mvt how;multivariate test how
description: Learn how to use the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] to create a [!UICONTROL Multivariate Test] (MVT).
title: How Do I Create a [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
hide: yes
hidefromtoc: yes
exl-id: be8ac6a4-cc69-47c1-8aba-84d162ef043c
---
# Create a Multivariate Test

The [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] makes it easy to create a [!UICONTROL Multivariate Test] and to modify portions of the page within [!DNL Target].

The [!DNL Target] point-and-click editor enables you to pick any location and add multiple offers.

The [!UICONTROL Multivariate Test] (MVT) takes a page-first report. In other words, the test runs on a specific URL, with the experiences you design for that page. 

1. Click **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   >[!NOTE]
   >
   >For more information about the various activity types available in [!DNL Target] and their differences, see [Activities](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). See [Target Activity types](/help/main/c-activities/target-activities-guide.md) to help you decide which activity type best suites your needs.

1. (Conditional) Choose the delivery type: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL Email], or [!UICONTROL Other/API].

1. (Conditional) If you are a [Target Premium](/help/main/c-intro/intro.md#premium) customer, [choose a workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specify the URL](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) for the page that you want to test, then click **[!UICONTROL Create]**.
   
   >[!NOTE]
   >
   >Use a complete URL, including HTTP or HTTPS at the beginning.

   If a message appears, asking you to enable your browser for mixed content, follow the instructions in the message. After enabling your browser for mixed content, begin again at Step 1.

   The [!UICONTROL Visual Experience Composer] opens.

1. 1. Click the **[!UICONTROL Rename]** icon ( ![Rename icon](/help/main/assets/icons/MoreSmallListVert.svg) ), click **[!UICONTROL Rename]**, specify a name for the activity, then click **[!UICONTROL Save]**.

   The activity name cannot begin with any of the following characters:

   | Character | Description |
   |--- |--- |
   |`=`|Equals to|
   |`+`|Plus|
   |`-`|Minus|
   |`@`|At sign|

   The activity name cannot contain any of the following character sequences:

   | Character Sequence | Description |
   |--- |--- |
   |;=|Semicolon, Equals to|
   |;+|Semicolon, Plus|
   |;-|Semicolon, Minus|
   |;@|Semicolon, At sign|
   |,=|Comma, Equals to|
   |,+|Comma, Plus|
   |,-|Comma, Minus|
   |,@|Comma, At sign|
   |`[`"|Open square bracket, Double quotation marks|
   |"`]`|Double quotation marks, Close square bracket|

1. [Create the offers in each location](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   You can add the following kinds of offers:

    * HTML 
    * Image 
    * Text

1. Click **[!UICONTROL Preview]** to [preview your experiences](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. Click the **[!UICONTROL Show Experiences]** icon ( ![Show Experiences icon](/help/main/assets/icons/WebPages.svg) ) to display the list of all experiences in the left frame.

1. Click a specific experience in the list to view that experience.

1. (Conditional) To exclude one or more experiences from the activity, click the **[!UICONTROL Manage Content]** icon ( ![Manage Experiences icon](/help/main/assets/icons/Experience.svg) ) to display the [!UICONTROL Manage Experiences] dialog box.

1. (Conditional) In the [!UICONTROL Manage Experiences] dialog box, click the **[!UICONTROL More Actions]** icon ( ![More Actions icon](/help/main/assets/icons/MoreSmallList.svg) ) next to the experience that you want to exclude, then click **[!UICONTROL Exclude]**.

   You might choose to exclude an experience that shows conflicting variations or an experience that is not aesthetically balanced.

1. (Conditional) To exclude multiple experiences, select the check boxes for the desired experiences, then click **[!UICONTROL Exclude]**.

1. [Use the Traffic Estimator](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) to test the feasibility of your test plan.

1. Click **[!UICONTROL Next]** to advance to the [!UICONTROL Targeting] page.

   The **Targeting** step looks familiar if you have used other [!DNL Target] activity types. Here you can select an audience and specify the percentage of visitors who see each experience.

   The flow diagram leads you through the steps of assigning an audience and its traffic percentage, selecting the traffic allocation method, and specifying the traffic allocation for each experience in the activity.

1. (Conditional) Click the **[!UICONTROL All Visitors]** control to select another audience for the activity.

   The [!UICONTROL All Visitors] audience is set as the default. If you select another audience, its name displays in the leftmost control.

   The right frame displays, which lets you add or delete an audience and assign the visitor percentage for the activity.

   1. To change the audience, click the **[!UICONTROL Replace] icon** ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) in the right frame.
   1. In the [!UICONTROL Add Audience] dialog box, [select the desired audience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), then click **[!UICONTROL Assign Audience]**.

      You can click **Combine Audiences** to [create an audience that combines multiple audiences](/help/main/c-target/combining-multiple-audiences.md). 

      If you need to create a new audience that is not already in the [!UICONTROL Audience Library], click **Create Audience**. During the [create-audience workflow](/help/main/c-target/c-audiences/audiences.md) you can choose from the following options:

      * **[!UICONTROL Audience Library]**: Create an on-demand audience that is saved to the [!UICONTROL Audience Library] that can be reused in other activities.
      * **[!UICONTROL This activity only]**: Create an [activity-specific audience](/help/main/c-target/creating-activity-only-audience.md) that is not saved to the [!UICONTROL Audience Library] and can be used in the current activity only.
   
   1. Click **[!UICONTROL Visitor Percentage]** in the right frame, then choose the percentage of qualifying visitors that you want to enter the activity.

   For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.

1. [Review the test summary](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) and make any desired changes, then click **[!UICONTROL Next]**.

1. [Specify the goals and settings](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) for the test.

1. Click **[!UICONTROL Save and Close]** to create the activity.

## Training video: Creating Multivariate Tests (9:25) ![Tutorial badge](/help/main/assets/tutorial.png)

This video demonstrates how to plan and create a multivariate test using the [!DNL Target] three-step guided workflow.

* Define and design a multivariate test 
* Create a multivariate test

>[!VIDEO](https://video.tv.adobe.com/v/17395)
