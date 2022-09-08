---
layout: landing
lang: en
ref: index
hidetitle: True
---
The [Welsh Revenue Authority (WRA)](https://gov.wales/welsh-revenue-authority) is responsible for the collection and management of [Land Transaction Tax (LTT)](https://gov.wales/land-transaction-tax-guide) in Wales. 

LTT is changing so that certain areas in Wales will charge an additional rate of tax for Second homes/Holiday Lets. To support this change we need to be able to identify land and property reliably at a more granular level than we do currently. The Land and Property Data Platform (LPDP) project explored how a data platform could meet these needs, but at the same time we’ve taken the opportunity to consider if we could create something that might be the foundation for wider uses, for the benefit of Wales. 

# What do we mean by “data platform”? 
A platform is digital infrastructure that can be used by many organisations. For example, the [Government Digital Service](https://www.gov.uk/government/organisations/government-digital-service) (GDS) delivers digital infrastructure to support all of UK government. Its platforms include [“Notify”](https://www.notifications.service.gov.uk/) and [“Pay”](https://www.payments.service.gov.uk/). 

Notify allows anyone who uses its code to send their own customised, bulk or individual postal letters and SMS to citizens. Pay is code that allows citizens to make payments for government services – whichever service that is, so that each service does not have to create its own payment process code from scratch.   

A “data” platform is shared capability that allows organisations to access a range of datasets allowing them to combine data in new and interesting ways. The [Office for National Statistics](https://www.ons.gov.uk/) have a data platform called the Integrated Data Programme (IDP) which allows analysts to access a wide range of ONS statistics. A land and property data platform for Wales would enable the combining of key location datasets together with mapping functionality so that users can explore location related data on a map. 

# Our work so far 
Earlier in the year we took a broad look at platforms and looked at potential benefits of platforms to services and policies in Wales, a summary of what we did and what we learnt can be found [here](https://welsh-revenue-authority.github.io/property-data-poc/en/2022/05/26/summary_proof_of_concept.html).  

Over the past few months we took a deeper narrow approach and focused on how a Land and Data Platform could help with Regional LTT.  

# We created prototypes to help us learn 
To help us learn we built a variety of different prototypes. We did these for a number of reasons: 

* to help us understand how service builders might use a platform, and what they might need from it 

* to learn about the shape and challenges with using disparate datasets 

* to explore different interaction patterns 

* to stimulate ideas about what might be possible 

We’ve written up our findings for each of the prototypes which you can see on the [“page per prototype”](https://welsh-revenue-authority.github.io/property-data-poc/en/prototypes/). 

# We did research to understand why location is sometimes inaccurate 

**Who we did research with:** 4 x agents and intermediaries 

**What we wanted to understand:** How a property’s location is identified 

## What we discovered: 

1. We discovered that different datasets were used by different people as their canonical source of truth. 

* Agents use the Land Title and what is written there as the definitive description of address whereas WRA use OS places as their canonical source. 

* The problem is that when the agent does a tax return they need to make address match their canonical source and the WRA need it to match theirs – it can’t always match both at the same time! 

* Having an agreed sense of what will form the canonical source of data will be essential to getting consistent and accurate data. 

2. The completion of the LTT return is subject to errors because of manual rekeying  

* The act of completing the return involves the rekeying of information - which is time consuming and error prone and involves a high cognitive load for those doing it as they have to flip between documents (physical and electronic) and in some cases cannot cut and paste the data. The manual work of doing this together with the fact that the person doing it may not "own" the data because they have not worked on the transaction - introduces a higher risk of error. 

## What we don’t know: 
### Canonical source of truth 

* What would be the best way to ensure that UPRN is attached to a location record? 

* Should the LTT return process be used to build a database of UPRN locations attached to Land Registry records that could be used to update Land Registry at some future point in time? 

### LTT return completion  

* How many agents have their own bespoke systems for processing transactions? 

* What level of complexity would be involved to provide an API to avoid the re-keying of agent data for the LTT return? 

We wrote a [blog post](https://welsh-revenue-authority.github.io/property-data-poc/en/2022/08/23/why-are-inaccuracies-creeping-into-addresses-on-the-land-transaction-tax-return.html) that summarised our findings about location data. 

# We did research to understand who might use the platform within WRA 
**Who we did research with:** 7 x WRA (4 x service owners, 3 x data managers) 
**What we wanted to understand:** Who and how are teams in WRA using land and property data? 

## What we discovered: 

 There are many staff doing individual ad hoc searches on openly available data [Land Reg/Companies House] but no systematic way to harness the power of that data in an automated way to verify accuracy of tax data submitted 

* These ad hoc searches are manual and time-consuming but all use common data sources 

2. WRA backend systems are optimised to show for a single tax – single transactions - rather than embedding thinking about the service journey of the user 

* The service journeys of individual users are not part of the current design thinking of the back end systems 

3. We heard from Landfill Disposal Tax that they want to explore how well their policy intent is being delivered by the legislation that has been passed but they struggle to get the data they need to do this. 

* Thinking about how the policy intent of a new policy will be measured and analysed to understand if it is working needs to be built in front the start.  
## What we don’t know: 

### Ad hoc searches 

* We don’t know how many teams across Welsh government need access to the same datasets and are all doing ad hoc searches. 

### Service journeys 

* We haven’t mapped the service journey of the different actors within the Land Transaction Tax return process – which would expose goals, needs and pain points for different people from start to finish. 

### Policy delivery measurement 

* We haven’t discussed what data would need to be captured to know if the policy that underpins the regional land transaction tax was delivering the policy intent 

# We did research to understand who might use the platform outside of WRA 

**Who we did research with:** 4 x Local authorities, 2 x public sector bodies delivering cross Wales services 

**What we wanted to understand:** How are local authorities/other public sector bodies using land and property data? 

## What we discovered:  

1. All the local authorities we spoke to used UPRN as unique identifier for property/land  

* They all used the centre point in the property or land(if no property) as the place to locate the UPRN. If there is a block of flats the UPRN's are stacked on top of each other. 

2. UPRN is commonly used but underlying processes may be different.  

* One participant assigned UPRN immediately even before planning application had been approved. Another only assigned it once planning had been approved.  
* So one authority could have 'Active", "historic" and "underconstruction" statuses applied to UPRN whereas another authority - if the UPRN was applied it was through planning. 

3. Cross Wales mapping requires good data matching  

* Both the emergency service project and an initiative to map fly-tipping sites across Wales required the bringing together of multiple local authority datasets.  

* In both cases there were challenges with the matching of address data. Literally the format of the address; eg. line 1, line 2 etc were not consistent and so it is harder to create alignment and consensus of location. 

## What we don’t know:  

### UPRN processes are different 

* The level of divergence of the processes around UPRN 

### UPRN processes are different 

* To what degree common cross Wales data standards have been defined and how consistently they have been deployed 

* Which cross Wales services exist that might benefit from a land and property data platform 

Our [blog post](https://welsh-revenue-authority.github.io/property-data-poc/en/2022/08/18/how-a-map-can-paint-a-bigger-picture.html) about mapping and location data.  

# How we explored data for the platform 
In the second phase we focused on using real data in the platform, such as consuming the publicly available house price data from land registry, to create the policy tool prototype. 

One key finding from this was that property data isn't consistent across datasets. For example, we have the Unique Property Reference Number (UPRN), Title numbers, local authority reference numbers all used, with no way currently to cross reference these different lists. This causes us not to be able to accurately combine datasets from different sources, which, if possible, could provide real insights for Ministers, the public and private sector and the public. 

The WRA will continue to work with our partner organisations to push for a greater consistency in the sharing of land and property data across organisations, to ensure property location data can be better used at the heart of the decision-making process.  

# The policy challenges we have been working through 
Through good policy you can deliver a tax that takes into account the aim of the tax and the impact it will have on taxpayers, local and national government, future taxes and more. 

Providing an excellent service has been at the forefront of everything that we have done throughout Phase 2, and we have gone in-depth on multiple policy areas to understand the questions we need to answer and the areas we need to focus on.  

Throughout our work completing user research and exploring real data, we have come to identify a number of policy questions that need to be addressed to allow the tax to be administered, and to be administered well. We will share these with our colleagues at Welsh Treasury so that they can take them forward with Local Authorities and produce solutions.  

These are the broad areas we have unanswered questions about: 

* The definition of a second home 

* Defining second homes areas 

* Property location  

* Border properties & apportionment  

A full blog post can be found [here](). 

# The technology we used 
The platform was designed using Open-Source components with Open standards in mind (avoiding licensing costs and vendor locking). For handling map layers and geographical queries, we used GeoServer middleware. Both presentation layer (frontend) and the API custom apps have been written using modern Python frameworks. API documentation is generated automatically (OpenAPI). 

We used serverless Azure components (including Azure database for PostgreSQL and App Services). Continues Integration (GitHub Actions) allows seamless deployments into dedicated WRA’s Azure Subscription (utilising WRA volume discounts with MS). To limit manual admin tasks and automate the infrastructure deployments, Infrastructure as a Code (PowerShell scripts) has been introduced. 

We’ve a more in-depth, technical overview of how we built the platform in [this blog post](/2022/09/07/technical-architecture.html). 

# What next for Regional Land Transaction Tax? 
Regional LTT will be able to benefit from all we have learnt about property data, users, technology and policy decisions. Despite not being able to fully use platform for LTT regional there will be many aspects of the platform work that will be transferred to the LTT Regional service team.  

# Key Lessons Learnt 
## What worked well 

* Working in the open (where possible) 

* Regular show and tells as governance  

* Autonomy to get on with it 

* Continuous planning 

* Starting small and iterating 

* Learning by making (as opposed to starting with a solution upfront) 

* Having LTT regional as a policy area to focus on 

## What could we have improved? 

* Having stable funding in place that would allow longer term planning 

* Engage more broadly to understand user needs of the platform and how it helps policy areas 

* Having a clearer message around the broader benefits of a platform outside of supporting LTT regional 

## Lessons for the next platform team 

* Be assertive about what it takes to run a sustainable platform 

* Ensure long term funding is in place 

* Appropriates skills, resources and knowledge 

* Ensure the platform is seen as a critical part of national infrastructure, rather than attached to a particular policy 
