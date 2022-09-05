---
title: Explore land and property data
lang: en
ref: explore-land-and-property-data
layout: post
author: The Land and Property Data Proof of Concept Team
---
This prototype aimed to explore two things.

Firstly, the extra open geospatial datasets we’d added to the platform meant we could test using multiple large datasets in one “service”. This would give us an idea of what issues service builders might face and how the platform might be able to help when things scale up.

And secondly, we wanted to try out some potential interaction patterns.

We want the platform to be as self-serve as possible. Therefore, users - service builders - need a way to discover what data the platform has. There are two main parts to that. They need to be able to know what data exists and then they need to know the shape of the data. 

We ended up building a prototype where users can explore the data visually via a map. Users can turn the various layers on the map on and off, exploring what the data for each one looks like. They can also click on individual features (or multiple) and explore the shape of the underlying data records.

### What we learnt

A lack of consistency in the available data makes it hard to build services. This means using open data, even from the same source (DataMapWales), is not plug and play. For example, for all the datasets we added the attribute used to provide the name of the thing the geospatial data represents is different. 

Similarly, when it comes to providing bilingual data, it is a mixed bag. Some datasets include it, some don’t. And when they do we have the same consistency problem. Different attributes will be used for the Welsh names.

Geospatial data can be very large, which can have significant performance implications. A question we have to answer is “what is the role the platform should play in helping users manage this?”

Quickly integrating with the Open Street Map address service demonstrated how easy and simple it is to build on other services when you follow a common web standards approach to building services.

### Issues to resolve

Maps should always be used along with a none map alternative. However to build alternatives the platform needs to expose ways of discovering what datasets it holds without a user a) having to know about it and b) having to access the complete dataset to explore what individual data records look like