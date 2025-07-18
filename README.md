# Analyse de la Dynamique Côtière à La Réunion (2015-2025)

![Illustration littorale moderne]([https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=800&q=80](https://github.com/Nathan17reunion/Extraction_Shoreline_By_SAET_jrr/blob/main/Beach_code.png))

## Introduction

Ce projet vise à documenter, traiter et analyser la dynamique multi-temporelle du trait de côte à La Réunion (2015-2025) à partir d’images Sentinel-2 et d’outils open source. L’ensemble des étapes s’inscrit dans une démarche scientifique reproductible et robuste : sélection rigoureuse des données, validation qualitative et quantitative, découpage thématique, extraction automatisée et analyse spatiale, le tout documenté pour être partagé publiquement sur GitHub.

---

## Démarche Synthétique

### 1. Sélection & Prétraitement des Données Satellite

- **Critère de couverture nuageuse** : max 30 % pour chaque année, afin d’assurer un échantillonnage homogène.
- **Téléchargement automatisé** : scripts pour recenser toutes les scènes et contrôler la concordance entre le nombre d’images téléchargées et traitées.
- **Gestion annuelle** : les années 2015-2016-2017 sont fusionnées en raison du faible nombre d’images en 2015.

### 2. Extraction et Correction des Traits de Côte

- **Extraction automatisée** du trait de côte pour chaque scène via SAET avec masquage des nuages.
- **Correction post-traitement** : suppression manuelle des traits aberrants, contrôle visuel et scripté pour valider l’alignement sur la High Water Line (HWL).
- **Structuration par cellule hydro-sédimentaire** et sites d’étude, permettant une analyse multi-échelle.

### 3. Association des Données Complémentaires

- **Dates précises** extraites de chaque image, associées :
  - aux données marégraphiques REFMAR,
  - et aux données de houle CANDHIS pour valider/stabiliser les résultats.

### 4. Fusion, Découpage et Analyse Dynamique

- **Fusion des traits de côte** annuels pour délimiter la mobilité sur 2015-2025.
- **Extraction par cellule et site d’étude** pour la production de statistiques fines et cartes thématiques.
- **Application de l’outil PyDSAS** (écrit pour Linux) afin de :
  - générer une baseline automatique,
  - calculer LRR, EPR, WLR, NSM, SCE,
  - exporter CSV et shapefiles pour cartographie/QGIS.
---

## Analyse Scientifique Structurée

### Analyse globale 2015-2025

- Tendances d’érosion/accrétion mesurées et cartographiées à l’échelle de l’île.  
- Prise en compte du biais engendré par la couverture nuageuse et les limites des outils de télédétection.

### Mobilité saisonnière

- **Saison cyclonique (nov-avr)** : dynamique plus marquée, impact des événements extrêmes.
- **Saison australe (mai-oct)** : évolution plus lente ou accrétion.

### Tendances pluriannuelles

- Calcul de moyennes et de tendances sur 8 périodes distinctes.
- Détection d’accélérations/décélérations ou d’évolutions atypiques en croisant avec les forçages (houle, marées).

---

## Ressources et Documentation

- [Script de sélection Sentinel-2](lien_script_selection)
- [Module SAET (extraction)](lien_saet)
- [Correction & fusion des traits de côte](lien_correction)
- [PyDSAS (analyse spatiale)](lien_pydsas)

---

## Structure du Dépôt GitHub


---

## Conseils pour lecture/enrichissement du projet

- **Reproductibilité :** Chaque script possède un mode automatique et manuel, conçu pour l’archivage et la transmission scientifique.
- **Visualisation :** Cartes générées sous QGIS, prêtes à l’usage pour publication ou valorisation grand public.
- **Contribution** : Voir le guide de contribution dans `/doc`.

---

> Ce dépôt a pour vocation de servir de base à d’autres analyses littorales à La Réunion ou dans l’Océan Indien, et toute remarque/collaboration est bienvenue.


---

*Merci et bonne exploration !*
