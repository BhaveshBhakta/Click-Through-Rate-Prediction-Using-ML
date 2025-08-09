## Click-Through Rate Prediction

### Project Overview

This project aims to predict the **Click-Through Rate (CTR)** on online advertisements based on user demographics and online behavior. By analyzing features such as daily time spent on a site, age, area income, daily internet usage, and user location, the goal is to develop a machine learning model that can accurately forecast whether a user will click on an ad. This is a critical task for digital marketing and ad targeting.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Click-Through Rate Prediction](https://www.kaggle.com/datasets/swekerr/click-through-rate-prediction)
  * **Size**: 10000 entries, 10 columns. After data cleaning (dropping duplicates) and feature engineering, the dataset is adjusted.
  * **Key Features**:
      * `Daily Time Spent on Site`, `Age`, `Area Income`, `Daily Internet Usage`, `Ad Topic Line`, `City`, `Gender`, `Country`, and new features engineered from `Timestamp`.
  * **Approach**:
      * **Data Cleaning**: Dropped duplicate rows.
      * **Feature Engineering**: The `Timestamp` column was converted to datetime objects, and new features like 'Year', 'Month', 'Day', 'Hour', 'Day\_of\_Week', 'Is\_Weekend', and 'Part\_of\_Day' were extracted. The original `Timestamp` column was then dropped.
      * **Exploratory Data Analysis**: Histograms, Boxplots, and a heatmap were used for visualization. Count plots were also used for categorical features.
      * **Label Encoding**: Applied to all columns, including categorical features and the numerical features and the target 'Clicked on Ad'.
      * **Binary Classification**: The target variable `Clicked on Ad` indicates whether an ad was clicked (`1`) or not (`0`). The dataset is fairly balanced.
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * 86.8% with XGBoost Classifier.
      * 84.8% with Random Forest Classifier.
      * 82.3% with Gradient Boosting Classifier.

-----

### Purpose and Applications

  * **Optimize ad placement and targeting** for digital marketing campaigns.
  * Improve ad relevance for users, leading to a better user experience.
  * Forecast campaign performance and allocate advertising budgets more effectively.
  * Support data-driven decision-making in the advertising technology (AdTech) industry.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Click-Through-Rate-Prediction-Using-ML.git
cd Click-Through-Rate-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for all models to achieve optimal performance.
  * Exploring more sophisticated feature engineering, particularly from the text-based columns like `Ad Topic Line` and `City`.
  * Investigating alternative encoding methods for categorical features (e.g., One-Hot Encoding) and comparing their impact on model performance.
  * Adding explainability (e.g., SHAP or LIME) to understand which user characteristics are the most significant drivers of ad clicks.
