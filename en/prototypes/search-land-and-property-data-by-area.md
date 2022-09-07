---
title: Search land and property data by area
lang: en
ref: search-land-and-property-data-by-area
layout: prototype
author: The Land and Property Data Proof of Concept Team
breadcrumb:
    en: Search for data by area
    cy: Chwilio am ddata fesul ardal
---
With this prototype we wanted to use some different functionality provided by the platform. Instead of returning complete datasets the platform now provides the ability for service builders to query subsets of the data. A user can provide a bounding box and receive only the data contained within it.

To be able to implement geographically varying policies it will be essential to be able to define new areas. In turn, these geometries would need to be available through the platform. We wanted to explore and demonstrate that the platform could make it easier to create tools to help users create the areas.

One potential approach and potential interaction pattern is a user drawing an area on the web-based maps we’ve added to previous prototypes.

We wanted to know if this was possible. What would be involved to add drawing capabilities to the maps? Would users be comfortable doing this? Would they only be comfortable if they’d had previous experience using GIS software? And is there a common pattern for this interaction that could be built into numerous services?

![A screen capture of the search land and property data by area prototype. It shows a user drawing an area. After the user draws a shape, a boundaing box is displayed around it. Then data from the platform is show within this box.](/property-data-poc/assets/images/prototype-search-land-and-property-data.gif){: .app-screenshot}

### What we learnt

**Drawing accurate shapes on a map is hard**

We have questions about the practicalities of using this pattern.

Generally, drawing accurate shapes on a map can be quite hard for users. Other projects have seen the same challenges so if this was part of any service we would need to do a lot of user research. 

We need to know the proficiency level of the users expected to create the shapes - are they experienced GIS officers?

We need to know what tools they currently use and which ones they are comfortable with. 

And we need to know what processes they follow. How do they draw it? Do they start and return to it? Do they edit it? Are multiple people involved?

It would also be important to figure out how accurate the shapes need to be, or what precision level is allowable?

**Partial features are returned by Geonode**

The intersecting query API, which is out the box functionality provided by Geonode, returns partial features. For example, if I draw an area that intersects with a National Park it will not return the complete national park boundary, it will return only the part of the national park geometry that is contained within the area.

### Issues to resolve

The API only allowed bounding box queries. This made it harder for the UI to reflect what was happening. If we wanted to take this further it wouldn’t be too hard to extend the API to allow bespoke shapes.
