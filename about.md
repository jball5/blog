---
layout: default
title: About
permalink: /about/
---
This page contains the authors bios.
{% for author in site.authors %}
  <div class="row justify-content-left">
    <div class="col-3">
      <img src="{{ author.image }}" class="img-fluid rounded" style="width: 150px; height: auto;">
    </div>
    <div class="col-9">
      <h4 class="text-dark">{{ author.name }}</h4>
      {{ author.title }}<br />
      {{ author.company }}<br />
      <span class="text-black-50 font-weight-lighter font-italic"><p>{{ author.content | markdownify }}</p></span>
    </div>
  </div>
{% endfor %}
