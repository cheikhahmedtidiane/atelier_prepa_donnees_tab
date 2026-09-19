# Atelier : Préparation de Données pour le Machine Learning (Smart Building)

Ce dépôt contient l'intégralité des travaux pratiques dédiés au **nettoyage, à l'analyse exploratoire et à la mise en place d'un pipeline complet de préparation de données (Data Preparation)** appliqués aux données des bâtiments intelligents (*Smart Buildings*).

L'objectif final est de transformer des mesures brutes de capteurs en un jeu de données sain et standardisé, prêt à alimenter un modèle de Machine Learning capable de prédire les alertes du système.

---

## Contenu du Projet

L'atelier est structuré en plusieurs phases clés, allant de la détection des anomalies jusqu'à l'industrialisation des traitements :

* **Analyse Exploratoire Visuelle** : Identification des distributions (symétrie, dispersion) et détection des valeurs extrêmes.
* **Nettoyage Textuel Avancé** : Normalisation des accents, correction des fautes de frappe (`bureau`/`bureu`) et harmonisation de la casse.
* **Stratégie de Capping** : Gestion des valeurs aberrantes par le traitement des percentiles (1% et 99%) à l'aide de `.clip()`.
* **Pipelines de Preprocessing Scikit-Learn** : 
  * Branche numérique : Imputation par la médiane et mise à l'échelle via `StandardScaler`.
  * Branche catégorielle : Imputation par le mode et encodage via `OneHotEncoder` et `OrdinalEncoder`.
* **Export & Industrialisation** : Génération d'un rapport flash de qualité des données et exportation du dataset nettoyé.

---

##  Structure des Fichiers

* `exports/smart_building_cleaned.csv` : Le jeu de données final, propre, borné et prêt pour le ML.
* `atelier_notebook.ipynb` : Le notebook contenant le code pas à pas et les visualisations Seaborn/Matplotlib.

---

## Installation & Lancement

1. Clonez ce dépôt sur votre machine :
```bash
git clone https://github.com
cd atelier_prepa_donnees_tab
```

2. Installez les dépendances requises :
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Lancez votre environnement de développement (Jupyter, VS Code) pour exécuter le script.
