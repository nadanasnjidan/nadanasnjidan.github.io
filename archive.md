---
layout: default
title: "Arhiv"
permalink: /archive/
---

<h1 class="page__title">Arhiv</h1>

{% if site.posts.size > 0 %}
<ul class="archive__list">
  {% for post in site.posts %}
  <li class="archive__item">
    <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%-d. %-m. %Y" }}</time>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>
{% else %}
<div class="empty">
  <p>Arhiv je še prazen.</p>
</div>
{% endif %}
