<span id="_pkdjqnxjjej" class="anchor"></span>---

layout: post
title: TERRA Ref Standards Committee Meeting: Hyperspectral Sensor Calibration and Applications
modified:
categories: blog
excerpt: Hyperspectral Sensor Calibration and Applications
tags: \[sensor, hyperspectral, calibration, standards committee\]
date: 2016-09-02T17:25:14-05:00

---

\* Table of Contents

{:toc}

TERRA Ref Standards Committee Meeting: Hyperspectral Sensor Calibration and Applications
========================================================================================

Friday, September 2

11-12 CST

Participants
------------

David LeBauer, UIUC
Solmaz, LemnaTec
Nadia Shakoor, DDPSC
Jeff White, USDA
Max Burnette, UIUC
Larry Biehl, Purdue
Craig Willis
Alex Thomasson, TAMU
Javi Ribera, Purdue student
Charlie Zender
Justin McGrath
Andries van der Meer
Dave Guarrera, ARPA-e
Andy French, USDA
Yuhao Chen
Justin Manzo, ARPA-e
Ben Niehaus, LemnaTec
Paul Bartlett

## Agenda
------

### Review:

1.  Lemnatec [*draft protocol for hyperspectral sensor calibration*](https://docs.google.com/document/d/1w_zHHlrPVKsy1mnW9wrVzAU2edVqZH8i1IZa5BZxVpo/edit). This will be a focus of discussion so please review this document in advance of the meeting. This document and supplementary information (sensor specs, factory calibration, calibration object) are in a [*shared folder*](https://drive.google.com/open?id=0By_PDCcY5g2JRWNnZ3E4akRHQTA) on Google Drive.

2.  Sample (uncalibrated) hyperspectral data product [*https://terraref.ncsa.illinois.edu/clowder/spaces/57aa3f60e4b0f7d0a1924a44*](https://terraref.ncsa.illinois.edu/clowder/spaces/57aa3f60e4b0f7d0a1924a44)

3.  References (below)

### Discuss:

Sample data and calibration protocols

Use cases:

-   How do you want to subset?

-   Subsetting

    -   on the fly?

-   How will these data be accessed?

-   Interest in leaf sample archiving or field sampling by other teams?

Larry: spectralon provides known reflectance; may not be brightest in view

Ben: reflectance can be &gt; target,e.g. If leaves are wet

At night, active illumination can be more certain that plants will not reflect &gt; 95%; active reflectance allows to use greater dynamic range of the calendar. See presentation [*https://docs.google.com/presentation/d/10Yl915Af5ZpgQ3G9sUJ97-Zpo-ESJRQ8BP0TVN04plA/edit?usp=sharing*](https://docs.google.com/presentation/d/10Yl915Af5ZpgQ3G9sUJ97-Zpo-ESJRQ8BP0TVN04plA/edit?usp=sharing)

### References:

GitHub Discussions:
-------------------

-   [*Convert exposure to reflectance*](https://github.com/terraref/computing-pipeline/issues/88)

-   [*Calibrating downwelling spectral radiances*](https://github.com/terraref/reference-data/issues/30)

-   [*Georeferencing hyperspectral data*](https://github.com/terraref/computing-pipeline/issues/144)

-   [*Access via THREDDS server?*](https://github.com/terraref/computing-pipeline/issues/155)

Software 
---------

-   Hyperspectral Pipeline scripts: [*scripts/hyperspectral/*](https://github.com/terraref/computing-pipeline/blob/master/scripts/hyperspectral/)

-   Description in [*README.md*](https://github.com/terraref/computing-pipeline/blob/master/scripts/hyperspectral/README.md)

Publications
------------

-   Robinson, B. F., and L. L. Biehl. "Calibration procedures for measurement of reflectance factor in remote sensing field research." 23rd Annual Technical Symposium. International Society for Optics and Photonics, 1979. [*(pdf)*](https://drive.google.com/open?id=0By_PDCcY5g2JODNCNWhlaU1mNHc)

-   Jackson, Ray D., Thomas R. Clarke, and M. Susan Moran. "Bidirectional calibration results for 11 Spectralon and 16 BaSO 4 reference reflectance panels." Remote Sensing of Environment 40.3 (1992): 231-239. ([*pdf*](https://drive.google.com/open?id=0By_PDCcY5g2Jb1doQ3RDTDJfUVU))

-   Singh, A., Serbin, S. P., McNeil, B. E., Kingdon, C. C. and Townsend, P. A. (2015), Imaging spectroscopy algorithms for mapping canopy foliar chemical and morphological traits and their uncertainties. Ecological Applications, 25: 2180–2197. doi:10.1890/14-2098.1 ([*pdf*](https://drive.google.com/open?id=0By_PDCcY5g2JNmctOEFqWVJONTg))
