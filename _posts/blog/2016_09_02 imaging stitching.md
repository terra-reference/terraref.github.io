<span id="_pkdjqnxjjej" class="anchor"></span>---

layout: post
title: TERRA Ref image stitching and tools
modified:
categories: blog
excerpt: Image stitching and tools
tags: \[sensor, hyperspectral, calibration, standards committee, image\]
date: 2016-09-02T17:25:14-05:00

---

\* Table of Contents

{:toc}

TERRA Ref image stitching and tools
===================================

Friday, September 2, 2016

11-12 CST

Agenda
------

### Review:

1.  [Create full field ](https://github.com/terraref/computing-pipeline/issues/85)[**stitched**](https://github.com/terraref/computing-pipeline/issues/85)[ mosaic](https://github.com/terraref/computing-pipeline/issues/85)

2.  [Sensor Fusion](https://github.com/terraref/computing-pipeline/issues/121)

### Discuss:

-   **When should this occur and what should we store**? E.g. when someone wants an entire plot?

    -   Stitching images on-the-fly when queried

    -   Maintaining full-field stitched mosaic and subsetting when queried

-   **Low-resolution daily mosaic preview** for visual inspection

    -   Useful for gantry operator

-   Who is doing what aspects of this? What can we have for November?

> **Zender/Jerome - pixel2Geographic.py**

-   Get individual pixel locations based on metadata and hard-coded offsets. We could generalize if the specific parameters are available in other sensor metadata.

-   [*pixel2Geographic.py script*](https://github.com/terraref/computing-pipeline/blob/fc0129ad3f2e984ca803db1e6b048005894e1e30/scripts/hyperspectral/pixel2Geographic.py)

-   [*\#144 Georeferencing hyperspectral data*](https://github.com/terraref/computing-pipeline/issues/144)

-   Pless - mapping of hyperspectral is different than that of other cameras due to axis of movement.

> **Yaping - geospatial extractor**

-   Store field-of-view and location of images from metadata

-   [*geospatial extractor root*](https://github.com/terraref/computing-pipeline/tree/geostreams_extractor/scripts/geospatial)

-   [*\#101 Store location and FOV associated with each file in Clowder*](https://github.com/terraref/computing-pipeline/issues/101)

**Solmaz - Sensor Fusion**

-   Overlay data from hyperspectral, stereo RGB, 3D scanner in plot level.

-   All the data separately needs to be stitched/registered and georeferenced. [*\#121 Sensor Fusion*](https://github.com/terraref/computing-pipeline/issues/121)

-   ![](https://github.com/terraref/terraref.github.io/blob/master/images/fusion%201.jpg) ![](https://github.com/terraref/terraref.github.io/blob/master/images/fusion%202.jpg)

**Pless/Zongyang - created full stitched mosaic using stereo top data**

[*Terra\_full\_stitched\_tiles.py*](https://github.com/terraref/computing-pipeline/tree/demosaic_extractor/scripts/stereoImager)

Examples(from 2016-06-20):

![](https://github.com/terraref/terraref.github.io/blob/master/images/pless%20example.png)

![](https://github.com/terraref/terraref.github.io/blob/master/images/pless%20example%202.png)

**Q) how to trigger the stitching on a big list of files?**

-   Collection is periodically updated and we can re-run when new files are added to it?

-   At the end of the day?

-   New type of file that is a computation-request file (or some other trigger)? Cron-job to trigger this? Provides logging + validation in pipeline

-   ZL script looks at entire field and puts out 1 plot of height from 3-4 swath captures, faster to make all plots at the same time.

-   Have a log file that lists files per day by sensor

-   Incremental stitching?

Look at mosaic extractor piece (related to demosaic) - points to directory in Globus that is a single day from stereo VIS sensor

3D laser scanner data -&gt; per plot/per day height distribs

1.  Generate list at end of day

2.  Send to clowder

3.  Clowder checks as collection accumulates files until they are all represented

4.  Trigger extractor to stitch those files into one and add to collection as new dataset

Solmaz

-   Store registration b/w 3D data and hyperspectral? Storing as 3 different band RGB image - how should we store?

-   This needs stereo+3d image, how do we extract specific plot positions from a bunch of data (especially for RGB)

-   Input: based on plot, F.O.V. is different for different sensors - **requires Yaping's extractor** to match by FoV and time
