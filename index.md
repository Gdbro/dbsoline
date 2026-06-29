---
layout: default
title: Accueil
description: Site de l'association Du Bruit Pour Soline, en soutien aux enfants nes avec une aplasie, une atresie ou une microtie.
permalink: /
---

<section class="hero">
  <div class="hero-copy">
    <p class="eyebrow">Association solidaire</p>
    <h1>Du Bruit Pour Soline</h1>
    <p class="lead">Soutien aux enfants nes avec des malformations rares de l'oreille: aplasie, atresie et microtie.</p>
    <p class="lead">Soline est nee en aout 2022 a Lens avec une microtie atresie de grade 3. L'association est nee pour l'aider, et pour soutenir d'autres enfants et familles confrontes aux memes enjeux.</p>
    <div class="hero-actions">
      <a class="button" href="{{ '/nous-soutenir/' | relative_url }}">Faire un don</a>
      <a class="button-secondary" href="{{ '/a-propos/' | relative_url }}">Decouvrir la cause</a>
    </div>
  </div>
  <aside class="hero-side">
    <div class="hero-badge">
      <strong>Point de contact principal</strong>
      <p>1bis, rue Jean Jaures<br>62670 Mazingarbe</p>
    </div>
    <div class="hero-badge">
      <strong>Collecte toujours active</strong>
      <p>La collecte de papier continue avec une organisation simplifiee, en priorite sur Mazingarbe.</p>
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
    <p>Informer, mobiliser et soutenir autour des malformations rares de l'oreille, avec une approche tres concrete: collecte, evenements, entraide et visibilite.</p>
    <a class="button-secondary" href="{{ '/a-propos/' | relative_url }}">Nos valeurs et actions</a>
  </article>
  <article class="card">
    <h2>Nos evenements</h2>
    <p>Le site d'origine annonçait peu d'evenements a date, mais la mobilisation locale continue. Le rythme depend des opportunites et des soutiens du terrain.</p>
    <a class="button-secondary" href="{{ '/evenements/' | relative_url }}">Voir la page evenements</a>
  </article>
  <article class="card">
    <h2>S'impliquer</h2>
    <p>Don, relais local, collecte de papier, proposition d'evenement, partage: plusieurs formes d'aide sont possibles pour soutenir l'association.</p>
    <a class="button-secondary" href="{{ '/nous-soutenir/' | relative_url }}">Comment aider</a>
  </article>
</section>

<section class="content-panel">
  <p class="eyebrow">Actualites</p>
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
