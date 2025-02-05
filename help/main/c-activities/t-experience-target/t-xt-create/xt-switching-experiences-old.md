---
keywords: priority;experience create;priority;experience;audience;experience;switching experiences;visual experience composer
description: Learn how visitors can switch between experiences in an [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activity as their profiles evolve.
title: Can Visitors Switch Experiences in an [!UICONTROL Experience Targeting] Activity?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
---
# Switching experiences in [!UICONTROL Experience Targeting]

With [!UICONTROL Experience Targeting], you can control which experience visitors see as their profiles evolve. 

The following list presents just a few scenarios in which visitors' profiles can evolve, and you might want to present different content based on those changes:

| Scenario | Details |
|--- |--- |
|Geographic Location|As visitors travel for business or pleasure, they might view your website or mobile app from different geographic locations.|
|Customer Status|Visitors might be considered prospects before creating an account or purchasing a product.|
|Category Affinity|The [category affinity](/help/main/c-target/c-visitor-profile/category-affinity.md) feature in [!DNL Target] automatically captures the categories visitors view and then calculates the visitors' affinity for the category for targeting purposes. For example, visitors who viewed several articles on your website about a particular subject are presented with content related to that subject.|
|Day of Week|As the weekend approaches, you might want to show visitors content about movies, dining, or other forms of entertainment.|

To use these capabilities in [!DNL Target], it is important to understand the following information as you work with [!UICONTROL Experience Targeting] activities:

* **Priority is controlled by the order of experiences, top to bottom.** If a visitor qualifies for more than two audiences, that visitor receives content from the higher priority experience. 
* **Visitors switch between experiences in an [!UICONTROL Experience Targeting] activity if they start qualifying for the audience of a higher-priority experience.**

  For example, in the following activity setup, a visitor accessed your website from the United States and then traveled to Germany and visited your website a second time. During the first visit, this visitor qualified for Experience A (US visitors). After viewing your website from Germany, this visitor switched to Experience B (Germany visitors).

  ![Priority US > Germany](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Visitors also switch between experiences if they stop qualifying for their current audience but start qualifying for a lower-priority experience.** 
* **If visitors stop qualifying for their current experience, and do not qualify for another experience, they see default content.**

  For example, in the following activity setup, a visitor accessed your website from the United States and then traveled to France and visited your website a second time. During the first visit, this visitor qualified for Experience A (US visitors). After viewing your website from France, this visitor remains in the original experience.

  ![Priority US > Germany](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **An experience targeted to "All Visitors" can be used as the last experience in the [!UICONTROL Experience Targeting] activity to "catch" any visitors that have not qualified for any other experience. If an experience targeted to "All Visitors" is not the last in the order, other targeted experiences listed lower than this experience are still evaluated.**

  For example, in the following activity setup, a visitor accessed your website from the United States and then traveled to Germany and visited your website a second time. During the first visit, this visitor qualified for Experience A (US visitors). After viewing your website from Germany, this visitor remains in Experience A (US visitors).

  ![Priority US > All Visitors](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

  If this is undesirable, you can create a new audience that is explicitly defined as the inverse of your targeted audience, as shown in the following example:

  ![Priority US > Not US](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **With a single-experience [!UICONTROL Experience Targeting] activity, visitors remain in an experience even if they cease to qualify for the audience that put them in that experience.**

  If this is undesirable, you could create another experience targeted to the inverse audience (for example, "Not United States" as opposed to "United States"). 
  
  As another option, you could create an [!UICONTROL A/B Test] activity targeted to your desired audience with 100% traffic allocation, as shown below:

  ![Priority one experience](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **The priority of experiences is defined by their order (top down) as they display in the [!DNL Target] UI.**

  This is important to keep in mind in scenarios where a visitor might qualify for more than one of your audiences. For example, if you have two experiences: one targeted to "United States" and one targeted to "New York," a visitor located in New York qualifies for both audiences. Therefore, you must ensure that the "New York" experience is defined before the "United States" experience in the [!DNL Target] UI. This practice ensures that the more targeted "New York" experience has the higher priority, as shown in the following example:

  ![Priority NY > US](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)
