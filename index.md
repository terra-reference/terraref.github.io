---
layout: page
title: "Welcome"
excerpt: ""
search_omit: true
---

### Live Sorghum Field

This is a live stream of the Lemnatec field scanner at the USDA Arid Land Research Station in Maricopa, Arizona:


<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Pp6IdkPtFC8?rel=0" frameborder="0" allowfullscreen></iframe>


### Latest Posts

<ul class="post-list">
{% for post in site.posts limit:10 %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>