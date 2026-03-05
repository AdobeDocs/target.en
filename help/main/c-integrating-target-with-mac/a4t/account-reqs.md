---
keywords: Analytics as reporting source;a4t;A4T;requirements
description: Learn how to configure the user account requirements necessary to create an Adobe Analytics-based activity in Adobe [!DNL Target] using Analytics for [!DNL Target] (A4T).
title: Which User Permission Requirements Are Needed for A4T?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
TQID: https://experienceleague.adobe.com/SGNIoARqe3yN4WvKF4JPIp0t0JCMiSgj--zrjt-ZXJQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# User permission requirements

Information about the user account requirements to create an [!DNL Adobe Analytics]-based activity in [!DNL Adobe Target] (A4T).

Before a report suite can be selected when defining an [!DNL Analytics] activity, you need both an [!DNL Analytics] user account and a [!DNL Target] user account. 

Your user accounts must be configured as described in the following sections:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Complete the following tasks in the [!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com):

### Link solution accounts to your Adobe ID

Your [!DNL Analytics] and [!DNL Target] user accounts must be linked to your Adobe ID.

For more information, see [Organizations and account linking](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en).

### Configure Experience Cloud group membership

You must be a member of one or more [!DNL Experience Cloud] groups that have access to [!DNL Analytics] and [!DNL Target].

For more information, see [Manage Experience Cloud users and products](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

To use A4T on a given report suite, you must have access to that report suite and grant access to the [!DNL Web Services Access] group. 

1. In **[!UICONTROL Admin Console]**, click an [!DNL Analytics] product profile, then click the **[!UICONTROL Permissions]** tab. 

   You can then see which report suites the profile has access to. 

1. Ensure that the report suite you want to have access to in [!DNL Target] is one of the ones listed in the product profile you are a part of.

   The following illustration is an example of a product profile that has access to all report suites:

   ![Admin Console Permission tab](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Configure access to the [!UICONTROL Web Services Access] group.

   Access to the [!UICONTROL Web Services Access] group in [!DNL Analytics] is required to be able to use [!DNL Analytics] as the reporting source for [!DNL Target].


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

No additional privileges are required.
