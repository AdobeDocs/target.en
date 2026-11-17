---
keywords: priority;experience create;priority;experience;audience;experience;switching experiences;visual experience composer
description: Learn how visitors can switch between experiences in an [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activity as their profiles evolve.
title: Can Visitors Switch Experiences in an [!UICONTROL Experience Targeting] Activity?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
TQID: 'https://experienceleague.adobe.com/4bBukCristluFUClhewMcSsNMTPjLjXEqM1QyyropKU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: b6f5758b-84f7-4943-8b05-1297a046943c
    internal-label: Experience target
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Switching experiences in [!UICONTROL Experience Targeting] {#switching-experiences}

>[!BEGINSHADEBOX]

**On this page:** Learn how priority works in an **[!UICONTROL Experience Targeting]** activity and when visitors switch between experiences as their profiles evolve.

>[!ENDSHADEBOX]

With **[!UICONTROL Experience Targeting]**, you can control which experience visitors see as their profiles evolve. The profile of a visitor can change in several ways, and you might want to present different content based on those changes. The following table lists a few examples:

| Scenario | Details |
|--- |--- |
|Geographic Location|As visitors travel for business or pleasure, they might view your website or mobile app from different geographic locations.|
|Customer Status|Visitors might be considered prospects before creating an account or purchasing a product.|
|Category Affinity|The [category affinity](/help/main/c-target/c-visitor-profile/category-affinity.md) feature in [!DNL Target] automatically captures the categories that visitors view and then calculates the affinity of the visitors for each category for targeting purposes. For example, visitors who viewed several articles on your website about a particular subject are presented with content related to that subject.|
|Day of Week|As the weekend approaches, you might want to show visitors content about movies, dining, or other forms of entertainment.|

To use these capabilities in [!DNL Target], it is important to understand the following information as you work with **[!UICONTROL Experience Targeting]** activities.

## How visitors are served {#how-visitors-are-served}

The order of the experiences in the [!DNL Target] UI, from top to bottom, controls their priority, so define the more targeted experience before the broader one. The following table summarizes what visitors see in each situation.

| Situation | What the visitor sees |
|--- |--- |
|The visitor qualifies for more than one audience.|The content of the experience that has the higher priority.|
|The visitor starts qualifying for the audience of a higher-priority experience.|The visitor switches to the higher-priority experience.|
|The visitor stops qualifying for the current audience but starts qualifying for a lower-priority experience.|The visitor switches to the lower-priority experience.|
|The visitor stops qualifying for the current experience and does not qualify for another experience.|Default content.|
|The visitor has not qualified for any other experience, and the last experience is targeted to "All Visitors".|The "All Visitors" experience. This experience "catches" the visitors that have not qualified for any other experience.|
|An experience targeted to "All Visitors" is not the last in the order.|The targeted experiences listed lower than the "All Visitors" experience are still evaluated.|
|The activity has a single experience, and the visitor ceases to qualify for its audience.|The visitor remains in the experience.|

## Examples {#examples}

The following examples illustrate these situations.

### Priority: New York and United States

If you have two experiences, one targeted to "United States" and one targeted to "New York", a visitor located in New York qualifies for both audiences. Therefore, you must define the "New York" experience before the "United States" experience in the [!DNL Target] UI. This practice ensures that the more targeted "New York" experience has the higher priority, as shown in the following example:

![Priority NY > US](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-refresh.png)

### Switching to a higher-priority experience: United States to Germany

In the following activity setup, a visitor accessed your website from the United States and then traveled to Germany and visited your website a second time. During the first visit, this visitor qualified for Experience A (US visitors). After viewing your website from Germany, this visitor switched to Experience B (Germany visitors).

![Priority US > Germany](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-refresh.png)

### Leaving the audience: United States to France

In the following activity setup, a visitor accessed your website from the United States and then traveled to France and visited your website a second time. During the first visit, this visitor qualified for Experience A (US visitors). After viewing your website from France, this visitor remains in the original experience.

![Priority US > Germany, visitor from France](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-refresh.png)

### Experience targeted to All Visitors

In the following activity setup, a visitor accessed your website from the United States and then traveled to Germany and visited your website a second time. During the first visit, this visitor qualified for Experience A (US visitors). After viewing your website from Germany, this visitor remains in Experience A (US visitors).

![Priority US > All Visitors](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-refresh.png)

If this is undesirable, you can create a new audience that is explicitly defined as the inverse of your targeted audience, as shown in the following example:

![Priority US > Not US](/help/main/c-activities/t-experience-target/t-xt-create/assets/not-us.png)

### Single-experience activity

With a single-experience **[!UICONTROL Experience Targeting]** activity, visitors remain in an experience even if they cease to qualify for the audience that put them in that experience. If this is undesirable, you can create another experience targeted to the inverse audience (for example, "Not United States" as opposed to "United States"). As another option, you can create an **[!UICONTROL A/B Test]** activity targeted to your desired audience with 100% traffic allocation, as shown in the following example:

![Priority one experience](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-refresh.png)
