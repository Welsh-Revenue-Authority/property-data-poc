---
title: Dywedwch wrthyf am leoliad
lang: cy
ref: tell-me-about-a-location
layout: prototype
author: The Land and Property Data Proof of Concept Team
breadcrumb:
    en: Tell me about a location
    cy: Dywedwch wrthyf am leoliad
---

-- Welsh text to be added --

**A location in Wales**

![A screen capture of the tell me about a location prototype. A user enters a location in Wales and is presented with all the information the platform has on it. Including which areas it is in such as the local authority. It also displays tax information for the location.](/property-data-poc/assets/images/prototype-tell-me-about-a-location-in-wales-cy.gif){: .app-screenshot}

**A location not in Wales**

![A screen capture of the tell me about a location prototype. A user enters a location that is not in Wales and is presented with confirmation that the location is not in Wales.](/property-data-poc/assets/images/prototype-tell-me-about-a-location-not-in-wales-cy.gif){: .app-screenshot}

### What we learnt

**The data is inconsistent**

Inconsistent data makes these services harder to build. There is no way to know which dataset a record belongs to if you look at it in isolation. This makes it harder to say the location is in the `name` National Park. The service builder needs to either check the data record looks like a record from the National Park dataset, or to know they are requesting data only from the National Park dataset.

Service builders also need to know what attributes are used in National park records and which attributes are used in Electoral Wards. For example, they can’t just assume there will be a `name` attribute used. Electoral Ward records include a `name` attribute. However, National Park records contain a `np_name` attribute.

![An image containing an example data record for a National Park, a Local Authority and a Ward. It shows all the attributes for each record, which demostrates how different they all are. Including all using a different attribute for the name of the thing](/property-data-poc/assets/images/prototype-inconsistent-geographies-3-examples.png)

We need to decide how much preprocessing the platform should do when it collects the data. Should the platform try to add consistency to the data or should the onus fall on to the creators of the data? 
Similarly, what tools are needed for service builders to be able to use the data effectively?

**Council tax is more complicated that the available data suggests**

We assumed the council tax dataset we were using would allow us to confidently say “this is how much you would pay for a band in a region”. Only by showing this in the prototype were we made aware of the nuances in the data that would mean it couldn’t be used as we’d intended. 

The data needed to show the amounts that make up the exact council tax amount are not all readily available. If they were, service builders could use the platform to calculate an accurate council tax amount for any property.

**Linking datasets adds value**

Another area where the platform can add value is by providing links between the disparate datasets. This would allow service builders to use data in ways that is currently hard to do. For example, the platform can determine which local authority and community a location is in. Then it can use these to return the council or community tax amounts for those areas.

Modelling relationships between data can be something the platform solves once so each service built on top of the data doesn’t have to repeat the same steps.

**It doesn't have to be a map**

We don’t always need a map to build a geographic-based service.

### Issues to resolve

The prototype doesn’t know how to handle situations where a location is near a boundary. In these cases, small inaccuracies in the data could lead to false results. So maybe the output needs to be less YES/NO and more degree of confidence.