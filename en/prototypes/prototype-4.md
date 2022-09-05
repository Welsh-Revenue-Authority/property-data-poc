---
title: Search land and property data by area
lang: en
ref: search-land-and-property-data-by-area
layout: post
author: The Land and Property Data Proof of Concept Team
---
With this prototype we wanted to use some different functionality provided by the platform. Instead of returning complete datasets the platform now let service builders query for subsets of the data. A user can provide a bounding box and receive only the data contained within it.

To be able to implement geographically varying policies it will be essential to be able to define new areas. In turn, these geometries would need to be available through the platform. We wanted to explore and demonstrate that the platform could make it easier to create tools to help users create the areas.

One potential approach and potential interaction pattern is a user drawing or creating an area on the web-based maps we’ve added to previous prototypes.

We wanted to know if this was possible? What would be involved to add drawing capabilities to the maps? And would users be comfortable doing this? Would they only be comfortable if they’d had previous experience using GIS software? And could this sort of web alternative be built into other services?

### What we learnt

We have questions about the practicalities of using this pattern.

Generally, drawing accurate shapes on a map can be quite hard for users. Other projects have seen the same challenges so if this was part of any service we would need to do a lot of user research. 

We would want to know the proficiency level of the users expected to create the shapes - they might be experienced GIS officers?

We would want to know what tools they currently use and which they are comfortable with. 

And we’d want to know what processes they follow. How do they draw it? Do they return to it? Do they edit it? Are multiple people involved?

It would also be important to figure out how accurate the shapes need to be, or what precision level is allowable?.

Interestingly, the API functionality provided by Geonode returns partial features. For example, if I draw an area that intersects with a National Park it will not return the complete national park boundary, it will return only the part of the national park geometry that is contained within the area.

### Issues to resolve

The API only allowed bounding box queries. This made it harder for the UI to reflect what was happening. If we wanted to take this further it wouldn’t be too hard to extend the API to allow bespoke shapes. It was a known problem so we wouldn’t have learnt much by solving it now.