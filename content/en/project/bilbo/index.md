---
title: Indexer toute l'information environnementale sur une grille vectorielle H3
summary: 

tags:
  - Science
  - dataviz
  - geoprocessing

date: 2022-01-01

authors:
- "Hugo Roussaffa"
- "Developpeur et administrateur"
---

## Description du projet 

Notre projet consiste à créer un système d'information décisionnel basé sur des données géographiques et environnementales. Il à pour vocation à exploiter des données sur les incendies, l'occupation des sols, les limites administratives et des indicateurs de sécheresse et de pollution lumineuse etc. Les données seront indexées sur une grille H3 pour une analyse spatiale fine. Les traitements seront réalisés à l'aide d'algorithmes Python et les datamarts seront générés à l'aide de DBT, un générateur SQL basé sur les templates Jinja.

Notre projet se distingue des projets de business intelligence standard par sa capacité à intégrer des données géographiques et environnementales, à effectuer une analyse spatiale fine grâce à l'indexation H3 et à être flexible pour répondre aux besoins spécifiques.

H3 est un système d'indexation spatiale hexagonale développé par Uber, qui permet de diviser la surface de la Terre en une grille de hexagones de tailles variables. Il est particulièrement utile pour l'analyse spatiale fine des données, car il permet de stocker les données à différents niveaux de granularité.

Les avantages d'utiliser H3 par rapport à un système d'information géographique standard sont nombreux:

- Il permet d'adapter la finesse de l'analyse spatiale des données, car il permet de stocker les données à différents niveaux de granularité spatiale.
-  Il est également plus efficace en termes de stockage de données, car il permet de stocker des données de différentes tailles dans une seule grille.
-  Il est facilement utilisable avec des outils de visualisation tels que des tableaux de bord géographiques, permettant une meilleure compréhension des données pour les utilisateurs.
	

En utilisant H3, nous pouvons mieux comprendre les risques liés aux incendies, la sécheresse et la pollution lumineuse. L'indexation H3 permet une analyse spatiale fine des données, cela signifie que nous pouvons identifier les zones les plus touchées par la sécheresse ou la pollution lumineuse avec une précision accrue.

DBT est un outil clé pour notre projet car il nous permet de générer des datamarts à partir de nos données. Il utilise des templates Jinja pour générer des requêtes SQL qui peuvent être utilisées pour créer des tableaux de bord géographiques et des rapports automatisés. Cela permet une meilleure compréhension des données pour les utilisateurs et une prise de décision plus efficace.

En résumé, notre projet est basé sur l'utilisation de données géographiques et environnementales, l'analyse spatiale fine grâce à l'indexation H3 et la flexibilité pour répondre aux besoins spécifiques en utilisant DBT pour générer des datamarts et des tableaux de bord géographiques et des rapports automatisés.


## Compétences exploitées et livrables 
Python
Data Visualisation
Data Management

## Galerie d’images

{{< gallery >}}
{{< /gallery >}}
