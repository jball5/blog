---
layout: default
title: Blog
permalink: /blog/
---
<div class="list-group">
  {% for post in site.posts %}
    <a href="{{ post.url }}" class="list-group-item list-group-item-action">
      <small class="text-success font-weight-bold">{{ post.categories | first }}</small>
      <div class="d-flex justify-content-between">
        <h3 class="mb-1 font-italic">{{ post.title }}</h3>
        <small>{{ post.date | date: "%-m/%-d/%Y" }}</small>
      </div>
        &nbsp;{% if post.image %}<img src="{{ post.image }}" class="img-fluid rounded shadow">&nbsp;{% endif %}
        <p class="text-muted">{{ post.excerpt | strip_html | strip_newlines | truncate: 175 }}</p>
    </a>
    <span>&nbsp;</span>
  {% endfor %}
</div>
