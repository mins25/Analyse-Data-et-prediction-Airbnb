# 🏠 Prédiction du Prix des Annonces Airbnb

Ce projet vise à analyser et prédire les **prix des logements Airbnb** à partir d'un ensemble de données fournies, en utilisant plusieurs techniques de visualisation, de prétraitement et de modélisation.

---

## 📁 Contenu

- `airbnb_train.csv` : Données d'entraînement.
- `airbnb_test.csv` : Données de test (sans prix).
- `prediction_example.csv` : Format de soumission.
- `notebook.py` ou `main.py` : Script principal contenant toutes les étapes d’analyse et de modélisation.
- `README.md` : Ce fichier.

---

## 📊 Objectifs

- Explorer et visualiser les données pour comprendre les facteurs influençant les prix.
- Prétraiter les données (nettoyage, encodage, imputation).
- Tester plusieurs modèles de régression pour prédire le `log_price`.
- Générer une prédiction sur le fichier `airbnb_test.csv`.

---

## 🧪 Méthodologie

### 1. Exploration des données
- Distribution des prix (`log_price`)
- Analyse par ville, type de propriété, type de chambre, etc.
- Visualisation via seaborn, matplotlib, folium (heatmap, clustering, etc.)

### 2. Prétraitement
- Détection et gestion des valeurs manquantes.
- Encodage des variables catégorielles avec `LabelEncoder`.
- Transformation des variables `amenities`, `review_scores`, etc.
- Sélection des features pertinentes.

### 3. Modélisation
Modèles testés :
- Régression Linéaire
- Régression Polynomiale (avec GridSearchCV)
- Gradient Boosting Regressor
- Random Forest Regressor

### 4. Évaluation
- Métrique utilisée : **R² Score**
- Meilleure performance : `RandomForestRegressor`

### 5. Prédiction
- Prédictions générées pour `airbnb_test.csv`
- Résultat sauvegardé dans `prediction_example.csv` avec la colonne `logpred`.

---

## 📈 Résultats des modèles

| Modèle                     | R² Score |
|---------------------------|----------|
| Régression Linéaire       | ≈ 0.59   |
| Régression Polynomiale    | ≈ 0.61   |
| Gradient Boosting         | ≈ 0.75   |
| Random Forest             | **≈ 0.78**   |

---

## 🛠️ Dépendances

```bash
pip install numpy pandas seaborn matplotlib scikit-learn folium
