---
name: hugo-portfolio-content
description: >-
  À utiliser pour ajouter, compléter ou améliorer des fiches de projet sur
  un portfolio Hugo bilingue (français/anglais) à partir de sources comme
  un cahier des charges, du code source ou des emails, en respectant le
  front matter existant et en assurant le maillage interne (tags,
  taxonomies, projets liés, menus).
license: MIT
compatibility: opencode
metadata:
  audience: agent-hugo-portfolio
  langues: fr,en
---

# Gestion de contenu — portfolio Hugo bilingue

Cette skill décrit la méthode à suivre pour intervenir sur un portfolio Hugo
**existant** : ajouter un projet, compléter une fiche, ou améliorer la
cohérence et le maillage du site, en français et en anglais.

## 1. Découvrir la structure du site avant d'écrire quoi que ce soit

Ne jamais supposer une structure standard : chaque portfolio Hugo a ses
propres conventions. Toujours vérifier :

- **Configuration** : `hugo.toml`, `config.toml`, ou `config/_default/*.toml`
  → repérer `defaultContentLanguage`, la liste `[languages]`, et si
  `contentDir` est défini par langue.
- **Organisation des langues dans `content/`**, deux cas fréquents :
  - dossiers séparés : `content/fr/projets/...` et `content/en/projects/...`
  - suffixes de fichier : `mon-projet.fr.md` / `mon-projet.en.md` dans le
    même dossier.
- **Archétype** : `archetypes/projet.md` ou équivalent — c'est le schéma de
  front matter de référence. À défaut d'archétype, ouvrir 2-3 fiches
  projet existantes et en déduire le schéma commun.
- **Taxonomies** définies dans la config (`tags`, `categories`,
  `technologies`, `clients`...) et la façon dont elles sont traduites
  (mêmes clés ou clés traduites par langue).
- **Maillage existant** : shortcode "projets liés"
  (ex. `{{< related-projects >}}`), section générée automatiquement par
  taxonomie, ou liens manuels en front matter (`related: [...]`).
- **Média** : page bundles (`content/.../mon-projet/index.md` + images à
  côté) vs dossier `static/`/`assets/` centralisé.

Commandes utiles :

```bash
# Vue d'ensemble
find . -maxdepth 2 -iname "*.toml" -o -iname "*.yaml" -o -iname "*.yml" | grep -i hugo
ls content/
cat archetypes/*.md 2>/dev/null
grep -RIn "related" layouts/ content/ --include="*.md" --include="*.html" | head -30
```

## 2. Extraire l'information des sources fournies

Les sources typiques : cahier des charges, code source du projet livré,
échanges email avec le client, notes de brief oral.

Pour chaque projet, chercher à établir :

| Champ | Où le trouver généralement |
|---|---|
| Nom du client / projet | cahier des charges, objet des emails |
| Contexte / problématique | intro du cahier des charges |
| Objectifs | cahier des charges, section "objectifs" |
| Rôle exact de l'auteur du portfolio | emails, code (commits, contributions) |
| Stack technique | code source, `package.json`, `requirements.txt`, README |
| Durée / dates | emails, cahier des charges, historique git |
| Résultats / impact | emails de clôture, retours client |
| Lien live / repo | emails, README |

**Ne jamais inventer** une donnée manquante (client, date, chiffre) : la
signaler comme manquante et la demander à l'utilisateur.

## 3. Rédiger le contenu

1. Rédiger d'abord la version française : contexte → objectifs →
   réalisation (stack, rôle) → résultat.
2. Produire une version anglaise **naturelle**, pas une traduction littérale
   — même structure et même niveau de détail, mais formulée comme un
   locuteur anglophone rédigerait la même fiche.
3. Garder un ton homogène avec le reste du portfolio (reprendre le
   registre observé dans les fiches existantes : plutôt formel/technique,
   ou plutôt narratif/personnel).
4. Réutiliser exactement le même vocabulaire de tags/technologies déjà
   utilisé ailleurs sur le site (voir taxonomies existantes) pour ne pas
   fragmenter les pages de filtrage.

## 4. Respecter le front matter existant

Ne pas ajouter ou renommer de clés à la légère. S'aligner sur l'archétype
ou les fiches existantes. Exemple générique (à adapter au schéma réel du
site) :

```yaml
---
title: "Nom du projet"
date: 2026-03-12
draft: false
summary: "Résumé en une phrase, utilisé sur la page de listing."
client: "Nom du client"
role: "Développement front-end"
technologies: ["Hugo", "Go", "Tailwind CSS"]
tags: ["site vitrine", "identité de marque"]
url: "https://exemple.com"
related: ["autre-projet-1", "autre-projet-2"]
weight: 10
---
```

Voir `references/frontmatter-template.md` pour un gabarit plus détaillé et
des variantes courantes (page bundle vs fichier unique, dates, images).

## 5. Assurer le maillage interne

- Ajouter le nouveau projet aux taxonomies pertinentes (mêmes valeurs des
  deux côtés FR/EN si le site les traduit).
- Mettre à jour la liste des "projets liés" sur les fiches concernées (le
  lien doit être réciproque quand c'est pertinent : si A référence B, B
  référence souvent A aussi).
- Vérifier que le nouveau projet apparaît bien dans les pages de listing
  (section, menu) sans modification manuelle nécessaire — sinon, mettre à
  jour le menu ou la page d'index correspondante.
- Utiliser les shortcodes internes du site (`{{< ref >}}` / `{{< relref >}}`)
  pour tout lien vers une autre page du site plutôt que des chemins en dur.

## 6. Vérifier la parité FR/EN

Checklist avant de conclure :

- [ ] La fiche existe dans les deux langues avec le même niveau de détail.
- [ ] Les taxonomies (tags, technologies) sont cohérentes entre les deux
      versions.
- [ ] Les liens "projets liés" existent des deux côtés.
- [ ] Les images/assets sont bien référencés dans les deux versions
      (chemins corrects selon la structure page bundle ou non).
- [ ] Le format de date et les clés de front matter sont identiques à celles
      des fiches existantes.

## 7. Valider

Si un binaire Hugo est disponible dans l'environnement :

```bash
hugo --minify --gc 2>&1 | tail -40
```

Signaler toute erreur de build, tout lien cassé, ou toute taxonomie
orpheline (créée mais qui ne correspond à aucune page de taxonomie stylée
côté layout).

## 8. Résumer le travail effectué

Toujours terminer par un résumé court : fichiers créés/modifiés (chemins
complets), langues couvertes, informations encore manquantes à demander à
l'utilisateur pour compléter la fiche.
