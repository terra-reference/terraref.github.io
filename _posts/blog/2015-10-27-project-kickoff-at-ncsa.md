---
layout: post
title: "Project Kickoff at NCSA"
modified:
categories: blog
excerpt:
tags: []
image:
  feature: bw_panorama.png
  credit: "Blue Waters, National Petascale Computing Facility"
  creditlink: "http://bluewaters.ncsa.illinois.edu/"
date: 2015-10-27T22:26:16-06:00
---

* Table of Contents
{:toc}

## Attendees

Gabrielle Allen, Maxwell Burnette, Doug Fein, Chris Harbourt, Rob Kooper, Daniel Lapine, David LeBauer, Stephen Long, Yan Liu, Paul Miller, David Raila, Jay Roloff, Aiman Soliman, Rachel Shekar, Edward Seidel, John Towns, Kandace Turner

## Agenda 

* 9:00-9:05 Welcome and introductions
* 9:05-9:20 David LeBauer: Introduction to the TERRAref program
* 9:20 - 9:50 Introductions to Collaborating NCSA Teams
  * Yan Liu: CyberGIS Center for Advanced Digital and Spatial Studies 
  * Ed Seidel: National Data Service (NDS)
  * Rob Kooper: Innovative Software and Data Analysis (ISDA)
* 9:50-10:05 Break
* 10:05-10:25 Open forum
* 10:25-10:55 Structured discussion
* 10:55-11:00 Summary and Closing

## Presentations

### David LeBauer, Project motivation and overview

<iframe src="https://docs.google.com/presentation/d/1N1ze3E1FLWqJrx-zfGGj2L01mqUWnW19mxXsd00ppy0/embed?start=false&loop=false&delayms=3000" frameborder="0" width="640" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
### Rob Kooper: ISDA, BrownDog, and Clowder

<iframe src="https://docs.google.com/presentation/d/1I4PYYJcFaO5NmI3a1c_a8sb9yCKrW84fYsggS2Ovzh4/embed?start=false&loop=false&delayms=3000" frameborder="0" width="640" height="509" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

### Yan Liu: CyberGIS

<iframe src="https://docs.google.com/presentation/d/1LYdQV3lvjo_DGm7VFBIV2gyTWGP2t8AIJwq8CNnfBco/embed?start=false&loop=false&delayms=3000" frameborder="0" width="640" height="509" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

### Ed Siedel: NDS, Midwest Big Data Hub

Ed Siedel described the [Midwest Big Data Hub](http://midwestbigdatahub.org), a project that was recently funded by NSF to coordinate Academic, Government, and Industry users and creators of Big Data. 
The Midwest Hub has many foci, one of which is 'Digitatl Agriculture'. 

Ed also described The National Data Service and the opportunity for the TERRA Ref project to serve as one of the initial projects featured in the NDS Labs. 

<!--<enter presentation here>-->

## Discussion Topics

### Data Access and Intellectual Property

Paul Miller from [Agrible](http://agrible.com/) expressed interest in using the reference data as well as the computing pipeline. 
Contributing to open source development of the cyberinfrastructure is an option. They are a user focused company aimed at helping farmers optimize their agronomic practices.

* Q: Are there any constraints on the use of data?
* A: The reference dataset and algorithms developed by TERRA Ref will be open-access, but the computing pipeline will be built to protect intellectual property of end users. 
* The platform will be designed for easy deployment on any OpenStack server, and components will function independently as well as within the overall pipeline.
* TERRAref will need to set up different levels of open access, but host all data/algorithms. Agrible needs to know the constraints on the data

### Data Volume

The funding agency ARPA-E has revised the system specifications, meaning that total data volume will be 10x larger than originally estimated: 10 PB instead of the 1 PB for which we have budgeted. There was a discussion about options for storing and managing this increased requirement.

The central resources used by the TERRA Ref team at NCSA will be ROGER, campus cluster, openstack NEBULA, and ADS. XSEDE and Blue Waters allocations may also be available.

* XSEDE allocations must be renewed annually; this is because it is not possible to predict future space and computing needs.
* TERRAref should ensure that software is capable of handling large data volumes.  This can be tested using synthetic data.

## Follow up

1. Apply for Blue Waters storage space. 
2. Address open questions:
 * What type of data access will we need to provide (when, how often, to whom)?  
 * Will the data be stored long term or will it be active data?
 * What are the computing requirements? Will they require specific archtectures or resources available through XSEDE or Blue Waters?
 * What data products will be kept in the long term? Raw or just products?  * What will the annual access patterns be?
 * What is the time and space dimension of data that algorithms will use?  
 * Will historical data only be accessible at limited times?
 * Will there be distributed data management?
 * What will happen with queries that are too large? How will we adapt to changing needs of end users?
3. Collaborate with Digital Agriculture Spoke of Midwest Big Data Hub

<div class="actions">
  <a href="{{site.github.repository_url}}/edit/master/{{ page.path }}">Edit this page</a>
</div>
