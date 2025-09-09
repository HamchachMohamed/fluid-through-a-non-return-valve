# Simulation CFD - Écoulement dans une Vanne Anti-Retour

## Description

Ce projet présente une simulation numérique complète de l'écoulement fluidique dans une vanne anti-retour utilisant la dynamique des fluides computationnelle (CFD). L'analyse permet d'étudier le comportement du fluide à travers le système et d'optimiser les performances de la vanne.

## Objectifs

- Analyser les caractéristiques d'écoulement dans une vanne anti-retour
- Identifier les zones de pression et de vitesse critiques
- Visualiser les lignes de courant et les zones de recirculation
- Évaluer les performances hydrauliques du système

## Configuration de la Simulation

### Conditions aux Limites
- **Entrée (Pressure Inlet 1)** : 
  - Type : Pression totale
  - Valeur : 3e5 Pa (300 kPa)
  
- **Sortie (Pressure Outlet 2)** :
  - Type : Pression fixe
  - Valeur : 0 Pa (pression manométrique)

### Paramètres de Contrôle
- **Temps de simulation** : 2500 secondes
- **Pas de temps (Delta t)** : 1 seconde
- **Intervalle d'écriture** : 2500 secondes
- **Algorithme de décomposition** : Scotch
- **Runtime maximum** : 1e4 secondes

### Maillage
- **Type** : Maillage adaptatif automatique
- **Algorithme** : Standard avec sizing automatique
- **Finesse** : 5
- **Courbure** : Automatique
- **Couches limites** : Activées
- **Maillage physique** : Activé
- **Raffinement automatique** : Activé

## Résultats

### Champs de Vitesse
- **Plage de vitesses** : 0 à 33,56 m/s
- **Zones à haute vitesse** : Identifiées dans les sections de restriction
- **Gradients de vitesse** : Visualisés par code couleur (bleu → vert → jaune → rouge)

### Visualisations Disponibles
1. **Contours de vitesse 2D** : Coupe transversale montrant la distribution des vitesses
2. **Lignes de courant 3D** : Trajectoires du fluide dans l'espace tridimensionnel
3. **Champs vectoriels** : Direction et magnitude des vitesses
4. **Vues en coupe** : Analyses détaillées des sections critiques

## Structure des Fichiers

```
projet-cfd-vanne/
├── README.md
├── conditions-limites/
│   ├── pressure-inlet-config.png
│   ├── pressure-outlet-config.png
│   └── simulation-control.png
├── maillage/
│   └── mesh-configuration.png
├── resultats/
│   ├── velocity-contours-2d.png
│   ├── streamlines-3d.png
│   ├── velocity-vectors.png
│   └── cross-sections/
└── donnees/
    └── simulation-data.csv
```

## Technologies Utilisées

- **Logiciel CFD** : ANSYS Fluent / OpenFOAM
- **Génération de maillage** : Maillage adaptatif automatique
- **Post-traitement** : Visualisation des contours et lignes de courant
- **Modèle de turbulence** : Automatique

## Installation et Utilisation

### Prérequis
- Logiciel de CFD (ANSYS Fluent, OpenFOAM, ou similaire)
- Minimum 8 GB RAM pour les calculs
- Processeur multi-cœur recommandé

### Étapes d'Exécution
1. Importer la géométrie de la vanne
2. Appliquer les conditions aux limites définies
3. Générer le maillage avec les paramètres spécifiés
4. Lancer la simulation avec les contrôles configurés
5. Post-traiter les résultats pour visualisation

## Interprétation des Résultats

### Analyse des Performances
- Les zones de vitesse élevée indiquent des pertes de charge potentielles
- Les zones de recirculation peuvent causer des inefficacités
- Les gradients de pression révèlent le comportement hydraulique

### Applications Pratiques
- Optimisation de la géométrie de la vanne
- Prédiction des pertes de charge
- Validation des spécifications de conception
- Amélioration de l'efficacité énergétique

## Développements Futurs

- Analyse transitoire pour étudier l'ouverture/fermeture
- Étude paramétrique pour différentes géométries
- Validation expérimentale des résultats
- Optimisation multi-objectifs

## Auteur

Projet de simulation CFD réalisé dans le cadre de l'analyse des systèmes fluidiques industriels.

## Licence

Ce projet est disponible sous licence MIT - voir le fichier LICENSE pour plus de détails.
