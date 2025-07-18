# DETECTION AUTOMATIQUE DU TRAIT DE CÔTE DE LA RÉUNION SUR UNE SÉRIE TEMPORELLE D'IMAGES SENTINEL-2 DE 2015 À 2025

<p align="center">
  <img src="https://raw.githubusercontent.com/Nathan17reunion/PyDSAS_Reunion_Island/main/images/Sans%20titre.jpg" alt="Logo 4" width="180"/>
  <img src="https://github.com/Nathan17reunion/PyDSAS_Reunion_Island/blob/main/images/univ_tana.png" alt="Logo 5" width="90"/>
</p>

<p align="center">
  <img src="https://github.com/Nathan17reunion/PyDSAS_Reunion_Island/blob/main/images/univ_reunion.png" alt="Logo 5" width="180"/>
  <img src="https://github.com/Nathan17reunion/PyDSAS_Reunion_Island/blob/main/images/fac_sciences_univ_reunion.png" alt="Logo 6" width="180"/>
  <img src="https://raw.githubusercontent.com/Nathan17reunion/PyDSAS_Reunion_Island/main/images/images.jpg" alt="Logo 6" width="60"/>
  <img src="https://raw.githubusercontent.com/Nathan17reunion/PyDSAS_Reunion_Island/main/images/Sans%20titre-1.png" alt="Logo 6" width="180"/>
</p>

<p align="center">***TRAITEMENT AVEC L'OUTIL SAET (Shoreline Automated and Extraction Tool)***</p>

<p align="center">***👋 HELLO & WELCOME!***</p>

