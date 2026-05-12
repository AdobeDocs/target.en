---
keywords: integration;roles;user permissions;admin console
description: Learn how to grant existing Adobe I/O integrations access to all workspaces with the desired role in Adobe Target.
title: How Do I Grant Adobe I/O Access to Workspaces and Assign Roles?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 62f6399f-c590-470c-ac3b-e0c84db63112
TQID: https://experienceleague.adobe.com/8WUCeb4ztjDdWUEtawLYeC-4FDgn1SiGarmS1hqGNgI
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
    internal-label: Integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Grant Adobe I/O integrations access to workspaces and assign roles

[!UICONTROL Enterprise Permissions] allows [!DNL Target] customers to use a single organization, but divide it into workspaces for their different teams or workflows.

>[!NOTE]
>
>Properties and Permissions functionality is available as part of the [Target Premium](/help/main/c-intro/intro.md#premium) solution. They are not available in [!DNL Target Standard] without a [!DNL Target Premium] license.

The [!UICONTROL Enterprise Permissions] feature facilitates effective scaling of optimization programs across teams. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier in 2019. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the [!DNL Target] September 2019 release, [!DNL Target] [!UICONTROL Enterprise Permissions] provides customers with the following access controls:

* You can choose the workspaces to which the integration can be applied
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

This update supports the following use cases:

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Grant the Adobe I/O integration the access to select workspaces with the appropriate role to allow a central team to make API-driven changes in only a few workspaces.
* Allow each team owning its workspace to have its own integration whenever the team is ready to explore APIs and choose the role accordingly.
* Mix and match any of above scenarios.

**Action Needed**: Those customers who are currently leveraging APIs for CRUD operations on resources (activities, audiences, offers, and reporting) across all workspaces need to grant their existing Adobe I/O integration access to all workspaces with the desired role as per their use case. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of choice made from the [!UICONTROL Product Role] drop-down list. You can now choose the desired role.

>[!NOTE]
>
>If this action is not performed, after the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. There is no adverse reaction to setting up integrations in advance. The sooner you make this change, the better. Depending on the number of workspaces in your organization, this process takes only a few clicks to add an existing integration into workspaces with the desired role.

**To grant Adobe I/O integrations access to workspaces and to assign roles:**

1. Open the **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Click the **[!UICONTROL Products]** tab, then select the name of the desired product.

   ![Choose product in Adobe Admin Console](/help/main/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Select the desired workspace (Product Profile).

   ![Select the product profile](/help/main/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Click the **[!UICONTROL Integrations]** tab.

   ![Integrations tab](/help/main/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Conditional) To add a new integration, click **[!UICONTROL Add Integration]**, select the desired integration, then click **[!UICONTROL Save]**.

1. From the **[!UICONTROL Product Role]** drop-down list, select the desired role for that workspace:

   | Role | Description |
   |--- |--- |
   |Approver|Can create, edit, and activate or stop activities.|
   |Editor|Can create and edit activities before they are live, but cannot approve the launch of an activity.|
   |Observer|Can view activities, but cannot create or edit them.|
   |Publisher|Similar to the Observer role (can view activities, but cannot create or edit them). However, the Publisher role has the additional permission to activate activities.|
