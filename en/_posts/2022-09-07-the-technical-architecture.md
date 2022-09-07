---
title: The technical architecture
lang: en
ref: technical-architecture
layout: post
author: Luke Sawicki
---

The platform was designed using Open-Source components with Open standards in mind (avoiding licensing costs and vendor locking). We used serverless Azure components (including Azure database for PostgreSQL and App Services). Continuous integration (GitHub Actions) allows seamless deployments into dedicated WRA’s Azure Subscription (utilising WRA volume discounts with MS). To limit the manual admin tasks and automate the infrastructure deployments, Infrastructure as a Code (PowerShell scripts) has been introduced.

<IMAGE>

The platform consists of several serverless components in a single Azure subscription. 

The core database for the platform is [PostgreSQL 13](https://www.postgresql.org/) – a free and open-source relational database management system (RDBMS) emphasizing extensibility and SQL compliance. It offers [PostGIS](https://postgis.net/) extension that we use to process spatial data. 

To avoid server administration overhead, we use Azure Database Flexible Server for PostgreSQL. It is a fully managed database as a service offering that can handle high workloads with predictable performance and dynamic scalability. 

A single Azure App Service plan (Linux) is used to deploy all applications within the platform. It is a fully managed service with built-in infrastructure maintenance, security patching and scaling. It offers built-in continuous integration and continuous delivery (CI/CD) with zero-downtime deployments. It is a cost-effective solution, as underlying infrastructure is shared. 

To manage and publish map layers we use [GeoServer](https://geoserver.org/), an open-source middleware that allows users to share, process and edit geospatial data. Designed for interoperability, it publishes data from any major spatial data source using open standards. 
GeoServer is deployed in Azure App Service as a pre-configured Docker container (using Azure Container Registry).  

The platform API is a custom-built (FastAPI/Python) application. It offers a REST API with auto generated [OpenAPI documents](https://www.openapis.org/). It also has command line scripts for batch data loading. It runs with Univicorn server and is deployed in Azure App Service plan described above. Source code is publicly available in GitHub. GitHub Actions are used for Continues Deployment. 

Azure “Time Triggered Functions” are used to execute regular/scheduled jobs like regular data imports. 

The storage account is a file store used to keep GeoServer’s configuration files (acts as a permanent storage when Docker Containers are being re-deployed). 

Azure Web Application Firewall (WAF) on Azure Front Door provides centralized protection for web applications. WAF defends web services against common exploits and vulnerabilities. 
WAF on Front Door is centralized solution, deployed on Azure network edge locations. WAF enabled web applications inspect every incoming request delivered by Front Door at the network edge and prevents malicious attacks close to the attack sources before they enter our Platform’s virtual network. 

We implement [Infrastructure as a Code](https://en.wikipedia.org/wiki/Infrastructure_as_code) (IaaS). Both Azure Infrastructure and Docker building scripts are publicly available in GitHub. 

# Platform data flows 

## Loading data 

Data is loaded to the platform both manually and automatically.  

In manual process, for the attribute tables, Analyst would use Import functionality of [pgAdmin](https://www.pgadmin.org/) (a free tool supplied with PostgreSQL). 

Geographical (spatial) data is validated and loaded using [Quantum GIS (QGIS)](https://www.qgis.org/en/site/) - an open-source desktop GIS (geographic information system) application. 
 
We also provide a set of python scripts for batch file processing. 

Automatic process currently covering property transaction data from Land Registry uses python script called by time triggered Azure Function. Script is pulling data from the [Land Registry Open Data API](https://landregistry.data.gov.uk/), using SPARQL queries.

<IMAGE>

## Sharing data 

Platform offers an API, part of which is publicly available. It also offers GeoServer for geographical queries/map layers with WMS/WFS protocols. 

Both API and GeoServer are utilised in [prototypes we built (such as the Policy Explorer)](https://welsh-revenue-authority.github.io/property-data-poc/en/prototypes/), which are hosted in separate Azure subscriptions/other hosting providers. 

To secure the entry point we use Azure Front Door.

<IMAGE>
