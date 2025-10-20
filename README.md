## Marketing Campaign Succes Estimation Project – Random Forest & KNN

This project develops predictive models to estimate customer responses to marketing campaigns. The goal is to classify whether a customer will respond positively (result = 0) or not (result = 1) using demographic and financial data.

## Dataset & Features
- Dataset: marketing.csv (training), marketing_test.xlsx (test)
- Target: result (0 = yes, 1 = no)
- Features include: ID, balance, age, day, month, job, marital, education, housing, loan, contact, campaign, response, age_group, balance_rate, is_high_risk

## Data Preprocessing
- Removed irrelevant columns (pdays, previous, default)
- Encoded categorical features (LabelEncoder & mapping)
- Outlier handling using IQR
- Normality check (Kolmogorov-Smirnov test)
- Feature selection via Spearman correlation and multicollinearity (VIF)
- Standardization and one-hot encoding for KNN

## Modeling & Evaluation
- Train/Test split: 70/30
- Random Forest:
  - Feature importance filtering (0.05–0.35)
  - Hyperparameter tuning with Optuna
- KNN:
  - Hyperparameter tuning with Optuna
- Evaluation metrics: Gini, ROC-AUC, Precision, Recall, confusion matrix

## Prediction Workflow
1. Preprocess test data
2. Feature engineering: age_group, balance_rate, is_high_risk
3. Outlier handling
4. One-hot encoding & scaling for KNN
5. Generate predictions and probability scores

## Technologies
Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn, Optuna, SciPy

