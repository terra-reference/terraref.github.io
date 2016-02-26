---
layout: page
title: "Welcome"
excerpt: ""
search_omit: true
---

### About the ARPA-E TERRA Program

The TERRA program is facilitating improvement of advanced biofuel crops, specifically energy sorghum, by developing and integrating cutting-edge remote sensing platforms, complex data analytics tools, and high-throughput plant breeding technologies.
Project teams are constructing automated systems to accurately measure and analyze crop growth in the field, thoroughly characterizing genetic potential and creating algorithms for selecting the best plants to reproduce.
These innovations will accelerate domestic production of sustainable, renewable, and affordable liquid transportation fuels.
The program will also generate the world's largest public reference database of sorghum plant characteristics and genetic composition that will facilitate research and development efforts across public and private sector institutions and in other important agricultural crops.

* [ARPA-E TERRA program home page](http://arpa-e.energy.gov/?q=programs/terra)

### The TERRA Reference Platform: A Reference Phenotyping System for Energy Sorghum

> The Donald Danforth Plant Science Center, along with its research partners, will coordinate a national network of test sites in AZ, KS, MO, SC and TX, to provide broad environmental and genetic diversity essential for understanding phenotype behavior.
The team will host a state-of-the-art plant phenotyping system to provide high-resolution evaluation of crops grown under field conditions.
In addition, comprehensive genomic analyses will be conducted to create a high-quality reference dataset of energy sorghum’s physical characteristics and genetic information.
The project will ultimately provide data in community-defined formats that will be made available to researchers in a high-performance computing environment and archived for public use.

- [ARPA-E press release](http://arpa-e.energy.gov/sites/default/files/documents/files/TERRA%20Project%20Descriptions_FINAL_v2.pdf)

### Further Reading

* [ARPA-E TERRA program home](http://arpa-e.energy.gov/?q=programs/terra)
  * Detailed technical overview of the ARPA-E TERRA program ([pdf](http://arpa-e.energy.gov/sites/default/files/documents/files/TERRA_ProgramOverview.pdf))
    * Funding announcement press release for all six funded projects ([pdf]())
    

### Live Sorghum Field

This is a live stream of the Lemnatec field scanner at the USDA Arid Land Research Station in Maricopa, Arizona:


<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Pp6IdkPtFC8?rel=0" frameborder="0" allowfullscreen></iframe>


### Latest Posts

<ul class="post-list">
{% for post in site.posts limit:10 %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>