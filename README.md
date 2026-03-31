# Predictive Analysis of Interview Success
### Using Linear and Logistic Regression

---

## Overview

This project predicts student placement outcomes using machine learning regression techniques. Given academic and soft-skill features of 10,000 students, two models are built:

- **Linear Regression** — predicts a student's *Aptitude Test Score* (continuous output)
- **Logistic Regression** — predicts *Placement Status* — Placed or Not Placed (binary classification)

The goal is to identify which factors most influence interview success and build a reliable predictor that can guide students and institutions alike.

---

## Dataset

**File:** `placementdata.csv`  
**Rows:** 10,000 students  
**Columns:** 12

| Column | Type | Description |
|---|---|---|
| StudentID | int | Unique student identifier |
| CGPA | float | Cumulative Grade Point Average |
| Internships | int | Number of internships completed |
| Projects | int | Number of projects done |
| Workshops/Certifications | int | Number of workshops or certifications |
| AptitudeTestScore | int | Score in aptitude test (0–100) |
| SoftSkillsRating | float | Soft skills rating (1–5) |
| ExtracurricularActivities | str | Yes / No |
| PlacementTraining | str | Yes / No |
| SSC_Marks | int | Class 10 marks |
| HSC_Marks | int | Class 12 marks |
| PlacementStatus | str | Placed / NotPlaced *(target)* |

---

## Project Structure

```
├── placementdata.csv              # Raw dataset
├── placement_prediction.ipynb     # Main Jupyter Notebook (20 cells)
└── README.md                      # Project documentation
```

---

## Notebook Structure

The notebook is divided into 20 clearly labelled cells:

| Cell | Description |
|---|---|
| 1 | Import libraries |
| 2 | Load dataset |
| 3 | Dataset overview and missing value check |
| 4 | Descriptive statistics |
| 5 | EDA — Placement status distribution (bar + pie) |
| 6 | EDA — Numerical feature distributions by placement |
| 7 | EDA — CGPA and Aptitude Score boxplots |
| 8 | EDA — Categorical features vs placement |
| 9 | EDA — Correlation heatmap |
| 10 | Data preprocessing and label encoding |
| 11 | Feature definition for each model |
| 12 | Train-test split and feature scaling |
| 13 | Linear Regression — training and evaluation |
| 14 | Linear Regression — visualisations |
| 15 | Logistic Regression — training and evaluation |
| 16 | Logistic Regression — confusion matrix and ROC curve |
| 17 | Logistic Regression — feature importance (log-odds) |
| 18 | Probability distribution plot |
| 19 | Model comparison summary |
| 20 | Predict for a new student |

---

## Models

### Linear Regression
- **Target:** `AptitudeTestScore`
- **Metrics:** MAE, MSE, RMSE, R²
- **Purpose:** Estimates how well a student is likely to perform in aptitude-based screening rounds

### Logistic Regression
- **Target:** `PlacementStatus` (1 = Placed, 0 = NotPlaced)
- **Metrics:** Accuracy, Precision, Recall, F1-Score, ROC-AUC
- **Purpose:** Predicts the probability of a student getting placed

---

## Tech Stack

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Plotting and visualisation |
| `seaborn` | Statistical visualisation |
| `scikit-learn` | Model building and evaluation |

---

## How to Run

1. Clone or download this repository
2. Make sure `placementdata.csv` is in the same folder as the notebook
3. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
4. Launch the notebook:
   ```bash
   jupyter notebook placement_prediction.ipynb
   ```
5. Run all cells in order (`Kernel → Restart & Run All`)

---

## Results Summary

| Model | Target | Key Metrics |
|---|---|---|
| Linear Regression | AptitudeTestScore | R², RMSE, MAE |
| Logistic Regression | PlacementStatus | Accuracy, ROC-AUC, F1-Score |

> Exact metric values will appear after running the notebook on your machine.

---

## Key Insights

- **CGPA** and **AptitudeTestScore** are the strongest predictors of placement
- Students who underwent **PlacementTraining** showed significantly higher placement rates
- **SoftSkillsRating** and **Internship** experience positively influence outcomes
- The logistic regression model outputs a placement *probability*, enabling nuanced counselling

---

## Use Case

This project can be used by:
- **Students** — to assess their placement readiness and identify areas to improve
- **Colleges** — to flag at-risk students early and offer targeted training
- **Recruiters** — to understand what profile traits correlate with test performance

---

## Author

> Add your name, roll number, institution, and course details here.

---

## License

This project is for academic purposes only.
