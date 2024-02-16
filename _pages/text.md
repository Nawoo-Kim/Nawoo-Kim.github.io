---
layout: page
permalink: /text/
title: Text
nav: true
nav_order: 30
---

<div class="post-info">
  <ul style="list-style: none; padding-left: 0;">
    <li style="border-bottom: 1px solid black; padding: 5px 0; font-weight: bold; text-decoration: underline;"></li>
    {% for post in site.text %}
      <li style="border-bottom: 1px solid black; padding: 5px 0;">
        <span style="font-size: 120%; font-weight: bold;">&rarr;</span> <a href="{{ post.url }}" style="color: black; text-decoration: none;">{{ post.title | markdownify }}</a> - {{ post.author }} - {{ post.date | date: "%Y. %m" }}
      </li>
    {% endfor %}
    <li style="border-bottom: 1px solid black; padding: 5px 0;"></li>
  </ul>
</div>



<!-- Posts List -->
<div class="posts">
  {% for post in site.text %}
    <article>
      <h2><a href="{{ post.url }}">{{ post.title | markdownify }}</a></h2>
      <p>... {{ post.excerpt }} ... <a href="{{ post.url }}">Read more</a></p>
    </article>
  {% endfor %}
</div>
