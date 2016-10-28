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

This video follows the slides above.    

<iframe width="560" height="315" src="https://www.youtube.com/embed/lP3vqh6HLG4?rel=0" frameborder="0" allowfullscreen></iframe>

It is about 80 minutes, much of which is just installing a development environment. If you open it in [YouTube](https://www.youtube.com/watch?v=lP3vqh6HLG4); the first comment contains the following bookmarks to jump to specific topics. 

* [Overview 0:00](https://youtu.be/lP3vqh6HLG4?t=0s)
* [Setting up a test environment 3:12](https://youtu.be/lP3vqh6HLG4?t=3m12s)
  * [Required software 3:38](https://youtu.be/lP3vqh6HLG4?t=3m38s)
  * [Docker (the 'easy' way) 5:58](https://youtu.be/lP3vqh6HLG4?t=5m58s)
  * [Running sample extractor 40:37](https://youtu.be/lP3vqh6HLG4?t=40m37s)
* [Extractor Basic Design 29:15](https://youtu.be/lP3vqh6HLG4?t=29m15s)
  * [PyClowder library 28:04](https://youtu.be/lP3vqh6HLG4?t=28m04s)
* [Writing an extractor 1:02:11](https://youtu.be/lP3vqh6HLG4?t=62m11s)
  * [Handling inputs and outputs 1:02:11](https://youtu.be/lP3vqh6HLG4?t=https://youtu.be/lP3vqh6HLG4?t=62m44s)
  * [Testing extractors  1:07:33](https://youtu.be/lP3vqh6HLG4?t=67m33s)

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
