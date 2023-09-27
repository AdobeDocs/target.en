---
keywords: multivariate test;mvt;full factorial;mvt or a/b;multivariate a/b;traffic estimator;when to use mvt;mvt considerations;multivariate;partial-factorial;partial factorial;full-factorial
description: Learn how to use a [!UICONTROL Multivariate Test] (MVT) in [!DNL Adobe Target] to compare combinations of offers in elements on a page to determine which combination performs the best.
title: What is a [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: c8b60011-cb3a-4e28-b84f-06910687b14b
---
# [!UICONTROL Multivariate Test] overview

A [!UICONTROL Multivariate Test] (MVT) activity in [!DNL Adobe Target] compares combinations of offers in elements on a page to determine which combination performs the best for a specific audience. A [!UICONTROL Multivariate Test] activity also helps to identify which element most impacts the activity's success.

Multivariate testing helps you discover the relative influence specific elements have on conversion, compared to other elements on the page. Multivariate testing can also help you refine a combination of elements that have been shown to be effective.

One advantage a [!UICONTROL Multivariate Test] provides compared to an A/B test is the ability to show which elements on your page have the greatest influence on conversion. This advantage is also known as the "main effect." This information is useful, for example, to help you determine where to place content that you want to receive the most attention.

[!UICONTROL Multivariate Test] activities also help you find compound effects between two or more elements on a page. For example, a particular ad might produce more conversions when combined with a certain banner or hero image. This is also known as the "interaction effect."

[!DNL Target] uses full-factorial multivariate tests to help you optimize your content. A full-factorial multivariate test examines all possible combinations of content with equal probability. For example, if you have two page elements with three offers each, there are nine possible combinations (3x3). Three elements, with two containing three possible offers and one with two offers, provide 18 options (3x3x2).

In [!DNL Target], each combination is one experience. The [!UICONTROL Multivariate Test] compares each experience so that you can learn which combinations are the most successful. At the same time, data is collected and analyzed to understand how each location and the offers influence the success metric.

![multivariate image](assets/multivariate.png)

Because of the number of combinations that can be generated, a [!UICONTROL Multivariate Test] requires more time and traffic than an A/B test. The page must receive enough traffic to produce statistically significant results for each experience. To obtain useful results, you must understand the amount of traffic your page receives and test the optimal number of combinations for the right amount of time to get the required results. 

Target's [Traffic Estimator](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) can help you design a test that works with your traffic. Before you use the Traffic Estimator, you should have good statistics showing the number of impressions and conversions your site normally receives. Consider your traffic levels per day. The more experiences in an activity, the more traffic the activity must include or the longer your activity must run. If your amount of traffic isn't high, you should test a few combinations; otherwise, the amount of time required to produce meaningful test results might be too long to be useful.

## MVT terminology {#section_DF475CA7F34B4CFDB7BE7363761D64AE}

When setting up a multivariate test, it is useful to understand some basic terminology.

There are multiple terms used in different ways across the industry. This section defines the terms used by [!DNL Target].

**Combination:** The content variations created when you test multiple content options in multiple locations. For example, if you are testing three locations, each with three content options, then there are 27 possible combinations (3x3x3). A visitor to your site sees one combination, also referred to as an experience.

**Content:** The text or image comprising a test variation within a location. In a multivariate test, several content options within multiple locations are compared. In MVT methodology, the content is sometimes referred to as a *level*.

**Element:** A DOM element containing content variations to be tested in the MVT test. See also *Location*.

**Location:** A specific content area on a page, often contained by a single DOM element. In MVT methodology, a location is sometimes referred to as a *factor*. A full-factorial multivariate test compares all possible combinations of offers in your locations.

## When to use [!UICONTROL Multivariate Test] vs A/B {#section_3D2B966B6671406C861A1843EA41D28C}

Multivariate tests can be used together with A/B tests to optimize your page. Examples of when you might want to use them together include:

* Use an A/B test to optimize your page layout, followed by an MVT test to determine the best content in each element on the page.

  An A/B test can provide important feedback on the layout, and MVT tests excel on testing the content within the elements in your page design. Running an A/B test on the layout before testing multiple content options can help you to determine the best layout and the most impactful content. 

* Use an MVT test to determine which element is the most important, then follow up with a more focused A/B test on that element.

  When the number of different experiences exceeds five and spans two or more elements, it's a good idea to consider an MVT test before running your A/B tests. The MVT test shows which areas on the page are most likely to improve conversion. These are the elements that a marketer should focus on. For example, the MVT test might show that the call to action is the most important element for meeting your goals. Once you have determined which elements and content are most useful for helping you meet your goals, you can run an A/B test to further refine the results. For example, you could test two specific images against each other, or compare the wording or colors of a call to action. By following an MVT test with one or more A/B tests, you can determine the best possible content for the results you desire.

## Considerations {#section_979FE3F398654C1EA1C86E7DBC9A8DAD}

* Use an MVT test when you have at least three elements to test. If you have fewer, run a series of A/B tests. 
* Select the page elements that you believe have the strongest impact on the results. 
* Don't include too many elements or locations in a test. The larger the number, the longer the test duration. 
* Plan the test design in advance. Do not edit a test after it goes live and data starts being collected and analyzed. 
* Elements should be independent of each other.

  For example, do not test your layout and content in the same test.

* Plan additional time for QA because of the increase in the number of experiences. You can also use partial-factorial testing to decrease the amount of traffic needed for a multivariate test. For more information, see Partial-factorial testing below:

## Partial-factorial testing

[!DNL Target] offers full-factorial multivariate testing as a built-in activity option. In statistics, 
"Design of Experiments" offers many approaches, or designs, to determine which factors influence results. One such approach is the [Taguchi Method](https://en.wikipedia.org/wiki/Taguchi_methods) for partial-factorial testing. Taguchi enables marketers to make a set of assumptions that reduce the number of permutations of experiences that must be tested, and in turn decreases the traffic requirements for a multivariate test. This functionality and testing approach can be applied in [!DNL Target] using this [offline spreadsheet](/help/main/assets/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx).

If your team uses other Design of Experiments approaches, you can use this calculation spreadsheet as a reference implementation for custom experiment designs.

As you use the offline calculation spreadsheet, consider the following tips:

* Pick the elements that you want to change and the number of versions of each element (3x2, 4x3, and so forth). 
* Keep the numbering consistent. For example, if the button is Element 1 and the options are Blue, Green, and Yellow, the blue button is 1-1, the green button is 1-2, and the yellow button is 1-3. 
* The offline spreadsheet provides the appropriate number of experiences needed (four for a 3x2, nine for a 4x3, and so forth). 
* Build the experiences in the A/B workflow with the [Visual Experience Composer (VEC)](/help/main/c-experiences/experiences.md). You can use custom code, edit HTML, WYSIWYG, or any combination. 
* After the activity is over (based on the sample size calculator), run the results through the spreadsheet to get the other details.

For more considerations and best practices, see [Multivariate Test Best Practices](/help/main/c-activities/c-multivariate-testing/best-practices.md#reference_53635817FFB741EF8C4E56CC70688EDD). 

## Training videos

The following videos contain more information about the concepts discussed in this article.

### Activity Types (9:03) ![Overview badge](/help/main/assets/overview.png)

This overview video explains the activity types available in [!DNL Target]. Multivariate testing is discussed beginning at 4:20.

* Describe the types of activities included in [!DNL Adobe Target] 
* Select the appropriate activity type to achieve your goals 
* Describe the three-step guided workflow that applies to all activity types

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Creating Multivariate Tests (9:25) ![Tutorial badge](/help/main/assets/tutorial.png)

This video explains how to understand, plan, and create a multivariate test using the [!DNL ]Target three-step guided workflow.

* Define and design a multivariate test 
* Create a multivariate test

>[!VIDEO](https://video.tv.adobe.com/v/17395)
