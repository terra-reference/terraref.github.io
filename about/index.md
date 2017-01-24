---
layout: page
title: Project Overview
excerpt: ""
search_omit: true
---

* Table of Contents
{:toc}

## Background and Objectives

Phenotypes are measurable features that indicate how they will grow and respond to stresses such as heat, drought, and pathogens.
  Breeding is currently limited by the speed at which phenotypes can be measured, and the information that can be extracted from these measurements.
  Currently, measurements used to predict yield include measuring leaf thickness with a caliper or height with a meter stick.
  More sophisticated instruments used to quantify plant architecture, carbon uptake, water use, and root growth do not scale to the thousands or tens of thousands of individual plants that need to be evaluated in a breeding program.
  
TERRA-REF will develop an integrated phenotyping system for energy Sorghum that leverages genetics and breeding, automation, remote plant sensing, genomics, and computational analytics. The complete system will include:

1. automated gantry field phenotyping system (LemnaTec field scanalyzer) provided by ARPA-E;
2. field phenotyping dervided from sensors on unmanned aerial and ground vehicles;
3. automated controlled-environment phenotyping of energy Sorghum;
4. computational solutions for phenotype selection and prediction;
5. genetics, genomics and bioinformatics for phenotype-to-genotype trait associations;
6. data processing and computational workflows for integrated phenotyping systems; and
7. phenotyping data and computational pipeline standards developed by a committee selected in collaboration with the TERRA program. 

## Reference Phenotyping System Team

| Institution                                         | Personnel             | Role                   |
|-----------------------------------------------------|-----------------------|------------------------|
| Donald Danforth Plant Science Center                | Todd Mockler          | Project Lead           |
|                                                     | Nadia Shakoor         | Associate Director     |
|                                                     | Noah Fahlgren         | Phenotyping            |
|                                                     | Erica Fishel          | Technology Transfer    |
|                                                     | Stuart Marshall       | Scanalyzer Operator    |
| Clemson University                                  | Stephen Kresovich     | Breeding               |
| HudsonAlpha Institute for Biotechnology             | Jeremy Schmutz        | Sequencing             |
| Kansas State University                             | Jesse Poland          | Phenotyping            |
|                                                     | Geoff Morris          | Gene-Trait Association |
| Saint Louis University                              | Abuduwasiti Wulamu    | Remote Sensing         | 
| Texas A&M University                                | William Rooney        | Breeding               |
| University of Arizona, Maricopa Agricultural Center | Pedro Andrade-Sanchez | Agronomy               |
|                                                     | Michael Ottman        | Agronomy               |
| USDA-ARS Arid Land Agriculture Research Center      | Jeff White            | Agronomy               |
| University of Illinois at Urbana-Champaign          | David LeBauer         | Computing              |
| Washington University at St. Louis                  | Robert Pless          | Image Analysis         |
|                                                     | Roman Garnett         | Prediction Algorithms  |

Digital traits that drive yield gain and bioenergy potential will be extracted from sensor data collected from sorghum grown under field and controlled environmental conditions. Over 750 lines from a sorghum diversity panel, biparental cross populations, and elite lines and hybrids from structured breeding populations will be evaluated. This reference system will be used to characterize phenotype-to-genotype associations, on a genomic scale, that will enable knowledge-driven breeding and the development of higher-yielding energy cultivars. Although the system will initially be used to improve energy sorghum, it is directly extendable to other crops of economic and energy significance. When combined with marker-assisted breeding and genome-wide selection for sorghum improvement, this system will increase the bioenergy contribution to our total energy supply and reduce greenhouse gas emissions.

## Computing Pipeline and Informatics Infrastructure Development

As part of the TERRA-REF platform, a team based at the University of Illinois and the National Center for Supercomputing Applications are developing a **data storage and computing system** that provides researchers with access to all of the 'raw' data and derived plant phenotypes (traits). Data from sensors at a variety of locations across the US will be transferred to Illinois.  A large volume of data will come from the automated [Lemnatec Scanalyzer Field System](http://www.lemnatec.com/products/hardware-solutions/scanalyzer-field/) in Arizona. In parallel, data will be collected from field plots in Arizona, South Carolina and Kansas using aerial, ground, and tractor-based field sensors. Plants grown indoors at the Donald Danforth Center uses a conveyor belt system to delivery of plants to and from sensors for automated repeated measurements.

We will integrate and develop existing software including as PlantCV, Breeding Management Systems, Clowder, BrownDog, PEcAn, and BETYdb into the data processing pipeline make it flexible and scalable.

The reference data will facilitate data sharing and re-use of data by providing metadata, provenance for derived data sets, and standardized data processing workflows. It will include geospatial infrastructure for efficiently querying and transforming key datasets and tools that enable researchers to access, archive, use, and contribute data products.

## Computing Pipeline Development Team


| Role | Name |
|---|---|
| Lead | David LeBauer | 
| Danforth Lead | Noah Fahlgren | 
| Project Manager | Rachel Shekar |
| Storage Architect | JD Maloney | 
| Senior Programmer | Rob Kooper |
| CyberGIS Senior Programmer |  Yan Liu | 
| ISDA Research Programmer |  Maxwell Bennett |
| Database Programmer | Scott Rohde |
| Image Compression, UCI | Charlie Zender| 


## Data Standard Products Committee

The Data Standards Committee will work together to create clear definitions of data formats, semantics, and interfaces, file formats, and representations of space, time, and genetic identity based on existing standards, commonly used file formats, and user needs to make it easier to analyze and exchange data and results. This essential contribution will facilitate research by ensuring that software and data are _interoperable, reusable, extensible, and understandable_.

Data Products will be published, reviewed, and updated each year of the project, beginning with version 0 to be released in fall 2016 and subsequent versions released annually thereafter. Public review and comment is welcome. 


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
| Shelly Petroy | NEON |
| Carolyn J. Lawrence-Dill | Iowa State | 
| Eric Lyons | University of Arizona / iPlant | 
| Ted Habermann | The HDF Group |

# Resources

For outreach and communication:

* [**Brochures**](https://drive.google.com/open?id=0By_PDCcY5g2JaDJRZFBzd2FaZlU) originally created for 2016 ARPA-E summit.
* **Logos** for the [TERRA REF project](https://drive.google.com/open?id=0By_PDCcY5g2JclZNN2NtaklXcE0) and [partnering institutions](https://drive.google.com/open?id=0By_PDCcY5g2JdTRySHR2NlJEZFE).
* [**Images**](https://drive.google.com/open?id=0By_PDCcY5g2JeE84YXh3eXgtaUU) of crops, sensors, phenotyping platforms, and other activities.

