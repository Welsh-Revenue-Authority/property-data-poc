---
title: Explore land and property data
lang: en
ref: explore-land-and-property-data
layout: prototype
author: The Land and Property Data Proof of Concept Team
breadcrumb:
    en: Explore land and property data
    cy: Archwilio data tir ac eiddo
---
This prototype aimed to explore two things.

Firstly, the extra open geospatial datasets we’d added to the platform meant we could test using multiple large datasets in one “service”. This would give us an idea of what issues service builders might face and how the platform might be able to help when things scale up.

And secondly, we wanted to try out some potential interaction patterns.

We want the platform to be as self-serve as possible. Therefore, users - service builders - need a way to discover what data the platform has. There are two main parts to that. They need to be able to know what data exists and then they need to know the shape of the data. 

We ended up building a prototype where users can explore the data visually via a map. Users can turn the various layers on the map on and off, exploring what the data for each one looks like. They can also click on individual features (or multiple) and explore the shape of the underlying data records.

![A screen capture showing a user exploring the data on a map. The users selects and deselects layers, their choices are reflected on the map. Then the user clicks on an item on the map. The data records for the clicked on features are displayed in a side panel for the user to examine.](/property-data-poc/assets/images/prototype-explore-land-and-property-data.gif){: .app-screenshot}

### What we learnt

**Available data lacks consistency**

A lack of consistency in the available data makes it hard to build services. This means using open data, even from the same source ([DataMapWales](https://datamap.gov.wales/)), is not plug and play. For example, for all the datasets we added the attribute used to provide the name of the thing the geospatial data represents is different. 

![An image containing an example data record for a National Park, a Local Authority and a Ward. It shows all the attributes for each record, which demostrates how different they all are. Including all using a different attribute for the name of the thing](/property-data-poc/assets/images/prototype-inconsistent-geographies-3-examples.png)

**Data is not always bilingual**

Similarly, when it comes to providing bilingual data, it is a mixed bag. Some datasets include it, some don’t. And when they do we have the same consistency problem. Different attributes will be used for the Welsh names.

**How should the platform handle large datasets**

Geospatial data can be very large, which can have significant performance implications. A question we have to answer is “what is the role the platform should play in helping users manage this?”

**Following standards makes it easier to integrate**

Quickly integrating with the Open Street Map address service demonstrated how easy and simple it is to build on other services when you follow a common web standards approach to building services.

### Issues to resolve

**Service builds need to access metadata about datasets**

We know that maps should always be used along with a non-map alternatives. However it is not possible for us to easily build them at the moment. To build alternatives the platform needs to expose ways of discovering what datasets it holds.

At the moment a user needs to already know a dataset exists - how do they find this out?

Then, they have to access the complete dataset to find out what it contains, see if it is complete and understand what attributes an individual record includes.

We need to provide service builders with the tools to be able to do this more easily.