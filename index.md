---
layout: default
title: Accueil
description: Site de l'association Du Bruit Pour Soline, en soutien aux enfants nés avec une aplasie, une atrésie ou une microtie.
permalink: /
---

<section class="hero">
  <div class="hero-copy">
    <p class="eyebrow">Association solidaire</p>
    <h1>Du Bruit Pour Soline</h1>
    <p class="lead">Soutien aux enfants nés avec des malformations rares de l'oreille: aplasie, atrésie et microtie.</p>
    <p class="lead">Soline est née en août 2022 à Lens avec une microtie atrésie de grade 3. L'association est née pour l'aider, et pour soutenir d'autres enfants et familles confrontés aux mêmes enjeux.</p>
    <div class="hero-actions">
      <a class="button" href="{{ '/nous-soutenir/' | relative_url }}">Faire un don</a>
      <a class="button-secondary" href="{{ '/a-propos/' | relative_url }}">Découvrir la cause</a>
    </div>
  </div>
  <aside class="hero-side">
    <figure class="hero-media">
      <img src="{{ '/assets/images/hero-soline.jpg' | relative_url }}" alt="Soline et l'association Du Bruit Pour Soline">
    </figure>
    <div class="hero-badge">
      <strong>Point de contact principal</strong>
      <p>1bis, rue Jean Jaurès<br>62670 Mazingarbe</p>
    </div>
    <div class="hero-badge">
      <strong>Collecte toujours active</strong>
      <p>La collecte de papier continue avec une organisation simplifiée, en priorité sur Mazingarbe.</p>
    </div>
    <div class="hero-badge">
      <strong>Suivre l'association</strong>
      <p><a href="{{ site.social.facebook }}">Facebook</a> · <a href="{{ site.social.instagram }}">Instagram</a> · <a href="{{ site.social.linkedin }}">LinkedIn</a></p>
    </div>
  </aside>
</section>

{% assign featured_post = site.posts | first %}
<section class="content-panel news-spotlight">
  <div class="news-spotlight-header">
    <p class="eyebrow">À la une</p>
    <h2 class="section-title">Les actualités passent en premier plan</h2>
    <p class="lead">Le cœur de la vie de l'association est ici: publications, avancées, événements, et mobilisation terrain.</p>
  </div>

  <div class="news-spotlight-grid">
    {% if featured_post %}
      <article class="featured-news-card">
        {% if featured_post.image %}
          <img src="{{ featured_post.image | relative_url }}" alt="{{ featured_post.title }}">
        {% endif %}
        <div class="featured-news-body">
          <time datetime="{{ featured_post.date | date_to_xmlschema }}">{{ featured_post.date | date: "%d/%m/%Y" }}</time>
          <h3>{{ featured_post.title }}</h3>
          <p>{{ featured_post.excerpt | strip_html | strip_newlines }}</p>
          <a class="button" href="{{ featured_post.url | relative_url }}">Lire l'actualité à la une</a>
        </div>
      </article>
    {% endif %}

    <aside class="news-quick-list">
      <h3>Plus récentes</h3>
      {% assign secondary_posts = site.posts | slice: 1, 3 %}
      {% for post in secondary_posts %}
        <article class="news-mini-item">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
          <h4><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h4>
        </article>
      {% endfor %}
      <a class="button-secondary" href="{{ '/actualites/' | relative_url }}">Voir toutes les actualités</a>
    </aside>
  </div>
</section>

<section class="grid-3">
  <article class="card">
    <h2>Notre cause</h2>
    <p>Informer, mobiliser et soutenir autour des malformations rares de l'oreille, avec une approche très concrète: collecte, événements, entraide et visibilité.</p>
    <a class="button-secondary" href="{{ '/a-propos/' | relative_url }}">Nos valeurs et actions</a>
  </article>
  <article class="card">
    <h2>Nos événements</h2>
    <p>Le site d'origine annonçait peu d'événements à date, mais la mobilisation locale continue. Le rythme dépend des opportunités et des soutiens du terrain.</p>
    <a class="button-secondary" href="{{ '/evenements/' | relative_url }}">Voir la page événements</a>
  </article>
  <article class="card">
    <h2>S'impliquer</h2>
    <p>Don, relais local, collecte de papier, proposition d'evenement, partage: plusieurs formes d'aide sont possibles pour soutenir l'association.</p>
    <a class="button-secondary" href="{{ '/nous-soutenir/' | relative_url }}">Comment aider</a>
  </article>
</section>

<section class="content-panel">
  <p class="eyebrow">Galerie</p>
  <h2 class="section-title">Visuels de l'association</h2>
  <div class="media-grid">
    <figure class="media-card">
      <img src="{{ '/assets/images/bandeau-asso.jpg' | relative_url }}" alt="Bandeau de l'association Du Bruit Pour Soline">
    </figure>
    <figure class="media-card">
      <img src="{{ '/assets/images/portrait-soline.jpg' | relative_url }}" alt="Portrait de Soline">
    </figure>
    <figure class="media-card">
      <img src="{{ '/assets/images/logo-asso.png' | relative_url }}" alt="Visuel de l'association">
    </figure>
  </div>
</section>

<section class="content-panel">
  <p class="eyebrow">Actualités</p>
  <h2 class="section-title">Dernières nouvelles</h2>
  <div class="posts-grid">
    {% assign latest_posts = site.posts | slice: 0, 3 %}
    {% for post in latest_posts %}
      <article class="post-card">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d/%m/%Y" }}</time>
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | strip_newlines }}</p>
        <a class="button-secondary" href="{{ post.url | relative_url }}">Lire</a>
      </article>
    {% endfor %}
  </div>
</section>

{% include facebook-feed.html %}
