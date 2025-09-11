# 🏦 Prédiction de l’attrition bancaire (Bank Churn Prediction)  

##  Contexte  
Dans un secteur bancaire hautement concurrentiel, la fidélisation des clients est un enjeu stratégique majeur.  
Ce projet vise à analyser les comportements clients afin de **détecter ceux susceptibles de quitter la banque (churn/attrition)**.  

##  Objectifs  
- Explorer et comprendre les profils clients grâce à l’analyse statistique et factorielle  
- Identifier des groupes homogènes de clients via des méthodes de **clustering**  
- Construire et comparer plusieurs modèles de **classification supervisée** pour prédire le churn  

##  Jeu de données  
- Source : [Kaggle – Credit Card Bank Churn Dataset](https://www.kaggle.com/datasets/anwarsan/credit-card-bank-churn)  
- Variables : données socio-démographiques, financières et comportementales  
- Taille : environ **10 000 clients**  

## 🛠 Méthodologie  

###  Analyse exploratoire des données (EDA)  
- Nettoyage et préparation : suppression des variables inutiles, gestion des valeurs inconnues  
- Statistiques descriptives et visualisations  

###  Méthodes factorielles  
- **ACP (Analyse en Composantes Principales)** : étude des corrélations entre variables quantitatives  
- **AFC (Analyse Factorielle des Correspondances)** : analyse des relations entre variables qualitatives  

###  Classification non supervisée  
- **Clustering hiérarchique (CAH)** pour regrouper les clients en profils homogènes  

### Classification supervisée  
- Données fortement déséquilibrées → **rééchantillonnage avec SMOTE**  
- Modèles testés :  
  - Régression logistique & Lasso  
  - Arbre de décision (CART)  
  - Random Forest  
  - AdaBoost  

###  Évaluation des performances  
- Indicateurs : **Accuracy**, **AUC-ROC**, **matrice de confusion**  
- Comparaison des performances entre modèles  

## 🛠 Outils utilisés  
- **Langage** : R  
- **Packages principaux** :  
  - `tidyverse` (manipulation et visualisation : dplyr, tidyr, ggplot2)  
  - `randomForest` (forêts aléatoires)  
  - `rpart`, `rpart.plot` (arbres de décision CART)  
  - `gbm` (AdaBoost)  
  - `glmnet` (régression logistique Lasso)  
  - `pROC` (courbes ROC et AUC)  
  - `DMwR` (rééchantillonnage SMOTE)  
  - `FactoMineR`, `factoextra` (ACP, AFC, visualisation)  
