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
  <p class="eyebrow">Actualités</p>
  <h2 class="section-title">Dernieres nouvelles</h2>
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
