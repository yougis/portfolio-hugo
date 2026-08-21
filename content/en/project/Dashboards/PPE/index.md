---
title: ESRI Dashboard / Water management
summary: Building a dashboard with ArcGIS Online about drinking water management in New Caledonia

tags:
  - Dashboard
date: 2022-01-01

authors:
- "Hugo Roussaffa"
- "Developpeur et administrateur"
---

### 📝 Drinking water resource monitoring project in New Caledonia

**Context:**
As part of my role within an environmental association, I was responsible for the information systems and geomatics projects division. I was given a simple mission: to design a **territorial dashboard for monitoring the drinking water resource** across New Caledonia, for a public institution (DAVAR).

**Objectives:**

* Identify, formalize and produce around ten relevant **geographic indicators** for monitoring the resource.
* Build a **sustainable and reproducible technical solution**, scalable in the long term.
* Automate the processing and aggregation of vector geographic data (provided by the contracting authority).

**Role and actions:**

* Design and **development of a scripted geospatial processing framework** (Python/GDAL, YAML), with geometric intersection, filtering, aggregation steps, etc.
* Structuring data according to a **bronze / silver / gold** logic (Data Lakehouse model adapted to geographic data).
* Setting up a **data catalog** and standardized models to facilitate multi-scale analysis.
* Explicit refusal of manual processing (QGIS-type), in favor of an **industrialized, reproducible and documented** system.
* Constant dialogue with public partners to refine indicators and anticipate future uses, applying an agile approach.

**Results and impacts:**

* Successful delivery of the first version of the dashboard and indicators.
* **Adoption of the framework as the technical foundation for all future environmental projects** of the observatory.
* Significant time savings in subsequent projects and greater reliability of processing.
* Building a **culture of automated and maintainable processing** within the team.

**Lessons learned:**

* The importance of imposing a **clear and robust technical vision**, even when it diverges from existing practices.
* **Training and pedagogy** are key factors in getting teams to adopt more advanced technical tools.
* A well-considered methodological choice can generate **a lasting leverage effect** at the scale of an organization.


## Skills used

{{< skills-grid >}}
- name: Data Visualisation
  icon: fas fa-chart-pie
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
{{< /skills-grid >}}


## Technologies used

{{< techno-cards >}}
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
{{< /techno-cards >}}


{{< python-libs-list>}}
- name: Pandas
  description: Library for data manipulation and analysis.
- name: rasterio
  description: Reading and writing geospatial raster data.
- name: geopandas
  description: Pandas extension for working with geospatial data.
- name: intake
  description: Data discovery, management and access.
- name: Dask
  description: Parallel processing of large-scale data.
{{< /python-libs-list>}}