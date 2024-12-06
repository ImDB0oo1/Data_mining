# US Accident Dataset Analysis and Classification

This repository explores the **US Accident Dataset** with an emphasis on preprocessing, exploratory data analysis, and classification tasks. The project is divided into two major components:

1. **Data Preprocessing and Cleaning** - Preparing the dataset by handling missing values, feature engineering, and removing outliers.
2. **Classification Models** - Applying various machine learning algorithms to predict the severity of accidents.

---

## 1. Data Preprocessing and Cleaning

The **Preprocessing** section ensures the dataset is clean and ready for analysis or modeling. It involves:

- **Handling Missing Values**:
  - Imputing missing values in features like `Wind_Speed(mph)` and `Precipitation(in)` using appropriate methods (e.g., median imputation).
  - Creating indicators for missing values for some features.
- **Datetime Feature Engineering**:
  - Extracting additional features from timestamps (`Year`, `Month`, `Day`, `Hour`, `Minute`, etc.).
  - Calculating the duration of accidents.
- **Outlier Removal**:
  - Removing records with unrealistic values for features like temperature, visibility, and wind speed.
- **Feature Standardization**:
  - Standardizing continuous features for better performance in machine learning models.
- **Categorical Feature Encoding**:
  - Encoding categorical variables for model compatibility.
- **Saving Processed Data**:
  - Saving cleaned datasets, including state-specific subsets (e.g., California), for further analysis.

---

## 2. Classification Models

The **Classification** component applies multiple supervised learning algorithms to predict accident severity. Key highlights include:

### **Algorithms Used**
1. **Decision Tree**:
   - Basic implementation and hyperparameter optimization using `GridSearchCV`.
   - Important feature identification.
2. **Naive Bayes**:
   - Gaussian Naive Bayes classifier for simplicity and fast computation.
3. **Support Vector Machines (SVM)**:
   - Kernel-based classification with hyperparameter tuning.
4. **Neural Networks**:
   - A simple multi-layer perceptron (MLP) with two hidden layers.
5. **LazyClassifier**:
   - Automated comparison of multiple models using the `lazypredict` library.

### **Class Balancing**
To handle class imbalance, upsampling was applied, ensuring equal representation of all severity classes.

### **Performance Metrics**
- Models are evaluated using:
  - **Accuracy**
  - **Classification Report**
  - **Confusion Matrix**

### **Visualization**
- Geographic visualization of accidents by severity using latitude and longitude data.
- Feature importance rankings for decision trees.
- Learning curves for neural network performance.

---
