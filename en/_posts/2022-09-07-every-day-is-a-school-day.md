---
title: Every day's a school day – lessons learned from the land and property platform
lang: en
ref: every-day-is-a-school-day
layout: post
author: Ashley Caddick
---

Since January 2021, we, the Welsh Revenue Authority (WRA) have been working with the Centre for Digital Public Services Wales (CDPS) through a dedicated delivery team from both originations to develop a land and property data platform for Wales. The intention for this platform was to provide a digital solution, at first to help the WRA to deliver regionalised land transaction tax (LTT) with the possibility for it to expand and support future policies or public sector organisations. We've now made the difficult decision to pause the development of the platform due to funding constraints as a result of the economic hardship the world is seeing. But don't worry, all the work so far won’t be wasted. We've already learnt so much that will support the WRA to continue to deliver regional Land Transaction Tax without a data platform. This blog outlines some of the key lessons from our journey to-date from a data perspective.

# Lesson 1 - Publicly available land and property data

We have learnt how to operate a small-scale platform by consuming the [price paid data](https://landregistry.data.gov.uk/app/ppd) from land registry. Through this we were able to load all the data for Wales since April 2018 and produce a prototype providing descriptive statistics for certain postcodes or areas. As part of this work, we also got to work with real life data for the first time. Here we noticed data quality issues where publicly available data was providing sales for properties with historic postcodes.  This is a key lesson for us that just because data is available it doesn't mean it is perfect. Any future team would need to make sure they consider applying rules and process when thinking about ingesting data to ensure that the quality of that source is considered.

# Lesson 2 - Consistency

This work has reiterated the need for consistent identifiers on property data across datasets. For example, we have seen the Unique Property Reference Number (UPRN), Title numbers & local authority reference numbers all used in various datasets, with no way currently for organisations to cross reference these different lists. This causes the data to lose some of its wider value of being able to accurately combine datasets from different sources to give a more comprehensive picture. This information is where real insights can be made to help leaders make better evidence-based decisions that are not currently available.

# Lesson 3 - User research
In a recent [blog](/2022/08/23/why-are-inaccuracies-creeping-into-addresses-on-the-land-transaction-tax-return.html) our excellent team outlined some areas of interest that arose during their user research. They spoke with people who complete the current LTT returns, focusing on the property location aspect. We are now actively considering this to hopefully improve the user experience whilst also improving the data quality for the WRA. The key findings and the current considerations are below.

| Issue      | Current thinking |
| ----------- | ----------- |
| When the address name from the WRA lookup doesn't exactly match the name the agents have, they modify the wording so that it matches what is on the title deed.| Identify the benefits of including a field where the title deed name can be entered or automatically populated alongside the property information|
|In every case the act of completing the return involves the rekeying of information - which is time consuming and error prone. |Consider whether we can, or should, develop application programming interfaces (APIs) which can enable third-party software to speak to WRA services to remove, some, or all, of the manual entry|
|There is generally only 1 known address, and this is used for the buyer, the seller and the property/land.|Try to better understand the barriers of why agents only have one address.|
|The LTT return asks for some information that is not part of the transaction process therefore there is no incentive to gather it now and it can result in delays to the return (e.g., hectares & VAT registration etc).|Assess the cost benefit of some of the fields within the return to see whether the potential delay is really necessary.|
|Location of land and property is rarely an issue for residential - usually only commercial land/property causes issues.|Re-evaluate the way we collect the land/property location information and whether different mechanisms need to be in place for different types of purchases.|

# Next steps

As mentioned at the start, the work will continue but differently. We will be working behind the scenes to develop a process for adapting the current LTT process to embed the regional aspect of the policy. As part of this we will continuously review the user research and carry on engaging with our users on how we best go about this. We will also be looking to work with Welsh Government and local government to shape regional LTT, such as how these areas are defined, and how we communicate this to the people of Wales. And finally, we will continue to work with other organisations to educate and share the benefits of location data. This will hopefully allow us to eventually continue our work on delivering a national strategic asset in the form of a land and property or a Welsh digital taxation platform which would enable cross government working and providing joined up services for the people of Wales. 
