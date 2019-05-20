---
title: "Influenzanet 2.0"
date: 2019-03-26T10:53:01+01:00
draft: false
---

<div style="padding-top:60px;padding-bottom:30px">
	<img src="/images/testlogo.png" alt="Logo (but not final)." width="100%">
</div>

InfluenzaNet 2.0 is the new version of InfluenzaNet currently in development. We redesigned InfluenzaNet to be able to ensure highest ethical, privacy and technical standards for now and the coming years.

InfluenzaNet is an online participatory monitoring system with the purpose of providing valuable information for researchers as well as ordinary citizens and is currently active in over 10 European countries. It brings major benefits to the research and detection of influenza-like-illnesses (ILI). It connects epidemiologists, medical researcher and ordinary citizens, benefiting each group with unique information. This allows better understanding of disease spreading in different countries and hopefully help develop better strategies to fight influenza-like-illnesses (ILI). The combination of InfluenzaNet with traditional monitoring methods provides valuable input for researching influenza and other contagious diseases.

However, InfluenzaNet relies on the active participation of volunteers. In order to get volunteers to participate, it is necessary to provide an  easy-to-use and efficient system, as well as addressing potential privacy concerns of the users. Furthermore, it is necessary to satisfy the diverse needs of the 11 current and additional aspiring member countries.

## History & Propagation

InfluenzaNet was introduced in 2003 and is now represented in eleven countries. It was first launched in the Netherland and Belgium (De Grote Griepmeting, 2003), to be followed by Portugal (Gripenet, 2005), Italy (Influweb, 2008), United Kingdom (Flusurvey, 2009.), Sweden (Hälsorapport, 2011), France (Grippenet, 2012), Spain (Gripenet.es, 2012), Ireland (Flusurvey.ie, 2013), Denmark (Influmeter, 2013) and Switzerland (Grippenet, 2016). The InfluenzaNet consortium was established in 2009, to introduce a uniform system for monitoring influenza-like-illnesses and stimulate collaboration among the different countries. Among the supporters of InfluenzaNet are private individuals, numerous national agencies and foundations, as well as the European Commission. Furthermore, InfluenzaNet inspired and supported similar systems outside of europe.

## Methods

Previously disease monitoring methods rely on the data collected from people seeking medical attention. InfluenzaNet allows participants, who do not necessarily seek medical attention, to provide data. The online self reporting system is available in realtime, which makes the process of detection possible contagion much faster.
It is then used by researchers in the medical and healthcare community to study the spread, the causes and potential ways to avoid influenza-like-illnesses.

InfluenzaNet provides benefits for each participant to help understand their individual risk factors. An important mission of InfluenzaNet is to inform the general public on influenza itself, how to behave in case of a pandemic, as well as aims at predicting the spread of influenza. Participants get insights into the data and its analysis and can even be warned to alter their behavior, in order to prevent the spread of influenza.
In 2018 a first approach with a native app, used to utilise mobile sensor data, to extend the weekly symptom reports with contact information, was made within the swiss Grippenet.

## Why we need a new version

Technological progress, political and cultural changes cause shift in people’s behaviour and expectations towards highly reliable and well maintained systems.
The current system was developed 13 years ago. Maintaining the monolithic and poorly documented code base has become a big burden. It became hard to integrate changes in privacy and ethics regulations.
The new system in developed is an open source solution using state of the art architecture and methods. It will provide benefits to different stakeholders:

**Benefits for User/Participants**
* support for widespread and accessible interfaces and devices eg. mobile phones and tablets
* highest ethical and privacy standards
* regular updates and new features for personalised experience in the future
* the participants will have easier access to results and other interesting information
* participation can be a more fun experience through eg. gamification or options of social features and community aspects

**Benefits for the research community**
* better outreach through modern, widely used clients that are accessible over all age groups (eg. web and mobile user interfaces), which leads to potentially more representative sample and more participants in general
* modular and adaptable data analytics
* easily integrate other (existing or ad hoc generated) systems through well documented and versatile interfaces
* main focus can be put on research rather than the technical limitations and problems
* access to a higher variety of information sources, like sensors and aggregated observations
* novel and interesting research opportunities

**Benefits for Operators**
* open source code - maintainable - community supported - well documented
* available as SaaS (software as a service) or self hosted with easy deployment through state of the art container technologies
* better scalability to ensure a responsive system even at high traffic periods
* modularity allows customization e.g. to specific regulatory needs in some regions

## Parties
The following parties are currently the main active contributors or contractors during the InfluenzaNet 2.0 development:

<div style="margin-bottom:50px">
  {{< parties >}}
</div>

<!--
* <a href="https://www.isi.it/en/home" target="_blank">ISI Foundation</a>, Turin, Italy - *project lead and coordination*
* <a href="https://www.dfki.de/en/web/" target="_blank">DFKI</a> - German Center for Artificial Intelligence, Kaiserslautern, Germany -  *research of technologies for privacy preserving, participatory data collection; master’s, bachelor thesis and student projects around Influenzanet 2.0*
* <a href="https://www.inserm.fr/en" target="_blank">INSERM</a>, Sorbonne Université, Institut Pierre Louis d'Epidemiologie et de Santé Publique Paris, France - *requirements engineering, development of data analytics methods*
* <a href="https://coneno.com" target="_blank">coneno</a>, Germany - *technical infrastructure and software development*
-->

## Roadmap for 2019
<div style="width: 100%; padding: 30px">
<img src="/images/roadmap.png" alt="roadmap" width="100%">
</div>
2019 Q1 - Implementation work on cloud infrastructure, deployment workflows, user management services - setting up frontend development

2019 Q2 - Implementation work on study and survey system on the backend side and frontend (webapp) for participants and instance managers (researcher/admin)

2019 Q3 - Launch of the first test deployment for participants (public beta) - Refinements on user management - Data analytics services - Bug fixes - Prepare for production launch

2019 Q3 end - Launch of the new production system (stable release)

2019 Q4 - Maintaining and monitoring system - Bug fixes - Next round of ideas for upcoming features
