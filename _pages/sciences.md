---
layout: page
title: sciences
permalink: /sciences/
description: Some science here.
nav: true
---

<div class="post">
  <div class="header-bar">
    <h1>Blog</h1>
    <h2>I'll write some science here</h2>
  </div>
  <ul class="post-list">  
  {% assign sorted_sciences = site.sciences | sort: "importance" %}
  {% for science in sorted_sciences %}
    <li>
      <h3><a href="{{ science.url | relative_url }}"></h3>
    </li>
  {% endfor %}
  </ul>
</div>
