---
keywords: faq;frequently asked questions;analytics for target;a4T;inflated;visit;visitor;partial hit;orphaned;orphan;partial-hit
description: Find answers to questions about inflated visit and visitor counts when using Analytics for [!DNL Target] (A4T). Learn how to minimize "partial data."
title: Where Can I Find FAQs About Inflated Visit and Visitor Counts with A4T?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
---
# Inflated visit and visitor counts - A4T FAQ

This topic contains answers to questions that are frequently asked about inflated visit and visitor counts when using Analytics as the reporting source for Target (A4T).

## I can see a spike in visits. How can I tell if I these visits are caused by partial-data hits? {#section_28506672C6224ED18AC74F6A02F6F811}

+++Answer
You can contact [Adobe Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to retrieve a Partial Data report. This information is not available directly in the [!DNL Analytics] UI.

+++

## What are the potential causes of partial-data hits? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

+++Answer
Partial-data hits are often the result from improper implementation, such as misaligned report suite IDs. There are also legitimate causes, which include slow pages, page errors, redirect offers in an activity, or outdated library versions.

+++

## Are there any particular types of [!DNL Target] activities that are more likely to cause partial-data hits? {#section_69837442A9B84366BEFDA4588B31E574}

+++Answer
Redirect offers immediately send a user to a different page, which means the [!DNL Analytics] call does not fire on the first page.

+++