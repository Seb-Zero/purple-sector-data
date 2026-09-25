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

**Ce dépôt n'accorde aucune licence sur les données qu'il contient.** Il est public parce
que l'app Purple Sector les lit par GitHub Pages ; ce n'est pas une mise à disposition.
Les résultats, chronos et statistiques de la Formule 1 sont revendiqués par les sociétés
Formula 1. **Toute donnée est retirée sur demande de leurs ayants droit** : ouvrir une
issue sur ce dépôt.

F1, FORMULA ONE, FORMULA 1, FIA FORMULA ONE WORLD CHAMPIONSHIP, GRAND PRIX et les marques
associées sont des marques de Formula One Licensing B.V.

---

*This repository grants no licence over the data it contains. It is public only because
the Purple Sector app reads it through GitHub Pages. Formula 1 results, timing data and
statistics are claimed by the Formula 1 companies; any data is removed at their request
(open an issue). This project is unofficial and is not associated in any way with the
Formula 1 companies.*
