---
keywords: random forest;decision tree;ap;Automated Personalization
description: Learn how [!DNL Adobe Target] uses the Random Forest algorithm in both [!UICONTROL Automated Personalization] (AP) and [!UICONTROL Auto-Target] activities.
title: How Does [!DNL Target] Use the Random Forest Algorithm?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
TQID: 'https://experienceleague.adobe.com/Ui8E8CkiiJSdqim9fzIgPDdsKG1MMtuu3EUuAqgmm0M'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Random Forest algorithm {#random-forest-algorithm}

>[!BEGINSHADEBOX]

**On this page:** Learn how [!DNL Target] uses the Random Forest algorithm to build the personalization models of **[!UICONTROL Automated Personalization]** and **[!UICONTROL Auto-Target]** activities.

>[!ENDSHADEBOX]

The main personalization algorithm used in both **[!UICONTROL Automated Personalization]** (AP) and **[!UICONTROL Auto-Target]** activities is Random Forest. It is a classification or regression method that operates by constructing a multitude of decision trees when it is being trained.

Random Forest is an ensemble method. When you think of statistics, a single regression model used to predict an outcome might come to mind. The latest data science research suggests that "ensemble methods," where multiple models are created from the same data set and then intelligently combined, produce better results than predicting based on a single model alone, or than could be obtained from any of the constituent learning algorithms.

## What is a decision tree? {#section_7F5865D8064447F4856FED426243FDAC}

A decision tree breaks down all the visit data that a system can learn from into groups. Visits within each group are as similar as possible to each other with regard to the goal metric (for example, conversion rate), and visits across groups are as different as possible. To do this, the tree looks at the variables in the training set and splits the data in a Mutually Exclusive Collectively Exhaustive (MECE) way into groups (or "leaves") that maximize this goal.

In the following simple example, the goal metric is conversion and there are two input variables:

* Gender (with two potential values, Male or Female)
* Zip Code (with five potential values in the small data set: 11111, 22222, 33333, 44444, or 55555)

### First split {#first-split}

The tree first determines which of the two variables explains the largest amount of variation in the conversion rate of the visit data. Assume that zip code is most predictive. This variable forms the first "branch" of the tree. The tree then splits the visit data into groups, as described above. Assume that 11111, 22222, and 33333 are one split, and 44444 and 55555 are a second split.

![First layer of the decision tree](assets/decsion_tree_1.png){width="440" align="center"}

### Split within each branch {#second-split}

The tree poses the question, "What is the most predictive variable?" again, and completes a similar exercise to split the data *within each branch*. Only gender remains, so it is the answer here. In the 11111, 22222, and 33333 branch, assume that there is a difference in conversion between men and women. There are then two leaves (men and women), and this branch is complete. In the 44444 and 55555 branch, assume that there is no statistical difference between how women and men convert. In this case, the first split is the final split.

![Complete decision tree](assets/decsion_tree_2.png){width="480" align="center"}

## How are decision trees used by Random Forest? {#section_536C105EF9F540C096D60450CAC6F627}

Decision trees are a useful statistical tool. However, they have some disadvantages. Most critically, they can "over-fit" the data, so that an individual tree poorly predicts future data that was not used to build the initial tree. This challenge is known as the [bias-variance tradeoff](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) in statistical learning.

Random forests help overcome this challenge. A random forest is a collection of hundreds of decision trees that are built slightly differently on the same data set and that "vote" together to yield a better model than an individual tree. The trees are built by randomly selecting a subset of visit records with replacement (known as bagging) and randomly selecting a subset of the attributes, so that the forest consists of slightly different decision trees. This method introduces small variations into the trees. Adding this controlled amount of variance helps improve the predictive accuracy of the algorithm.

## How do the [!DNL Target] personalization algorithms use Random Forest? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### How models are built

[!DNL Target] uses data that it collects automatically, and custom data provided by you, to build its personalization algorithms. The following diagram summarizes how models are built for **[!UICONTROL Auto-Target]** and **[!UICONTROL Automated Personalization]** activities:

![Flow that summarizes how Random Forest models are built](assets/random_forest_flow.png){width="850" zoomable="yes"}

1. [!DNL Target] collects data on visitors while randomly serving experiences or offers.
1. After [!DNL Target] hits a critical mass of data, [!DNL Target] performs feature engineering.
1. [!DNL Target] builds Random Forest models for each experience or offer.
1. [!DNL Target] validates the model by checking whether it meets a threshold quality score.
1. [!DNL Target] pushes the model to production to personalize future traffic.

These models predict the best experience or offer to show to visitors. Generally, one model is built per experience (in an **[!UICONTROL Auto-Target]** activity) or per offer (in an **[!UICONTROL Automated Personalization]** activity). [!DNL Target] then displays the experience or offer that yields the highest predicted success metric (for example, conversion rate). The models must be trained on randomly served visits before they can be used for prediction. As a result, even the visitors who are in the personalized group are randomly shown different experiences or offers when an activity first starts, until the personalization algorithms are ready.

Models are validated based on their Area Under the Curve (AUC), to ensure that each model is good at predicting the behavior of visitors before it is used in your activity. The exact time when a model starts serving personalized experiences depends on the details of the data, because the model must be validated first. In practice, and for traffic planning purposes, it usually takes more than the minimum number of conversions before each model is valid.

When a model becomes valid for an experience or offer, the clock icon to the left of the experience or offer name changes to a green checkbox. When there are valid models for at least two experiences or offers, some visits start to become personalized.

### Feature transformation

Before the data goes through the personalization algorithm, it undergoes a feature transformation, which can be thought of as preparing the data collected in the training records for use by the personalization models. The transformation depends on the type of attribute (or "feature," as data scientists sometimes describe it):

| Feature type | Description | Transformation |
|---|---|---|
| **Categorical** | Cannot be counted but can be sorted into different groups, such as country, gender, or zip code. | A set of all possible features is maintained and the likelihood transformation is used to reduce the data size. |
| **Numeric** | Can be measured or counted, such as age or income. | Rescaling ensures that the features are comparable across the board. |

### Balancing learning versus personalizing with the multi-armed bandit

After [!DNL Target] has built the personalization models, you face a tradeoff for future visitors to your activity. You can personalize all the traffic based on the current model, or you can continue to learn from new visitors by randomly serving them random offers. The personalization algorithm should always learn about new trends in your visitors while it personalizes most of the traffic. The multi-armed bandit is how [!DNL Target] meets this goal: it ensures that the model always "spends" a small fraction of traffic to continue to learn throughout the life of the activity and to prevent over-exploitation of previously learned trends.

In the data-science world, the multi-armed bandit problem is a classic example of the exploration versus exploitation dilemma, in which a collection of one-armed bandits, each with unknown reward probability, is given. The key idea is to develop a strategy that results in the arm with the highest success probability being played, so that the total reward obtained is maximized. The multi-armed bandit is used in the system for online scoring after the online models are built. This process helps with online learning during exploration. The current multi-armed algorithm is an epsilon (ε) greedy algorithm. In this algorithm, with probability 1 - ε, the best arm is chosen. With probability ε, any other arm is randomly chosen.
