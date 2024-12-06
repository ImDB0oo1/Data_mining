# Fraud Detection with Transaction Data

This repository demonstrates an end-to-end fraud detection pipeline using transaction data. The project includes data preprocessing, exploratory data analysis, feature engineering, and machine learning model implementations to classify fraudulent transactions.

---

## Table of Contents

- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Engineering](#feature-engineering)
- [Modeling and Evaluation](#modeling-and-evaluation)
  - [Without PCA](#without-pca)
  - [With PCA](#with-pca)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)

---

## Exploratory Data Analysis

- **Dataset Summary**:
  - Columns include `type`, `amount`, `oldbalanceOrig`, `newbalanceOrig`, and more.
  - Target variable: `isFraud`.
  - Proportion of fraudulent transactions: 0.13%.

- **Visualizations**:
  - Distribution of transaction types, amounts, and balances.
  - Correlation heatmaps for numerical features.

- **Insights**:
  - Fraudulent transactions are concentrated in specific transaction types.
  - Imbalances in data distribution necessitate resampling.

---

## Feature Engineering

1. **New Features**:
   - `balancediffOrig`: Difference between old and new balance for origin.
   - `balancediffDest`: Difference between old and new balance for destination.
   - `merchant`: Boolean indicating merchant-related transactions.

2. **Handling Imbalances**:
   - Undersampling was applied to balance the classes for training.

3. **One-Hot Encoding**:
   - Encoding of categorical features like `type`.

4. **Principal Component Analysis (PCA)**:
   - Dimensionality reduction to 4 components for enhanced performance and interpretability.

---

## Modeling and Evaluation

### Without PCA

Models implemented on the full feature set:

1. **Decision Tree**:
   - Used for initial exploration and feature importance ranking.
   - Visualization of decision tree structure.

2. **Logistic Regression**:
   - Baseline model for comparison.

3. **XGBoost**:
   - Gradient boosting for high performance.
   - Feature importance plotted based on the learned model.

4. **Random Forest**:
   - Ensemble learning technique for improved accuracy.

### With PCA

Models implemented on reduced feature set:

1. **Decision Tree**:
   - Evaluated on the 4 principal components.
   - Feature importance visualization for PCA components.

2. **Logistic Regression**:
   - Evaluated on PCA components for performance benchmarking.

3. **XGBoost**:
   - Gradient boosting with PCA for feature importance and high precision.

4. **Random Forest**:
   - Evaluated on PCA-transformed data.

---

## Results

### Top Features Impacting Fraud Detection
Key features identified during modeling:
- `type`: Transaction type.
- `amount`: Transaction amount.
- `balancediffOrig`: Difference in origin balances.
- `balancediffDest`: Difference in destination balances.

### Model Performance (Without PCA)
| Model               | Precision | Recall | F1-Score | AUC  |
|---------------------|-----------|--------|----------|------|
| Decision Tree       | 0.92      | 0.91   | 0.91     | 0.95 |
| Logistic Regression | 0.85      | 0.84   | 0.84     | 0.87 |
| XGBoost             | 0.94      | 0.93   | 0.93     | 0.97 |
| Random Forest       | 0.93      | 0.92   | 0.92     | 0.96 |

### Model Performance (With PCA)
| Model               | Precision | Recall | F1-Score | AUC  |
|---------------------|-----------|--------|----------|------|
| Decision Tree (PCA) | 0.90      | 0.88   | 0.89     | 0.93 |
| Logistic Regression | 0.83      | 0.82   | 0.82     | 0.85 |
| XGBoost (PCA)       | 0.93      | 0.92   | 0.92     | 0.95 |
| Random Forest (PCA) | 0.91      | 0.90   | 0.90     | 0.94 |

---

## References

- [XGBoost Documentation](https://xgboost.readthedocs.io)
- [Scikit-learn](https://scikit-learn.org)


