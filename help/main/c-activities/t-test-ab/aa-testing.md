---
keywords: a/b;a/a;aa;
description: Learn what an A/A test is, why you might want to perform an A/A test, how long you should run the test, and how to interpret the results.
title: What is A/A Testing?
feature: A/B Tests
exl-id: 7489f4f5-3655-45f9-a743-651ba1c23c53
TQID: 'https://experienceleague.adobe.com/-kLz0mG8LaFqEbB-9M89vJWTFjfypupbcOQ3MjQz-jQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# A/A testing {#aa-testing}

>[!BEGINSHADEBOX]

**On this page:** Learn what an A/A test is, why you might run one, why you might see lift between identical experiences, and the best practice for running an A/A test in [!DNL Target].

>[!ENDSHADEBOX]

Before performing an A/A test on your site using [!DNL Adobe Target], it is important to understand what an A/A test is, why you might want to perform an A/A test, how long you should run the test, and how to interpret the results.

## What is A/A testing? {#what-is-aa}

An A/A test differs from a standard A/B test in the way traffic is allocated and in what you want to learn:

* **A/B test:** Traffic is allocated to two or more different experiences. One experience is typically the "control," and variations of the experience are tested against the control to see which experience creates the most lift in a given metric. You typically want to discover a lift in conversion.
* **A/A test:** Traffic is allocated to two identical experiences, normally with a 50/50 traffic allocation split. Your goal is usually to determine that there is *no* difference in lift between the identical experiences.

## Why run an A/A test? {#why-aa}

Some organizations perform A/A testing when implementing a new testing tool, such as [!DNL Target], to determine whether:

* The activity was set up correctly
* The code was implemented correctly
* The reporting is accurate

Although few organizations run A/A tests, it is good practice to run them as "sanity" experiments to build trust after implementing the tool or before performing A/B tests that could impact conversion and revenue.

## Why identical experiences can show lift {#why-lift}

There are numerous reasons why you might see lift in one experience over another (identical) experience:

### The A/A test was monitored continually

A common problem in running any kind of test, including an A/A test, is to look at the results continually, and prematurely stop a test when you see statistical significance, and declare a winning experience. Analysts often do what is called "data peeking." Data peeking involves looking at the test data early and frequently while trying to determine which experience is performing better. The risk is to stop the test prematurely, which could invalidate the results.

In an A/A test, data peeking can often cause analysts to see lift in one experience, when in fact there should be no difference, because the two experiences are identical. In fact, with continuous peeking, A/A tests are *guaranteed* to show "statistical significance" (namely, a confidence above a certain threshold, such as 95%) at some point during the test.

### Statistical significance impacts your test results

The significance level of a test determines how likely it is that the test reports a significant difference in conversion rates between two different offers when, in fact, there is no real difference. This is known as a false positive, or a Type I error. The significance level is a threshold specified by the user and there is a trade-off between the tolerance for false positives and the number of visitors that must be included in the test in choosing the proper significance level.

A commonly used significance level in A/A and A/B testing is 5%, which corresponds to a confidence level of 95% (confidence level = 100% - significance level). A confidence level of 95% means that every time you perform a test, there is a 5% chance of detecting a statistically significant lift even if there is no difference between the experiences.

Suppose you want to achieve a 95% confidence level with your A/A test. With a 95% confidence level, 1 in 20 A/A tests could show statistically significant lift in conversions. With a 90% confidence level, 1 in 10 tests could show lift in conversions when testing identical experiences.

## Best practice {#best-practice}

If you decide that an A/A test is necessary in your organization, be aware that the identical experiences might temporarily show a difference from the control. This can be normal, depending on the time the test is allowed to run. The difference should shrink given more time and visitors.

Use regular A/B testing methodology:

1. Decide ahead of time what sample size to use, based on the minimum effect size (the minimum lift below which an effect is not important to your business), power, and significance levels you find acceptable. The **[!UICONTROL Adobe Target Sample Size Calculator]** is an important tool to help you determine what sample size you should aim for and how long you should run the test. See the [Adobe Target Sample Size Calculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

1. Allow adequate time and visitors before you reach any conclusions. In an A/A test, the goal is to *not* see a statistically significant result after your test has reached the desired sample size.

1. Remember that, depending on the significance level of your test, there is a chance that one experience will show a difference in lift, and even be declared the winner.

For information about how long you should run an activity, and other helpful tips and tricks, see the following articles:

* [How long should you run an A/B test?](/help/main/c-activities/t-test-ab/sample-size-determination.md)
* [Ten common A/B pitfalls and how to avoid them](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md)
