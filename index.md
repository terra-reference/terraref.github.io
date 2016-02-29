---
layout: page
title: "Field crop analytics that will revolutionize plant breeding"
excerpt: ""
search_omit: true
---
#### The Transportation Energy Resources from Renewable Agriculture Phenotyping Reference Platform (TERRA-REF) is a national high-throughput phenotyping platform that aims to revolutionize plant breeding.

#### <i>Our goal is to accelerate breeding and the commercial release of high-yield bioenergy sorghum hybrids.</i>

## Critial elements to TERRA-REF's integrated phenotyping system.

### Field phenotyping field scanner system
This is a live stream of the Lemnatec Field Scanalyzer at the USDA Arid Land Research Station in Maricopa, Arizona.  It is the largest field crop analytics robot in the world. This high-throughput phenotyping field-scanning robot has a 30-ton steel gantry
that autonomously moves along two 200-meter steel rails while continuously imaging the crops growing below it with a diverse array of cameras and sensors.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Pp6IdkPtFC8?rel=0" frameborder="0" allowfullscreen></iframe>


### Automated controlled-environment phenotyping
The Bellwether Foundation Phenotyping Facility is a climate controlled 70 m<sup>2</sup> growth house with a conveyor belt system for moving plants to and from fluorescence, color, and nearinfrared imaging cabinets. This automated, high-throughput platform allows repeated non-destructive time-series image capture and multi-parametric analysis of 1,140 plants in a single experiment.

### Phenotyping sensors on Unmanned Aerial Vehicles
UAVs will repeatedly fly precision passes over crops Phenotyping sensors on Unmanned Aerial Vehicles to provide autonomous image surveys, with onboard sensors georegistering the data and stitching together the captured images based on vehicle positions. The use
of UAVs will provide rapid coverage of areas that are much larger than what can be covered with ground-based systems.

### Phenotyping sensors on piloted ground vehicles
Multiple vehicles outfitted with instruments that measure canopy height, temperature, and spectral reflectance at three
wavelengths will be used to collect plot-level data georeferenced at centimeter accuracy. Plot scale data is relevant for traits
that are strongly influenced by interplant competition and crop geometry such as light interception and canopy temperature.

### Genomic and genetic data and computational platform
We will conduct whole-genome resequencing on a diverse set of 400 sorghum accessions included in the Bioenergy Association Panel to measure the landscape of genetic variation in the selected germplasm and provide whole-genome sequences for association mapping. In addition, we will conduct genotyping by-sequencing on 400 lines from two recombinant inbred line (RIL) populations. The genomic data will then be used to identify the differences between each line and the reference genome sequence for sorghum. We will use bioinformatics and quantitative genetics to characterize the observed genetic variation and identify genomic regions controlling biomass, plant architecture, and photosynthetic traits.

### High performance data storage and computing system
The system will provide public access to raw data, metadata, derived data, provenance for derived data, and standardized 
data processing workflows. This open-source compute platform will be used to provide open access to huge datasets that will
guide breeding decisions, facilitate collaboration, and allow unprecedented data sharing.

### Latest Posts

<ul class="post-list">
{% for post in site.posts limit:10 %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
