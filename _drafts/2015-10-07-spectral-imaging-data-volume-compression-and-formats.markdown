---
layout: post
title: "Spectral Imaging Data Volume, Compression, and Formats"
modified: null
categories: null
excerpt: null
tags: []
image: 
  feature: null
date: {}
published: true
---



* Notes on existing standards and formats: https://github.com/terraref/documentation/blob/master/existing_data_standards.md#sensor-data
* Example data products from other programs (NASA, NEON, etc): https://uofi.app.box.com/files/0/f/4299753901
* proposed format for hyperspectral data: https://github.com/terraref/reference-data/issues/14
* proposed meta-data content for Lemnatec system: https://github.com/terraref/reference-data/issues/2

### Sensor Data Sheets:

<iframe  src="https://app.box.com/embed_widget/s/r5udfu1z7kpf07ryzvdorla3l5g9dto3?view=list&sort=name&direction=ASC&theme=gray" width="800" height="550" frameborder="0" allowfullscreen webkitallowfullscreen msallowfullscreen></iframe>

### Compression ...


```sh
# Download sample Hyperspectral data from NEON
# http://neondataskills.org/HDF5/Plot-Hyperspectral-Pixel-Spectral-Profile-In-R/

curl -O http://neonhighered.org/Data/HDF5/SJER_140123_chip.h5

## Commands tested:

## uncompress
time ncks -O SJER_140123_chip.h5 uncompressed.h5
## two types of compression
time ncks -O -L 1 uncompressed.h5 compressedL1.h5
time ncks -O --ppc default=3 uncompressed.h5 compressed_ppc3.h5

\ls -ltr *.h5

time ncdump -v Reflectance uncompressed.h5 > foo
time ncdump -v Reflectance compressedL1.h5 > foo
time ncdump -v Reflectance compressed_ppc3.h5 > foo

