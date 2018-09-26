---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
<section class="posts">
                {% for post in site.posts limit:3 %}
                {% assign mod3 = forloop.index | modulo: 3 %}
  								<article>
  									<header>
  										<span class="date">{{ post.date | date_to_string }}</span>
  										<h2><a href="{{ post.url | absolute_url }}">{{ post.title }}</a></h2>
  									</header>
  									<a href="{{ post.url | absolute_url }}" class="image fit"><img src="{{ post.image | absolute_url }}" alt="" /></a>
  									<p>{{ post.excerpt }}</p>
  									<ul class="actions">
  										<li><a href="{{ post.url | absolute_url }}" class="button">Full Story</a></li>
  									</ul>
  								</article>
                  {% if mod3 == 0 %}
                  <article>
  									<header>
  										<h2><a href="#">Sponsored</a></h2>
  									</header>

  								</article>
                  {% endif %}
                {% endfor %}

</section>

[Link to a document]({{ site.baseurl }}{% link _posts/2018-09-16-welcome-to-jekyll.markdown %})
[Link to a post]({{ site.baseurl }}{% link _posts/2018-09-16-welcome-to-jekyll.markdown %})
[Link to a page]({{ site.baseurl }}{% link _posts/2018-09-16-welcome-to-jekyll.markdown %})
[Link to a file]({{ site.baseurl }}{% link _posts/2018-09-16-welcome-to-jekyll.markdown %})
