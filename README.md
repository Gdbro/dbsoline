# Du Bruit Pour Soline

Premier socle Jekyll du site `dbsoline`, reconstruit a partir du miroir du site existant.

## Lancer en local

```bash
bundle install
bundle exec jekyll serve
```

Le site sera disponible sur `http://127.0.0.1:4000/dbsoline/`.

## GitHub Pages

Le depot contient un workflow GitHub Actions qui construit et publie le site sur GitHub Pages.

Points a verifier dans GitHub:

1. Activer GitHub Pages avec la source `GitHub Actions`.
2. Pousser sur `develop` ou `main`.
3. Ajuster `baseurl` dans `_config.yml` si vous utilisez un domaine personnalise.

## Contenu repris

- pages principales: accueil, a propos, soutien, collecte, actualites, evenements, contact
- trois actualites migrees depuis le miroir Wix
- structure simple pour poursuivre la migration page par page
