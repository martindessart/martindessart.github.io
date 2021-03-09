---
layout: page
title: blegs
permalink: /blegs/
description: Stuffsss
nav: true
---

<div class="blegs grid">

  {% assign sorted_blegs = site.blegs | sort: "importance" %}
  {% for bleg in sorted_blegs %}
  <div class="grid-item">
    {% if bleg.redirect %}
    <a href="{{ bleg.redirect }}" target="_blank">
    {% else %}
    <a href="{{ bleg.url | relative_url }}">
    {% endif %}
  </div>
  {% endfor %}

</div>
