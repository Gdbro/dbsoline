---
layout: page
title: Actualites
description: Les actualites reprises du site existant et migrees dans le nouveau socle Jekyll.
permalink: /actualites/
---

Cette page reprend les premieres actualites migrees du site miroir afin d'initialiser une base editable dans le depot.

<div class="posts-grid">
{% for post in site.posts %}
  <article class="post-card">
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
    <h3>{{ post.title }}</h3>
    <p>{{ post.excerpt | strip_html | strip_newlines }}</p>
    <a class="button-secondary" href="{{ post.url | relative_url }}">Lire l'article</a>
  </article>
{% endfor %}
</div>
