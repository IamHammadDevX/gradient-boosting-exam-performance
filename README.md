# Gradient Boosting Exam Performance Prediction

## Overview
This project builds a complete machine learning pipeline to predict exam performance using Gradient Boosting Regression. The workflow is organized into three phases:
- Phase A: model selection and hyperparameter tuning
- Phase B: cross-validation
- Phase C: final model training and test evaluation

The notebook follows a structured approach with clear data preparation, model comparison, and evaluation steps.

## Dataset
The dataset is provided as an Excel file:
- Data_Project.xlsx

It includes demographics and household context features along with an ordinal exam performance label.

## Features and Target
Predictors (up to 6 features):
- Age (encoded from age ranges)
- Gender (Male/Female encoded)
- Household size (encoded)
- Marital status (encoded)
- Child in family (encoded)
- Experience (numeric)

Target:
- Exam_Performance encoded to a 1-5 ordinal scale

## Methodology
1. Data preparation and encoding
2. Stratified train-test split (70/30)
3. Baseline model vs all-features model comparison
4. GridSearchCV hyperparameter tuning with stratified 5-fold CV
5. Model validation with QWK, MAE, and Accuracy
6. Final model training and held-out test evaluation

## Metrics
The notebook reports:
- Quadratic Weighted Kappa (QWK)
- Mean Absolute Error (MAE)
- Accuracy
- Confusion matrix and distribution plots

## How to Run
1. Open [main.ipynb](main.ipynb) in Jupyter or VS Code.
2. Ensure Data_Project.xlsx is in the same folder as the notebook.
3. Run the cells from top to bottom.

## Requirements
This notebook uses standard Python ML tooling:
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

If needed, install dependencies with:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Project Structure
- main.ipynb
- Data_Project.xlsx
- Project_GB Regressor.docx

## Notes
- The test set is used only in Phase C to avoid data leakage.
- The model predictions are rounded and clipped to the 1-5 ordinal scale.
