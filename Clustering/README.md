# Clustering Analysis on Credit Card General Dataset

This repository contains an end-to-end implementation of clustering techniques applied to a Credit Card dataset. The project involves preprocessing, dimensionality reduction, and the application of clustering algorithms to derive meaningful insights from customer data.

---

## Project Objectives

1. **Exploratory Data Analysis (EDA):**
   - Understand the dataset structure and clean missing values.
   - Detect and handle outliers using statistical methods.
   - Visualize data distribution and relationships using histograms, scatter plots, and correlation heatmaps.

2. **Preprocessing:**
   - Scale numerical features for clustering using `StandardScaler`.
   - Perform dimensionality reduction using Principal Component Analysis (PCA).

3. **Clustering Algorithms:**
   - Explore various clustering techniques including:
     - **Agglomerative Clustering**
     - **K-Means Clustering**
     - **K-Medoids Clustering**
     - **Gaussian Mixture Models (GMM)**
     - **DBSCAN**
   - Evaluate clustering results using metrics like:
     - Silhouette Score
     - Davies-Bouldin Index
     - Calinski-Harabasz Index

4. **Insights Extraction:**
   - Analyze clusters to identify customer segments based on key features such as:
     - Balance
     - Purchases
     - Cash Advances
     - Credit Limit
     - Payment Behavior

---

## Key Features

### 1. Exploratory Data Analysis (EDA)
- Identified missing values and imputed them using mean values.
- Detected outliers and addressed them to refine data quality.
- Visualized feature distributions using histograms and KDE plots.
- Analyzed correlations between variables through heatmaps.

### 2. Preprocessing and PCA
- Standardized features for uniform scaling.
- Reduced data dimensions to 2 and 3 components using PCA.
- Visualized principal components to understand data variance.

### 3. Clustering Techniques
#### Agglomerative Clustering
- Applied hierarchical clustering with linkage methods like Ward, Average, and Complete.
- Compared clustering performance using evaluation metrics.

#### K-Means Clustering
- Used the Elbow Method to determine the optimal number of clusters.
- Compared clustering results for 2 and 3 PCA components.

#### K-Medoids Clustering
- Experimented with distance metrics (Manhattan, Euclidean, Cosine) to improve cluster quality.
- Visualized clustering results and centroids.

#### Gaussian Mixture Models (GMM)
- Evaluated clustering results for covariance types: Full, Tied, Diagonal, and Spherical.
- Generated scatter plots to analyze clustering performance.

#### DBSCAN
- Tuned hyperparameters like epsilon (`eps`) and minimum samples to identify clusters.
- Compared performance metrics to select the optimal model.

### 4. Cluster Analysis
- Segmented customers into distinct groups based on clustering results.
- Analyzed key features such as Balance, Purchases, and Credit Limit for each cluster.
- Provided detailed histograms and scatter plots for visual comparison of clusters.

---

