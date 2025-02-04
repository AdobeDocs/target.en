---
keywords: Create A/B;A/B test;A/B activity;new a/b activity;create a/b
description: Learn how to use the Visual Experience Composer (VEC) in Adobe [!DNL Target] to create your A/B Test activity directly on a [!DNL Target]-enabled page.
title: How Do I Create an A/B Test?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
---
# Create an A/B Test

Use the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] to create your [!UICONTROL A/B Test] activity directly on a [!DNL Target]-enabled page and to modify portions of the page within [!DNL Target].

>[!NOTE]
>
>In addition to the Manual (Default) [!UICONTROL A/B Test] activity (discussed in this article), [!DNL Target] provides two additional types of [!UICONTROL A/B Test] activities: [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target].
>
>See [Types of A/B Testing activities](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B Test overview*.

To create a manual [!UICONTROL A/B Test] activity:

1. From the **[!UICONTROL Activities]** list, click **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Create Activity drop-down list](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >The available activity types depend on your [!DNL Target] account. Some activity types might not appear in your list. For example, [!UICONTROL Recommendations] is a [Target Premium feature](/help/main/c-intro/intro.md#premium).
   >
   >For information about the various activity types, see [Activities](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) and the [Target activities guide](/help/main/c-activities/target-activities-guide.md).

1. From the Create A/B Test Activity dialog, select **[!UICONTROL Visual (Default)]**, if necessary.

   If you prefer to use the [!UICONTROL Form-Based Experience Composer], select [!UICONTROL Form]. See [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >In addition to the VEC and [!UICONTROL Form-Based Experience Composer], [!DNL Target] offers the Single Page Application VEC. For more information about the various composers, see [Experiences and Offers](/help/main/c-experiences/experiences.md).
   >
   >For troubleshooting information about the VEC, should you have problems, see [Troubleshooting the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Conditional) If you are a [Target Premium customer](/help/main/c-intro/intro.md#premium), from the **[!UICONTROL Choose Workspace]** drop-down list, choose a [workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   The [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) option in the preceding illustration is a [Target Premium](/help/main/c-intro/intro.md) feature and might not display if your organization has a [!UICONTROL Target Standard] license.

1. In the **[!UICONTROL Enter Activity URL]** box, specify your [activity URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), then click **[!UICONTROL Create]**.

   If your account is [configured with a default URL](/help/main/administrating-target/visual-experience-composer-set-up.md), that URL appears by default. You can change from the default to another URL if necessary.

   The [!UICONTROL Visual Experience Composer] opens, showing the page specified in the URL.

1. Click **[!UICONTROL Untitled Activity]** at the top of the VEC, then specify a name for the activity in the space provided.

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
   
1. Create any new experiences by changing the elements on the page.

   The [!UICONTROL Visual Experience Composer] displays two tabs on the left side after you create a new activity: Experience A and Experience B. Experience A is the control experience. Your focus is on the Experience B tab, which you can modify as desired. Experience B is the alternate experience that you can add to your test. You can add multiple experiences to the test. You can also delete Experience A from the activity if you don't want to include a default site experience as an option.

   For more information about adding and modifying experiences in the [!UICONTROL Visual Experience Composer], see [Add Experience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). To modify Experience B, start with Step 2. 

1. Click **[!UICONTROL Targeting]** at the top of the [!UICONTROL Visual Experience Composer] to move to the next step in the three-step guided workflow.

   The flow diagram opens.

   ![A/B Test Targeting step](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   The flow diagram leads you through the steps of choosing the audience for the activity and setting up experiences.

1. In the **[!UICONTROL Audience]** box, click the edit icon (the vertical ellipsis), click **[!UICONTROL Replace Audience]**, then [select the audience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) for your activity.

   By default, the audience is set to [!UICONTROL All Visitors]. 

1. Choose the percentage of qualifying visitors that you want to enter the activity.

   ![Audience percentage](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   For example, you might limit entries to 50% of all visitors or 45% of your "Californians" audience.

1. Set up your traffic allocation.

   You can show multiple experiences to the same audience. A diagram displays showing your selected audience and the experiences that you added to the activity.

   Choose your desired traffic allocation method:

   * **[!UICONTROL Manual (Default)]**: Specify the percentage of entrants that you want to see each experience. You can split the percentages evenly between all experiences, or specify higher or lower percentages for each experience. The total for all experiences must equal 100%.

   * **[!UICONTROL Auto-allocate to best experience]**: Most activity entrants are automatically directed to higher-performing experiences. Some visitors are allocated to all experiences, to maintain exploration of experiences and to recognize changes in performance trends. For more information, see [[!UICONTROL Auto-Allocate] overview](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] uses advanced machine learning to personalize content and drive conversions by identifying multiple high-performing, marketer-defined experiences, and then serving the most tailored experience to visitors based on their individual customer profiles and past behaviors of similar visitors. For more information, see [Auto-Target overview](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   You can also click **[!UICONTROL Add]** to add another experience to the activity.

1. When you are satisfied with your audience, experience choices, and traffic allocation choices, click **[!UICONTROL Next]** to move to the third step of the three-step guided workflow.

1. Specify the [goals and settings](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) for the activity.

1. Click **[!UICONTROL Save & Close]** or **[!UICONTROL Save]**.

After you create the activity, the [!UICONTROL Overview] tab shows information about the activity, including a diagram of your activity.

## Training video: Creating A/B Tests (8:36) ![Tutorial badge](/help/main/assets/tutorial.png)

This video demonstrates how to create an A/B test using the [!DNL Target] three-step guided workflow.

* Create an [!UICONTROL A/B Test] activity in [!DNL Adobe Target] 
* Allocate traffic using a manual split or automatic traffic allocation

>[!VIDEO](https://video.tv.adobe.com/v/17391)
