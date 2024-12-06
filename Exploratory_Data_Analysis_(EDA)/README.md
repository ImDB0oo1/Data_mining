# Exploratory Data Analysis (EDA) Repository

This repository contains two projects showcasing Exploratory Data Analysis (EDA) techniques and feature extraction. The projects focus on understanding datasets through visualization, statistical analysis, and preparation for machine learning.

---

## Projects Overview

### 1. **EDA and Feature Extraction on Bike Dataset**
**Objective:** Analyze and preprocess a bike-sharing dataset to understand its patterns and prepare it for predictive modeling.

- **Key Steps:**
  - **Data Cleaning:**
    - Handled duplicate values and missing data.
    - Converted categorical variables into numerical using one-hot encoding.
  - **Visualization:**
    - Explored relationships between features using box plots and pair plots.
    - Created correlation heatmaps to identify significant relationships.
  - **Feature Scaling:**
    - Used `MinMaxScaler` to normalize numerical features for better model compatibility.
  - **EDA Techniques:**
    - Plotted distributions of bike-sharing counts (`cnt`) against various features like season, weather, and holidays.

- **Notable Libraries:**
  - `dataprep` for missing data visualization and correlation analysis.
  - `seaborn` and `matplotlib` for detailed visualizations.

➡️ **[Explore the Bike Dataset EDA Project](./EDA_and_feature_extraction_on_bike_dataset.ipynb)**

---

### 2. **EDA on US Counties 2022 COVID-19 Dataset**
**Objective:** Analyze COVID-19 case and death trends across US counties and states for the year 2022.

- **Key Steps:**
  - **Data Transformation:**
    - Added a `day` feature to track the progression of the pandemic.
    - Aggregated data by day and state for trend analysis.
  - **Time Series Analysis:**
    - Computed 7-day moving averages for cases, deaths, and mortality rates to smooth out fluctuations.
    - Visualized trends in cases, deaths, and mortality rates over time.
  - **State-Level Analysis:**
    - Compared COVID-19 metrics across key states like California, Texas, and Florida.
    - Created bar and pie charts for cases, deaths, and mortality rates per state.
  - **Visualization:**
    - Line plots for overall trends.
    - Comparative bar and pie charts for state-level insights.

- **Notable Libraries:**
  - `matplotlib` for comprehensive time-series and state-level visualizations.
  - `pandas` for data transformation and aggregation.

➡️ **[Explore the US Counties COVID-19 Dataset Project](./EDA_on_us_counties_2022_corona_dataset.ipynb)**

---

## Repository Highlights
- **Comprehensive EDA Workflow:** Both projects demonstrate the process of data cleaning, visualization, and feature extraction.
- **Diverse Visualizations:** Includes correlation heatmaps, box plots, moving averages, bar plots, and pie charts for clear insights.
- **Ready-to-Use Code:** The notebooks are well-documented for easy understanding and adaptation.

---

