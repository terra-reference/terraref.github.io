---
layout: post
title: "August 2016 Algorithms Standards Committee Meeting Notes"
modified: 
categories: blog
excerpt: "Use of Clowder to Automate and Develop; Reproducibilty"
tags: [standards, reference data, algorithms, clowder]
image:
  feature:
date: 2016-08-03T20:43:38-05:00
---


* Table of Contents                                                                                 
{:toc}

**August 2016 Algorithms Standards Committee Meeting Notes**

## **Participants**

David LeBauer, Max Burnette ( [mburnet2@illinois.edu](mailto:mburnet2@illinois.edu), Cheryl Porter, Barnabas Poczos. Justin McGrath, Robert Pless

## **Agenda**

### **Infrastructure Overview**

 ![](https://github.com/terraref/terraref.github.io/blob/master/images/Pipeline%20July%202016.png)
 
### **Using Clowder: Developing Extractors**

- Development instance: [https://terraref.ncsa.illinois.edu/clowder-dev/](https://terraref.ncsa.illinois.edu/clowder-dev/)
- [https://terraref.ncsa.illinois.edu/clowder/](https://terraref.ncsa.illinois.edu/clowder-dev/)

- Slides and video for installation/deployment: [https://opensource.ncsa.illinois.edu/confluence/display/CATS/Documents](https://opensource.ncsa.illinois.edu/confluence/display/CATS/Documents)

- Demonstrate tool launcher

- General discussion of workflow opportunities

### **Computing Resources at NCSA       **

ROGER: https://wiki.ncsa.illinois.edu/display/ROGER/ROGER+User+Guide

XSEDE: [https://www.xsede.org/](https://www.xsede.org/)

### **Suggestions**

 Robert Pless suggested we re-visit the degrees to which we will support reproducibility.

Associating data with software versions

Standard process for updating software versions and re-running code

Provide ability for end-users to test out different algorithms

- g. provide a list that users can choose from
- access algorithms via git repositories
- configure new docker tools;


_Update_: David followed up with Bertram Ludaescher, who replied

> I'd like to understand more about the user stories and requirements that come from TERRA ref - What kind of reproducibility (and provenance?) capabilities do you need to help your users?  Then we could figure which of the technologies we're working with or developing would be most relevant.
(e.g., the Whole Tale project might also be an opportunity for collaboration, but first we need to understand your requirements better).

We are now collecting use cases to present at a meeting Wednesday Aug 26: https://github.com/terraref/computing-pipeline/issues/149

And some links he passed on:

* Whole Tale project. http://wholetale.org/
* Dagstuhl report: http://drops.dagstuhl.de/opus/volltexte/2016/5817/
* Quick-start to YW:
https://github.com/yesworkflow-org/yw-prototypes