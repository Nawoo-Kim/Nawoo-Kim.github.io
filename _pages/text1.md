---
layout: page
permalink: /text1/
title: Text1
nav: true
nav_order: 31
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
