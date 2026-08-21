---
title: Helper d'annotations QGIS
summary: Plugin QGIS pour l'intégration des recollements au standard GEOcalédonien
tags:
  - QGIS
  - Géoreférencement
  - RECOLLEMENTS
  - AEP
date: 2025-01-01
authors:
- "Hugo Roussaffa"
- "Insight NC"
---

## Description du projet

Le plugin **Annotation AEP Helper** a été développé dans le cadre de la préparation de la présentation **GIS DAY 2025**. Il vise à faciliter l'intégration des recollements (annotations géométriques) au standard GEOcalédonien pour les projets d'observation de la Terre et d'aménagement du territoire.

## Objectifs

- Automatiser la création de recollements géométriques conformes au standard GEOcalédonien
- Réduire le temps de préparation des données d'observation de la Terre
- Assurer la compatibilité des annotations avec les systèmes d'information géographique locaux
- Favoriser la réutilisabilité des données d'annotations entre projets

## Fonctionnalités

- Importation de fichiers d'annotations existants
- Conversion automatique aux formats de recollements GEOcalédonien
- Validation géographique des recollements par rapport aux standards locaux
- Export vers les formats courants (Shapefile, GeoJSON, GeoPackage)
- Interface utilisateur intuitive dans l'interface QGIS

## Technologies utilisées

- **QGIS** : interface et traitement des géométries
- **Python** : développement du plugin et logique de géoréférencement
- **Standard GEOcalédonien** : format et contraintes spécifiques
- **AEP** : activités d'observation de la Terre

## Galerie d'images

![Capture interface plugin](annotation_aep_helper_screenshot1.png)
![Capture fenêtre des recollements](annotation_aep_helper_screenshot2.png)

## Installation

```bash
# Via le dépôt GitHub
git clone https://github.com/yougis/annotation_AEP_helper

# Ou installation manuelle
# Instructions détaillées dans le README du dépôt
```

## Liens utiles

- **Dépôt source** : [https://github.com/yougis/annotation_AEP_helper](https://github.com/yougis/annotation_AEP_helper)
- **Présentation GIS DAY 2025** : fichier disponible dans l'espace de travail partagé
- **Documentation technique** : README inclus dans le dépôt
---