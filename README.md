# Telecom Customer Churn Prediction 📊🧠

This project focuses on predicting customer attrition (Churn) for a telecommunications company using Machine Learning. The goal is to identify high-risk customers proactively so the business can take retention actions.

## 📌 Project Overview
Customer churn is a critical metric for telecom companies. In this project, we analyze customer behaviors, demographics, and contract types to build a predictive model.

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Random Forest)
* **Imbalanced Data Handling:** Imbalanced-Learn (SMOTE)

## 📊 Key Insights from EDA (Exploratory Data Analysis)
* The original dataset suffers from class imbalance: **~26.5% of customers churned**, while ~73.5% stayed.
* Customers with **Month-to-month contracts** show a significantly higher churn rate compared to one or two-year contracts.

## ⚙️ Data Preprocessing & Cleaning
* Handled hidden missing values in the `TotalCharges` column and converted it to numerical.
* Dropped irrelevant columns like `customerID`.
* Encoded categorical variables using One-Hot Encoding (`pd.get_dummies`).
* Split the dataset into 80% training and 20% testing sets.

## 🚀 Model & Results

### 1. Baseline Random Forest
* **Global Accuracy:** 78.54%
* **Churn Recall (Class 1):** 48% (The model missed about half of the leaving customers due to class imbalance).

### 2. Random Forest + SMOTE (Optimized)
To fix the imbalance, we applied **SMOTE** (Synthetic Minority Over-sampling Technique) to clone minority class examples synthetically.
* **Churn Recall (Class 1):** Boosted to **57%** 🚀
* **Business Impact:** The model is now much more aggressive and effective at detecting customers who are actually planning to leave, allowing the marketing team to target them efficiently.
