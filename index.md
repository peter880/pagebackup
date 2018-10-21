---
layout: default_custom
title: 痞德趴趴走
tagline: Supporting tagline
---
{% include JB/setup %}


<ul class="posts">
  {% for post in site.posts limit:10 %}
    <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    <p>{{ post.date | date_to_string }}</p>
    <p>{{ post.content | strip_html | truncasteword:10}}</p>
    <a href="{{BASH_PATH}}{{post.url}}">Read More..</a>
    <hr>
  {% endfor %}
</ul>



