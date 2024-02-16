---
layout: page
permalink: /text2/
title: Text2
nav: true
nav_order: 32
---

<!-- Posts List -->
<div class="posts">
  {% for post in site.posts %}
    {% if post.categories contains 'text' %}
      <article>
        ## [{{ post.title }}]({{ post.url }})
        {{ post.excerpt }}
        [Read more]({{ post.url }})
      </article>
    {% endif %}
  {% endfor %}
</div>