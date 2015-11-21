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

  Our goal is to transform plant breeding by advancing the science of phenotyping. Phenotypes are measurable features that indicate how they will grow and respond to stresses such as heat, drought, and pathogens.
  Breeding is currently limited by the speed at which phenotypes can be measured, and the information that can be extracted from these measurements.
  Currently, measurements used to predict yield include measuring leaf thickness with a caliper or height with a meter stick.
  More sophisticated instruments used to quantify plant architecture, carbon uptake, water use, and root growth do not scale to the thousands or tens of thousands of individual plants that need to be evaluated in a breeding program.
  
We will develop an integrated phenotyping system for energy Sorghum that leverages genetics and breeding, automation, remote plant sensing, genomics, and computational analytics. The complete system will include: 1) the reference field phenotyping system (GFE gantry system) provided by ARPA-E; 2) field- and controlled-environment phenotyping of energy Sorghum; 3) computational solutions for phenotype selection and prediction; 4) genetics, genomics and bioinformatics for phenotype-to-genotype trait associations; 5) data processing and computational workflows for integrated phenotyping systems; and 6) phenotyping data and computational pipeline standards developed by a committee selected in collaboration with the TERRA program. 

Phenotyping will focus on traits that drive yield gain and bioenergy potential and will be conducted under field and controlled environmental conditions using a sorghum diversity panel, biparental cross populations, and elite lines and hybrids from structured breeding populations. This reference system will be used to characterize phenotype-to-genotype associations, on a genomic scale, that will enable knowledge-driven breeding and the development of higher-yielding energy cultivars. Although the system will initially be used to improve energy sorghum, it is directly extendable to other crops of economic and energy significance. When combined with marker-assisted breeding and genome-wide selection for sorghum improvement, this system will increase the bioenergy contribution to our total energy supply and reduce greenhouse gas emissions.



## Reference Phenotyping System Team

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


# Computing Pipeline and Informatics Infrastructure Development

As part of this project, a team based at the University of Illinois and the National Center for Supercomputing Applications will develop a data storage and computing system that provides researchers with access to all of the 'raw' data and derived plant phenotypes (traits). 
Most of the data volume will come from a [Lemnatec Scanalyzer Field System](http://www.lemnatec.com/products/hardware-solutions/scanalyzer-field/) platform in Arizona, and will be accompanied by data from aerial, ground, and tractor-based field sensors. 
Danforth has an indoor phenotyping system - automated sensing of plants in boxes. At the USDA research station in Maricopa, AZ a Lemnatec field platform will be installed over a field of sorghum and run for four years. This will be complimented by an indoor system for automated sensing of plants in boxes.

The data processing pipeline that integrates existing tools such as PlantCV, BrownDog, PEcAn, BETYdb, and other software into a flexible, scalable computing pipeline. This will include geospatial infrastructure for efficiently querying and transforming key datasets and tools that enable researchers to access, archive, use, and contribute data products at each step in the pipeline. 

## Computing Pipeline Development Team


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

| Name | Institution | Subcommittee|
|:--|:--|:--|
|**Coordinators** | | | 
| David Lee | ARPA-E | 
| David LeBauer | UIUC / NCSA | 
|**TERRA Project Representatives** | | 
| Paul Bartlett | Near Earth Autonomy | 
| Jeff White | USDA ALARC |
| Melba Crawford | Purdue |
| Michael Gore | Cornell | 
| Matt Colgan | Blue River | 
| Christer Jansson | Pacific Northwest National Laboratory | 
| Barnabas Poczos | Carnegie Mellon | 
| Alex Thomasson | Texas A&M University |
|**External Advisors** | | | 
| Cheryl Porter| ICASA / AgMIP / USDA | 
| Shawn Serbin | Brookhaven National Lab | 
| Shelly Petroy and Christine Laney | NEON |
| Carolyn J. Lawrence-Dill | Iowa State | 
| Eric Lyons | University of Arizona / iPlant |  


# Latest Posts

<ul class="post-list">
{% for post in site.posts limit:10 %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
