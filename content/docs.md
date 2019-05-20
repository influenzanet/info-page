---
title: "Influenzanet 2.0 - Docs"
date: 2019-03-26T12:07:55+01:00
draft: false
---

# Documentation

This documentation page, aims to give an overview over the technical concepts of the new Influenzanet system and is continously been updated. More details about the system's requirements and architecture can be found here:
<ul>
	<li><a href="/InfluenzaNet2.0-Requirements-v1.5.pdf" target="_blank">InfluenzaNet 2.0: Requirements Collection</a></li>
	<li><a href="/InfluenzaNet2.0-Architecture-v1.3.pdf" target="_blank">InfluenzaNet 2.0: Architecture Draft</a></li>
</ul>

## System Overview
To create a sustainable and flexible system and being able to handle all future challenges, we defined the main components to be mostly technologically independent from each other.
These main components are: the clients, the public API, the cloud services and the databases for the different instances. Of course, all data storage and transport is fully state-of-the-art encrypted.

<img src="/images/high-level-overview.jpg" alt="overview" width="100%">

### Clients

Influenzanet will come with a default client application, but also allows member institutions to have their own applications for specific user groups.
Client applications can be developed as a web application, native mobile apps or any thinkable future platform which supports standard HTTP communication.

### Public API
This flexibility is achieved by a well defined interface to the cloud services based on standard communication protocols. Currently, we support a *REST-like* HTTP interface but it is already planned to add gRPC support for more advanced features. More details will be available soon.

### Cloud Services - Backend

On the backend side, we designed a micro service architecture based system for better scalability and a more flexible development process.
We are leveraging state of the art design concepts, programming languages and communication standards to create a performant and well maintainable service.
The backend will be offered as Software as a Service (Saas) but can also be downloaded as a self-hosted version. More  information about this will be detailed here soon.

### Databases

**Instances**
A single backend installation - which is not storing any data - supports the connection of multiple database instances, for example to store data of different regions separately.
This is useful to fulfil the requirements of different legislations and privacy policies the different InfluenzaNet members are bound to, and at the same time reducing overall operational costs.
Each instance consists of their own seperate user, survey and content data base.

**User DB**
Only personalized user related data (e.g. email address, system preferences, etc.) are stored in this database.

**Survey DB**
This data base holds only research study related information provided by the participants (e.g. survey answers, sensor data, etc.) or third party sources (e.g. weather data). All data points here are anonymized and once a user is deleted from the *User DB*, the entries cannot linked to a person any more.

**Content DB**
High level analytics and other content that was generated specifically for an *Instance* can be stored and accessed in the content DB.
