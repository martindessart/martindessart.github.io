---
layout: page
title: Blog
permalink: /wrong/
description:
nav: true
order: 4
---

<div class="post">
  <div class="header-bar">
    <h1>Billets de réflexion <br>(ou pas)</h1>
  </div>
  <ul class="post-list">  
  {% assign sorted_sciences = site.sciences | sort: "importance" %}
  {% for science in sorted_sciences %}
    <li>
      <h2><a class="post-title" href="{{ science.url | relative_url }}">{{ science.title }}</a>
      <p class="post-meta">{{ science.date | date: '%B %-d, %Y' }}</p>
      </h2>
    </li>
  {% endfor %}
  </ul>
</div>
