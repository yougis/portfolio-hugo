---
title: Dashboard ESRI / Gestion de l'eau
summary: Réalisation d'un dashboard avec Arcgis Online à propos de la gestion de l'eau potable en Nouvelle-Calédonie

tags:
  - Dashboard
date: 2022-01-01

authors:
- "Hugo Roussaffa"
- "Developpeur et administrateur"
---

### 📝 Projet de suivi de la ressource en eau potable en Nouvelle-Calédonie


**Contexte :**
Dans le cadre de mes fonctions au sein d’une association environnementale, j’ai assuré la responsabilité du pôle système d’information et projets géomatique. Une mission simple m'a été confié pour concevoir un **tableau de bord territorial de suivi de la ressource en eau potable** à l’échelle de la Nouvelle-Calédonie, à destination d'une institution publique (DAVAR).

**Objectifs :**

* Identifier, formaliser et produire une dizaine d’**indicateurs géographiques** pertinents pour le suivi de la ressource.
* Construire une **solution technique pérenne et reproductible**, évolutive à long terme.
* Automatiser le traitement et l’agrégation des données géographiques vectorielles (fournies par le commanditaire).

**Rôle et actions :**

* Conception et **développement d’un framework de traitements géospatiaux scriptés** (Python/GDAL, YAML), avec des étapes de croisement géométrique, filtrage, agrégation, etc.
* Structuration des données selon une logique **bronze / argent / or** (modèle de Data Lakehouse adapté aux données géographiques).
* Mise en place d’un **catalogue de données** et de modèles standardisés pour faciliter l’analyse multi-échelles.
* Refus explicite des traitements manuels (type QGIS), au profit d’un système **industrialisé, reproductible et documenté**.
* Dialogue constant avec les partenaires publics pour affiner les indicateurs et anticiper les usages futurs, applicant ainsi une approche agile.

**Résultats et impacts :**

* Livraison réussie de la première version du tableau de bord et des indicateurs.
* **Adoption du framework comme socle technique pour l’ensemble des projets environnementaux** future de l’observatoire.
* Gain de temps significatif dans les projets ultérieurs et meilleure fiabilité des traitements.
* Structuration d’une **culture de traitement automatisé et maintenable** au sein de l’équipe.

**Enseignements :**

* L’importance d’imposer une **vision technique claire et robuste**, même lorsqu’elle diverge des pratiques en place.
* La **pédagogie** et la formation est un facteur clé pour faire adhérer les équipes à des outils techniques plus avancés.
* Un choix méthodologique assumé peut générer **un effet levier durable** à l’échelle d’une organisation.


## Compétences exploitées

{{< skills >}}
- name: Data Visualisation
  icon: fas fa-chart-pie # Exemple Font Awesome pour graphique
- name: Data Management
  icon: fas fa-database
- name: Python Development
  icon: fab fa-python
- name: Data Automation
  icon: fas fa-robot
- name: Data Lakehouse
  icon: fas fa-water
- name: Data Processing
  icon: fas fa-cogs
- name: Data Analysis
  icon: fas fa-search
- name: Data Engineering
  icon: fas fa-wrench
{{< /skills >}}


## Technologies utilisées

{{< technologies >}}
- name: Python
  icon: fab fa-python
- name: GDAL
  icon: fas fa-map-marked-alt
- name: YAML
  icon: fas fa-file-alt
- name: DBT
  icon: fas fa-server
- name: ArcGIS Online
  icon: fas fa-cloud
- name: ArcGIS
  icon: fas fa-globe-americas
{{< /technologies >}}


{{< pylib>}}
Pandas
rasterio
geopandas
intake
Dask
{{< /pylib>}}


