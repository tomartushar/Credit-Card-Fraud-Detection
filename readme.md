# Credit Card Fraud Detection

Design a model to recognize fraudulent credit card transactions.

## Dataset

The dataset is available on [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

* Instead of actual features, PCA components are available in the dataset along with transaction amount and elapsed time.
* Data-Splits: Train/Dev/Test

## Analysis

* Perform basic data exploration.
* Check for missing values.
* Check for outliers.
* Perform univariate analysis (using ANOVA technique).
* Perform bivariate analysis.

## Utilities

* **Feature Scaling**: *RobustScaler* is used in logistic regression modeling.
* **Feature Selection**: *Recursive Feature Elimination* algorithm is used to determine the best feature combination.
* **Data Imbalance**: *SMOTEENN* Hybrid and *ClusterCentroid* downsampling algorithms have been experimented with to address class imbalance problems.
* **Hyperparameter Tuning**: *GridSearchCV* algorithm is used to set the hyperparameter values.

## Evaluation

* *Area Under Precision-Recall* curve is used as the main metric in imbalanced data settings.
* Also, the *F1-score* is reported.

## Results

| Model               | F1-score | AUPR |
|---------------------|----------|------|
| Logistic Regression | 0.76     | 0.59 |
| Decision Tree       | 0.67     | 0.60 |
| Random Forest       | 0.72     | 0.63 |
| XGBoost             | 0.67     | 0.61 |

