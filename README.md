# Au fil de l’archipel — site Jekyll

1. Adapter `url` et `baseurl` dans `_config.yml`.
2. Pousser le dossier sur GitHub, puis Settings → Pages → Deploy from a branch (`main`, `/ (root)`).
3. Ajouter un article : créer `_posts/AAAA-MM-JJ-titre.md` avec les champs `title`, `categorie`, `chapo`, `extrait` (optionnels : `art`, `lecture`, `auteur`, `sources`).
Test local : `bundle exec jekyll serve` (avec un Gemfile `github-pages`).
