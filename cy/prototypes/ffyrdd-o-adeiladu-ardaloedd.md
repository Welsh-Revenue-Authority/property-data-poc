---
title: Ffyrdd o adeiladu ardaloedd
lang: cy
ref: ways-to-construct-areas
layout: prototype
author: The Land and Property Data Proof of Concept Team
breadcrumb:
    en: Ways to construct areas
    cy: Ffyrdd o adeiladu ardaloedd
---
For geographically varied policies a key need is defining the geography or area the policy will apply to.

There are many ways to do this, whether you are starting with a point, a pre-existing geometry or planning on defining your own bespoke one. The policy pattern work from phase 1 explains a few of the approaches.

This prototype tests out a few interaction patterns for how areas could be defined.

Showing them within the same prototype means it is easier to assess their differences and explore the nuances that need to be considered if using.

![A screen capture showing 3 different ways users could define an area. First, there is clicking on the map which draws a circle around a point. Second is drawing an area on the map. And the third option is selecting pre-existing shapes.](/property-data-poc/assets/images/prototype-ways-to-construct-areas-cy.gif){: .app-screenshot}

### What we learnt

Radius round a point needs to be an editable option. Will there be multiple points or one? How will you handle cross overs?

As previously mentioned Drawing areas has usability challenges.

Using pre-existing areas comes with its own challenges. Firstly, they were created for a specific purpose, meaning their granularity and characteristics might not suit the purpose of the new policy. For example, a local authority can include a wide range of different types of neighbourhood and you’d only want certain policies to apply to certain neighbourhoods.

Another thing to consider is that pre-existing areas change over time, how will the policy handle this? Will it be tied to a snapshot of the given area or will it adapt as the area changes? E.g. the boundaries of where the new policy applies changes along with the electoral wards…

### Issues to resolve

The platform functionality that lets us select pre-existing areas currently only works with geometries that are Polygons. A lot of the pre-existing areas are multi-polygons so we will need to extend the platform functionality to handle these.