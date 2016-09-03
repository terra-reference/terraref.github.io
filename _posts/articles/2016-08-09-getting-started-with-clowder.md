---
layout: post
title: "Tutorial for developers: Adding algorithms to the phenomics pipeline"
excerpt: "Max introduces the use of Clowder to automate algorithms"  
categories: articles
tags: [clowder, pipeline, reference data, algorithms]
image: 
  feature: logos/clowder_long.png
  thumb: logos/clowder_smallcat.png
  credit: Clowder
date: 2016-08-09
---



* Table of Contents
{:toc}

NCSA Research Programmer Max Burnette has recorded a tutorial for computational scientists interested in adding their algorithms to Clowder. _NOTE: This is aimed at pipeline developers rather than data users_. 

The TERRA REF program has an instance of Clowder at https://terraref.ncsa.illinois.edu/clowder being used for the TERRA REF data stream.  
<!--Max: please summarize content here; one paragraph is sufficient--> 

## Slides

<iframe src='https://onedrive.live.com/embed?cid=62A7CDC1353EF6B0&resid=62A7CDC1353EF6B0%211988&authkey=ALJbJ7PqsDaYAxU&em=2&wdAr=1.7777777777777777' width='610px' height='367px' frameborder='0'>This is an embedded <a target='_blank' href='https://office.com'>Microsoft Office</a> presentation, powered by <a target='_blank' href='https://office.com/webapps'>Office Online</a>.</iframe>

## Video

<iframe width="560" height="315" src="https://www.youtube.com/embed/lP3vqh6HLG4?rel=0" frameborder="0" allowfullscreen></iframe>

### Next steps

Please get in touch or create a github issue once you are starting to actually develop your extractor and I can help get you off to a good start. 

Contact Max Burnette via [email, phone](http://www.ncsa.illinois.edu/assets/php/directory/contact.php?contact=mburnet2), on GitHub, or on our [Slack Channel](https://terra-ref.slack.com/)

## References

* Orignially posted on the [Clowder wiki](https://opensource.ncsa.illinois.edu/confluence/display/CATS/Documents)
* [Clowder Documentation](https://clowder.ncsa.illinois.edu/docs/)
* [Use of Clowder within TERRA REF](https://terraref.gitbooks.io/terraref-documentation/content/clowder.html)
* [`docker-compose.xml`](https://opensource.ncsa.illinois.edu/bitbucket/projects/CATS/repos/clowder/browse/docker-compose.yml?at=refs%2Fheads%2Fdevelop&raw) file you can use to start the Clowder stack  
* Sample extractor [`wordcount.py`](https://opensource.ncsa.illinois.edu/bitbucket/projects/CATS/repos/pyclowder/browse/sample-extractors/wordcount). See also `config.py`
* [Clowder API documentation](https://terraref.ncsa.illinois.edu/clowder/assets/docs/api/index.html)

<div class="actions">
  <a href="{{site.github.repository_url}}/edit/master/{{ page.path }}">Edit this page</a>
</div>
