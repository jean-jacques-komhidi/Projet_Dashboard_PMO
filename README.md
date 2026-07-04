# Dashboard PMO — Pilotage des Projets IT & Marketing

**Tableau de Bord Décisionnel Power BI**

Tableau de bord Business Intelligence interactif conçu pour le Project Management Office (PMO) d'une entreprise internationale de produits de grande consommation. Il permet de suivre, analyser et piloter la performance de **247 projets** IT et Marketing répartis sur **4 régions géographiques**, avec détection automatique des projets en alerte.

[![Power BI](https://img.shields.io/badge/Power_BI-Desktop-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://www.microsoft.com/fr-fr/power-platform/products/power-bi/desktop)
[![DAX](https://img.shields.io/badge/DAX-Mesures-01B8AA?style=flat-square)]()
[![Power Query](https://img.shields.io/badge/Power_Query-M-6C2585?style=flat-square)]()
[![Azure Maps](https://img.shields.io/badge/Azure_Maps-Géospatial-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)](https://azure.microsoft.com/products/azure-maps/)
[![Projets](https://img.shields.io/badge/Projets-247-success?style=flat-square)]()
[![License](https://img.shields.io/badge/License-Academic-lightgrey?style=flat-square)]()

---

## Table des matières

- [Contexte](#contexte)
- [Objectifs](#objectifs)
- [Indicateurs clés (KPI)](#indicateurs-clés-kpi)
- [Périmètre des données](#périmètre-des-données)
- [Stack technique](#stack-technique)
- [Architecture du dashboard](#architecture-du-dashboard)
- [Fonctionnalités](#fonctionnalités)
- [Modèle de données](#modèle-de-données)
- [Installation](#installation)
- [Aperçu](#aperçu)
- [Compétences démontrées](#compétences-démontrées)
- [Livrables](#livrables)
- [Auteur](#auteur)

---

## Contexte

| Élément | Détail |
|---------|--------|
| Nature | Projet Business Intelligence — tableau de bord décisionnel |
| Secteur | Produits de grande consommation (entreprise internationale) |
| Commanditaire | Project Management Office (PMO) |
| Périmètre | 247 projets IT et Marketing |
| Couverture | 4 régions géographiques, période 2018 — début 2022 |
| Livrable | Rapport Power BI (.pbix) à 4 pages interactives |

Le dashboard remplace un suivi de projets manuel et fragmenté par une solution décisionnelle centralisée, offrant à chaque niveau hiérarchique — de la Direction Générale aux Directeurs Pays — une vue adaptée à son périmètre, avec identification immédiate des projets à risque.

---

## Objectifs

Le tableau de bord permet aux directeurs de :

- **Suivre** l'avancement de 247 projets IT et Marketing à travers 4 régions
- **Identifier** automatiquement les projets en alerte (écart ≥ 15% sur coûts, délais ou livrables)
- **Comparer** les performances entre régions, pays et types de projets
- **Décider** de façon stratégique sur la base de données consolidées et à jour

---

## Indicateurs clés (KPI)

Trois indicateurs de performance sont surveillés en continu.

| Indicateur | Formule | Seuil d'alerte |
|------------|---------|----------------|
| **Écart Coût (%)** | `(Coût Réel − Coût Prévu) / Coût Prévu × 100` | ≥ 15% |
| **Écart Durée (%)** | `(Durée Réelle − Durée Prévue) / Durée Prévue × 100` | ≥ 15% |
| **Écart Livrables (%)** | `(Livrables Réels − Livrables Prévus) / Livrables Prévus × 100` | ≥ 15% |

**Règle d'alerte** : un projet est considéré **en alerte** si l'écart atteint **≥ 15%** sur **au moins un** des trois indicateurs.

Code couleur appliqué à l'ensemble des visuels : 🟢 conforme · 🟡 vigilance · 🔴 en alerte.

---

## Périmètre des données

| Dimension | Détail |
|-----------|--------|
| Régions | Europe occidentale · EMEA · Amérique du Nord et latine · Asie-Pacifique |
| Types de projets | IT (6 phases, A → F) · Marketing (4 phases, 1 → 4) |
| Période couverte | 2018 — début 2022 |
| Volume analysé | 247 projets |

---

## Stack technique

| Couche | Technologies |
|--------|--------------|
| Conception & design | Power BI Desktop |
| Transformation (ETL) | Power Query (langage M) — nettoyage, fusion, automatisation |
| Calculs & mesures | DAX (écarts, alertes, KPI, agrégations) |
| Cartographie | Azure Maps (visualisation géographique interactive) |
| Planification | Gantt Chart (timeline des phases) |
| Analyse financière | Waterfall Chart (dépassements de coûts) |
| Modélisation | Schéma en étoile (table de faits + dimensions) |

Fonctions DAX principales utilisées : `CALCULATE`, `FILTER`, `DIVIDE`, `SUMX`, `DISTINCTCOUNT`, ainsi que des mesures conditionnelles pour les alertes automatiques.

---

## Architecture du dashboard

Le rapport s'organise en 4 pages, chacune destinée à un niveau de décision.

### Page 1 — Vue d'ensemble
**Cible : Directeur Général**

- 4 KPI Cards : total projets, projets en alerte, taux d'alerte (%), budget total
- Carte géographique interactive (Azure Maps) avec code couleur 🟢🟡🔴
- Top 10 des pays comptant le plus de projets en alerte
- Comparaison IT vs Marketing (Normal / En alerte)
- Double Donut Chart : répartition par Région + Type de projet
- Filtres : Type de projet, Année

### Page 2 — Analyse détaillée
**Cible : Directeurs Régionaux & Directeurs Pays**

- Zone de filtres avancés (Région, Pays, Type, Phase, Plage de dates)
- 4 KPI Cards contextuels réagissant aux filtres
- Tableau détaillé : ID Projet, Phase, Pays, Écarts (%), Statut 🔴/🟢
- Graphiques Prévu vs Réel par indicateur (barres groupées)
- Courbes d'évolution temporelle des écarts

### Page 3 — Suivi temporel
**Cible : Tous les directeurs**

- Diagramme de Gantt : timeline des phases (Normal / Retard / En cours)
- Graphique en cascade (Waterfall) : Budget Initial → +Retards → +Scope → +Ressources → Budget Final
- Nuage de points : corrélation Écart Durée vs Écart Coût
- Filtres avancés : Région, Pays, Type, Phase, Période, ID Projet

### Page 4 — Documentation
**Cible : Tous les utilisateurs**

- Guide d'utilisation du dashboard
- Définitions des 3 indicateurs et du seuil d'alerte (15%)
- Méthodologie et sources de données
- Fréquence de mise à jour (hebdomadaire) et contact support

---

## Fonctionnalités

| Fonctionnalité | Description |
|----------------|-------------|
| Interactivité croisée | Tous les visuels interconnectés : un clic sur une région filtre automatiquement l'ensemble des graphiques |
| Filtres contextuels | Chaque utilisateur analyse selon son périmètre (région, pays, type de projet) |
| Alertes visuelles | Code couleur 🟢🟡🔴 pour repérer instantanément les projets à risque |
| Drill-down | Navigation fluide de la vue macro (Page 1) au détail projet (Page 2) |
| Analyse multi-niveaux | Double Donut Chart pour croiser Région et Type de projet simultanément |
| Analyse temporelle | Suivi de l'évolution des écarts pour détecter les tendances |

---

## Modèle de données

Le modèle repose sur un **schéma en étoile** garantissant performance et lisibilité des relations.

<details>
<summary><b>Table de faits</b></summary>

- **Faits_Projets** — ID projet, coût prévu, coût réel, durée prévue, durée réelle, livrables prévus, livrables réels, écart coût (%), écart durée (%), écart livrables (%), statut d'alerte

</details>

<details>
<summary><b>Tables de dimensions</b></summary>

- **Dim_Géographie** — région, pays, coordonnées (latitude / longitude pour Azure Maps)
- **Dim_Type_Projet** — type (IT / Marketing), phase (A→F / 1→4)
- **Dim_Temps** — année, trimestre, mois, date de début, date de fin
- **Dim_Statut** — libellé du statut, code couleur associé

</details>

Les mesures DAX (écarts, taux d'alerte, comptages conditionnels) sont centralisées et réutilisées sur l'ensemble des pages pour garantir la cohérence des chiffres.

---

## Installation

### Prérequis

- **Power BI Desktop** (gratuit) — [Télécharger](https://www.microsoft.com/fr-fr/power-platform/products/power-bi/desktop)

### Étapes

```
1. Télécharger le fichier dashboard_PMO.pbix
2. L'ouvrir avec Power BI Desktop
3. Actualiser les données si nécessaire (bouton « Actualiser » du ruban)
4. Explorer les 4 pages interactives
5. Utiliser les filtres pour analyser selon le périmètre souhaité
```

---

## Aperçu

<table>
<tr>
<td width="50%"><b>Page 1 — Vue d'ensemble</b><br><img width="1733" height="814" alt="Vue d'ensemble" src="https://github.com/user-attachments/assets/6ea09390-7ab2-4585-8a98-485c9a396e68"></td>
<td width="50%"><b>Page 2 — Analyse détaillée</b><br><img width="1774" height="817" alt="Analyse détaillée" src="https://github.com/user-attachments/assets/66232094-2ce5-4abd-9682-1915a76b305d"></td>
</tr>
<tr>
<td><b>Page 3 — Suivi temporel</b><br><img width="1624" height="816" alt="Suivi temporel" src="https://github.com/user-attachments/assets/e32228f6-ff90-4789-9a51-e7b8654a5ee5"></td>
<td><b>Page 3 — Suivi régional</b><br><img width="1462" height="824" alt="Suivi régional" src="https://github.com/user-attachments/assets/550583a8-a07d-40ea-a322-a6bb80496cd5"></td>
</tr>
</table>

---

## Compétences démontrées

**Business Intelligence & Data Analysis**
- Analyse des besoins métier (Product Strategy Canvas, User Stories)
- Conception de tableaux de bord orientés décision pour plusieurs niveaux hiérarchiques
- Définition d'indicateurs de performance (KPI) et de seuils d'alerte

**Data Engineering**
- Modélisation en schéma en étoile (table de faits + dimensions)
- Fusion et transformation de données hétérogènes (Power Query)
- Automatisation du nettoyage de données et gestion des relations

**DAX & Calculs**
- Mesures complexes : écarts, filtres, agrégations
- Fonctions avancées : `CALCULATE`, `FILTER`, `DIVIDE`, `SUMX`, `DISTINCTCOUNT`
- Mesures conditionnelles et alertes automatiques

**Data Visualization**
- Visualisations interactives et intuitives (Azure Maps, Gantt, Waterfall, Double Donut)
- Choix des graphiques adaptés au message à transmettre
- Code couleur cohérent et accessibilité visuelle

**Project Management**
- Structuration d'un projet BI de bout en bout
- Gestion des livrables et méthodologie agile itérative

---

## Livrables

- [x] **Product Strategy Canvas** complété (PDF)
- [x] **Tableau de bord Power BI** (.pbix) — 4 pages interactives
- [x] **Modèle de données** documenté (schéma en étoile)
- [x] **Mesures DAX** automatisées et optimisées
- [x] **Documentation intégrée** au dashboard (Page 4)
- [x] **Captures d'écran** des pages principales

---

## Auteur

Projet réalisé dans le cadre d'une démarche de Business Intelligence appliquée au pilotage de projets.

---

## License

Projet académique — usage pédagogique et démonstratif.
