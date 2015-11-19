---
layout: post
title: "Project Kickoff at NCSA"
modified:
categories: blog
excerpt:
tags: []
image:
  feature:
date: 2015-10-27T22:26:16-06:00
---



* Table of Contents
{:toc}

## In attendance: 

Gabrielle Allen, Maxwell Burnette, Doug Fein, Rob Kooper, Tim Kuehlhorn, Daniel Lapine, David LeBauer, Stephen Long, Yan Liu Paul Miller, David Raila, Scott Rohde, Jay Roloff, Aiman Soliman, Rachel Shekar, Edward Seidel, John Towns, Kandace Turner

## Introduction to the UI/NCSA TERRA Ref team 

* **Max Burnette** is a research programmer in the Innovative Software and Data Analysis Division at NCSA. Prior to NCSA, he was a computer programmer and lead geographic information systems (GIS) scientist at Ploughman Analytics for 8 years, where he drove in a wide variety of software development and data analysis projects. He received his bachelor's degree in CS from the University of Illinois at Urbana Champaign in 2010. 

* **Rob Kooper** is a Senior Research Programmer for the Innovative Software and Data Analysis Division at NCSA.  Since joining NCSA, Rob has worked on spectral image analyses and on management and retrieval of information from large databases using fuzzy statements. Currently he is working on scalability options using high performance computing (HPC) and cloud computing environments as well as on extraction of information from complex documents, analyses of the extracted information and visualization of large datasets.

* **Dan Lapine** is the head of the Scientific Computing Services Division at NCSA. He received his B.S. in CS from the University of Illinois at Urbana-Champaign in 2001. He was previously the lead for the Technology Evaluation Group as part of XSEDE's Technology Investigation Service, and had served as the lead system administrator for several HPC clusters at NCSA since 2001. He has participated in several efforts for both the TeraGrid and XSEDE projects during his time at NCSA. Prior to that, he had served with the US Air Force for 10 years, working with Mission Simulator operations and software development.

* **David LeBauer**  is a Research Scientist in the Institute for Genomic Biology. He is also a Fellow at the National Center for Supercomputing Applications.  David's background is in ecosystem ecology, and he studies of agricultural and other managed ecosystems. As Research Manager for the Ecosystem Modeling Program with the Energy Biosciences Institute, he developed PEcAn and BETYdb to support the evaluation and optimization of bioenergy crops.

* **Yan Liu**  is a Senior Research Programmer for Geography and Geographic Information Sciences.  His primary interest is the development of high performance and scalable algorithms and software, with a particular interest in high-performance heuristic algorithms. He develops extreme scale geospatial code for Blue Waters and leads the architecture and software development groups in the CyberGIS Center for Advance Digital and Spatial Studies at NCSA

* **David Raila** is a Research Programmer in the National Data Service at NCSA.  He has extensive technical knowledge in advanced computational hardware, software, networking, and development and deployment practices – from chip/ device architectures and systems software through scalable HPC and Cloud systems.

* **Scott Rohde** has led development of the Biofuel Ecophysiological Traits and Yields database (betydb.org) as a Scientific Web Programmer with the Energy Biosciences Institute since 2012. He has also supported the PEcAn ecosystem modeling workflow engine (pecanproject.org) and the BioCro crop simulation model (github.com/biocro).
 
* **Rachel Shekar** is the Project Manager for the TERRA Ref and Plants in Silico projects, and the Assistant Program Manager for the RIPE project. Rachel is also Executive Editor of the international journals Global Change Biology and GCB Bioenergy. She received her BS in Biology from Juniata College and went on to the University of Illinois for her MS in Plant Biology. Rachel has experience in plant ecology and physiology research and research laboratory management.

## Presentations:

### David LeBauer, Project motivation and overview

<iframe src='https://uillinoisedu-my.sharepoint.com/personal/dlebauer_illinois_edu/_layouts/15/WopiFrame.aspx?sourcedoc={61310592-9603-4c97-8620-c68c3e8fa2d2}&action=embedview&wdAr=1.7777777777777777' width='610px' height='367px' frameborder='0'>This is an embedded <a target='_blank' href='http://office.com'>Microsoft Office</a> presentation, powered by <a target='_blank' href='http://office.com/webapps'>Office Online</a>.</iframe>

### Rob Kooper: ISDA, BrownDog, and Clowder

<iframe src='https://uillinoisedu-my.sharepoint.com/personal/dlebauer_illinois_edu/_layouts/15/WopiFrame.aspx?sourcedoc={c089c797-680c-4cc4-9b60-c7a01b9c53c0}&action=embedview&wdAr=1.3333333333333333' width='610px' height='481px' frameborder='0'>This is an embedded <a target='_blank' href='http://office.com'>Microsoft Office</a> presentation, powered by <a target='_blank' href='http://office.com/webapps'>Office Online</a>.</iframe>

### Yan Liu: CyberGIS

<iframe src='https://uillinoisedu-my.sharepoint.com/personal/dlebauer_illinois_edu/_layouts/15/WopiFrame.aspx?sourcedoc={658571ae-037e-4527-af1d-8782d8c36416}&action=embedview&wdAr=1.3333333333333333' width='610px' height='481px' frameborder='0'>This is an embedded <a target='_blank' href='http://office.com'>Microsoft Office</a> presentation, powered by <a target='_blank' href='http://office.com/webapps'>Office Online</a>.</iframe>

### Ed Siedel: NDS, Midwest Big Data Hub

embed presentation iframe here

## Discussion

### Agrible

* What they do: 
  * Remote sensing, image processing, analysis
  * Long term planning (3 yr)
  * Testing systems 
  * Running processes

They have staff for marketing, customer service, user-based. Agrible is willing to work with TERRAref.  They can possibly contribute to the development of software, data products, and application programming interfaces. 


* Q: Are there constraints on data? - Data can be open, algorithms kept closed

TERRAref will need to set up different levels of open access, but host all data/algorithms. Agrible needs to know the constraints on the data


### Storage and Computing resources

Current plan is to use ROGER, campus cluster, openstack NEBULA, ADS, XSEDE.

A key issue is that the predicted data volume has increased from 1 PB accumulating over four years to 10-20PB, mostly from the imaging spectrometers and 3D scanner. It costs many millions of dollars to store so much data even for these few years. So we need to a) identify options other than the original plan for providing 1 PB of storage online (CyberGIS center has offered to provide this capacity on Roger).

For storage, John Towns suggests that TERRAref needs to know:
* What are the data sources?
* What type of access is needed?  
* Does TERRAref need access, storage, both?
* Will the data be stored long term or will it be active data?
* Does TERRAref have other requirements?
* How much data will there be?
* Will “raw” data be kept in the long term or just the products?  
* What will the annual access patterns be?
* Will algorithms run on last 3 months, on historical data, or both?  
* Will historical data only be accessible at limited times?
* Will there be distributed data management?
* What will happen with queries that are too large?  Will they bounce back?

John Towns noted that XSEDE storage is only offered one year at a time; they found that users needed to reapply annually anyhow because it is not possible to predict future space needs 

TERRAref also needs to ensure that its software is capable of handling this volume.  This can be tested using synthetic data.

TERRAref will need to secure two computers just in case of break (unless running on VM, but then the rate will not as fast)

<div class="actions">
  <a href="{{site.github.repository_url}}/edit/master/{{ page.path }}">Edit this page</a>
</div>
