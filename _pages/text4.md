---
layout: page
permalink: /text4/
title: Text4
nav: true
nav_order: 34
---

<div class="post-info">
  <ul style="list-style: none; padding-left: 0;">
    {% for post in site.text %}
      <li style="border-bottom: 1px solid black; padding: 5px 0;">
        <span style="font-size: 120%;">&rarr;</span> <a href="{{ post.url }}" style="color: black; text-decoration: none;">{{ post.title }}</a> - {{ post.author }} - {{ post.date | date: "%Y. %m" }}
      </li>
    {% endfor %}
    <li style="border-bottom: 1px solid black; padding: 5px 0;"></li>
  </ul>
</div>


<!-- Posts List -->
<div class="posts">
  {% for post in site.text %}
    <article>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
      <p><a href="{{ post.url }}">Read more</a></p>
    </article>
  {% endfor %}
</div>
