---
title: Summarising the Proof of Concept
lang: en
ref: proof-of-concept
layout: post
author: Anthony Pritchard, Richard Pope
---
This is a summary of the work we presented at the week 12 showcase for the land and property data platform proof of concept.

![Slide with text: The Welsh Revenue Authority needs to support geographically varied land and property taxes. We’re exploring if a data platform for land and property in Wales could be the foundation for something more.](/property-data-poc/assets/images/poc-mission.png)

It’s an exciting time for devolved taxation in Wales. The Welsh Revenue Authority will likely need to support geographically varied land and property taxes. There’s also work on [Council Tax reform](https://gov.wales/council-tax-reform-planned) and early discussions about a Tourism Levy. 

We wanted to learn how the WRA can support geographically varied taxes and, by taking a platform approach and ‘learning by making’, start to understand whether this could also be the foundation for something for all of Wales.
A reminder that when we talk about ‘platforms’, we mean things that make it simpler and faster to deliver public-facing services and deliver on policy intent. 

![A slide with image of a horizontal platform supporting  multiple services and the text: Reminder: platforms make it faster and simpler to deliver better services and implement policy intent](/property-data-poc/assets/images/platform-model.png)
  
And that our approach was to look at thin slices of functionality and data to help us explore the opportunities and challenges of a land and property data platform to understand how that might look for Wales.


![A slide with similar image to previous slide, but with a single service and ‘rules’ and ‘data’ platforms selected, and the text: Reminder: we took a thin slice](/property-data-poc/assets/images/platform-slice.png)
  
  
![A slide with an image showing example services, example rules and example data, such as property extents. It has the text: to understand how that might look for Wales.](/property-data-poc/assets/images/platform-vision.png)
  
Finally, a reminder that our work is speculative and all the data we used was synthetic. Place names, and locations were [inspired by a Wikipedia entry](https://en.wikipedia.org/wiki/Category:Fictional_populated_places_in_Wales) and sited on military/ex-military land. We also made up two ‘tax zones’ (North East and South West) to illustrate the idea of locally varied taxes. Again these were fictional - we didn’t want to set any hares racing during the proof of concept!
  
  
![](/property-data-poc/assets/images/synthetic-data.png)

We set ourselves 4 objectives to meet within 12 weeks, which we’ll step through with examples of work we’ve done and things we’ve learned.

![Slide with text: 1) Bring the opportunities and challenges to life 2) Give Ministers potential policy options 3) Demonstrate new ways of working 4) Clear about the scale of ambition and where to start](/property-data-poc/assets/images/poc-objectives.png)
  
## 1. Bringing the opportunities and challenges to life
We built a [platform prototype](https://land-property-platform.herokuapp.com/) using synthetic data. It's working code, but a small-scale model of the real thing.  It’s helped us think about how [a data platform for land and property](https://land-property-platform.herokuapp.com/) might work in reality.
(image7)
ALT: A gif clicking through the features of the platform website. The features are explained in the text below this image.
  
We know that good platforms do a few simple things well. Through research, we learned that making these clear to any potential users is vital.

For example, we listed its [features](https://land-property-platform.herokuapp.com/features) and tried to explain how they help users solve their problems:
- Verify whether a property is in Wales.  Less straightforward than it sounds.
- Provide tax rates for an imagined local Land Transaction Tax
- And look up any property in Wales based on a Unique Property Reference Number (UPRN)

We know that potential users will want to have a poke around and play before they [get started](https://land-property-platform.herokuapp.com/features) so we’ve added [documentation](https://welsh-revenue-authority.github.io/property_platform_app/) and a way to [explore APIs](https://land-property-platform.herokuapp.com/docs). 
  
To test the platform, we built a really simple service on top of it called [Is It In Wales?](http://www.isitin.wales) You’ve guessed it: it tells you whether a property is In, Not In or Partially in Wales.
(image8)
ALT: A gif showing UPRN’s being entered into the Is It In Wales website and getting different answers.

It sounds so simple, but actually due the ambiguity and complexity of different datasets that currently exist, there’s not always a simple answer to this question.  The platform makes answering it trivial.
### Using a platform to surface information at different stages throughout the buying process

Platforms enable multiple services, so we wanted to think through how information might be surfaced at different stages of someone buying a property.

One scenario we explored was how property search engines, like Rightmove, might present geographically varied taxes. How would that look and feel to a home buyer? Could we explain localised land and property taxes in ways that people understand?
(image)
  
