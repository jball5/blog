---
layout: default
title: About
permalink: /about/
---
This page contains the authors bios.

{% for author in site.authors %}
  <h2>
    <a href="{{ author.url }}">
      {{ author.name }} - {{ author.title }}
    </a>
  </h2>
  <p>{{ author.content | markdownify }}</p>
{% endfor %}
