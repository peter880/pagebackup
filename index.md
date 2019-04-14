---
layout: page
title: 彼得趴趴走
tagline: 熱愛生活 ‧ 不遺餘力
---
{% include JB/setup %}

<h2>新文章</h2>
{% for post in site.posts limit:6 %}
<div class="row">
  <div class="col-md-4">  
      <img src="{{ post.pic }}" class="img-thumbnail" >
  </div>
  <div class="col-md-8">  
  <a href="{{ BASE_PATH }}{{ post.url }}"><h2>{{ post.title }}</h2></a>
      <h5><span class="glyphicon glyphicon-time"></span> {{ post.date | date_to_string }}</h5>
      {% if post.content contains "<!--more-->" %}
        <p>{{ post.excerpt }}</p>
      {% else %}
        <p>{{ post.content | strip_html | truncasteword:50}}</p>
      {% endif %}
      <p><a class="btn btn-default" href="{{BASH_PATH}}{{post.url}}" role="button">Read More &raquo;</a></p>
  </div>
</div>
<hr>
{% endfor %}

