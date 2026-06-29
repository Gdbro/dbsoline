---
layout: page
title: Actualités
description: Les actualités reprises du site existant et migrées dans le nouveau socle Jekyll.
permalink: /actualites/
hero_image: /assets/images/bandeau-asso.jpg
---

Cette page reprend les actualités de l'association avec une mise en avant claire de l'information principale.

{% assign top_post = site.posts | first %}
{% if top_post %}
<section class="content-panel news-spotlight">
  <p class="eyebrow">Publication prioritaire</p>
  <article class="featured-news-card">
    {% if top_post.image %}
      <img src="{{ top_post.image | relative_url }}" alt="{{ top_post.title }}">
    {% endif %}
    <div class="featured-news-body">
      <time datetime="{{ top_post.date | date_to_xmlschema }}">{{ top_post.date | date: "%d/%m/%Y" }}</time>
      <h3>{{ top_post.title }}</h3>
      <p>{{ top_post.excerpt | strip_html | strip_newlines }}</p>
      <a class="button" href="{{ top_post.url | relative_url }}">Lire l'article à la une</a>
    </div>
  </article>
</section>
{% endif %}

<h2>Archives des actualités</h2>

<div class="posts-grid">
{% for post in site.posts offset:1 %}
  <article class="post-card">
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
    <h3>{{ post.title }}</h3>
    <p>{{ post.excerpt | strip_html | strip_newlines }}</p>
    <a class="button-secondary" href="{{ post.url | relative_url }}">Lire l'article</a>
  </article>
{% endfor %}
</div>

{% include facebook-feed.html %}
