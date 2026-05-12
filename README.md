# 🏁 Formula 1 Machine Learning Project

> **Course:** Machine Learning — Prof. Fahd Kalloubi  
> **Student:** Bounhar ElMahjoub | **Apogée:** 2330686 | **ISI-S6**  
> **Dataset:** [Formula 1 Complete History 1950–2026](https://www.kaggle.com/datasets/patelris/formula-1-complete-dataset-1950-2026)

---

## Project Overview

This project applies Machine Learning techniques to Formula 1 race data (1950–2026) to solve three problems:

| Problem | Type | Goal |
|---|---|---|
| **Problem 1** | Classification | Predict whether a driver will **win** the race |
| **Problem 2** | Regression | Predict the **exact finishing position** of each driver |
| **Problem 3** | Clustering | Discover natural **driver archetypes** (Champions, Regulars, Midfield, Backmarkers) |

---

##  Project Structure

```
F1-ML-Project/
├── Bounhar-ELMahjoub-ML-project-final.ipynb   # Main notebook
├── results.csv                                  # Dataset (download from Kaggle)
├── README.md                                    # This file
└── .gitignore
```

---

##  Models Implemented

### Classification (Problem 1)
- Decision Tree (CART, Gini)
- K-Nearest Neighbors
- Random Forest (Bagging) ⭐ Best AUC
- AdaBoost (Boosting)
- Logistic Regression (Ridge/L2)

### Regression (Problem 2)
- Ridge Regression
- Decision Tree Regressor
- Random Forest Regressor ⭐ Best R²

### Clustering (Problem 3)
- K-Means (Elbow + Silhouette)
- DBSCAN (outlier detection)
- Hierarchical Clustering (Ward linkage, dendrogram)

---

##  Key Results

| Model | Metric | Score |
|---|---|---|
| Random Forest Classifier | AUC-ROC | ~0.998 |
| Random Forest Regressor | R² | ~0.992 |
| K-Means | Silhouette Score | ~0.35 |

###  F1 2026 Championship Prediction (after 3 races)

| # | Driver | Points | Win Probability |
|---|---|---|---|
|  1| Andrea Kimi Antonelli | 68 | 48.5% |
| 2 | George Russell | 55 | 37.5% |
| 3 | Charles Leclerc | 42 | 0.7% |
| 4 | Lewis Hamilton | 35 | 1.3% |
| 5 | Lando Norris | 20 | 0.0% |

---

##  Feature Engineering

All features derived from `results.csv` alone:

| Feature | Description |
|---|---|
| `driver_win_rate` | Historical win rate per driver |
| `driver_avg_finish` | Average finishing position |
| `driver_avg_pts` | Average points per race |
| `constructor_avg_pts` | Team average points (car strength) |
| `grid_improvement` | Positions gained/lost vs starting grid |
| `finished` | Whether the driver completed the race |
| `is_winner` | Binary target: 1 = winner, 0 = not winner |

---

##  How to Run

### 1. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
```

### 2. Download the dataset
Download `results.csv` from [Kaggle](https://www.kaggle.com/datasets/patelris/formula-1-complete-dataset-1950-2026) and place it in the project root.

### 3. Launch the notebook
```bash
jupyter notebook Bounhar-ELMahjoub-ML-project-final.ipynb
```

### 4. Run all cells
`Kernel → Restart & Run All`

> The notebook auto-detects column names — works with both old and new versions of the Kaggle dataset.

---

##  Course Topics Applied

| Topic | Where Applied |
|---|---|
| Decision Trees (CART/ID3, Gini/Entropy) | Problem 1 |
| K-Nearest Neighbors | Problem 1 |
| Random Forest (Bagging) | Problems 1 & 2 |
| AdaBoost (Boosting) | Problem 1 |
| Logistic Regression (Ridge/L2) | Problem 1 |
| K-Means Clustering | Problem 3 |
| DBSCAN | Problem 3 |
| Hierarchical Clustering (Ward) | Problem 3 |
| Bias-Variance Tradeoff | Model comparison |
| Confusion Matrix, F1, AUC-ROC | Classification evaluation |
| MAE, RMSE, R² | Regression evaluation |
| Silhouette Score, SSE/Elbow | Clustering evaluation |
| StratifiedKFold Cross-Validation | All supervised models |
| StandardScaler / Normalization | KNN, Clustering preprocessing |
| Class imbalance handling | `class_weight='balanced'`, AUC over Accuracy |

---

##  Author

**Bounhar ElMahjoub**  
Apogée: 2330686 | ISI-S6  
Machine Learning — Prof. Fahd Kalloubi
