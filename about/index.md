---
layout: page
title: Project Overview
excerpt: ""
search_omit: true
image:
  feature: mac_sorghum_20150911.jpg
  credit: Pedro Andrade, Maricopa Agricultural Center
  creditlink: http://cals-mac.arizona.edu/
---

* Table of Contents
{:toc}

# Background and Objectives

We are building a suite of data products and computing tools to support remote observation of plants.

  Our goal is to transform plant breeding by advancing the science of phenotyping. Phenotypes are measurable features that indicate how they will grow and respond to stresses such as heat, drought, and pathogens.
  Breeding is currently limited by the speed at which phenotypes can be measured, and the information that can be extracted from these measurements.
  Currently, measurements used to predict yield include measuring leaf thickness with a caliper or height with a meter stick.
  More sophisticated instruments used to quantify plant architecture, carbon uptake, water use, and root growth do not scale to the thousands or tens of thousands of individual plants that need to be evaluated in a breeding program.

# Data Storage and Computing Pipeline

We will develop a data storage and computing system that provides researchers with access to all of the 'raw' data and derived plant phenotypes (traits). 
Most of the data volume will come from a [Lemnatec Scanalyzer Field System](http://www.lemnatec.com/products/hardware-solutions/scanalyzer-field/) platform in Arizona, and will be accompanied by data from aerial, ground, and tractor-based field sensors. 
Danforth has an indoor phenotyping system - automated sensing of plants in boxes. At the USDA research station in Maricopa, AZ a Lemnatec field platform will be installed over a field of sorghum and run for four years. This will be complimented by an indoor system for automated sensing of plants in boxes.

# TERRA Reference Phenotyping System For Energy Sorghum Team

| Institution                                         | Personnel             | Role                   |
|-----------------------------------------------------|-----------------------|------------------------|
| Donald Danforth Plant Science Center                | Todd Mockler          | Project Lead           |
|                                                     | Rob Alba              | Project Director       |
|                                                     | Noah Fahlgren         | Phenotyping            |
|                                                     | Erica Fishel          | Technology Transfer    |
| Clemson University                                  | Stephen Kresovich     | Breeding               |
| HudsonAlpha Institute for Biotechnology             | Jeremy Schmutz        | Sequencing             |
| Kansas State University                             | Jesse Poland          | Phenotyping            |
|                                                     | Geoff Morris          | Gene-Trait Association |
| Texas A&M University                                | William Rooney        | Breeding               |
| University of Arizona, Maricopa Agricultural Center | Pedro Andrade-Sanchez | Agronomy               |
|                                                     | Michael Ottman        | Agronomy               |
| USDA-ARS Arid Land Agriculture Research Center      | Jeff White            | Agronomy               |
| University of Illinois at Urbana-Champaign          | David LeBauer         | Computing              |
| Washington University at St. Louis                  | Robert Pless          | Image Analysis         |
|                                                     | Roman Garnett         | Prediction Algorithms  |


# Computing Pipeline and Informatics Infrastructure Development Team

This project will implement a data processing pipeline that integrates existing tools such as PlantCV, BrownDog, PEcAn, BETYdb, and other software into a flexible, scalable computing pipeline. This will include geospatial infrastructure for efficiently querying and transforming key datasets and tools that enable researchers to access, archive, use, and contribute data products at each step in the pipeline.  


| Role | Name |
|---|---|
| Lead | David LeBauer | 
| Danforth Lead | Noah Fahlgren | 
| Promect Manager | Rachel Shekar |
| Storage Architect | Dan Lapine | 
| Senior Programmer | Rob Kooper |
| CyberGIS Senior Programmer |  Yan Liu | 
| ISDA Research Programmer |  Maxwell Bennett |
| NDS Research Programmer | David Railia|

# Data Standards Committee

The Data Standards Committee will be define the core reference platform data and meta-data products. The data product specification will define the types of data formats, semantics, and interfaces, file formats, and representations of space, time, and genetic identity based on existing standards, commonly used file formats, and user needs.

The objective of this committee is to facilitate research by ensuring that software and data are _interoperable, reusable, extensible, and understandable_. Providing clear definitions of common formats will make it easier to analyze and exchange data and results. 


## Committee Members

| Name | Institution | Email|
|:--|:--|:--|
|**Coordinators** | | | 
| David Lee | ARPA-E | david.lee2_at_hq.doe.gov|
| David LeBauer | UIUC / NCSA | dlebauer_at_illinois.edu|
|**TERRA Project Representatives** | | | 
| Paul Bartlett | Near Earth Autonomy | www.nearearth.aero|
| Jeff White | USDA ALARC | Jeffrey.White_at_ars.usda.gov|
| Melba Crawford | Purdue | melbac_at_purdue.edu|
| Carl Bernacchi | UIUC / USDA | bernacch_at_illinois.edu|
| Matt Colgan | Blue River | matt.c_at_bluerivert.com|
| Christer Janssen | Pacific Northwest National Laboratory | georg.jansson_at_pnnl.gov|
| Barnabas Poczos | Carnegie Mellon | bapoczos_at_cs.cmu.edu|
| Alex Thomasson | Texas A&M University | thomasson_at_tamu.edu|
|**External Advisors** | | | 
| Cheryl Porter| ICASA / AgMIP / USDA |  |
| Shawn Serbin | Brookhaven National Lab | sserbin_at_bnl.gov |
| Shelly Petroy and Christine Laney | NEON | |


# Latest Posts

<ul class="post-list">
{% for post in site.posts limit:10 %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
