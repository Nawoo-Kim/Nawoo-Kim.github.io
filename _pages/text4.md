---
layout: page
permalink: /text4/
title: Text4
nav: true
nav_order: 34
---

<!-- Title, Author, Date List -->
<div class="post-info">
  <ul>
    {% for post in site.text %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.author }} - {{ post.date | date: "%Y. %m" }}
      </li>
    {% endfor %}
  </ul>
</div>

<!-- Posts List -->
<div class="posts">
  {% for post in site.text %}
    <article>
      ## [{{ post.title }}]({{ post.url }})
        {{ post.excerpt }}
        [Read more]({{ post.url }})
    </article>
  {% endfor %}
</div>