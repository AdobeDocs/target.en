# Snippets

## Target Premium features {#premium-note}

>[!NOTE]
>
>This functionality is available as part of the [Target Premium](/help/main/c-intro/intro.md#premium) license. This functionality is not available in [!DNL Target Standard].

## Target permissions update {#permissions-update}

>[!IMPORTANT]
>
>[!DNL Target] users with [!UICONTROL Product Administrator] and [!UICONTROL System Administrator] rights can edit all settings on the [!UICONTROL Administration] pages, regardless of their role in [!DNL Target]. Users without these permissions have read-only access to these settings.

## Updated Target UI {#updated-ui}

>[!NOTE]
>
>New in 2025, [!DNL Target] introduced an updated UI and [!UICONTROL Visual Experience Composer] (VEC). Click the following links to learn more:
>
>* [[!DNL Target Standard/Premium] 25.2.1 (February 17, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Provides a summary of the key UI changes in [!DNL Target] for [!UICONTROL Activities], [!UICONTROL Recommendations], and the [!UICONTROL Visual Experience Composer] (VEC).
>
>* [[!DNL Target Standard/Premium] 25.1.1 (January 9, 2025) release notes](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Provides a summary of the key UI changes in [!DNL Target] for the [!UICONTROL Offers Library].
>
>* [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): Provides a brief overview to help you get familiarized with [!DNL Target] and provides links for more in-depth information and step-by-step instructions.
>
>* [[!UICONTROL Visual Experience Composer] changes](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): The [!DNL Adobe Target Standard/Premium] 25.2.1 release (February 17, 2015) introduces an updated [!UICONTROL Visual Experience Composer] (VEC). This article explains the differences between the legacy and updated versions of the VEC.
>
>* [[!UICONTROL Visual Experience Composer] options](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): This article explains the updated VEC UI and its options.
>
>* [[!DNL Target] UI update FAQs](/help/main/c-intro/updated-ui-faq.md): This FAQ addresses common questions about the new [!DNL Target] UI and [!UICONTROL Visual Experience Composer] (VEC), including navigation changes, feature locations, and the deprecation of the temporary UI version toggle. Whether you are a marketer, developer, or admin, this FAQ helps you transition smoothly and make the most of the updated UI.
## Activity name rules {#activity-name-rules}

The activity name cannot begin with `=`, `+`, `-`, or `@`. The activity name also cannot contain any of the following character sequences: `;=`, `;+`, `;-`, `;@`, `,=`, `,+`, `,-`, `,@`, `["`, or `"]`.

## Select an audience in the Targeting step {#audience-selection-steps}

1. To change the audience, click the **[!UICONTROL Replace]** icon ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) in the right frame.

1. In the **[!UICONTROL Add Audience]** dialog box, [select the desired audience](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), then click **[!UICONTROL Assign Audience]**.

   To create an audience that combines several audiences, click **[!UICONTROL Combine Audiences]**. For details, see [Combine multiple audiences](/help/main/c-target/combining-multiple-audiences.md).

   To create a new audience that is not already in the [!UICONTROL Audience Library], click **[!UICONTROL Create Audience]**. In the [create-audience workflow](/help/main/c-target/c-audiences/audiences.md), choose one of the following options:

   * **[!UICONTROL Audience Library]**: Create an on-demand audience that is saved to the [!UICONTROL Audience Library] and can be reused in other activities.
   * **[!UICONTROL This activity only]**: Create an [activity-specific audience](/help/main/c-target/creating-activity-only-audience.md) that is not saved to the [!UICONTROL Audience Library] and can be used in the current activity only.

1. Click **[!UICONTROL Visitor Percentage]** in the right frame, then choose the percentage of qualifying visitors that you want to enter the activity.


