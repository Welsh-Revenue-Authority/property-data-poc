---
title: Find your local authority
lang: en
ref: find-your-local-authority
layout: post
author: The Land and Property Data Proof of Concept Team
---

We built a very basic prototype service using the first set of publicly available data we added to the platform.

It is a narrow thread showing how the data we collect and store in the platform can be consumed and used in services.

We had collected local authority boundaries from [DataMapWales]())https://datamap.gov.wales/) so built a prototype that would let a user select a point on the map and the service would work out which local authority it was in.

We also added an integration with [What Three Words](https://what3words.com/pretty.needed.chill) to show how using open web technologies makes it easier to integrate with other services. And how these services can improve the experience of your own service. For example, where an address doesn’t exist for a transaction a user could provide the What Three Words combination and we can use that to determine the exact location.

### What we learnt

#### Working with geospatial data

A lot of the publicly available (gov) data is in OS grid format - a less widely used format than the web standard WGS84 format. Each coordinate reference system (CRS) has its advantages and disadvantages but we decided to prioritise interoperability and convert all the data we collected to WGS84. This provides the consistency needed to be able to more easily build services using it. We need to be mindful that converting between different CRSs, although relatively trivial (and is a solved problem), causes a loss of accuracy.

The [GOVUK standard for exchange of location point](https://www.gov.uk/government/publications/open-standards-for-government/exchange-of-location-point) is WGS84.

Getting an accurate location is a common problem that lots of people try to fix. This means there are lots of services we can integrate with that might help us create better services for our users. Using the WGS84 CRS makes this easier to do and integrate with map frameworks such as mapbox/maplibre.

#### Making data available via the platform

Although it was single, fairly simple dataset we were able to demonstrate how we could collect and add the local authority data into the basis of what could become a land and property platform. And with the data held in the platform we were able to build a simple API that called the data allowing this prototype to be built.

### Issues to resolve

The map starts zoomed out to the full extent of Wales. The only way to focus in on an area of concern is to pan and zoom the map. This means a user needs to have a pretty good understanding of the geography of Wales to do this effectively.

The “tax rate” field is always blank because we don’t yet have the land transaction tax rate data in the platform.