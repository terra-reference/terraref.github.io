---
layout: post
title: Feb 2016 Trait Data Meeting Notes
modified:
categories: blog
excerpt:
tags: []
image:
  feature:
date: 2016-02-18T19:48:45-06:00
---

* Table of Contents
{:toc}

## Participants

Max Burnette, Darwin Campbell, Noah Fahlgren, David LeBauer, David Lee, Cheryl Porter, Geoff Morris, Jeffrey White, Jack Gardiner

## Agenda

The goal of this meeting was to learn about and learn from other efforts to standardize agricultural data.

First, Cheryl Porter described her work with AgMIP to harmonize Agricultural databases. Then, Darwin Campbell described the multi-site genomes2fields Maize breeding consortium.

### ICASA / NARDN

Cheryl Porter presented information about ICASA, NARDN, USDA efforts at database harmonization. Much of this work is motivated by the [Agricultural Model Intercomparison Project](http://www.agmip.org/). They are working with modeling teams around the world to build a harmonized data structures. the use of ICASA standards within AgMIP and the development of a suite of translators for translating heterogeneous data into a harmonized data format - a json structure for crop model inputs. json has key value pairs with each key being an ICASA variable, as laid out in the ICASA data dictionary. The ICASA data dictionary forms the backbone of AgMIP data interoperability system, and the [core experimental meta-data for ICASA / NARDN (draft)](https://github.com/terraref/reference-data/files/15501/Core.Harmonized.Crop.Experiment.Data_JWW_chp.docx). Data translation tools allow AgMIP to bring data in from various sources, mostly from spreadsheet templates into a harmonized format, and from the harmonized format into crop model inputs.

In fall of 2015, Cheryl, Jeff, Jim Jones, and colleagues were invited to submit a proposal to USDA that would support scaling up of USDA, NAL, NIFA, using the AgMIP format as standard for translating across databases; if funded, this major new effort would begin start in fall 2016. They have also been working with CGIAR centers on ontologies that will connect different types of data from breeding programs and other agronomic research. They are working to link ICASA with crop ontology. Also working with [GODAN](http://www.godan.info/).

One current focus of extending ICASA is to move from daily to subdaily time step. This will be required for  measurements of gas exchange, timing of irrigation. Also, ICASA is moving more toward focus on the data dictionary while reducing the formats (spreadsheets, json, relational and noSQL databases). 

* [Further Discussion in Github issue 18: Agronomic data / meta-data Formats](https://github.com/terraref/reference-data/issues/18)

### Genomes2Fields 

Darwin Campbell (Iowa State) gave an overview of the [genomes2fields](http://www.genomes2fields.org/) project. G2F is a multi-institutional effort to study gene by environment interactions in Corn. There are twenty-five locations across North America participating, using common methods to study corn traits. They plant the same genotypes at many sites and collect a set of fourteen traits and eleven meterological variables. 

To support this work, they use iPlant for collaboration and data management, Google Spreadsheets with templates and instructions for collecting data, and are using [BMS](https://www.integratedbreeding.net/) and [GOBII](http://www.gobiiproject.org/). Effort is under way to link field data into BMS.

Key recommendations:

* g2f uses iPlant (now CyVerse) for sharing data and information via the wiki, for running BMS virtual machines on their Atmosphere platform, and they are working with iPlant to develop an image analysis pipeline using Bisque. iPlant provides lots (many TB) of storage to the group and the iPlant team has been very helpful.
* Protocols are comprehensively documented and shared among researchers.
* They learned a lot in 2014 and improved the protocols for 2015; we should learn from them, and are free to adopt and adapt their documentation and protocols.

### Presentation ([YouTube](https://youtu.be/HvrkxXuAMIk))

<iframe width="480" height="360" src="https://www.youtube.com/embed/HvrkxXuAMIk?rel=0" frameborder="0" allowfullscreen></iframe>

[Slides](https://goo.gl/f8aMXk)

<div class="actions">
  <a href="{{site.github.repository_url}}/edit/master/{{ page.path }}">Edit this page</a>
</div>
