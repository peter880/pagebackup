---
layout: page
title: 痞德趴趴走
tagline: Supporting tagline
---
{% include JB/setup %}


<ul class="posts">
  {% for post in site.posts limit:10 %}
    <a href="{{ BASE_PATH }}{{ post.url }}"><h3>{{ post.title }}</h3></a>
    <p>{{ post.date | date_to_string }}</p>

    {% if post.content contains "<!--more-->" %}
      <p>{{ post.excerpt }}</p>
    {% else %}
      <p>{{ post.content | strip_html | truncasteword:10}}</p>
    {% endif %}

    <a href="{{BASH_PATH}}{{post.url}}">Read More..</a>
    <hr>
  {% endfor %}
</ul>



