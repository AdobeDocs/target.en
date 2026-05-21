---
keywords: automated personalization;ap
description: Learn how to create an [!UICONTROL Automated Personalization] (AP) activity using the [!UICONTROL Visual Experience Composer].
title: How Do I Create an [!UICONTROL Automated Personalization] Activity?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
TQID: https://experienceleague.adobe.com/5eUFwob4BekIJP4SM2lrSDQam4h1AXIByJjM7-1RNL8
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Create an [!UICONTROL Automated Personalization] activity

Create an [!UICONTROL Automated Personalization] (AP) activity in [!DNL Adobe Target] using the [!UICONTROL Visual Experience Composer] (VEC).

The [!UICONTROL Automated Personalization] (AP) activity workflow in [!DNL Target] varies from the workflow of the other activity types.

This procedure follows the three-step guided workflow in the [!UICONTROL Visual Experience Composer]:

1. [Step 1: Build experiences](#build-experiences)
1. [Step 2: Set targeting](#set-targeting)
1. [Step 3: Configure goals and settings](#configure-goals-and-settings)

## Step 1: Build experiences {#build-experiences}

Define the pool of content variations that [!UICONTROL Automated Personalization] can personalize against. The richer and more distinct your experiences and offers, the better the algorithm can match the right content to each visitor.

1. From the [!DNL Target] [!UICONTROL Activities] list, click **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

1. To use the [!UICONTROL Visual Experience Composer] (VEC), click **[!UICONTROL Visual]**.

   To use the [!UICONTROL Form-Based Experience Composer], select [!UICONTROL Form]. See [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >In addition to the VEC and [!UICONTROL Form-Based Experience Composer], [!DNL Target] offers the [!UICONTROL Single Page Application VEC]. For more information about the various composers, see [Experiences and Offers](/help/main/c-experiences/experiences.md).
   >
   >For troubleshooting information about the VEC, see [Troubleshooting the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
 
1. (Conditional) [Choose a workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. In the **[!UICONTROL Enter Activity URL]** box, specify your [activity URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md).

   If your account is [configured with a default URL](/help/main/administrating-target/visual-experience-composer-set-up.md), that URL appears by default. You can change from the default to another URL if necessary.

   [!DNL Target] does not differentiate between URL protocols ([!DNL https] and [!DNL http]). As a result, [!DNL `http://www.adobe.com`] and [!DNL `https://wwww.adobe.com`] both match.

1. Click **[!UICONTROL Create]**.

   The page with the specified URL opens in the VEC.
 
1. To name the activity, click the **[!UICONTROL Edit]** icon ( ![Edit icon](/help/main/assets/icons/Edit.svg) ) next to "[!UICONTROL Untitled Activity]," specify a descriptive name for the activity, and then click **[!UICONTROL Save]**.

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

1. Modify page elements as explained in [Visual Experience Composer options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   You can select multiple images at once from the asset manager. This lets you quickly view the page with each of the images configured for the activity. You can also easily edit text elements in your offers. When you edit an element, bars appear on that element to indicate you have changed it.

1. Click the **[!UICONTROL Manage Content]** icon ( ![Manage Content icon](/help/main/assets/icons/Experience.svg) ) to configure the available combinations.

   A dialog box displays with two tabs: [!UICONTROL Experiences] and [!UICONTROL Offers]. The [!UICONTROL Experiences] tab lists each piece of content and the location it is assigned to. To exclude one or more experiences, select the corresponding checkboxes and click the [!UICONTROL Exclude] icon. For more options, see [Managing exclusions](/help/main/c-activities/t-automated-personalization/managing-exclusions.md).

   >[!IMPORTANT]
   >
   >**Best practice:** For optimal performance, limit [!UICONTROL Automated Personalization] and [!UICONTROL Auto-Target] activities to 4–6 locations with 4–6 offers per location. The total number of experiences grows from the cartesian combination of locations and offers. Larger configurations can lead to slow loading or editing in the [!UICONTROL Visual Experience Composer]. Keep the total under 5,000 experiences for best results; the hard limit is 30,000 (the same limit applies when the [!UICONTROL Disallow Duplicates] option is enabled).

1. (Conditional) Click **[!UICONTROL Offers]** to select pieces of content and assign them to reporting groups or only allow certain visitors to see certain offers with targeting.

   For more information about reporting groups, see [Offer reporting groups in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

<!--
1. (Conditional) Click **[!UICONTROL Exclusion Groups]** to choose any combination of elements that you want to exclude from the activity.

   ![Exclusion Groups tab of Manage Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the [!UICONTROL Disalow Duplicates] option.

   If you do not currently have any exclusion groups included in your activity, click **Create Exclusion Group**. You can filter to create a list that shows only the combinations you want to exclude. Name your exclusion group, then click **Save**.

   To edit an existing exclusion group, hover over the group you want to edit, then click the pencil icon.
-->

1. Click **[!UICONTROL Done]** when you have finished setting up the content of your activity.

## Step 2: Set targeting {#set-targeting}

Decide which visitors enter the activity and how much of your traffic is exposed. Pair them with a control group so [!DNL Target] can measure the lift personalization delivers.

1. Click **[!UICONTROL Targeting]** at the top of the [!UICONTROL Visual Experience Composer] to move to the next step in the three-step guided workflow.

   The **Targeting** step looks familiar if you have used other [!DNL Target] activity types. Here you can select an audience and specify the percentage of visitors who see each experience.

1. The flow diagram leads you through the steps of assigning an audience and its traffic percentage, selecting the traffic allocation method, and specifying the traffic allocation for each experience in the activity.

   ![AP Test Targeting step](/help/main/c-activities/t-automated-personalization/assets/ap-traffic-flow.png)

1. (Conditional) Click the **[!UICONTROL All Visitors]** control to [select another audience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) for the activity and set its visitor percentage.

   The [!UICONTROL All Visitors] audience is set as the default. If you select another audience, its name displays in the leftmost control, e.g. you might limit entries to 50% of all visitors or 45% of your "Californians" audience.

1. Click the **[!UICONTROL Traffic Allocation]** control to choose from the following options:

   ![Traffic Allocation Goal options](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap-new.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** If your goal is to test the algorithm, use a 50/50 percent split of visitors between the control and the targeted algorithm. This split gives the most accurate estimate of the lift. Suggested for use with "random experiences" as your control.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** If your goal is to create an "always on" activity, put 10% of the visitors into the control. This option ensures that there is enough data for the algorithms to continue learning over time. The tradeoff here is that in exchange for personalizing a larger proportion of your traffic, you have less precision in what the exact lift is. No matter your goal, this option is the recommended traffic split when using a specific experience as the control.
   * **[!UICONTROL Custom Allocation]:** Manually split the percentage as desired.

1. (Conditional) From the [!UICONTROL Control] drop-down list, [select a specific experience to be used as control](/help/main/c-activities/t-automated-personalization/experience-as-control.md) or select [!UICONTROL Random Experience.]

   The control experience provides a comparison to determine how much lift is provided by the automated test.

   [!UICONTROL Automated Personalization] always measures performance against a control group. Best practice is to place at least 10% of entrants into the control group. If your goal is to test if the personalization algorithm on the data it is given performs better than no personalization (for example, the randomly served control), a 50/50 percent traffic split between the control and the personalization algorithm is the fastest and most accurate way to achieve this goal. If you want to maximize the amount of traffic that is personalized and you are less concerned with understanding the exact lift your activity is generating, a 10/90 percent traffic split between the control and the personalization algorithm is the fastest and most accurate way to achieve this goal.

   >[!NOTE]
   >
   >In [!UICONTROL Automated Personalization] activities, entry criteria (URL targeting, template rules, and audience targets) are evaluated for each request. In previous versions, entry criteria were evaluated once per session.

## Step 3: Configure goals and settings {#configure-goals-and-settings}

Tell [!DNL Target] what success looks like. The optimization goal you choose is the metric the personalization algorithm trains against, so pick the outcome that matters most for this activity.

1. Click **[!UICONTROL Next]** to display the **[!UICONTROL Goals & Settings]** page.
1. Configure the activity with the following settings, then click **[!UICONTROL Save & Close]**.

   | Setting | Description |
   |--- |--- |
   |[!UICONTROL Name]|Name the activity. Give the activity a name that is descriptive enough that team members can recognize it in the [!UICONTROL Activities] list. Consult the table above to see which characters are not allowed in an activity name.|
   |[!UICONTROL Objective]|(Optional) Type the objective of the test. The objective helps you remember the purpose of the activity.|
   |[!UICONTROL Priority]|Depending on your settings, the [!DNL Target] UI and options for [!UICONTROL Priority] vary. You can use the legacy settings of [!UICONTROL Low], [!UICONTROL Medium], or [!UICONTROL High], or you can enable fine-grained priorities from 0 to 999.<P>The priority is used if multiple activities are assigned to the same location with the same audience. If two or more activities are assigned to the location, the activity with the highest priority displays.<P>If this option is not enabled in [!UICONTROL Administration] > [!UICONTROL Reporting] (the default), specify a priority: [!UICONTROL Low], [!UICONTROL Medium], or [!UICONTROL High].<P>To enable fine-grained priorities, click [!UICONTROL Administration] > [!UICONTROL Reporting], then toggle the [!UICONTROL Enable Fine-Grained Priorities] option to the "On" position.<P>If this option is enabled, specify a value from 0 through 999:<ul><li>0 = Low</li><li>999 = High</li></ul>For activities created in previous versions of [!DNL Target Standard/Premium], [!UICONTROL Low] priority is converted to 0, [!UICONTROL Medium] priority is converted to 5, and [!UICONTROL High] priority is converted to 10. You can adjust these values as necessary.<P>**Note**: Before you can disable this option after using fine-grained priories, all priorities must be set back to 0, 5, and 10.|
   |[!UICONTROL Duration]|Set the start and end dates for the activity. You can select [!UICONTROL When Activated] or you can specify a specific date and time.|
   |[!UICONTROL Optimization Goal]|Specify the optimization goal, which consists of two parameters:<ul><li>What you want to measure with the activity</li><li>The action taken by an activity entrant that shows that the goal has been achieved.</li></ul>You can choose to name the optimization goal by selecting the three dots to the right of [!UICONTROL My Primary Goal]. [!UICONTROL Automated Personalization] activities can measure [!UICONTROL Conversion] or [!UICONTROL Revenue]. Conversion can be achieved by viewing a page or by viewing an mbox. Clicks can also be tracked.<P>The primary goal also becomes the modeling metric used by the modeling system to calculate the success of the experience.<P>Visitors can be kept in the activity for tracking purposes after reaching the modeling goal. For example, often an [!UICONTROL Automated Personalization] activity is used to improve click-rates, and that is set as the modeling goal. However, it's important to see how increased click-rates lead to final conversion, so tracking through the final conversion is essential.<P>You can provide dependency on multiple metrics along with the flexibility to choose whether the metric should be reached or not reached for the count to increase.<P>You must define both (or multiple) success metrics before you can make one dependent on another.<P>The [!UICONTROL Add Dependency] option allows the success metric to increment if another success metric has been reached or has not been reached.<P>To add a dependency:<ol><li>After adding additional metrics, click **[!UICONTROL Advanced Settings]** under the three-dot menu to the right of [!UICONTROL Additional Goal].</li><li>Click the **[!UICONTROL Add Dependency]** option at the bottom of the [!UICONTROL Reporting Settings] section.</li><li>Drag and drop the desired metrics from the left pane into the right pane, then click [!UICONTROL Reached] to toggle the setting between [!UICONTROL Reached] and [!UICONTROL Not Reached].</li></ol>You can edit or remove dependencies after adding them.|
   |[!UICONTROL Conversion Metric]|By default, the conversion metric is the same as the optimization goal metric. However, you can define a separate conversion metric by unchecking the [!UICONTROL Same as Optimization Goal] option.|
   |[!UICONTROL Additional Metrics]|Add any additional reporting metrics that you want to use. You can add conversion or revenue metrics.<P>**Note**: The [!UICONTROL Engagement] metric is not supported as an additional metric. The [!DNL Target] UI might let you select the [!UICONTROL Engagement] metric, but the data does not display accurately in reports.|
   |[!UICONTROL Audiences for Reporting]|Add audiences to enable filtering by audiences in reports. By default, the report shows results for all qualified visitors. Add audiences to filter results for more specific subsets of visitors.<P>**Note**: Unlike other activity types, [!UICONTROL Automated Personalization] cannot use [!UICONTROL Adobe Analytics] as its reporting source (A4T).|
   |[!UICONTROL Notes]|Type any information about your activity that is useful for you or for other team members. The [!UICONTROL Notes] pane is resizable.|

   When you name or rename a metric, the following characters are not allowed:

   | Character | Description |
   |--- |--- |
   |/|Forward slash|
   |?|Question mark|
   |#|Number sign|
   |:|Colon|
   |=|Equals to|
   |+|Plus|
   |-|Minus|
   |@|At sign|

After you click **[!UICONTROL Save & Close]**, the activity's [!UICONTROL Overview] page displays. Click **Preview Experiences** to preview how your experiences look when delivered. A pop-up appears that you can use to view and share links to your AP experiences on your site to get a "true preview" of the experiences outside of the [!UICONTROL Target] [!UICONTROL Visual Experience Composer] (VEC). You must share the links from the message to share the preview. Clicking a link and then copying the URL directly from the browser does not work. Copying the link causes the URL to contain a parameter that displays the page correctly only when you access the page from the link in the message. 

For information about reporting, see [Automated Personalization Reports](/help/main/c-reports/personalization-reports/reports-ap.md).
