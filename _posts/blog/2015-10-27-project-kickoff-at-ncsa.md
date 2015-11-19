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

Terraref OPS kickoff notes
October 27, 2015

## In attendance: 

Gabrielle Allen, Maxwell Burnette, Doug Fein, Chris Harbourt, Rob Kooper, Daniel Lapine, David LeBauer, Stephen Long, Yan Liu Paul Miller, David Raila, Jay Roloff, Aiman Soliman, Rachel Shekar, Edward Seidel, John Towns, Kandace Turner

## Presentations:

### David LeBauer, Project motivation and overview

<iframe src='https://uillinoisedu-my.sharepoint.com/personal/dlebauer_illinois_edu/_layouts/15/WopiFrame.aspx?sourcedoc={61310592-9603-4c97-8620-c68c3e8fa2d2}&action=embedview&wdAr=1.7777777777777777' width='610px' height='367px' frameborder='0'>This is an embedded <a target='_blank' href='http://office.com'>Microsoft Office</a> presentation, powered by <a target='_blank' href='http://office.com/webapps'>Office Online</a>.</iframe>

### Rob Kooper: ISDA, BrownDog, and Clowder

<iframe src='https://uillinoisedu-my.sharepoint.com/personal/dlebauer_illinois_edu/_layouts/15/WopiFrame.aspx?sourcedoc={c089c797-680c-4cc4-9b60-c7a01b9c53c0}&action=embedview&wdAr=1.3333333333333333' width='610px' height='481px' frameborder='0'>This is an embedded <a target='_blank' href='http://office.com'>Microsoft Office</a> presentation, powered by <a target='_blank' href='http://office.com/webapps'>Office Online</a>.</iframe>

### Yan Liu: CyberGIS

embed presentation iframe here

### Ed Siedel: NDS, Midwest Big Data Hub

embed presentation iframe here

## Discussion

### Agrible

What they do: 
Remote sensing, image processing, analysis
Long term planning (3 yr)
Testing systems 
Running processes

They have staff for marketing, customer service, user-based

Agrible is willing to work with TERRAref.  They can possibly contribute software

They asked:
Are there constraints on data? - Data can be open, algorithms kept closed

TERRAref will need to set up different levels of open access, but host all data/algorithms. Agrible needs to know the constraints on the data


### Storage and Computing resources

 on ROGER, campus cluster, openstack NEBULA, ADS, XSEDE

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
