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

## NCSA / UIUC Team

This project will provide support for personnel and computing via the following groups at NCSA:

* **ISDA** Will support implementation of a data processing pipeline that integrates modular tools: PlantCV, BrownDog, PEcAn, BETYdb, and other software.
* **CyberGIS** will implement geospatial infrastructure for efficiently querying and transforming key datasets.
* **NDS** The National Data Service will develop tools that researchers can use to access, archive, use, and contribute data products at each step in the pipeline.  

| Role | Name | email|
|---|---|----|
| NCSA Lead | David LeBauer | dlebauer@illinois.edu|
| Danforth Lead | Noah Fahlgren | | 
| Promect Manager | Rachel Shekar | |
| Storage Architect | Dan Lapine | |
| Architect / Senior Programmer | Rob Kooper | |
| Architect / Senior Programmer |  Yan Liu | |
| ISDA Research Programmer |  Maxwell Bennett |
| NDS Research Programmer | David Railia|  |


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