---
keywords: activity change log;change log
description: Access an activity's change log in Adobe [!DNL Target] to view a record of who changed your activities and when the changes occurred.
title: How Can I See an Activities Change Log?
feature: Activities
exl-id: 72a901c1-4fba-4044-b72b-393cab56b936
TQID: 'https://experienceleague.adobe.com/YmadzVwbj4Hy1bk3Q7a0hp9oZ7-lSgl12ImQaEsiDwU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Activity change log {#change-log}

>[!BEGINSHADEBOX]

**On this page:** Learn how to view the actions performed on an activity, who performed them, and when.

>[!ENDSHADEBOX]

The [!DNL Adobe Target] **[!UICONTROL Change Log]** records the actions performed on an activity, including what changed, who made the changes, and when they occurred. It gives a clear history of the activity, and the **[!UICONTROL Change Log]** page is populated for real-time insights.

To access the **[!UICONTROL Change Log]** page:

1. Click **[!UICONTROL Activities]**, then click the activity in the list.
1. Click **[!UICONTROL Change Log]** in the left rail.

    The page lists the action performed, the date of the action, and the user who performed it any time an activity is created, updated, activated, or deactivated. Changes to custom targets and offers used in the activity are also listed.

    ![Change log menu](assets/change_logs.png)

1. To list the actions in ascending or descending order, click the **[!UICONTROL Date]** column header.

1. Refresh the page to see status changes. 

## Target audit log APIs

* [Revisions: Get the audit log by last author's name and a modified-after timestamp](https://developer.adobe.com/target/administer/admin-api/#tag/Revisions){target=_blank}
* [List activity changelog](https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/getChangelog){target=_blank}
