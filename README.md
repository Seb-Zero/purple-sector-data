# purple-sector-data

Données publiées de [Purple Sector](https://github.com/Seb-Zero/purple-sector).
**Aucun code ici** — uniquement des JSON produits par
[`purple-sector-pipeline`](https://github.com/Seb-Zero/purple-sector-pipeline) et servis
par GitHub Pages.

Ce dépôt est séparé pour que les milliers de commits de données ne polluent pas
l'historique du code, et pour pouvoir purger ou republier sans toucher au projet.

## Contrat

```
v1/index.json                                 saisons disponibles
v1/<saison>/index.json                        événements
v1/<saison>/<event>/index.json                séances, statut, rev, signature
v1/<saison>/<event>/<session>/session.json    méta + pilotes
v1/<saison>/<event>/<session>/laps.json       tours normalisés
v1/<saison>/<event>/<session>/analysis.json   classement, secteurs, tour théorique
```

Un fichier de séance est **immuable** : une correction de calcul incrémente `rev` dans
l'index de l'événement plutôt que de réécrire le fichier.

Tous les chronos sont des **entiers de millisecondes**. Une valeur absente vaut `null`,
jamais `0`.

## Provenance et usage

Données de chronométrage à titre informatif, reconstruites depuis
[FastF1](https://github.com/theOehrly/Fast-F1). Projet indépendant, non affilié à la
Formule 1, à la FIA ou aux écuries.
