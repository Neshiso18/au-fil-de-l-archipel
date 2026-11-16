# Au fil de l'archipel

Revue personnelle d'analyse politique et géopolitique du Japon contemporain. Site statique Jekyll, hébergé gratuitement sur GitHub Pages.

## Arborescence

```
_config.yml        réglages (titre, url, baseurl)
_posts/            un fichier .md par article
_layouts/          modèles (default, post, page)
_includes/         en-tête, carte d'article, date et temps de lecture
_data/fr.yml       noms des mois en français
assets/css/        style.css (toute l'identité visuelle, variables en haut)
assets/img/        photographies, favicon
index.html         accueil        analyses.html  archive filtrable
demarche.md        page Démarche  a-propos.md    page À propos
```

## Publier un article

1. Crée `_posts/AAAA-MM-JJ-titre-court.md` (la date du nom de fichier = date de publication).
2. Mets en tête :

```yaml
---
title: "Titre de l'article"
subtitle: "Sous-titre facultatif"
category: Défense
summary: "Résumé de deux ou trois phrases."
image: /assets/img/mon-image.jpg
image_alt: "Description de l'image"
image_caption: "Légende"
image_credit: "Crédit : auteur / source"
featured: true     # facultatif : article « À la une » (sinon, le plus récent)
---
```
3. Rédige en Markdown : `##` intertitres, `###` sous-titres, `>` citations, `[^1]` notes de bas de page, puis les sections `## Notes` et `## Bibliographie et sources`.
4. Japonais dans le texte : `<span lang="ja">外務省</span>`.
5. Dépose l'image dans `assets/img/` et envoie le tout sur GitHub : l'accueil, l'archive, les filtres, le flux RSS et le sitemap se mettent à jour seuls.

Les trois articles `exemple-*` portent `demo: true` (badge « Exemple ») : supprime-les avant de publier pour de vrai. Pour un `featured`, un seul article à la fois.

Les catégories sont libres : une nouvelle catégorie écrite dans un article apparaît automatiquement comme filtre.

## Modifier l'apparence

Couleurs et polices : variables en tête de `assets/css/style.css` (`--bg`, `--tx`, `--red`, `--serif`). Les polices viennent de Google Fonts (gratuit) ; pour supprimer ce service externe, héberge les fichiers dans `assets/` avec `@font-face`.

## Mise en ligne gratuite avec GitHub Pages

1. Sur github.com, ouvre ton dépôt (ou crée-en un, public).
2. Envoie tous les fichiers de ce dossier à la racine (bouton *Add file → Upload files*, ou `git add . && git commit -m "Première version" && git push`).
3. *Settings → Pages* : *Source* = **Deploy from a branch**, branche **main**, dossier **/(root)**, puis *Save*.
4. Attends 1 à 2 minutes : le site est à `https://<pseudo>.github.io/<nom-du-depot>/`.
5. Dans `_config.yml`, renseigne `url: "https://<pseudo>.github.io"` et, si le dépôt n'est pas nommé `<pseudo>.github.io`, `baseurl: "/<nom-du-depot>"`. Commit.

## Test en local (facultatif)

`bundle install && bundle exec jekyll serve` puis http://localhost:4000
