---
title: "Scraping de point d'interêt (POI)"
subtitle: Extraction et structuration des données géospatiales
date: "2024-02-14T10:00:00+01:00"
tags: ["gis", "scraping", "osm", "google maps", "postgis"]
categories: ["scraping"]
summary: "Extraire et structurer des points d’intérêt issus d’openstreetmap (OSM) et google maps"
draft: true

authors:
- "Hugo Roussaffa"
- "Developpeur"
---

**Objectif** : démontrer comment extraire des POI d'openstreetmap et google maps, nettoyer les données, les stocker dans postgis, et les visualiser de manière interactive.


## Les points clés :

- scraping et extraction : utilisation de l'overpass api (OSM) et de Google Places API pour récupérer des données.
- gestion et traitement : manipulation avec python, pandas et geopandas.
- stockage spatial : insertion dans postgis via psycopg2.
- visualisation interactive : carte simple réalisée avec folium.
- environnement moderne : gestion des dépendances avec poetry et documentation via quarto.

Le rapport complet et interactif, généré avec quarto, détaille chaque étape et présente les résultats. pour en savoir plus, consultez le rapport interactif détaillé.

[Consulter le rapport interactif complet](https://yougis.github.io/scraping-poi-osm-googlemap/scraping_osm.html) 



<iframe src="https://yougis.github.io/scraping-poi-osm-googlemap/scraping_osm.html#fig-map-osm-hospitals" width="100%" height="600px"></iframe>

## Exemple de cas d’usage addressés :

- L’analyse de la répartition des commerces et des services d'une ville ou un pays,
- L’étude de la concurrence et des tendances du marché via des données spatialisées.

## Ce que vous allez découvrir :
- **Comment je scrapes des POI** avec l'Overpass API d'OSM et la Google Places API.
- **Je vais structurer et stocker les données** dans des fichiers CSV, Excel geoJson et même dans une base PostGIS 
- **Vous permettre de visualiser mes résultats** sur une carte interactive grâce à Folium.
- **Comment on gére tout cela d'un environnement de developpement à la production** avec Poetry, tester et documenter le tout.


## Mes compétences en action

Plusieurs compétences techniques sont déployées dans ce projet :

1. **Scraping et extraction de données**
   - **Overpass API (OSM)** : Extraire des données géospatiales en interrogeant l'API d'OpenStreetMap.
   - **Google Places API** : Récupérer des informations complémentaires sur les POI en interrogeant l'API de google map.

2. **Gestion et traitement de données**
   - **Python & Requests** : Rédiger des scripts efficaces pour interroger les API.
   - **Pandas & GeoPandas** : Manipuler et nettoyer les données obtenues.
   - **JSON** : Structurer les réponses API de façon lisible et exploitable.

3. **Stockage dans une base de données**
   - **PostGIS** : Créer une base de données spatiale pour stocker et interroger les POI.
   - **SQL & Psycopg2** : Insérer et gérer les données via des scripts automatisés.

4. **Visualisation interactive**
   - **Folium** : Afficher les POI sur une carte interactive pour une visualisation immédiate.
   - **Deck.gl (optionnel)** : Explorer des représentations en 3D pour les plus curieux.

5. **Gestion de l'environnement et documentation**
   - **Poetry** : Simplifier la gestion des dépendances et la reproductibilité de l'environnement.
   - **Quarto** : Générer des rapports interactifs et bien documentés qui détaillent chaque étape du projet.

## La démarche en 5 étapes

1. **Extraction des POI**  
   On commence par lancer un script Python pour interroger l’Overpass API. Le résultat est stocké dans un fichier JSON, qui contient une liste de POI (par exemple, des hôpitaux à Paris).

2. **Nettoyage et validation**  
   Un coup d'œil dans le JSON pour s'assurer que les données sont complètes et bien structurées. On élimine les doublons ou les données incomplètes.

3. **Insertion dans PostGIS**  
   Les données validées sont insérées dans une base PostGIS, ce qui permet d’effectuer des analyses spatiales avancées par la suite.

4. **Visualisation interactive**  
   Grâce à Folium, les POI sont affichés sur une carte interactive. Vous pouvez zoomer, cliquer et explorer pour voir comment les données se répartissent géographiquement.

5. **Documentation technique via Quarto**  
   L’ensemble du processus est documenté dans un notebook Quarto qui génère un rapport interactif. Ce rapport est accessible directement depuis mon portfolio et permet aux curieux de reproduire l’expérience.

## Conclusion et perspectives

Ce projet démontre que le scraping de POI n’est pas qu’une simple extraction de données, c’est une démarche complète qui allie rigueur technique et créativité. Grâce à une gestion moderne avec Poetry et à une documentation soignée via Quarto, il est aisé de reprendre ce projet, de l'adapter à d'autres territoires (comme l'Australie ou les Philippines) et d'en exploiter tout le potentiel pour des analyses SIG poussées.

Envie d’en savoir plus ? Consultez le rapport interactif détaillé ci-dessous et n’hésitez pas à me laisser vos retours ou questions !