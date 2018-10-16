---
layout: default_custom
title: 痞德趴趴走
tagline: Supporting tagline
---
{% include JB/setup %}


<ul class="posts">
  {% for post in site.posts %}
    <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    <p>{{ post.date | date_to_string }}</p>
    <hr>
  {% endfor %}
</ul>



