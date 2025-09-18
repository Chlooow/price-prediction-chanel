# Prédiction de prix sur des produits Chanel

L’objectif de ce projet est de développer un modèle de machine learning capable de prédire le prix des produits de la maison Chanel à Singapour en fonction de leurs caractéristiques (catégorie, niveau de luxe, etc.).
Ce travail s’inscrit dans une logique d’exploration de l'apprentissage statistique appliquée au secteur du luxe, avec un focus sur l’interprétabilité des résultats et la rigueur de la démarche scientifique.

## Dataset

Les données utilisées proviennent du dataset public Chanel Product Prices Singapore disponible sur [Hugging Face](https://huggingface.co/datasets/DBQ/Chanel.Product.prices.Singapore).
Elles recensent plusieurs produits Chanel vendus à Singapour, avec leurs catégories, noms et prix.

## Démarche suivie

### Analyse exploratoire (EDA)
Étude de la distribution des prix et mise en évidence d’une forte asymétrie.

### Visualisations (histogrammes, boxplots, heatmaps) 
pour comprendre l’influence des catégories.

### Prétraitement & Feature Engineering
- Nettoyage des données gestion des valeurs manquantes, doublons.
- Création de nouvelles variables (is_high_end, luxury_level_num, etc.).
- Log-transform et standardisation de la cible pour stabiliser la variance et améliorer les performances.

### Modélisation
- Régression Linéaire (SGDRegressor) comme premier modèle de référence.
- Évaluation par RMSE, MAE, R² sur données de test et via validation croisée.

### Évaluation & Visualisation

- Comparaison prédictions vs valeurs réelles.
- Analyse des résidus pour vérifier la validité des hypothèses.
- Test sans transformation pour montrer l’impact négatif de la dispersion des prix, ce qui constitue un apprentissage clé du projet.

## Résultats principaux
- Score R² ~ 0.85 (sur données transformées).
- RMSE ~ 0.38 et MAE ~ 0.30 sur cible standardisée/log-transformée.
Importance des catégories et du niveau de luxe confirmée comme facteurs clés dans la prédiction.

## Retombées possibles pour une maison comme Chanel

- Stratégie de pricing : affiner les prix selon les catégories et le positionnement luxe (Ce qui est déjà fait)
- Analyse concurrentielle : extension du modèle pour benchmarker les concurrents (Idem).
- Optimisation interne : intégration potentielle dans un outil de pricing ou un tableau de bord data-driven.

## Outils & Technologies utilisés

- Python (pandas, numpy, matplotlib, seaborn, scikit-learn)
- Jupyter Notebook pour la démarche exploratoire et la modélisation
- Méthodes de ML supervisé : Régression linéaire, validation croisée

Ce projet illustre ma capacité à mener un projet de machine learning de bout en bout à partir des connaissances que j'ai eu en Licence, 
de l’analyse exploratoire à l’interprétation des résultats, 
en gardant un souci d’applicabilité réelle dans le secteur du luxe. Ceci m'aide à me rappeler et pratiqué les notions déjà utilisé.
