# Student-Performance-HybridML

## Overview
This project explores the use of machine learning models to predict student academic performance based on socio-economic, behavioral, and academic attributes. A hybrid ensemble classifier was developed and evaluated using the UCI Student Performance dataset. The study includes subgroup fairness analysis to assess performance across different student backgrounds.

## Research Goal
To build a robust and interpretable machine learning model that predicts student performance categories (Low, Medium, High) using a hybrid ensemble approach, while identifying disparities in prediction accuracy across socio-economic subgroups.

## Dataset
- Source: [UCI Student Performance Dataset](https://archive.ics.uci.edu/ml/datasets/Student+Performance)
- File: `student-mat.csv`
- 395 student records with 33 features including:
  - Parental education
  - Family support
  - Internet access
  - Study time
  - Failures
  - Absences
  - Previous grades (G1, G2)

## Key Components

### 1. Data Preprocessing
- Mapped binary and categorical features
- Applied one-hot encoding for multi-category fields
- Discretized final grade (G3) into 3 performance classes:
  - `0 = Low` (0–9), `1 = Medium` (10–14), `2 = High` (15–20)

### 2. Model Architecture
- Base models:
  - Random Forest
  - Gradient Boosting
- Combined using a **soft voting ensemble**
- GridSearchCV used for hyperparameter tuning

### 3. Evaluation Metrics
- Accuracy: 88.61%
- Macro-averaged F1-score: 0.89
- Confusion matrix and class-wise precision/recall

### 4. Fairness Analysis
- Evaluated performance across:
  - Gender (M vs F)
  - Internet access (yes vs no)
  - Family support (yes vs no)
  - Parental education (low vs high)
- Noted disparities in accuracy, suggesting potential bias

## Technologies Used
- Python
- pandas, NumPy
- scikit-learn
- seaborn, matplotlib
- Jupyter Notebook


