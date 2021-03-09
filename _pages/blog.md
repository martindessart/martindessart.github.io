---
layout: page
title: blogs
permalink: /blogs/
description: REAL BLOG.
nav: true
---
<div class="blogs grid">

  {% assign sorted_blogs = site.blogs | sort: "importance" %}
  {% for blog in sorted_blogs %}
  <div class="grid-item">
    {% if blog.redirect %}
    <a href="{{ blog.redirect }}" target="_blank">
    {% else %}
    <a href="{{ blog.url | relative_url }}">
    {% endif %}

  </div>
    {% endfor %}

  </div>
