---
keywords: Create auto-target;A/B test;auto-target activity;new a/b activity;auto target;auto-target for personalized experiences;personalized;optimization
description: Learn how to use the [!UICONTROL Visual Experience Composer] (VEC) to create an [!UICONTROL Auto-Target] A/B Test activity.
title: How Do I Create an [!UICONTROL Auto-Target] Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
---
# Create an [!UICONTROL Auto-Target] activity

Use the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] to create your [!UICONTROL Auto-Target] [!UICONTROL A/B Test] activity directly on a [!DNL Target]-enabled page and to modify portions of the page within [!DNL Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] is available as part of the [!DNL Target Premium] solution. This feature is not available in [!DNL Target Standard] without a [!DNL Target Premium] license. For more information about the advanced features this license provides, see [Target Premium](/help/main/c-intro/intro.md).

To create an [!UICONTROL Auto-Target] activity:

1. From the **[!UICONTROL Activities]** list, click **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

1. From the [!UICONTROL Create A/B Test Activity] dialog, select **[!UICONTROL Visual]**, if necessary.

   If you prefer to use the [!UICONTROL Form-Based Experience Composer], select [!UICONTROL Form]. See [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >In addition to the VEC and [!UICONTROL Form-Based Experience Composer], [!DNL Target] offers the [!UICONTROL Single Page Application] VEC. For more information about the various composers, see [Experiences and Offers](/help/main/c-experiences/experiences.md).
   >
   >For troubleshooting information about the VEC, see [Troubleshooting the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Conditional) If you are a [Target Premium customer](/help/main/c-intro/intro.md#premium), from the **[!UICONTROL Choose Workspace]** drop-down list, choose a [workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   The [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) option is a [Target Premium](/help/main/c-intro/intro.md) feature and might not display if your organization has a [!UICONTROL Target Standard] license.

1. In the **[!UICONTROL Enter Activity URL]** box, specify your [activity URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md).

   If your account is [configured with a default URL](/help/main/administrating-target/visual-experience-composer-set-up.md), that URL appears by default. You can change from the default to another URL if necessary.

1. Click **[!UICONTROL Create]**.

   The [!UICONTROL Visual Experience Composer] opens, showing the page specified in the URL.

1. Click the **[!UICONTROL Rename]** icon ( ![Rename icon](/help/main/assets/icons/MoreSmallListVert.svg) ), click **[!UICONTROL Rename]**, specify a name for the activity, then click **[!UICONTROL Save]**.

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
   
1. Create new experiences by changing the elements on the page.

   The [!UICONTROL Visual Experience Composer] displays two tabs on the left side after you create a new activity: [!UICONTROL Experience A] and [!UICONTROL Experience B]. [!UICONTROL Experience A] is the control experience. Your focus is on the [!UICONTROL Experience B] tab, which you can modify as desired. [!UICONTROL Experience B] is the alternate experience that you can add to your test. You can add multiple experiences to the test by clicking the [!UICONTROL Add] icon ( ![Add icon](/help/main/assets/icons/Add.svg) ) at the top of the [!UICONTROL Experiences] pane. You can also delete Experience A from the activity if you don't want to include a default site experience as an option.

   For more information about adding and modifying experiences in the [!UICONTROL Visual Experience Composer], see [Add Experience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). To modify Experience B, start with Step 2. 

1. Click **[!UICONTROL Targeting]** at the top of the [!UICONTROL Visual Experience Composer] to move to the next step in the three-step guided workflow.

   The flow diagram opens.

   ![A/B Test Targeting step](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   The flow diagram leads you through the steps of assigning an audience and its traffic percentage, selecting the traffic allocation method, and specifying the traffic allocation for each experience in the activity.

1. (Conditional) Click the **[!UICONTROL All Visitors]** control to select another audience for the activity.

   The [!UICONTROL All Visitors] audience is set as the default. If you select another audience, its name displays in the leftmost control.

   The right frame displays, which lets you add or delete an audience and assign the visitor percentage for the activity.

   1. To change the audience, click the **[!UICONTROL Replace] icon** ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) in the right frame.
   1. In the [!UICONTROL Add Audience] dialog box, [select the desired audience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), then click **[!UICONTROL Assign Audience]**.

      You can click **Combine Audiences** to [create an audience that combines multiple audiences](/help/main/c-target/combining-multiple-audiences.md). 

      If you need to create a new audience that is not already in the [!UICONTROL Audience Library], click **Create Audience**. During the [create-audience workflow](/help/main/c-target/c-audiences/audiences.md) you can choose from the following options:

      * **[!UICONTROL Audience Library]**: Create an on-demand audience that is saved to the [!UICONTROL Audience Library] that can be reused in other activities
      * **[!UICONTROL This activity only]**: Create an [activity-specific audience](/help/main/c-target/creating-activity-only-audience.md) that is not saved to the [!UICONTROL Audience Library] and can be used in the current activity only 
   
   1. Click **[!UICONTROL Visitor Percentage]** in the right frame, then choose the percentage of qualifying visitors that you want to enter the activity.

   For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.

1. Click the **[!UICONTROL Traffic Allocation]** control, then choose the desired traffic allocation method in the right pane. In this scenario, click **[!UICONTROL Auto-Taget for personalized experiences]**.

    ![Traffic Allocation Method settings](/help/main/c-activities/assets/auto-target.png)

   The following traffic allocation methods are available:

   * **[!UICONTROL Manual (Default)]**: Specify the percentage of entrants that you want to see each experience. You can split the percentages evenly between all experiences, or specify higher or lower percentages for each experience. The total for all experiences must equal 100%.

   * **[!UICONTROL Auto-Allocate to best experience]**: Most activity entrants are automatically directed to higher-performing experiences. Some visitors are allocated to all experiences, to maintain exploration of experiences and to recognize changes in performance trends. For more information, see [[!UICONTROL Auto-Allocate] overview](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] uses advanced machine learning to personalize content and drive conversions by identifying multiple high-performing, marketer-defined experiences, and then serving the most tailored experience to visitors based on their individual customer profiles and past behaviors of similar visitors. For more information, see [Auto-Target overview](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Click **[!UICONTROL Experiences]** in the right pane, then specify the desired traffic allocation for each experience.

1. When you are satisfied with your audience, experience choices, and traffic allocation choices, click **[!UICONTROL Next]** to move to the third step of the three-step guided workflow.

1. Specify the [goals and settings](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) for the activity.

   >[!NOTE]
   >
   >If you want to use [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) with this activity, see important information in [A4T support for Auto-Allocate and Auto-Target activities](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Click **[!UICONTROL Save & Close]** or **[!UICONTROL Save]**.

After you create the activity, the [!UICONTROL Overview] tab shows information about the activity, including a diagram of your activity.