![Bannière LinkedIn](https://raw.githubusercontent.com/Nathan17reunion/PyDSAS_Reunion_Island/main/images/Banni%C3%A8re%20LinkedIn%20professionnel%20moderne%20marketing%20orange%20noir.png)

<p align="center">**Jonathan Rayan Rower MITANTSOA NY HAJA HARILALA**</p>

<p align="center"> 🎓 🌍 🛰️ 🌊 🏖️ 🐍 💧 💻  🌐 📄 📚 🎯 🤝 </p>

<p align="center">AUTOMATED SHORELINE DETECTION OF REUNION ISLAND USING A TEMPORAL SERIES OF SENTINE-2 IMAGES FROM 2015 TO 2025</p>

## Introduction

Ce projet vise à documenter, traiter et analyser la dynamique multi-temporelle du trait de côte à La Réunion (2015-2025) à partir d’images Sentinel-2 et d’outils open source. L’ensemble des étapes s’inscrit dans une démarche scientifique reproductible et robuste : sélection rigoureuse des données, validation qualitative et quantitative, découpage thématique, extraction automatisée et analyse spatiale, le tout documenté pour être partagé publiquement sur GitHub.

---

## Démarche Synthétique

### 1. Sélection & Prétraitement des Données Satellite

- **Critère de couverture nuageuse** : [**max 30 %**]([https://colab.research.google.com/drive/1eaZ2gPq6NLtHNE8UdS0oXeqNdcGytrdg#scrollTo=qTDxCiLDXIkh](https://colab.research.google.com/drive/129-k3fK3jIHa9m0XrzR0xZ6waJ_wKdMx)) pour chaque année, afin d’assurer un échantillonnage homogène.
- **Téléchargement automatisé** : scripts pour recenser toutes les scènes et contrôler la concordance entre le nombre d’images téléchargées et traitées.
- **Gestion annuelle** : les années 2015-2016-2017 sont fusionnées en raison du faible nombre d’images en 2015.

### 2. Extraction et Correction des Traits de Côte

- **Extraction automatisée** du trait de côte pour chaque scène via [SAET](https://github.com/jpalomav/SAET_master) avec masquage des nuages.
- **Correction post-traitement** : suppression manuelle des traits aberrants, contrôle visuel et scripté pour valider l’alignement sur la High Water Line (HWL).
- **Structuration par cellule hydro-sédimentaire** et sites d’étude, permettant une analyse multi-échelle.

### 3. Association des Données Complémentaires

- **Dates précises** extraites de chaque image, associées :
  - aux données marégraphiques [**REFMAR**](https://data.shom.fr/donnees/refmar/download#001=eyJjIjpbLTY2MjgwNyw1ODIyOTI3XSwieiI6NiwiciI6MCwibCI6W3sidHlwZSI6IklOVEVSTkFMX0xBWUVSIiwiaWRlbnRpZmllciI6IkZEQ19HRUJDT19QWVItUE5HXzM4NTdfV01UUyIsIm9wYWNpdHkiOjEsInZpc2liaWxpdHkiOnRydWV9XX0=),
  - et aux données de houle [**CANDHIS**](https://candhis.cerema.fr/_public_/campagne.php?Y2FtcD05NzQwMw==) pour valider/stabiliser les résultats.

### 4. Fusion, Découpage et Analyse Dynamique

- **Fusion des traits de côte** annuels pour délimiter la mobilité sur 2015-2025.
- **Extraction par cellule et site d’étude** pour la production de statistiques fines et cartes thématiques.
- **Application du programme PyDSAS** (écrit pour Linux) afin de :
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

- [Script de sélection Sentinel-2](https://github.com/jpalomav/SAET_master/blob/main/sp_searching_run.py)
- [Module SAET (extraction)](https://github.com/jpalomav/SAET_master/blob/main/sp_processing_run.py)
- [Correction & fusion des traits de côte](https://github.com/Nathan17reunion/Extraction_Shoreline_By_SAET_jrr/blob/main/Correction_TDC.py)
- [PyDSAS (analyse spatiale)](https://github.com/Nathan17reunion/PyDSAS_Reunion_Island/blob/main/PyDSAS.py)

---

## Conseils pour lecture/enrichissement du projet

- **Reproductibilité :** Chaque script possède un mode automatique et manuel, conçu pour l’archivage et la transmission scientifique.
- **Visualisation :** Cartes générées sous QGIS, prêtes à l’usage pour publication ou valorisation grand public.
- **Contribution** : Voir le guide de contribution dans `/doc`.

---

> Ce dépôt a pour vocation de servir de base sur la dynamique littorale de La Réunion, et toute remarque/collaboration est bienvenue.

Nous accueillons chaleureusement toute contribution, amélioration ou suggestion pour enrichir ce projet et ses analyses.   
Pour faciliter votre implication, voici des ressources clés liées à ce travail :

- **Rédaction en cours du rapport de stage** : [Document Google Docs collaboratif](https://docs.google.com/document/d/190akoMxUDB6AHJ9KRo8jI1dy8AUbmUYjJdoy6uzg9Jw/edit?tab=t.0)  
  (Vous êtes invité(e) à consulter, commenter ou proposer des modifications)

- **Version finale du rapport** (mis en forme professionnelle avec LaTeX) : [Projet Overleaf](https://www.overleaf.com/project/685e25af1c60a82c10462f55)  
  (Accès en lecture, n’hésitez pas à faire des retours pour enrichir le contenu)

---

Votre expertise, idées ou contributions techniques seront très appréciées pour renforcer la qualité, l’ergonomie et l’impact de cette étude.  
Que vous soyez spécialiste en géomatique, en traitement d’images satellitaires, en modélisation côtière ou simplement curieux, votre aide est bienvenue !

N’hésitez pas à ouvrir une issue ou proposer une pull request. Ensemble, nous pouvons faire avancer la compréhension de la dynamique littorale à La Réunion.

---

![Illustration littorale moderne](https://github.com/Nathan17reunion/Extraction_Shoreline_By_SAET_jrr/blob/main/Beach_code.png)

---

<p align="center">***Thank you for visiting my git!***</p>

> ### **Contact**
> 🏠 Cité Internationale   
> 97490 Saint-Denis La Réunion (France)  
> ✉️ [jrayan.mitantsoanyhaja@gmail.com](mailto:jrayan.mitantsoanyhaja@gmail.com)
>   
> 📞 +262 693 81 23 59  
> 
>  <a href="https://www.facebook.com/profile.php?id=61571394063716">
>   <img src="https://img.freepik.com/psd-gratuit/conception-du-logo-medias-sociaux_23-2151296987.jpg?semt=ais_hybrid&w=740" alt="Facebook" width="28" />
>   Jonathan Rayan Rower
> </a>

<p align="center">🌍 I am passionate about Earth sciences and tropical environments, with a special interest in:
🛰️ remote sensing, 🚜 agriculture, 🌋 seismology, 🌊 oceanography, 🏖️ beaches and coral reefs, 🏝️ coastal geomorphology, ⚠️ natural hazards, 🤝 volunteering, 🐍 Python programming, 📊 data analysis with R, 💧 hydrology, and much more!</p>
