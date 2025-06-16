# PCOS Detection using Machine Learning

This repository contains a pipeline for predicting Polycystic Ovary Syndrome (PCOS) using clinical dataset and traditional ML algorithms.

## 🚀 Project Overview

- **Goal**: Build a ML model to detect PCOS from clinical and biochemical patient data.
- **Dataset**: 541 patient records with 34 features (e.g., age, BMI, hormone levels, glucose).
- **Features**: Numerical (lab results), categorical (symptoms), and derived features.
- **ML Models**: Random Forest, Logistic Regression, SVM, Decision Tree.
- **Outcome**: Best model achieved **83.5% accuracy**, demonstrating strong diagnostic potential.

## Prerequisites
- Python 3.8+
- Install dependencies:
  ```bash
  pip install -r requirements.txt

## Run the pipeline

### Preprocess data:
python src/data_preprocessing.py --input data/raw_data.csv --output data/processed.csv

### Feature selection & engineering:
python src/feature_selection.py --data data/processed.csv --output data/selected.csv

### Train and evaluate models:
python src/train_model.py --data data/selected.csv --model random_forest
python src/evaluate_model.py --data data/selected.csv --model random_forest
## 📊 Results
The Random Forest model achieved:

Accuracy: 83.48%

ROC-AUC: ~0.87

Selected top 10 predictors based on feature importance.

## 🔍 Insights
Hormonal measurements (e.g., LH, FSH) and BMI were among the top predictive features.

The model can assist healthcare practitioners with early PCOS screening.

## ⚙️ Next Steps
Test on larger, multi-center datasets for generalization.

Improve interpretability using SHAP or LIME.

Transition to a RESTful API for deployment in clinical settings.

## 📚 References
Scikit-learn documentation and tutorials.

Medical studies correlating biochemical markers with PCOS risk.

