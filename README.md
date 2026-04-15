# 🏥 Hospital Medical Expenses Prediction  etu- sedougq kenza

## 📌 Project Overview

This project aims to analyze hospital data and build a machine learning model to predict **medical expenses** based on operational and patient-related factors.

The project covers the full Data Science workflow:

* Data Cleaning
* Feature Engineering
* Exploratory Analysis
* Machine Learning Modeling
* Model Evaluation
* Prediction Export for Visualization (Power BI)

---

## 📂 Dataset

The dataset contains hospital-related information such as:

* Doctors Count
* Patients Count
* Department
* Location
* Admission & Discharge Dates
* Medical Expenses

---

## 🧹 Data Preprocessing

The following steps were applied:

* Removed duplicates
* Cleaned column names
* Converted text fields to proper format
* Converted numeric columns and handled errors
* Parsed date columns
* Removed invalid negative values

---

## ⚙️ Feature Engineering

New features were created to improve model performance:

* **Stay_Days** = مدة إقامة المريض
* **Cost_per_Patient** = التكلفة لكل مريض
* **Year / Month** from admission date

---

## 🤖 Machine Learning Model

### Model Used:

* Random Forest Regressor

### Features:

* Doctors_Count
* Patients_Count
* Stay_Days
* Department (encoded)
* Location (encoded)

---

## 📊 Model Evaluation

The model was evaluated using:

* **R² Score** → Measures how well the model explains the data
* **MAE (Mean Absolute Error)** → Average prediction error

---

## 🔧 Model Optimization

Hyperparameter tuning was applied using **GridSearchCV**:

* n_estimators: [100, 200]
* max_depth: [5, 10, 15]

Best parameters were selected automatically.

---

## 📈 Feature Importance

The most influential features in predicting medical expenses were:

* Patients_Count
* Doctors_Count
* Stay_Days

This indicates that both hospital load and patient duration significantly impact costs.

---

## 🔮 Predictions

The model was used to generate predictions for the dataset:

* A new column **Predicted_Expenses** was added
* Results exported to `predictions.csv`
* Used later in Power BI for visualization

---

## 📊 Power BI Dashboard

A dashboard was built to visualize:

### 🔹 KPIs:

* Total Medical Expenses
* Total Patients
* Total Doctors
* Average Stay Days

### 🔹 Analysis:

* Expenses by Department
* Expenses over Time
* Geographic Distribution

### 🔹 Machine Learning Insights:

* Actual vs Predicted Expenses
* Error Analysis

---

## 🚀 Key Insights

* Patient volume is the strongest driver of expenses
* Longer stays increase total costs significantly
* Some locations/departments show higher prediction errors
* Resource allocation (doctors vs patients) impacts efficiency

---

## 🛠️ Technologies Used

* Python (Pandas, NumPy, Scikit-learn)
* Machine Learning (Random Forest)
* Power BI (Data Visualization)

---

## 📁 Project Structure

```
├── Hospital_Data.csv
├── predictions.csv
├── notebook.ipynb
├── README.md
```

---

## ✅ Future Improvements

* Add more features (e.g., patient conditions)
* Try advanced models (XGBoost, LightGBM)
* Deploy as a web app (Flask / Streamlit)
* Automate data pipeline

---

## 📌 Conclusion

This project demonstrates an end-to-end Data Science workflow, combining data preprocessing, machine learning, and business intelligence to generate actionable insights in the healthcare domain.
