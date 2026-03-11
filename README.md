
# Analyse et Prévision de la Qualité de l’Air

## Introduction

Ce projet vise à analyser et prévoir des indicateurs de qualité de l’air à partir de séries temporelles environnementales.

L’objectif est d’étudier les dynamiques temporelles de la pollution atmosphérique et de comparer différentes approches de modélisation :

- modèles statistiques
- modèles de machine learning
- réseaux de neurones

Le dataset utilisé provient du **UCI Machine Learning Repository – Air Quality Dataset**, contenant des mesures issues de capteurs environnementaux.

---

## Importation et Prétraitement des Données

Les données ont été importées et traitées avec **Python (Pandas, NumPy)**.

Principales étapes :

- importation du dataset
- conversion des variables temporelles
- transformation des valeurs en format numérique
- structuration du dataset sous forme de série temporelle

Le dataset contient environ **9 000 observations** et **une centaine de variables** issues de capteurs de gaz (CO, NOx, benzène, etc.).

---

## Ajout des Features Complémentaires

Afin d’améliorer la capacité prédictive des modèles, plusieurs variables supplémentaires ont été construites :

- variables temporelles (heure, jour, mois)
- variables retardées (lags)
- vrariables environnementales


Ces features permettent de capturer **les dépendances temporelles et les dynamiques environnementales**.

---

## Évaluation de la Qualité de l’Air

Une analyse exploratoire a été réalisée afin de mieux comprendre les niveaux de pollution :

- distribution des concentrations de polluants
- évolution temporelle des mesures
- variations journalières et saisonnières

Cette étape permet d’identifier **des tendances et anomalies dans les données**.

---

## Interpolation des Données Manquantes

Les données issues de capteurs environnementaux contiennent souvent des valeurs manquantes.
Un interpolation linéaire est appliqués.

Ces méthodes permettent de **préserver la cohérence des séries temporelles**.

---

## Nettoyage des Données

Le nettoyage des données comprend :

- suppression des valeurs invalides
- traitement des valeurs aberrantes
- normalisation de certaines variables

Cette étape garantit **la fiabilité des données utilisées pour l’apprentissage**.

---

## Analyse des Données

Une analyse exploratoire approfondie a été réalisée :

- analyse de corrélation entre polluants
- distribution des variables
- visualisation des séries temporelles

Cette analyse aide à **identifier les relations entre variables et orienter la modélisation**.

---

## Train-Test Split

La séparation entre données d’entraînement et de test respecte l’ordre temporel afin d’éviter les fuites d’information.

Division typique :

- 60 % données d’entraînement
- 40 % données de test

---

# Modélisation

## Premiers Modèles

Des modèles de base ont été implémentés pour établir une référence de performance.

---

## SARIMA

Les modèles SARIMA permettent de capturer :

- les dépendances temporelles
- la saisonnalité
- les composantes autoregressives et moving average

---

## SARIMAX

Le modèle SARIMAX permet d’intégrer **des variables exogènes** afin d’améliorer la prévision.

---

# Machine Learning

## Random Forest

Le modèle **Random Forest** permet de capturer des relations non linéaires entre les variables environnementales.

Avantages :

- robuste au bruit
- efficace sur données tabulaires
- capable de modéliser des interactions complexes

---

## Boosting

Les méthodes de boosting ont été utilisées pour améliorer les performances via des ensembles de modèles faibles.

---

## Bagging

Les approches de bagging permettent de réduire la variance et d'améliorer la stabilité des prédictions.

---

# Réseaux de Neurones

## MLP

Un réseau **MLP (Multi-Layer Perceptron)** a été implémenté comme modèle de base en deep learning.

---

## LSTM

Les réseaux **LSTM** permettent de capturer les dépendances temporelles longues dans les séries chronologiques.

---

## GRU

Les réseaux **GRU** constituent une alternative plus légère aux LSTM, avec un nombre de paramètres réduit.

---

# Comparaison des Modèles

Les performances des modèles ont été évaluées à l’aide de métriques classiques :

- RMSE
- MSE

Exemple de résultats :

- SARIMA : RMSE ≈ 30
- GRU : MSE ≈ 1500

Les modèles statistiques montrent de bonnes performances sur ce dataset de taille modérée.

---

# Conclusion

Ce projet montre l’intérêt de comparer différentes approches de modélisation pour la prévision de la qualité de l’air.

Principaux enseignements :

- les modèles statistiques restent très compétitifs sur des datasets de taille modérée
- les méthodes de machine learning capturent certaines relations non linéaires
- les réseaux de neurones nécessitent souvent plus de données pour surpasser les approches classiques

Des travaux futurs pourraient inclure :

- des datasets environnementaux plus larges
- des architectures deep learning plus avancées
- des modèles hybrides statistiques / deep learning