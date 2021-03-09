---
layout: page
title: sciences
permalink: /sciences/
description: Some science here.
nav: true
---

<div class="sciences grid">

  {% assign sorted_sciences = site.sciences | sort: "importance" %}
  {% for science in sorted_sciences %}
  <div class="grid-item">
    {% if science.redirect %}
    <a href="{{ science.redirect }}" target="_blank">
    {% else %}
    <a href="{{ science.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if science.img %}
        <img src="{{ science.img | relative_url }}" alt="science thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ science.title }}</h2>
          <p class="card-text">{{ science.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if science.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ science.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if science.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ science.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
