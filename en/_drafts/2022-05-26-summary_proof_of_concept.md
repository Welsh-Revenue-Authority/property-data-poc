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
  
  
![A reminder that the prototypes use synthetic data](/property-data-poc/assets/images/synthetic-data.png)

We set ourselves 4 objectives to meet within 12 weeks, which we’ll step through with examples of work we’ve done and things we’ve learned.

![Slide with text: 1) Bring the opportunities and challenges to life 2) Give Ministers potential policy options 3) Demonstrate new ways of working 4) Clear about the scale of ambition and where to start](/property-data-poc/assets/images/poc-objectives.png)
  
## 1. Bringing the opportunities and challenges to life
We built a [platform prototype](https://land-property-platform.herokuapp.com/) using synthetic data. It's working code, but a small-scale model of the real thing.  It’s helped us think about how [a data platform for land and property](https://land-property-platform.herokuapp.com/) might work in reality.

![A gif clicking through the features of the platform website. The features are explained in the text below this image.](/property-data-poc/assets/images/platform-prototype.gif)
  
We know that good platforms do a few simple things well. Through research, we learned that making these clear to any potential users is vital.

For example, we listed its [features](https://land-property-platform.herokuapp.com/features) and tried to explain how they help users solve their problems:
- Verify whether a property is in Wales.  Less straightforward than it sounds.
- Provide tax rates for an imagined local Land Transaction Tax
- And look up any property in Wales based on a Unique Property Reference Number (UPRN)

We know that potential users will want to have a poke around and play before they [get started](https://land-property-platform.herokuapp.com/features) so we’ve added [documentation](https://welsh-revenue-authority.github.io/property_platform_app/) and a way to [explore APIs](https://land-property-platform.herokuapp.com/docs). 
  
To test the platform, we built a really simple service on top of it called [Is It In Wales?](http://www.isitin.wales) You’ve guessed it: it tells you whether a property is In, Not In or Partially in Wales.

![A gif showing UPRN’s being entered into the Is It In Wales website and getting different answers.](/property-data-poc/assets/images/isitin.wales.gif)

It sounds so simple, but actually due the ambiguity and complexity of different datasets that currently exist, there’s not always a simple answer to this question.  The platform makes answering it trivial.

### Using a platform to surface information at different stages throughout the buying process

Platforms enable multiple services, so we wanted to think through how information might be surfaced at different stages of someone buying a property.

One scenario we explored was how property search engines, like Rightmove, might present geographically varied taxes. How would that look and feel to a home buyer? Could we explain localised land and property taxes in ways that people understand?

![A mockup of a page on the Rightmove website showing links to potential taxes for a property that is for sale. It’s shown on an iphone on a wooden table.](/property-data-poc/assets/images/rightmove-prototype.png)

How would it feel when people were switching mode from searching for a house to actually buying it? This is a mocked up a tax calculator to illustrate how that might work.

![A mockup of a results page of a Welsh Government branded tax calculator showing which ‘tax zone’ a property is in.](/property-data-poc/assets/images/Local-LTT-calculator.gif)

Finally, we wanted to explore the idea of creating a digital proof of transaction. A land and property platform might be the first place that a transfer of ownership is recorded. Could that become a jumping off point for future joined-up services? 

![ALT: A paper mockup of a Land Transaction Tax certificate in English and Welsh. It includes a signed QR code and a one-time code that can be used as part of a ‘tell us once’ service for moving home.](/property-data-poc/assets/images/digital-proof.gif)

### Property-per-page
Imagine being able to type in a postcode on [GOV.WALES](https://gov.wales) and being able to see information about that property and its locale - a bit like Google search does for maps.  It could form the launchpad to national and local services as well as lots of other useful information.  

A property data platform would make this simple to deliver and low cost to maintain.

![An animated gif of a postcode being entered into the search box on wales.gov. The user is shown a list of addresses, then clicks through to see information about that property, including it;s energy rating and bin collection day.](/property-data-poc/assets/images/page-per-property.gif)

All these examples are speculative prototypes. They aim to show the range of services that could be supported by a platform and some of the opportunities it might open up.

## 2. Giving Ministers potential policy options

There’s been a lot of discussions within the Welsh government about [what devolved taxes look like in the future](https://research.senedd.wales/research-articles/taxing-times-in-the-sixth-senedd/).  One of our objectives was to explore the potential policy options that a land and property platform might make possible and how it might support the [devolved tax framework](https://gov.wales/tax-policy-framework-html) that underpins it.

A common platform for land and property data in Wales means that new types of services and previously impossible (or at least difficult) policy options can be made a reality.

### New paradigms for the design of services

Taking service design first, the archetypal government digital service generally looks something like this:

![A simplified wireframe of a 7 step, generic government web form, including the option to review answers entered and a reference number on the last page.](/property-data-poc/assets/images/transactional-services.png)

Typically you might enter some data on a web form, submit it and then wait for something to happen. In the meantime you might get an email confirmation and you’ll be able to check progress. In this scenario people are expected to enter information that they might have already told the government about; plus they have to wait for something to happen.  

Platforms offer the potential to offer more real-time services that reduce this administrative burden and save time.  Maybe like this, where information that is already held can (with appropriate oversight and permission) be reused:

![A simplified wireframe of a 3 step, future government web form where data already held by the government is played back to a user and they are given a QR code as a digital proof.](/property-data-poc/assets/images/realtime-services.png)

Bringing together information from across government into a single service:

![A simplified wireframe of a start page of a government service called. The title of the page is: Sign in to manage your household account.](/property-data-poc/assets/images/household-account.png)

or helping people to interact with the Welsh Government and local authorities at the same time:

![A simplified wireframe of a web page from a government service with the title::Please review the data we hold about you. It has two lines pointing to ‘local government’ and ‘Welsh government’](/property-data-poc/assets/images/joined-up-services.png)

One of the areas we’ve discussed during the proof of concept is the potential to support a Tourism Levy where accommodation businesses in Wales register themselves to collect a tourist levy. This could be supported by a land and property platform that draws together information from different bits of government, or supports private sector organisations (e.g. Airbnb) with the appropriate permissions to safely use some of this data too.

![A simplified wireframe of a government service called ‘Registered tourism accommodation account’. It includes a checklist of information a user has provided already, and a single item outstanding. ON the right of the screen, there are options to report changes, update contact preferences, view and pay the amount of visitor levey, and link the account to AirBnB.](/property-data-poc/assets/images/tourism-account.png)

Or imagine how having a shared, common identifier for tourism business to surface the impact of policies. Here is an entirely speculative mock-up of a door sticker that would allow people to scan a QR-code to see how the Tourism Levy is being spent in the local area.

![A mockup of a bilingual government branded sticker in the window of a green door.](/property-data-poc/assets/images/door-sticker.png)

These examples are not attempting to provide the answer - that comes from incremental delivery and research. Hopefully they do point to some of the things that might become simpler with a common platform.

### New policy tools

The land and property platform could enable new ways of designing and testing policy.  We experimented with a tool called [Jupyter Notebook](https://jupyter.org/) to explore how we might implement ‘policy as code’.

![An animated gif of Jupyer Notebook showing a localised tax calculator and maps of Wales.](/property-data-poc/assets/images/Jupyter-notebook.gif)


The idea of codifying policy as a combination of text and code means that it is understandable by humans and computers.  It has the potential to allow policymakers to test the impact of their policy design.

During the proof of concept we use it to test the ideas of ‘Local Land Transaction Tax’ by [working up a number of examples](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/2022-01-31) and [modelling fictional geographical boundaries](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/2022-02-07).

### New policy levers

What kind of policy levers would a digital-first approach enable?  We’ve described these as ‘policy patterns’ - a list of types of policy options a platform could make possible.  We’ve been using these to help us develop some shared language between policy and digital specialists.

![Picograms and text showing different policy patterns, which are explained in the text below.](/property-data-poc/assets/images/patterns.gif)

For example, a property and land data platform could enable:

- **Tax zones** are based on any area you could draw on a map: postcode, Local Authority, a National park, 10 miles from the sea.

- **Market context**: link tax rates to other data sets like the prevalence of second homes.  That would be very hard to do in an analogue system.

- **Taper rate** would give policymakers great levels of control over the variance of tax to them fairer

- **Physical attributes** of land and property, like solar panels, could be added to the platform and used as a basis for taxation.  Over time, more data that is added to the platform will open up more policy options

## 3. Showing new ways of working

We set ourselves the objective of demonstrating new ways of working.  For the 12-weeks of the proof of concept the team worked in weekly (‘agile’) sprints and committed themselves to working in the open to share progress as we went.

### Working in the open

![An animated gif of a scrolling web page showing our team’s week notes and project website.](/property-data-poc/assets/images/team-website.gif)

Early on we created a [team website](https://welsh-revenue-authority.github.io/property-data-poc/en/) which we used to share progress through [weeknotes](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/) and thinking-out-loud blog posts.  These were an effective way of explaining what we’re doing to people outside of our team and organisation.  We believe they’ve improved how we communicate and collaborate and see loads of [benefits of working in the open](https://welsh-revenue-authority.github.io/property-data-poc/en/2022/04/05/what-we-learned-working-open.html).

### Github is our documentation
We’ve used Github as our documentation.  For example, what we learned about the [Welsh land and property data landscape](https://github.com/welsh-revenue-authority/data-landscape/blob/main/index.md) is available for everyone to see and amend.  It’s built on other people’s great work that they’ve shared in the open.

![A page from GitHUb with the title: Land and Property platform user research](/property-data-poc/assets/images/research-library.png)

### Show & Tells
We’ve used Show & Tells to people inside and outside of the WRA interested in the project up to date.  They form an important part of our governance. 

![A slide showing a circular diagram of our weekly rhythm, with planning on Tuesday stand-ups on Wednesday, Thursday and Friday, and show and tell on Mondays.](/property-data-poc/assets/images/show-tell.png)

For 30 minutes every Monday, the team demonstrates progress (work done, things learned) to attendees.  It gives stakeholders, collaborators, and experts in the field a chance to ask questions and challenge the team.  

The forum provides independent scrutiny and hopefully builds confidence and trust in the team. It lets sponsors assess whether the team is delivering value.  

Show & Tells help ensure the team is delivering the right thing in the right way by turning governance into ongoing engagement. 

### Incremental delivery approach
Each week the team needs to balance the trade-offs between learning, meeting the needs of users, delivering policy intent and building organisational capability.  By delivering in small increments the team aims to deliver something of [potential value](https://richardpope.org/blog/2022/03/16/UPC-measure-value-digital-service-work/) each week.

![A 3 axes graph with the labels ‘user needs’, ‘capacity to operate’ and ‘policy intent’. A link shows all of them increasing over time. To the right the title is “balancing needs, policy intent and capability building”.](/property-data-poc/assets/images/upc.png)

## 4. The scale of ambition and where to start
The final aim of the proof of concept was to be clearer about the scale of ambition and where to start. Based on what we learned, this is our proposed, high-level approach to how we grow capability:

![A roadmap with sections for now (learning to operate a simple platform), 3-6  months (adding our first service) and 9-12 months (growing the number of external users).](/property-data-poc/assets/images/roadmap.png)


![A roadmap showing a single ‘platform and services team’ splitting into a platform team and a service team. Then, after 9 months, possible splitting again.](/property-data-poc/assets/images/team.png)

The timings are speculative but illustrate that this is just the start of something.

### Start small, aim big

The ambition for the land and property platform is not about a single policy or initiative.  It’s for the long term.  It’s for Wales. A land and property data platform could mean better policy outcomes and a different approach to how public services can be designed.

![A slide with an image showing example services, example rules and example data, such as property extents. It has the text: Joined-up, real-time services. Central, local, public and private. Code as rules enabling digital approaches to policy Data maintained collaboratively, operated as infrastructure, for the long-term and for all of Wales.](/property-data-poc/assets/images/ambiton.png)

If you have questions or want to hear more about this work then feel free to [get in touch](mailto:dataproject@wra.gov.wales)





