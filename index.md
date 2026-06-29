---
layout: default
title: Accueil
description: Suivez le voyage de Soline aux États-Unis pour son opération. Départ le 12 juillet 2026.
permalink: /
---

<section class="hero">
  <div class="hero-copy">
    <p class="eyebrow">📅 Départ le 12 juillet 2026</p>
    <h1>Du Bruit Pour Soline</h1>
    <p class="lead">Soline a 3 ans. Elle est née avec une microtie atrésie de grade 3 — une malformation rare de l'oreille. Grâce à la mobilisation de centaines de personnes, sa famille part aux États-Unis cet été pour l'opérer.</p>
    <div class="hero-actions">
      <a class="button" href="{{ '/journal/' | relative_url }}">📖 Suivre le journal de bord</a>
      <a class="button-secondary" href="{{ '/soutenir/' | relative_url }}">Soutenir</a>
    </div>
  </div>
  <aside class="hero-side">
    <figure class="hero-media">
      <img src="{{ '/assets/images/hero-soline.jpg' | relative_url }}" alt="Soline">
    </figure>
    <div class="hero-badge">
      <strong>🎯 Objectif atteint</strong>
      <p>Les 150 000 € nécessaires ont été réunis grâce à votre soutien.</p>
    </div>
    <div class="hero-badge">
      <strong>📲 Suivre en direct</strong>
      <p><a href="{{ site.social.facebook }}">Facebook</a> · <a href="{{ site.social.instagram }}">Instagram</a></p>
    </div>
  </aside>
</section>

{% assign latest = site.posts | first %}
<section class="content-panel">
  {% if latest %}
    <p class="eyebrow">Dernière entrée du journal</p>
    <time datetime="{{ latest.date | date_to_xmlschema }}">{{ latest.date | date: "%-d %B %Y" }}</time>
    <h2>{{ latest.title }}</h2>
    {% if latest.image %}
      <img src="{{ latest.image | relative_url }}" alt="{{ latest.title }}" class="post-image">
    {% endif %}
    <p>{{ latest.excerpt | strip_html | strip_newlines | truncatewords: 40 }}</p>
    <a class="button-secondary" href="{{ '/journal/' | relative_url }}">Lire tout le journal →</a>
  {% else %}
    <p class="eyebrow">Journal de bord</p>
    <h2>Le voyage commence le 12 juillet</h2>
    <p>Le journal de bord sera mis à jour depuis les États-Unis dès notre arrivée. Revenez ici pour suivre chaque étape en direct.</p>
    <a class="button-secondary" href="{{ '/journal/' | relative_url }}">Aller au journal →</a>
  {% endif %}
</section>

<section class="grid-2">
  <article class="card">
    <h2>L'histoire de Soline</h2>
    <p>Née en août 2022 à Lens avec une microtie atrésie de grade 3. Deux ans de mobilisation, de collectes et d'entraide pour lui offrir une opération aux États-Unis.</p>
    <a class="button-secondary" href="{{ '/soline/' | relative_url }}">Découvrir son histoire</a>
  </article>
  <article class="card">
    <h2>Soutenir l'association</h2>
    <p>Don, collecte de papier, partage sur les réseaux — chaque geste compte pour Soline et pour d'autres enfants après elle.</p>
    <a class="button-secondary" href="{{ '/soutenir/' | relative_url }}">Comment aider</a>
  </article>
</section>
