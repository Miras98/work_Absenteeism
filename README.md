# 📊 Work Absenteeism Analysis using Logistic Regression  

## 📌 Project Overview  
Employee absenteeism is a key factor affecting workplace productivity. 
This project aims to analyze absenteeism patterns and predict **excessive absence** using **Logistic Regression**. 
The **absence time (in hours)** was transformed into a **binary target variable** based on the **median absence hours** as a threshold.

---

## 📂 Dataset Information  
The dataset contains records of employee absenteeism, including personal, social, and work-related factors. 
Key features include:  

- **ID**: Employee ID  
- **Reason for Absence**: Categorical reasons for missing work  
- **Date**: The month in which absence occurred  
- **Transportation Expense**: Cost incurred for commuting  
- **Distance from Residence to Work**: Distance in kilometers
- **Age** : Employee age 
- **Work Load Average/Day**: Average daily workload  
- **BMI**: Body Mass Index of the employee  
- **Education**: Level of education  
- **Children**: Number of children  
- **Pet**: Number of pets  
- **Time Absence (Hours)**: Total hours absent from work  

---

## 🎯 Problem Statement  
The goal is to **predict whether an employee has excessive absence or normal absence** based on various personal and job-related factors.  

- **Target Variable**: `Excessive_Absence`  
- **Transformation**:  
  - If **Time Absence (Hours) > Median**, then **Excessive_Absence = 1** (High Absenteeism)  
  - Otherwise, **Excessive_Absence = 0** (Normal Absenteeism)  

---

## 📊 Data Preprocessing & Feature Engineering  
- **Handling Missing Values**:  
  - Imputed missing values using median or mode based on the feature type.  
- **Encoding Categorical Variables**:  
  - One-hot encoding for categorical variables such as "Reason for Absence."  
- **Feature Scaling**:  
  - Standardized numerical features using **StandardScaler** to improve model performance.  
- **Outlier Detection & Removal**:  
  - Used **IQR method** to filter out extreme outliers in numerical columns.  

---

## 🧠 Model Training: Logistic Regression  
- **Train-Test Split**:  
  - 80% Training Data  
  - 20% Testing Data  
- **Algorithm**:  
  - Logistic Regression (`sklearn.linear_model.LogisticRegression`)  
- **Evaluation Metrics**:  
  - **Accuracy**  
  - **Precision & Recall**  
  - **F1-Score**  
  - **Confusion Matrix**  

---

## 📈 Results & Key Findings  
1. **Feature Importance**:  
   - Factors such as **transportation expenses, workload, and BMI** influenced absenteeism.  
2. **Model Performance**:  
   - The model achieved **82.09% accuracy** in predicting excessive absenteeism.  
3. **Insights**:  
   - Employees with **higher transportation expenses** and **longer commutes** showed increased absenteeism.  
   - **Social smokers** had a higher likelihood of excessive absence.  

---

## 🚀 Recommendations  
1. **Work-from-Home Policy**: Implement flexible or remote work options for employees with **long commutes** to reduce absenteeism.  
2. **Health & Wellness Programs**: Introduce **fitness and mental health initiatives** to reduce absenteeism due to **BMI-related issues**.  
3. **Employee Assistance Programs**: Provide **support for social smokers** to reduce their absenteeism rates.  

---
