# Projet_Dashboard_PMO
# 📊 Dashboard de Pilotage des Projets IT &amp; Marketing  Tableau de bord Power BI interactif permettant de suivre et analyser la performance de 247 projets à travers 4 régions géographiques.**

# 📊 Dashboard PMO - Pilotage des Projets IT & Marketing

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge)

## 📸 Aperçu du Dashboard

### Page 1 : Vue d'ensemble
![Page 1](screenshots/Captured'écran2026-02-08180754.png)

### Page 2 : Analyse détaillée
![Page 2](screenshots/Captured'écran2026-02-08180814.png)

### Page 3 : Suivi temporel
![Page 3](screenshots/Captured'écran2026-02-08180830.png)

---

## 🎯 Objectif du Projet

Création d'un **tableau de bord décisionnel Power BI** pour le Project Management Office (PMO) d'une entreprise internationale spécialisée dans la fabrication et commercialisation de produits de grande consommation.

Le dashboard permet aux directeurs de :
- ✅ Suivre l'avancement de **247 projets** IT et Marketing à travers **4 régions**
- ✅ Identifier automatiquement les **projets en alerte** (écart ≥15% sur coûts/délais/livrables)
- ✅ Comparer les performances entre régions, pays et types de projets
- ✅ Prendre des **décisions stratégiques** basées sur les données en temps réel

---

## 📈 Indicateurs Clés de Performance (KPI)

### Les 3 KPI principaux surveillés :

| Indicateur | Formule | Seuil d'alerte |
|------------|---------|----------------|
| **📊 Écart Coût (%)** | `(Coût Réel - Coût Prévu) / Coût Prévu × 100` | ≥ 15% |
| **⏱️ Écart Durée (%)** | `(Durée Réelle - Durée Prévue) / Durée Prévue × 100` | ≥ 15% |
| **📦 Écart Livrables (%)** | `(Livrables Réels - Livrables Prévus) / Livrables Prévus × 100` | ≥ 15% |

**🚨 Seuil d'alerte** : Un projet est considéré **en alerte** si l'écart est **≥ 15%** sur **au moins un** des 3 indicateurs.

---

## 🗺️ Données Analysées

- **📍 Périmètre géographique** : 4 régions
  - Europe occidentale
  - Europe de l'Est / Moyen-Orient / Afrique (EMEA)
  - Amérique du Nord et latine
  - Asie-Pacifique

- **🔧 Types de projets** :
  - **IT** : 6 phases (A → F)
  - **Marketing** : 4 phases (1 → 4)

- **📅 Période couverte** : 2018 - début 2022

- **📊 Volume** : 247 projets analysés

---

## 🛠️ Technologies Utilisées

| Technologie | Utilisation |
|-------------|-------------|
| **Power BI Desktop** | Création et design du dashboard interactif |
| **Power Query (M)** | Nettoyage, transformation et fusion automatisée des données |
| **DAX** | Mesures calculées (écarts, alertes, KPI, agrégations) |
| **Azure Maps** | Visualisation géographique interactive avec code couleur |
| **Gantt Chart** | Timeline et planification temporelle des projets |
| **Waterfall Chart** | Analyse des dépassements de coûts par catégorie |

---

## 📊 Architecture du Dashboard

### 📄 **Page 1 : Vue d'ensemble**
**Utilisateur cible** : Directeur Général

**Contenu** :
- 🎯 4 KPI Cards (Total projets, Projets en alerte, Taux d'alerte %, Budget total)
- 🗺️ Carte géographique interactive (Azure Maps) avec code couleur 🟢🟡🔴
- 📊 Top 10 pays avec le plus de projets en alerte
- 📈 Comparaison IT vs Marketing (Normal / En alerte)
- 🍩 Double Donut Chart : Répartition par Région + Type de projet
- 🎛️ Filtres : Type de projet, Année

---

### 📄 **Page 2 : Analyse détaillée**
**Utilisateurs cibles** : Directeurs Régionaux & Directeurs Pays

**Contenu** :
- 🎛️ Zone de filtres avancés (Région, Pays, Type, Phase, Plage de dates)
- 🎯 4 KPI Cards contextuels (qui changent selon les filtres)
- 📋 Tableau détaillé : ID Projet, Phase, Pays, Écarts (%), Statut 🔴/🟢
- 📊 Graphiques Prévu vs Réel par indicateur (barres groupées)
- 📈 Graphique d'évolution temporelle des écarts (courbes)

---

### 📄 **Page 3 : Suivi temporel** *(optionnel)*
**Utilisateurs** : Tous les directeurs

**Contenu** :
- 📅 Diagramme de Gantt : Timeline des phases avec code couleur (Normal/Retard/En cours)
- 💰 Graphique en cascade (Waterfall) : Analyse des dépassements de coûts
  - Budget Initial → +Retards → +Scope → +Ressources → Budget Final
- 🔍 Graphique de dispersion : Corrélation Écart Durée vs Écart Coût
- 🎛️ Filtres avancés : Région, Pays, Type, Phase, Période, ID Projet

---

### 📄 **Page 4 : Documentation**

**Contenu** :
- 📖 Guide d'utilisation du dashboard
- 📊 Définitions des 3 indicateurs
- 🎯 Explication du seuil d'alerte (15%)
- 🗂️ Méthodologie et sources de données
- 🔄 Fréquence de mise à jour (hebdomadaire)
- 📧 Contact pour support

---

## 🎨 Fonctionnalités Principales

| Fonctionnalité | Description |
|----------------|-------------|
| ✨ **Interactivité** | Tous les visuels interconnectés : clic sur une région → filtrage automatique de tous les graphiques |
| 🎯 **Filtres contextuels** | Chaque utilisateur filtre selon son périmètre (région, pays, type de projet) |
| 🚨 **Alertes visuelles** | Code couleur 🟢🟡🔴 pour identifier rapidement les projets problématiques |
| 🔍 **Drill-down** | Navigation fluide de la vue macro (Page 1) à la vue micro (Page 2 - détail projet) |
| 📊 **Multi-niveaux** | Double Donut Chart pour analyser Région ET Type de projet simultanément |
| 📈 **Analyse temporelle** | Suivi de l'évolution des écarts dans le temps pour détecter les tendances |

---

## 🎓 Compétences Démontrées

### **Business Intelligence & Data Analysis**
- ✅ Analyse et compréhension des besoins métier (Product Strategy Canvas, User Stories)
- ✅ Conception de tableaux de bord orientés décision pour différents niveaux hiérarchiques
- ✅ Définition d'indicateurs de performance (KPI) et seuils d'alerte

### **Data Engineering**
- ✅ Modélisation de données (schéma en étoile : table de faits + dimensions)
- ✅ Fusion et transformation de données hétérogènes (Power Query)
- ✅ Automatisation du nettoyage de données
- ✅ Gestion de relations entre tables

### **DAX & Calculs**
- ✅ Création de mesures DAX complexes (écarts, filtres, agrégations)
- ✅ Utilisation de fonctions avancées : CALCULATE, FILTER, DIVIDE, SUMX, DISTINCTCOUNT
- ✅ Mesures conditionnelles et alertes automatiques

### **Data Visualization**
- ✅ Design de visualisations interactives et intuitives
- ✅ Utilisation de visuels personnalisés (Azure Maps, Gantt, Waterfall, Double Donut)
- ✅ Choix des graphiques adaptés selon le message à transmettre
- ✅ Code couleur cohérent et accessibilité visuelle

### **Project Management**
- ✅ Structuration d'un projet BI de A à Z
- ✅ Gestion des livrables (Canvas, Dashboard, Documentation)
- ✅ Méthodologie agile et itérative

---

## 📦 Livrables du Projet

- [x] **Product Strategy Canvas** complété (PDF)
- [x] **Tableau de bord Power BI** (.pbix) avec 4 pages interactives
- [x] **Modèle de données** documenté (schéma en étoile)
- [x] **Mesures DAX** automatisées et optimisées
- [x] **Documentation intégrée** dans le dashboard (Page 4)
- [x] **Screenshots** des pages principales

---

## 🚀 Utilisation

### **Prérequis**
- **Power BI Desktop** (gratuit) : [Télécharger ici](https://www.microsoft.com/fr-fr/power-platform/products/power-bi/desktop)

### **Installation**
1. 📥 Téléchargez le fichier `dashboard_PMO.pbix`
2. 📂 Ouvrez-le avec Power BI Desktop
3. 🔄 Actualisez les données si nécessaire (bouton "Actualiser" dans le ruban)
4. 🎨 Explorez les 4 pages interactives
5. 🎛️ Utilisez les filtres pour analyser selon vos besoins

---

## 📚 Structure du Projet
