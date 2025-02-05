---
keywords: Experience Targeting;xt;create
description: Learn how to use the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] to create an [!UICONTROL Experience Targeting] (XT) activity.
title: How Do I Create an [!UICONTROL Experience Targeting] Activity?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
---
# Create an [!UICONTROL Experience Targeting] (XT) activity

Use the [!UICONTROL Visual Experience Composer] (VEC) to create an [!UICONTROL Experience Targeting] (XT) activity on a [!DNL Target]-enabled page and to modify portions of the page within [!DNL Adobe Target].

[!UICONTROL Experience Targeting] (XT) delivers content to a specific audience based on a set of marketer-defined rules and criteria.

[!UICONTROL Experience Targeting], including [geo-targeting](/help/main/c-target/c-audiences/c-target-rules/geo.md), is valuable for defining rules that target a specific experience or content to a particular audience. Several rules can be defined in an activity to deliver different content variations to different audiences.

For more information about [!UICONTROL Experience Targeting], a use-case scenario, and training videos, see [Experience Targeting](/help/main/c-activities/t-experience-target/experience-target.md).

**To create an [!UICONTROL Experience Targeting] activity:**

1. From the [!UICONTROL Activities] list, click **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   ![Create Activity > Experience Targeting](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >The available activity types depend on your [!DNL Target] account. Some activity types might not appear in your list. For example, [!UICONTROL Automated Personalization] is a [Target Premium feature](/help/main/c-intro/intro.md#premium).
   >
   >For more information about the various activity types available in [!DNL Target] and their differences, see [Activities](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). See [Target Activity types](/help/main/c-activities/target-activities-guide.md) to help you decide which activity type best suites your needs.

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   If you prefer to use the [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md), select [!UICONTROL Form].

   >[!NOTE]
   >
   >In addition to the VEC and [!UICONTROL Form-Based Experience Composer], [!DNL Target] offers the Single Page Application VEC. For more information about the various composers, see [Experiences and Offers](/help/main/c-experiences/experiences.md).
   >
   >For troubleshooting information about the VEC, see [Troubleshooting the Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Conditional) If you are a [!DNL Target Premium] customer, [choose a workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   The [!UICONTROL Choose Workplace] option is a [Target Premium](/help/main/c-intro/intro.md) feature. If your organization has a [!DNL Target Standard] license if you do not see this option.

1. Specify your [activity URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), then click **[!UICONTROL Create]**.

   If your account is [configured with a default URL](/help/main/administrating-target/visual-experience-composer-set-up.md), that URL appears by default. You can change from the default to another URL, if necessary.

   The VEC opens, showing the page specified in the URL.

   ![Experience Targeting activity within the VEC](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Type a name for the activity in the space provided.

   ![Name field](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

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

1. Create new experiences targeted to different audiences.

   For step-by-step instructions, see [Add experience](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Specify the [goals and settings](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) for the activity.
