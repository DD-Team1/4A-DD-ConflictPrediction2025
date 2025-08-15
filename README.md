# Conflict Prediction Project

*William Smith, Romain Jaffuel, Florian Grolleau 4A-DD 2025-2026*
**Sciences Po Saint-Germain-en-Laye, CY TECH**



## 📌 Description
Projet de prédiction des conflits à partir d'indicateurs politiques, économiques et sociaux.  
Objectif : créer un outil capable d'anticiper différents types de conflits (guerres civiles, conflits inter-étatiques) à partir de données fiables issues d'indices internationaux et de bases spécialisées (type API).

Le projet inclut :
- Collecte et intégration de données multi-sources (CSV, JSON, API)
- Analyse exploratoire et création de variables pertinentes, telles que des données géospatiales
- Développement d'un modèle de machine learning / deep learning (à déterminer)
- Visualisation géospatiale des résultats / Learning Curve / Table de Reporting
- Rapport en LaTeX
- Livraison potentielle sous forme d'application utilisable (CLI, .exe, Android, etc.)

---

## 📂 Structure du projet

---
├── data/ # CSV / JSON / données brutes
├── notebooks/ # Jupyter Notebooks d'exploration et de prototypage
├── src/ # Code source (ETL, modèles, utils)
├── reports/ # Documents, rapports LaTeX
├── scripts/ # Scripts utilitaires
└── README.md # Documentation du projet
---

## 📊 Sources de données

**Indices politiques et économiques :**
- Corruption Perceptions Index — Transparency International (1995-…)
- Democracy Index — Economist Intelligence Unit (2006-…)
- Economic Freedom Index — The Heritage Foundation (1995-…)
- Fragile States Index — The Fund for Peace (2005-…)
- Freedom in the World Index — Freedom House (1973-…)
- Global Peace Index — Institute for Economics & Peace (2007-…)
- Global Terrorism Index — Institute for Economics & Peace (2000-…)
- Human Freedom Index — Cato Institute & Fraser Institute (2000-…)

## 📚 Sources de données complémentaires

Afin d’enrichir le modèle et couvrir à la fois les causes structurelles et les déclencheurs conjoncturels des conflits, voici une liste de sources pertinentes :

| Domaine | Source | Lien | Format | Fréquence de mise à jour |
|---------|--------|------|--------|--------------------------|
| **Conflits & sécurité** | UCDP (Uppsala Conflict Data Program) | https://ucdp.uu.se/ | CSV | Annuel |
| | PRIO Conflict Data | https://www.prio.org/data/ | CSV | Annuel |
| | GDELT Project | https://www.gdeltproject.org/ | CSV / API | Quasi temps réel |
| | UNHCR Refugee Data | https://www.unhcr.org/refugee-statistics/ | CSV | Annuel |
| | Small Arms Survey | http://www.smallarmssurvey.org/ | PDF / CSV | Variable |
| **Économie & développement** | World Bank Open Data | https://data.worldbank.org/ | CSV / API | Variable |
| | IMF Data | https://www.imf.org/en/Data | CSV / API | Trimestriel / Annuel |
| | FAO Food Price Index | https://www.fao.org/worldfoodsituation/foodpricesindex | CSV | Mensuel |
| | OECD Statistics | https://stats.oecd.org/ | CSV / API | Variable |
| **Politique & société** | Polity IV Project | https://www.systemicpeace.org/polityproject.html | CSV | Irrégulier |
| | V-Dem (Varieties of Democracy) | https://v-dem.net/ | CSV | Annuel |
| | Political Terror Scale | https://www.politicalterrorscale.org/ | CSV | Annuel |
| | CIRI Human Rights Dataset | http://www.humanrightsdata.com/ | CSV | Annuel |
| **Environnement & climat** | EM-DAT (International Disaster Database) | https://www.emdat.be/ | CSV | Continu |
| | NASA Earth Observations | https://neo.gsfc.nasa.gov/ | GeoTIFF / CSV | Continu |
| | NOAA Climate Data | https://www.ncdc.noaa.gov/cdo-web/ | CSV / API | Continu |
| | Global Land Cover & Resource Data | https://www.usgs.gov/ | GeoTIFF / CSV | Variable |
| **Géospatial & démographie** | GeoNames | https://www.geonames.org/ | TXT / CSV | Continu |
| | UN Population Data | https://population.un.org/ | CSV | Annuel |
| | Gridded Population of the World (GPW) | https://sedac.ciesin.columbia.edu/data/collection/gpw-v4 | GeoTIFF / CSV | Variable |
| | OpenStreetMap (OSM) | https://www.openstreetmap.org/ | OSM / CSV | Continu |

---

## 🛠️ Stack technique

- **Langages** : Python (pandas, geopandas, scikit-learn, PyTorch/TensorFlow)
- **Bases de données** : PostgreSQL + PostGIS pour les données géospatiales
- **Visualisation** : matplotlib, plotly, folium, leaflet, kepler.gl, qgis etc
- **Gestion de versions** : Git (workflow branches par membre)
- **Documentation** : LaTeX, Markdown

---

## 🚀 Workflow Git

- `main` : branche stable
- `william/` : développement par William
- `romain/` : développement par Romain
- `florian/` : développement par Florian  
💡 Toute **pull request** doit être validée par un autre membre.

---

## 🗺️ Fonctionnalités prévues

- **ETL** pour unifier et nettoyer les datasets
- Indexation géospatiale des événements
- Modèle prédictif entraîné sur données historiques
- Interface simple (CLI, app, ou web)
- Visualisation des risques de conflit sur carte

---

## 🔄 Pipeline du projet

1. **Collecte des données**
   - Récupération des CSV/JSON depuis les sources identifiées (API, Kaggle, portails open data).
   - Stockage brut dans `data/raw/`.

2. **Nettoyage & intégration**
   - Harmonisation des formats (dates, pays, unités).
   - Jointure des datasets par codes normalisés (ISO 3166-1 alpha-3).
   - Gestion des valeurs manquantes et outliers.

3. **Enrichissement**
   - Calcul d’indicateurs dérivés (ratios, moyennes mobiles, variations annuelles).
   - Ajout de variables géospatiales (indexation PostGIS, shapefiles, coordonnées).
   - Fusion des données structurelles et conjoncturelles.

4. **Analyse exploratoire (EDA)**
   - Visualisations statistiques et cartes.
   - Corrélations entre indicateurs et historique des conflits.

5. **Modélisation**
   - Séparation entraînement/test.
   - Sélection et entraînement du modèle (ML/DL).
   - Évaluation (accuracy, F1, AUC selon le cas d’usage).

6. **Prédiction & visualisation**
   - Génération de cartes de risque.
   - Export des résultats (CSV, API interne).

7. **Déploiement**
   - Intégration dans une app CLI / web ou export en `.exe`/Android.
   - Documentation et rapport LaTeX.

---
