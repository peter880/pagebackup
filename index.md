---
layout: page
title: 彼得趴趴走
tagline: 熱愛生活 ‧ 不遺餘力
---
{% include JB/setup %}

<hr>

<div class="row">
<h2>旅遊雜記</h2>
{% for post in site.posts limit:3 %}
  <div class="col-md-4">
  
  <a href="{{ BASE_PATH }}{{ post.url }}"><h2>{{ post.title }}</h2></a>
      <h5><span class="glyphicon glyphicon-time"></span> {{ post.date | date_to_string }}</h5>
      <img src="{{ post.pic }}" class="img-thumbnail" >
      {% if post.content contains "<!--more-->" %}
        <p>{{ post.excerpt }}</p>
      {% else %}
        <p>{{ post.content | strip_html | truncasteword:10}}</p>
      {% endif %}

      <p><a class="btn btn-default" href="{{BASH_PATH}}{{post.url}}" role="button">Read More &raquo;</a></p>

  </div>
{% endfor %}
</div>

<hr>

<div class="col-sm-12" style="background-color:lavenderblush">
  <h2>Category</h2>
</div>
