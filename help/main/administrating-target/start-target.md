---
keywords: Administration;approver role;approver
description: Perform the first tasks Adobe Target administrators should take after receiving the emailed invitation to Adobe Experience Cloud.
title: Where Do I Get Started Administering [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: b60236da-20ae-4bab-b261-6a33d2f70e23
TQID: 'https://experienceleague.adobe.com/GfadY-knTwzXCB-n1AZ9u3PtoAyJokn1OXu3elRhgXk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Administrator first steps

Complete these steps after you receive an invitation to join [!DNL Adobe Target] through the [!DNL Adobe Experience Cloud]. When you are ready to configure account defaults, see [How Do I Administer Target?](/help/main/administrating-target/administrating-target.md). For help finding **[!UICONTROL Administration]** in the UI, see [Understand the [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md).

**Workflow overview**

1. [Get invited to Target](#task_3E0817630774431983FAA3D2CB2E75BD): A system administrator adds you in the [!DNL Adobe Admin Console].
1. [Accept the invitation](#task_24FE66659E634B24AB61DB8497772E17): Sign in to [!DNL Experience Cloud] and link your [!DNL Target] account.
1. [Assign yourself the Approver role](#task_15CAA437A71444E2932B333D5E66A3C7): Confirm access and permissions for your license type.
1. [User management](/help/main/administrating-target/c-user-management/user-management.md): Add users and assign roles for [!DNL Target Standard] or [!DNL Target Premium].

## Get invited to [!DNL Target] {#task_3E0817630774431983FAA3D2CB2E75BD}

A system administrator in the [!DNL Adobe Admin Console] must add you as a user in [!DNL Target] by inviting you to join. The administrator should also add you to one or more role-specific product profiles (groups of users). Both tasks are done in the [Adobe Admin Console](https://adminconsole.adobe.com).

For step-by-step guidance, see [Learn how to manage users and product profiles](https://helpx.adobe.com/enterprise/using/users.html) in the Adobe Enterprise documentation.

After the administrator completes these steps, you receive an invitation email.

## Accept the invitation {#task_24FE66659E634B24AB61DB8497772E17}

After you receive the invitation to join the [!DNL Adobe Experience Cloud], accept it, sign in, and accept the [!UICONTROL End User License Agreement] (EULA).

Use the following steps to accept the invitation and link [!DNL Target] to your [!DNL Experience Cloud] account:

1. Accept the invitation to the [!DNL Adobe Experience Cloud].
1. If you do not already have an Adobe ID, you are prompted to create one.

   If you already have an Adobe ID, sign in when prompted.

1. Accept the [!UICONTROL Terms of Use].

1. Review the summary of what you have done so far, then click **[!UICONTROL Continue to Experience Cloud]**.

1. Sign in to the [!DNL Adobe Experience Cloud] and click **[!UICONTROL Link Account]**.

   >[!NOTE]
   >
   >If you do not link your account, you cannot access [!DNL Target].

   All [!UICONTROL Experience Cloud] products appear on the linking page. Click **[!UICONTROL Link Target]**, then enter your [!DNL Target] username and password.
1. Click **[!UICONTROL Continue to Experience Cloud]**.

   At this point, you might not yet have product profiles with entitlements to link; your system administrator can assign those in the [!DNL Adobe Admin Console].
1. Optionally, watch the video that introduces the [!DNL Adobe Experience Cloud].
1. To refresh your privileges and open the product, sign out of [!DNL Adobe Experience Cloud], then sign back in.
1. Continue to [Assign yourself the Approver role](#task_15CAA437A71444E2932B333D5E66A3C7).

## Assign yourself the Approver role {#task_15CAA437A71444E2932B333D5E66A3C7}

After you accept the invitation and sign in, confirm that [!DNL Target] appears in your [!DNL Experience Cloud] account, then assign yourself the [!UICONTROL Approver] role for [!DNL Target].

Choose the guidance that matches your license:

* If your organization has a [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) license, see [Learn how to specify roles and permissions](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Users*.
* If your organization has a [Target Premium](/help/main/c-intro/intro.md#premium) license, see [Step 6: Specify roles and permissions](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configure enterprise permissions*.

You can then set up users for [!DNL Target Standard] or [!DNL Target Premium]. See [User management](/help/main/administrating-target/c-user-management/user-management.md) for an overview and links to the correct workflow for your license.

## Permissions required for editing [!UICONTROL Administration] settings {#admin-permissions}

**Before April 22, 2025**: Users with [!UICONTROL Approvers] rights in the [!DNL Adobe Admin Console] could edit or change all settings on the [[!UICONTROL Administration]](/help/main/administrating-target/administrating-target.md) pages in [!DNL Target], regardless of their [!DNL Target] role.

**Effective April 22, 2025**: Only [!UICONTROL Product] and [!UICONTROL Solutions] admins can update settings in the [[!UICONTROL Administration]](/help/main/administrating-target/administrating-target.md) sections, regardless of their roles in [!DNL Target] workspaces. Users without this permission have read-only access to the [!UICONTROL Administration] sections.

This change improves organizational control over [!DNL Target] instance configuration and helps prevent accidental updates that could affect activity delivery across testing and personalization teams.
