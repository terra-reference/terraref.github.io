---
layout: page
title: Welcome Page
excerpt: ""
search_omit: true
---

* Table of Contents
{:toc}

# About this site

This is a sandbox for development of an open-access data and computing platform support the assessment of crop yield potential using sensors, robots, high performance computing within a collaborative, cross-disciplinary research and development

* Most information about the project is under the documentation tab
* Meeting notes are under the notes tab
* This site is likely to change
* Find us and contribute, request features, report bugs, and share ideas on
  * [Github at github.com/terraref](https://github.com/terraref)

# Latest Posts

<ul class="post-list">
{% for post in site.posts limit:10 %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
