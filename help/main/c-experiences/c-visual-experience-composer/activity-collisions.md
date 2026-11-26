---
keywords: targeting;collisions;conflicts
description: Prevent content delivery collisions on the same page by configuring activities correctly in Adobe Target.
title: How Can I Avoid Activity Collisions?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
TQID: 'https://experienceleague.adobe.com/R6cwp4KnoYPO9Wxr47HswtBX6jKPJ0i-UGdtA1ZHawU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Activity collisions {#activity-collisions}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use the **[!UICONTROL Collisions]** tab to find activities that might deliver content to the same page.

>[!ENDSHADEBOX]

An activity collision occurs when multiple activities are set up to deliver content to the same page. If an activity collision occurs, the expected content might not appear on the page.

The **[!UICONTROL Collisions]** tab on the **[!UICONTROL Activity Overview]** page in [!DNL Adobe Target] lists the activity collisions on the site, and shows whether an activity contains potential collisions. The **[!UICONTROL Collisions]** list helps to:

* Identify whether a test is already running on a page before a new activity is set up
* Troubleshoot an activity if the expected content does not appear

## Access the Collisions tab {#access-collisions}

Click **[!UICONTROL Activities]**, click the desired activity from the list, then access  the **[!UICONTROL Collisions]** menu.

  ![Configure icon](assets/collisions_1.png)

All activities on the same URL are listed, regardless of any audience targeting in each activity. The tab lists the activities that might be colliding. If the collision alters the expected experience, edit the activity.

## Read the Collisions list {#collisions-list}

The **[!UICONTROL Collisions]** list shows every [!DNL Target] scenario where the mbox is used and that uses the same URL. For each potential collision, the list shows the Activity URL, the mbox name where the collision might occur, and any activities that match both of those criteria. If there are multiple mboxes, they are each listed.

The list also shows the status and priority of each potential collision, along with other information. The status and priority help determine the likelihood of a collision occurring. For two activities that might collide:

* If one activity is not currently active, a collision cannot occur. A collision is only possible if the inactive activity becomes active.
* If the potential collision is between two live activities with the same priority and the same audience, a collision occurs. The priority or the status can be changed to prevent the collision.
* If the audiences are different, there is still a potential collision, because a particular visitor could belong to multiple audiences. 
