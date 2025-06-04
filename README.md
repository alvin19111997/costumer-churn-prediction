# Customer Churn Prediction Project (PRCL-0017)

## 📌 Overview

This project focuses on predicting customer churn for *No-Churn Telecom, a European telecom operator aiming to reduce customer attrition through machine learning. The model generates a **Churn Risk Score* and a *binary CHURN-FLAG*, enabling business teams to identify high-risk customers and launch targeted retention campaigns.

---

## 🎯 Project Goals

1. Identify the key variables influencing customer churn.
2. Create Churn Risk Scores to guide retention strategies.
3. Generate a CHURN-FLAG (YES = 1, NO = 0) to segment customers for personalized campaigns.

---

## 🗂 Dataset Description

- *Source*: Provided telecom dataset
- *Total Records*: 4,617 customers
- *Features*:
  - Categorical: State, Area Code, International Plan, VMail Plan
  - Numerical: Account Length, Minutes & Charges (Day, Evening, Night), International Usage, Customer Service Calls
  - Target: Churn (0 = No, 1 = Yes)

---

## 🧠 Machine Learning Workflow

### 📌 Preprocessing
- Dropped identifier columns (Phone)
- Scaled numerical features using MinMaxScaler
- Applied appropriate encoding (Ordinal/Binary/OneHot)

### 🔍 EDA
- Detected imbalance in churn labels (~11% churned)
- Visualized feature distributions and correlations

### ⚙ Models Trained
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost ✅ (Best performing model)

### 📈 Evaluation Metrics
| Model             | Accuracy | Precision (Class 1) | Recall (Class 1) | F1 Score (Class 1) |
|------------------|----------|----------------------|------------------|--------------------|
| *XGBoost*       | 0.95     | 0.85                 | 0.80             | 0.82               |
| Gradient Boosting| 0.93     | 0.74                 | 0.82             | 0.78               |
| Random Forest    | 0.94     | 0.76                 | 0.81             | 0.79               |

---

## 🔑 Key Deliverables

- ✅ Trained churn prediction model (XGBoost)
- ✅ Churn_Risk_Score and CHURN-FLAG generation
- ✅ Exported list of churn-prone customers with their risk scores
- ✅ Business-ready report in Word format

---

## 📤 Output Files

- final_churn_dataset.csv — Cleaned and feature-engineered dataset
- churn_predictions.csv — Predictions including:
  - Phone, State, Churn_Risk_Score, CHURN-FLAG
- Churn_Report.docx — Summary report for business stakeholders

---

## 🛠 Tools & Libraries

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Seaborn & Matplotlib
- Jupyter Notebook

---

## 🔍 How to Use

1. Clone the repository  
2. Run the Jupyter Notebook: Customer_Churn_Prediction.ipynb
3. Replace the dataset with new customer records (if needed)
4. Re-run prediction and export results

---

## 💡 Business Impact

- Enables retention-focused marketing via churn segmentation
- Supports customer service prioritization for high-risk users
- Reduces churn rate with data-backed campaign targeting

---

## 📎 Appendix

- Model trained on 75% of the dataset (random split)
- SMOTE applied to balance class distribution
- Threshold for CHURN-FLAG set at *0.5*

