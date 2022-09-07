---
title: Provide a location journey
lang: en
ref: provide-a-location-journey
layout: prototype
author: The Land and Property Data Proof of Concept Team
breadcrumb:
    en: Provide a location journey
    cy: Darparu taith lleoliad
---
Building on the prototype created to test using the local authority boundary data we created a sample “provide a location” journey.

Users are asked to provide an address when they submit a Land Transaction Tax (LTT) return. In most cases they have an address and are able to provide it. WRA then use the address to determine the location. However there are some cases when there is no address, this could be because the transaction is for a piece of land that doesn’t have an address.

In these cases there needs to be an alternative way to provide the location. At the moment the user has to describe the location in words.

This prototype demonstrates how that journey could be improved even if the only other data available was the local authority boundaries.

A user is likely, but not guaranteed, to know the local authority the property or parcel of land is in. By asking them that upfront we can then focus the map on this local authority, making it easier for them to select the location.

![A screen capture showing a user providing a location when they don't know the address. They first choose a local authority and then the map loads focused on the selected local authority. The user can now place a marker on the map.](/property-data-poc/assets/images/prototype-provide-a-location-journey.gif){: .app-screenshot}

### What we learnt

**Different formats and different cuts of data**

Service builders need to be able to get data in forms and formats other than GeoJSON. Getting all the GeoJSON is useful for displaying the boundaries on a map but is less practical for other purposes. For example a service builder might want to list all the local authorities in Wales, to do this they shouldn’t need to get all the GeoJSON and then ignore the majority of it.

Rather than fetching the complete dataset - local authority boundaries - a service builder might want to take cuts of the data - in this case a single local authority boundary

**Geospatial data changes over time**

These maps are a visual representation of the data at single period in, however the data can change, boundaries can be redefined. We need to think about this when building the platform and services. Service builders will need to access the data for the time period they care about. And the services should keep the users informed about the relevant time period being shown.

### Issues to resolve

The service still expects users to know the geography of local authority area.