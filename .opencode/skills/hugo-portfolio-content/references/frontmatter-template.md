# Gabarits de front matter — fiches projet

Ces gabarits sont des points de départ génériques. **Toujours les adapter**
au schéma réel observé dans l'archétype ou les fiches existantes du site :
ne jamais imposer ce schéma s'il diffère de l'existant.

## Cas 1 — fichier unique par langue, mêmes clés

`content/fr/projets/mon-projet.md`

```yaml
---
title: "Refonte du site vitrine — Atelier Dupont"
date: 2026-03-12
draft: false
summary: >-
  Refonte complète du site vitrine, migration vers Hugo et mise en place
  d'une identité visuelle cohérente avec la nouvelle charte graphique.
client: "Atelier Dupont"
role: "Développement front-end & intégration"
technologies: ["Hugo", "Tailwind CSS", "Alpine.js"]
categories: ["Data Visualisation", "Data Management"]
tags: ["site vitrine", "refonte", "identité de marque"]
url: "https://atelier-dupont.example.com"
repo: ""
related: ["identite-visuelle-dupont"]
cover: "images/atelier-dupont-cover.jpg"
weight: 10
---

Corps de la fiche : contexte, objectifs, réalisation, résultat.
```

`content/en/projects/mon-projet.md` (même clés, contenu adapté, pas traduit
mot à mot) :

```yaml
---
title: "Website Redesign — Atelier Dupont"
date: 2026-03-12
draft: false
summary: >-
  Full redesign of the showcase website, migration to Hugo, and a visual
  identity aligned with the new brand guidelines.
client: "Atelier Dupont"
role: "Front-end development & integration"
technologies: ["Hugo", "Tailwind CSS", "Alpine.js"]
tags: ["showcase website", "redesign", "brand identity"]
url: "https://atelier-dupont.example.com"
repo: ""
related: ["dupont-visual-identity"]
cover: "images/atelier-dupont-cover.jpg"
weight: 10
---
```

## Cas 2 — page bundle avec assets locaux

```
content/fr/projets/mon-projet/
├── index.md
├── cover.jpg
└── screenshot-1.jpg
```

Dans `index.md`, référencer les images par chemin relatif :

```yaml
---
title: "..."
cover: "cover.jpg"
gallery: ["screenshot-1.jpg"]
---
```

## Points d'attention récurrents

- **Slugs de taxonomie** : si le site traduit les taxonomies (ex. `tags`
  en FR vs EN), vérifier que la correspondance FR ↔ EN est déclarée dans
  la config (souvent via `translationKey` en front matter, ou fichiers
  `i18n/`). Si `translationKey` est utilisé, l'ajouter systématiquement
  pour lier les deux versions de la page entre elles.
- **Dates** : respecter le format déjà en usage (`2026-03-12` vs
  `2026-03-12T09:00:00+01:00`).
- **`draft`** : ne jamais passer à `false` sans confirmation explicite si
  cela publie réellement le contenu.
- **`weight`** : s'il est utilisé pour l'ordre d'affichage du portfolio,
  vérifier la position logique du nouveau projet plutôt que de mettre une
  valeur arbitraire.
