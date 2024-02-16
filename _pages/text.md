---
layout: page
permalink: /text/
title: Text
nav: true
nav_order: 30
---

<!-- Title, Author, Date List -->
<div class="post-info">
  <ul>
    {% for post in site.text %}
      <li>
        [{{ post.title }}]({{ post.url }}) - {{ post.author }} - {{ post.date | date: "%Y. %m" }}
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

