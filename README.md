# Machine Learning Hyperparameter Tuning - Time Performance Analysis

## Project Overview
This project performs comprehensive hyperparameter tuning on three different machine learning models using the Breast Cancer dataset with MLflow tracking.

## Models and Configurations

### 1. Decision Tree Classifier
**Total Runs:** 294

**Hyperparameters:**
- `max_depth`: [1, 3, 30, 50, 70, 100, 150] (7 values)
- `min_samples_split`: [2, 4, 25, 60, 75, 120, 200] (7 values)
- `criterion`: ["gini", "entropy", "log_loss"] (3 values)
- `splitter`: ["best", "random"] (2 values)

**Grid Size:** 7 × 7 × 3 × 2 = **294 combinations**

BEST RESOLTS
**max_depth:** 3
**min_samples_split:** 4
**criterion:** entropy
**splitter:** best

BEST METRICS:
**accuracy:** 0.9734
**precision:** 0.9677
**recall:** 0.9917
**f1_score:** 0.9796
**average:** 0.9781


### 2. Random Forest Classifier
**Total Runs:** 490

**Hyperparameters:**
- `n_estimators`: [10, 50, 100, 150, 200] (5 values)
- `max_depth`: [1, 3, 30, 50, 70, 100, 150] (7 values)
- `min_samples_split`: [2, 4, 25, 60, 75, 120, 200] (7 values)
- `criterion`: ["gini", "entropy"] (2 values)

**Grid Size:** 5 × 7 × 7 × 2 = **490 combinations**

BEST RESOLTS:

**n_estimators:** 10
**max_depth:** 100
**min_samples_split:** 25
**criterion:** entropy

BEST METRICS:
**accuracy:** 0.9787
**precision:** 0.9756
**recall:** 0.9917
**f1_score:** 0.9836
**average:** 0.9824


### 3. AdaBoost Classifier
**Total Runs:** 210

**Hyperparameters:**
- `n_estimators`: [10, 30, 50, 70, 100, 150, 200] (7 values)
- `learning_rate`: [0.01, 0.1, 0.5, 1.0, 1.5, 2.0] (6 values)
- `random_state`: [42, 123, 456, 789, 101112] (5 values)

**Grid Size:** 7 × 6 × 5 = **210 combinations**

## Total Experiments
**994 model runs** across all three algorithms


**n_estimators:** 50
**learning_rate:** 1.5
**random_state:** 42

BEST METRICS:
**accuracy:** 0.9840
**precision:** 0.9917
**recall:** 0.9835
**f1_score:** 0.9876
**average:** 0.9867
