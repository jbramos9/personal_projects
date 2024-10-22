# Credit Card Fraud Analysis

### Problem
Credit card companies need to accurately identify fraudulent transactions to protect customers from unauthorized charges. The challenge is that fraudulent transactions make up only a small portion of all transactions, leading to a highly imbalanced dataset. With limited data on fraudulent activities (0.172% of transactions), the task of detecting fraud becomes more difficult. Furthermore, the dataset is anonymized with PCA-transformed features, adding another layer of complexity to the analysis.

### Objective
The objective is to develop a machine learning model that can effectively detect fraudulent credit card transactions, despite the significant class imbalance. The model's performance will be evaluated using the Area Under the Precision-Recall Curve (AUPRC), which is more suitable for imbalanced classification problems than traditional accuracy metrics.

### Dataset Description
The dataset consists of credit card transactions made by European cardholders in September 2013. It includes 284,807 transactions over a two-day period, with 492 fraudulent transactions (0.172%). Due to confidentiality concerns, the original features have been transformed using Principal Component Analysis (PCA). The dataset contains the following variables:
- V1 to V28: Principal components derived from PCA.
- Time: The seconds elapsed between each transaction and the first transaction in the dataset.
- Amount: The transaction amount, which can be used for cost-sensitive learning.
- Class: The target variable, where 1 represents fraud and 0 represents non-fraud.

Dataset source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

### Methodology

1. Data Ingestion
   - The dataset was loaded and prepared for analysis, ensuring that all necessary data points were included for further processing.
2. Data Quality Checks
   - Data Imbalance: Addressed the significant class imbalance issue, with fraud transactions making up only 0.172% of the data.
   - Missing Values: Checked for any missing values that could impact the model's performance.
   - Duplicates: Identified and handled duplicate entries to maintain data integrity.
3. Exploratory Data Analysis (EDA)
   - Auto-EDA: Used automated exploratory techniques to quickly gain insights from the data.
   - Outlier Analysis: Investigated and handled any outliers that could distort model results.
   - Correlation Analysis: Analyzed the correlation between features to understand relationships and reduce redundancy.
4. Data Preparation
   - Prepared the data for modeling by applying necessary transformations and handling class imbalance.
5. Modelling
    - Approaches
      - Regular Training: Standard logistic regression training.
      - Feature Selection: Selected important features to improve model efficiency.
      - Undersampling & Oversampling: Handled class imbalance by undersampling the majority 
    - Models
      - Logistic Regression
      - Decision Trees
      - Random Forest
      - XGBoost
6. Results
   - Evaluated the performance of the models using appropriate metrics, given the class imbalance, with a focus on precision-recall metrics to avoid misleading accuracy results.

### Libraries
Scikit-Learn, XGBoost, NumPy, Pandas, Plotly, Seaborn, Matplotlib, Pandas Profiling