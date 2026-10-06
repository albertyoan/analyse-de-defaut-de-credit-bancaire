# analyse-de-defaut-de-credit-bancaire
Ce projet a pour objectif d'analyser et de prédire le risque de défaut de crédit bancaire à partir de données issues du secteur financier
#  Credit Risk Analysis — Home Credit Default Risk

##  Présentation du projet

L'objectif est d'adopter une approche complète de **Data Analytics et Data Science**, allant de l'exploration et du nettoyage des données jusqu'à la construction d'un modèle de Machine Learning permettant d'estimer le risque de défaut d'un emprunteur.

Le projet s'appuie sur le dataset **Home Credit Default Risk**, qui contient plusieurs tables décrivant les caractéristiques des clients, leurs demandes de crédit, leur historique de crédit ainsi que leurs paiements.

---

##  Problématique

Lorsqu'une banque accorde un crédit, elle doit être capable d'évaluer le risque que l'emprunteur ne rembourse pas correctement son prêt.

La problématique principale de ce projet est donc :

> **Quels sont les facteurs associés au défaut de crédit et peut-on prédire le risque de défaut d'un client à partir de ses caractéristiques financières et de son historique bancaire ?**

---

##  Objectifs

### Objectif principal

Construire une solution permettant d'analyser et d'estimer le **risque de défaut de crédit**.

### Objectifs secondaires

* Comprendre la structure des données bancaires.
* Nettoyer et préparer les données.
* Réaliser une analyse exploratoire des données (EDA).
* Identifier les principaux facteurs associés au défaut.
* Créer de nouvelles variables pertinentes grâce au Feature Engineering.
* Construire des indicateurs de risque bancaire.
* Développer plusieurs modèles de Machine Learning.
* Comparer leurs performances.
* Interpréter les prédictions du modèle avec SHAP.
* Construire un dashboard interactif avec Power BI.
* Produire des recommandations permettant d'améliorer l'analyse du risque crédit.

---

##  Données

Le projet utilise le dataset **Home Credit Default Risk**.

Le dataset est composé de plusieurs tables contenant différentes informations sur les clients et leurs historiques financiers.

Les principales tables utilisées sont notamment :

* `application_train.csv` — demandes de crédit et informations clients.
* `application_test.csv` — données de test.
* `bureau.csv` — historique des crédits auprès d'autres institutions financières.
* `bureau_balance.csv` — historique mensuel des crédits présents dans `bureau`.
* `previous_application.csv` — anciennes demandes de crédit.
* `installments_payments.csv` — historique des paiements des crédits précédents.
* `POS_CASH_balance.csv` — historique des crédits POS et cash.
* `credit_card_balance.csv` — historique des cartes de crédit.
* `HomeCredit_columns_description.csv` — description des variables.

La variable cible principale est :

```text
TARGET
```

avec :

* `0` → client n'ayant pas connu de défaut selon la définition du dataset.
* `1` → client ayant connu un défaut selon la définition du dataset.

---

##  Méthodologie

Le projet sera réalisé progressivement selon plusieurs étapes.

### 1. Compréhension des données

* Inventaire des fichiers.
* Analyse des dimensions des tables.
* Étude des variables.
* Identification des clés et relations entre les tables.
* Analyse de la variable cible.

### 2. Nettoyage des données

* Gestion des valeurs manquantes.
* Détection des valeurs aberrantes.
* Correction des types de données.
* Suppression ou traitement des variables inutiles.
* Vérification de la cohérence des données.

### 3. Analyse exploratoire

Analyse des relations entre :

* revenus ;
* montant du crédit ;
* âge ;
* emploi ;
* niveau d'endettement ;
* historique de paiement ;
* nombre de crédits ;
* durée des crédits ;
* caractéristiques des demandes précédentes.

L'objectif sera notamment d'identifier les profils présentant les taux de défaut les plus élevés.

### 4. Feature Engineering

Création de variables permettant de mieux représenter le risque financier.

Exemples :

```text
Debt-to-Income Ratio
Credit-to-Income Ratio
Payment Delay Rate
Previous Application Count
Previous Refusal Rate
Average Payment Delay
Total Previous Credit
```

Ces variables seront construites à partir des différentes tables du dataset.

### 5. Machine Learning

Plusieurs modèles seront étudiés et comparés :

* Logistic Regression
* Decision Tree
* Random Forest
* XGBoost

Les performances seront évaluées avec plusieurs métriques :

* Precision
* Recall
* F1-score
* ROC-AUC
* PR-AUC
* Confusion Matrix

L'objectif ne sera pas uniquement de maximiser l'accuracy, mais de rechercher un modèle adapté à un contexte de **Credit Risk**.

### 6. Explainable AI

Le modèle final sera interprété à l'aide de **SHAP**.

Cette étape permettra notamment de répondre à la question :

> **Pourquoi le modèle considère-t-il qu'un client présente un risque élevé de défaut ?**

### 7. Power BI

Les résultats de l'analyse seront présentés dans un dashboard interactif.

Le dashboard pourra notamment présenter :

* nombre total de crédits ;
* montant total des crédits ;
* taux de défaut ;
* profil des clients ;
* défaut selon le revenu ;
* défaut selon l'âge ;
* défaut selon le montant du crédit ;
* analyse des différents profils de risque.

---

##  Technologies utilisées

### Analyse de données

* Python
* Pandas
* NumPy

### Visualisation

* Matplotlib
* Seaborn
* Power BI

### Machine Learning

* Scikit-learn
* XGBoost

### Explainable AI

* SHAP

### Environnement

* Visual Studio Code
* Jupyter Notebook
* Git / GitHub

---

##  Structure du projet

```text
credit-risk-analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb
│   ├── 04_feature_engineering.ipynb
│   ├── 05_model_training.ipynb
│   └── 06_model_explainability.ipynb
│
├── src/
│   ├── data_processing.py
│   ├── feature_engineering.py
│   ├── modeling.py
│   └── evaluation.py
│
├── dashboard/
│   └── credit_risk_dashboard.pbix
│
├── reports/
│   └── project_report.pdf
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

##  Résultats attendus

À la fin du projet, nous souhaitons obtenir :

* une analyse détaillée du portefeuille de crédits ;
* une identification des principaux facteurs associés au défaut ;
* un ensemble de variables financières pertinentes ;
* plusieurs modèles de prédiction comparés ;
* un modèle final permettant d'estimer le risque de défaut ;
* une interprétation des prédictions avec SHAP ;
* un dashboard Power BI interactif ;
* une synthèse des résultats et recommandations métier.

---

##  Limites du projet

Les résultats obtenus par les modèles ne doivent pas être considérés comme une décision bancaire automatique.

Le projet est réalisé dans un objectif **pédagogique et analytique**. Une utilisation réelle dans le secteur bancaire nécessiterait notamment une validation réglementaire, une gouvernance des données, une analyse approfondie des biais ainsi qu'une validation métier.

---

##  Auteur

**TAGNE Albert Yoan**

Etudiant cycle ingenieur — EFREI Paris

Projet personnel — Analyse de données et Machine Learning

---

##  Source des données

Dataset : **Home Credit Default Risk**

Source : Kaggle — Home Credit Group
