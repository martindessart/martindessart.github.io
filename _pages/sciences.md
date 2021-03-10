---
layout: page
title: sciences
permalink: /sciences/
description:
nav: true
order: 4
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
      <h3><a href="{{ science.url | relative_url }}">{{ science.title }}</a>
      <p class="post-meta">{{ science.date | date: '%B %-d, %Y' }}</p>
      <p>{{ science.description }}</p>
      </h3>
    </li>
  {% endfor %}
  </ul>
</div>
