---
layout: default
title: Blog
permalink: /blog/
---
<div class="container">
  <div class="row">
    <div class="list-group">
      {% for post in site.posts limit:10 %}
        <a href="{{ post.url }}" class="list-group-item list-group-item-action">
          <strong class="text-info">{{ post.categories | first | downcase }}</strong>
          <div>
            <div class="d-flex justify-content-between">
              <h3 class="mb-1 font-italic">{{ post.title }}</h3>
              <p class="text-muted d-none d-md-block">{{ post.date | date_to_string: "ordinal", "US" }}</p>
            </div>
            <div class="d-flex justify-content-center">
              <p class="text-muted d-block d-sm-block d-md-none mt-2">{{ post.date | date_to_string: "ordinal", "US" }}</p>
            </div>
            {% include mini_author_snippet.html %}
          </div>
            {% if post.youtubeurl contains 'youtube' %}&nbsp;{% youtube post.youtubeurl %}&nbsp;{% endif %}
            {% if post.image contains 'cloudinary' %}&nbsp;<img src="{{ post.image }}" class="img-fluid rounded shadow">&nbsp;{% endif %}
            <p class="text-muted">{{ post.excerpt | strip_html | strip_newlines | truncate: 175 }}</p>
        </a>
        <span>&nbsp;</span>
      {% endfor %}
    </div>
  </div>  
</div>
