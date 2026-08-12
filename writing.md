---
layout: page
title: Writing archive
permalink: /writing/
---

This site used to be a blog. These older pieces live on here for posterity.

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) <span class="archive-date">— {{ post.date | date: '%B %Y' }}</span>
{% endfor %}
