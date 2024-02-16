---
layout: page
permalink: /text3/
title: Text3
nav: true
nav_order: 34
---

<!-- Title, Author, Date List -->
<div class="post-info">
  <ul>
    {% for post in site.posts %}
      {% if post.categories contains 'text' %}
        <li>
          [{{ post.title }}]({{ post.url }}) - {{ post.author }} - {{ post.date | date: "%Y. %m" }}
        </li>
      {% endif %}
    {% endfor %}
  </ul>
</div>

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