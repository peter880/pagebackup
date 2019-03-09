---
layout: page
title: 痞德趴趴走
tagline: Supporting tagline
---
{% include JB/setup %}

<div class="col-sm-12" style="background-color:rgb(255,220,200);">

<h4>Travel Daily</h4>
{% for post in site.posts limit:3 %}
  <div class="col-sm-6">
    <div class="thumbnail">
      <a href="{{ BASE_PATH }}{{ post.url }}"><h2>{{ post.title }}</h2></a>
      <h5><span class="glyphicon glyphicon-time"></span> {{ post.date | date_to_string }}</h5>

      {% if post.content contains "<!--more-->" %}
        <p>{{ post.excerpt }}</p>
      {% else %}
        <p>{{ post.content | strip_html | truncasteword:10}}</p>
      {% endif %}

      <a href="{{BASH_PATH}}{{post.url}}">Read More..</a>
  </div>
    </div>
{% endfor %}
</div>

<div class="col-sm-12" style="background-color:lavenderblush">
  <h5>Category</h5>
</div>
