---
title: Tell me about a location
lang: en
ref: tell-me-about-a-location
layout: prototype
author: The Land and Property Data Proof of Concept Team
---
So far our prototypes have focused on getting a location or showing a user what data the platform held.

Getting a location is usually the first step in a process. A service needs to determine a location to then be able to do that something else.

Often policies and rules apply to specific geographic regions. Geographic areas can be large, like nations (e.g. in Wales, Land Transaction Tax is paid on property purchases) or small, like wards (e.g. to vote you must go to this polling station). First, you need a location; then you can figure out what geographic policies apply.

With this prototype, we wanted to show how the platform makes building these services easier.
During the Proof of concept phase, the team built the “is it in Wales” service. The team used synthetic data to build the proof-of-concept service. We wanted to prove we could rebuild a similar service using real data we’d already managed to collect for the platform.

We wanted to build something that would determine the users’ location, work out what we know about this location and then cross reference the location with any other data to see what applies to the location.

### What we learnt

Inconsistent data makes these services harder to build. There is no way to know which dataset a record belongs to if you look at it in isolation. This makes it harder to say the location is in the `name` National Park. The service builder needs to either check the data record looks like one from the National Park dataset, or to know they are requesting data only from the National Park dataset.

Similarly, the service builder needs to know what attributes are used in National park records and which attributes are used in Electoral Wards. For example, they can’t just assume there will be a `name` attribute used.

There is an open question about how much preprocessing the platform should do when it collects the data? And what tools are needed for service builders to be able to use the data effectively?

We assumed the council tax dataset we were using would allow us to confidently say “this is how much you would pay for a band in a region”. Only by showing this in the prototype were we made aware of the nuances in the data that would mean it couldn’t be used as we’d intended. 

The data needed to show the amounts that make up the exact council tax amount are not all readily available. If they were, service builders could use the platform to always calculate an accurate and informative council tax amount for a property.

Another area where the platform can add value is by providing links between the disparate datasets. This would allow service builders to use data in ways that is currently hard to do. For example, the platform can determine which local authority and community a location is in. Then it can use these to return the council or community tax amounts for those areas.

Modelling relationships between data can be something the platform solves once so each service built on top of the data doesn’t have to repeat the same steps.

We don’t always need a map to build a geographic-based service.

### Issues to resolve

The prototype doesn’t know how to handle situations where a location is near a boundary. In these cases, small inaccuracies in the data could lead to false results. So maybe the output needs to be less YES/NO and more degree of confidence.