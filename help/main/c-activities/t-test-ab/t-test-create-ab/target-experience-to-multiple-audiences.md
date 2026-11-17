---
keywords: multiple audiences;experience versions;target experience versions
description: Discover how to target different audience segments with versions of the same experience in A/B activities.
title: Can I Use Multiple Experience Versions in an A/B Activity?
feature: A/B Tests
exl-id: 7afe36f0-ec46-4d63-bfff-45d2c8923a04
TQID: 'https://experienceleague.adobe.com/FleyH-u5cWI5vku9E4-RMWeIc95WgPy-VQ-eytxka18'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Multiple experience audiences in an A/B Test {#multiple-experience-audiences}

>[!BEGINSHADEBOX]

**On this page:** Learn how to target different audiences with versions of the same experience in an A/B activity, illustrated by a use case with the steps to follow, and the best practices.

>[!ENDSHADEBOX]

In [!DNL Adobe Target] A/B activities, you can target versions of the same experience to different audiences. You can set up multiple audiences for an experience in the **[!UICONTROL Visual Experience Composer]** (VEC) or in the Form-Based Experience Composer.

Data is collected for the experience regardless of version, so the report shows the performance of the experience, not of each version. Visitors can also switch between experience audiences as their profile changes. They are not stuck in the same experience for the lifetime of the activity.

## Use case {#use-case}

You are testing two experiences: 

* a geo-targeted banner

* a generic banner. 

The banner for each geography needs to be different, but the goal of the test is to determine whether geo-targeting performs better than generic content.

If you set up a separate experience for each location, you measure how each geography performs against the others. You do not measure whether geo-targeting helps meet your success goals when compared with the generic banner.

In this case, you need geo-specific versions of the experience, so that you can test the geo-targeted experience against a non-geo-targeted control.

To set up the geo-specific versions:

1. [Create an A/B activity](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) as you normally would.

   When you configure the experience that has multiple versions, select the audience for each version, as described in the following steps.

1. Select the experience, then click **[!UICONTROL Configure]** > **[!UICONTROL Multiple Audiences]**.

1. In the **[!UICONTROL Experience Audiences]** pane, click the **[!UICONTROL Add Audience]** icon ( ![Add icon](/help/main/assets/icons/Add.svg) ), then select the first audience that you want to target. Repeat for each audience.

   If the audience does not exist yet, [create the audience](/help/main/c-target/c-audiences/create-audience.md) and set it up.

1. Continue setting up the activity.

## Best practices {#best-practices}

* Choose mutually exclusive audiences. If a visitor qualifies for more than one audience, the content for all of these audiences is returned, and the content of the audience listed last is displayed on the page. This applies to activities created in the VEC.
* Activity-entry audiences that are defined in the diagram are combined with the experience audiences by using an AND condition. To enter the activity, a visitor must qualify for the activity audience and for one of the experience audiences.
* Add the same audiences as segments for reports. This helps you look at the test results at the high level of experience A versus B, and at the lower level of experience A versus B for only "browser lang ja_JP". This works only for [!DNL Target]-based reports, not for [!DNL Analytics]-based reports.
