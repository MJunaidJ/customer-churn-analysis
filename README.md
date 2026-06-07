# Customer Churn Analysis (Telco Dataset)

## Project Overview

Customer churn is one of the most important business challenges faced by subscription-based companies. Customer churn occurs when a customer stops using a company's products or services.

This project analyzes a Telco Customer Churn dataset, performs data cleaning and exploratory data analysis (EDA), and builds a Machine Learning model to predict whether a customer is likely to churn.

The goal is to identify patterns and factors associated with customer churn and develop a predictive model that can help businesses improve customer retention strategies.

---

## Dataset

The dataset contains information about 7,000+ telecom customers, including:

* Customer demographics
* Service subscriptions
* Contract information
* Billing information
* Monthly charges
* Total charges
* Churn status

### Features Included

* Gender
* Senior Citizen
* Partner
* Dependents
* Tenure
* Phone Service
* Multiple Lines
* Internet Service
* Online Security
* Online Backup
* Device Protection
* Tech Support
* Streaming TV
* Streaming Movies
* Contract Type
* Paperless Billing
* Payment Method
* Monthly Charges
* Total Charges

### Target Variable

* Churn

  * Yes = Customer left the service
  * No = Customer remained with the service

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## Project Workflow

### 1. Data Loading

The Telco Customer Churn dataset was loaded into a Pandas DataFrame for analysis.

### 2. Data Exploration

Performed:

* Dataset shape inspection
* Data type analysis
* Descriptive statistics
* Missing value detection

### 3. Data Cleaning

The following preprocessing steps were performed:

* Identified blank values in the TotalCharges column
* Replaced blank values with NaN
* Converted TotalCharges to numeric format
* Removed rows containing missing values
* Removed the customerID column since it does not contribute to prediction

### 4. Feature Engineering

The target variable (Churn) was converted into binary format:

* Yes → 1
* No → 0

Categorical features were converted using One-Hot Encoding.

### 5. Exploratory Data Analysis (EDA)

Several visualizations were created to understand customer behavior:

#### Churn Distribution

* Examined the balance between churned and retained customers.

#### Monthly Charges vs Churn

* Customers with higher monthly charges showed a higher tendency to churn.

#### Tenure vs Churn

* Customers with shorter tenure were more likely to churn.

### 6. Model Building

A Logistic Regression model was trained using:

* Train-Test Split (80%-20%)
* Feature Scaling using StandardScaler
* Logistic Regression Classification

### 7. Model Evaluation

The model was evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report

---

## Results

### Model Accuracy

Accuracy: 78.75%

### Confusion Matrix

| Actual / Predicted | No Churn | Churn |
| ------------------ | -------- | ----- |
| No Churn           | 915      | 118   |
| Churn              | 181      | 193   |

### Classification Metrics

| Metric    | No Churn | Churn |
| --------- | -------- | ----- |
| Precision | 0.83     | 0.62  |
| Recall    | 0.89     | 0.52  |
| F1-Score  | 0.86     | 0.56  |

---

## Key Insights

* Customers with higher monthly charges are more likely to churn.
* Customers with shorter tenure have a higher churn rate.
* Contract type plays a significant role in customer retention.
* Logistic Regression achieved nearly 79% prediction accuracy on unseen data.

---

## Future Improvements

Possible enhancements include:

* Random Forest Classifier
* XGBoost Classifier
* Hyperparameter Tuning
* Feature Selection
* Handling Class Imbalance using SMOTE
* Model Deployment using Flask or FastAPI
* Interactive Dashboard using Streamlit

---

## Repository Structure

```text
customer-churn-analysis/
│
├── Customer_Churn_Analysis.ipynb
├── README.md
└── Telco Customer Churn Dataset.csv
```

---

## Author

Muhammad Junaid Jamshed

Software Engineering Graduate | Data Analytics & Machine Learning Enthusiast

GitHub: https://github.com/MJunaidJ
