---
layout: default
title: Главная
---

<h1>Лента записей</h1>
<ul>
  {% for post in site.posts %}
  <li>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <time>{{ post.date | date: "%d %B %Y" }}</time>
    <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
  </li>
  {% endfor %}
</ul>
