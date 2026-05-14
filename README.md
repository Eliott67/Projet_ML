# Prédiction du Risque Cardiovasculaire et du Cholestérol LDL

## Objectif du Projet
Ce projet a pour but de modéliser et de prédire les risques liés aux maladies cardiovasculaires à partir de dossiers médicaux. L'étude se divise en deux tâches principales d'apprentissage automatique : 
1. **Classification :** Prédire le risque d'accident cardiaque (`Heart_Disease_Risk`) à partir des caractéristiques des patients.
2. **Régression :** Prédire le taux de "mauvais" cholestérol (`Cholesterol_LDL`) en fonction des autres variables cliniques et comportementales.

## 📥 Récupération des données
Les données utilisées sont issues d'un jeu de données synthétiques de la plateforme Kaggle. Bien que synthétiques, elles respectent les heuristiques médicales et les corrélations réalistes (ex: relation entre âge, IMC et pression artérielle).

🔗 [Télécharger le dataset Cardiovascular Disease Risk Prediction ici](https://www.kaggle.com/datasets/bertnardomariouskono/cardiovascular-disease-risk-prediction-dataset)

## Données
Le dataset contient les profils de 15 000 patients répartis sur 19 variables :
* **Variables quantitatives :** Âge, Taille, Poids, IMC, Pressions artérielles (Systolique/Diastolique), Cholestérol (Total, LDL, HDL), Glycémie à jeun, Heures de sommeil.
* **Variables qualitatives :** Genre, Statut tabagique, Consommation d'alcool, Niveau d'activité physique, Antécédents familiaux, Niveau de stress, Risque cardiaque (cible binaire).

## Méthodologie
L'analyse s'articule autour d'une démarche complète en Data Science :
1. **Analyse Exploratoire (EDA) :** Étude uni/bi-dimensionnelle et Analyse en Composantes Principales (ACP) pour identifier les corrélations sous-jacentes.
2. **Prétraitement :** Nettoyage, encodage des variables qualitatives et standardisation.
3. **Modélisation (Classification & Régression) :** * Modèles linéaires (Régression Logistique / Linéaire, pénalisations Lasso/Ridge).
   * Machines à Vecteurs de Support (SVM / SVR).
   * Modèles ensemblistes (Arbres de décision, Random Forest, Gradient Boosting).
   * Réseaux de Neurones (Perceptron Multicouche).
4. **Optimisation et Évaluation :** Recherche d'hyperparamètres par validation croisée et évaluation finale sur un échantillon test (20% des données) via des métriques adaptées (Accuracy, AUC-ROC, RMSE).

## Résultats Principaux (Classification du Risque Cardiaque)
* **Performance :** La Régression Logistique s'est imposée comme le modèle optimal, atteignant les meilleures performances (AUC-ROC > 0.80) face aux algorithmes "boîte noire" (Réseaux de neurones, Boosting) qui n'ont pas apporté de gain prédictif significatif sur ces données.
* **Interprétabilité :** Le tabagisme et les antécédents familiaux ont été isolés comme les principaux vecteurs de risque cardiovasculaire. À l'inverse, l'activité physique se distingue comme le facteur protecteur majeur.

## Structure du projet
```text
└── Projet_ML_Cardio/
    ├── notebook_Python.ipynb        # Modélisation et Machine Learning en Python
    ├── notebook_R.ipynb          # Modélisation et Machine Learning en R
    ├── ML-Project-4MA-2526.pdf      # Consignes et description du projet
    ├── dataset.csv                  # Jeu de données (à télécharger)
    └── README.md                    # Description du projet

## Authors
* **Oster Eliott**
* **Paulien-Camy Lucas**
* **Costadau Lila**
* **Fauli Lukas**
*Projet réalisé dans le cadre de la 4ème année au département GMM de l'INSA Toulouse.*
