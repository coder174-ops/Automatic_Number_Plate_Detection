# 📊 HR Analytics – Employee Attrition Prediction

## 🎯 Overview
End-to-end HR analytics project analyzing 1,470 employee records (after removing duplicates) to identify attrition drivers using Python, machine learning, and Power BI visualization.

## 🔍 Problem Statement
High employee attrition impacts recruitment costs and productivity. This project identifies key turnover factors and evaluates whether at-risk employees can be predicted from workforce data.

## 📂 Project Components

### 1. Data Cleaning & EDA (Python)
- Started with 1,480 employee records across 38 attributes; removed 10 duplicate records (1,470 final)
- Dropped constant/no-value columns (EmployeeCount, Over18, StandardHours)
- Imputed missing tenure values (YearsWithCurrManager) using median
- Performed EDA and correlation analysis across demographic, compensation, and tenure attributes
- Identified attrition drivers: overtime, salary band, job level, tenure, and commute distance

### 2. Predictive Modeling (Machine Learning)
- Built and compared **two classification models**: Logistic Regression and Random Forest
- Applied one-hot encoding for nominal categorical features (Department, Job Role, Marital Status, etc.)
- Addressed class imbalance (only ~16% attrition) using class weighting and decision threshold tuning
- Evaluated both models using Accuracy, Precision, Recall, and F1-Score
- **Selected Logistic Regression as the final model** — while Random Forest had higher accuracy and precision, Logistic Regression achieved substantially better Recall and F1-score, which matters more for identifying at-risk employees in an imbalanced problem
- Generated feature importance rankings from the Random Forest model to support the exploratory analysis

### 3. Interactive Dashboard (Power BI)
- Real-time attrition metrics and KPIs (headcount, attrition rate, average salary, average tenure)
- Department-wise, role-wise, gender-wise, and salary-band analysis
- Interactive filters and slicers for workforce insights
- Built independently on the raw dataset using Power BI's own data-cleaning layer (Power Query)

## 🔑 Key Findings

| Factor | Impact |
|---|---|
| Salary Range | Upto 5K: 21.76% attrition vs. 15K+: 3.76% attrition (~6x difference) |
| Overtime | ~30% attrition for employees working overtime vs. ~10% for those who don't — the strongest single driver |
| Job Level | Lower job levels correlate with higher turnover |
| Tenure | More years at company, in current role, and with current manager = lower attrition risk |
| Commute Distance | Longer distance shows a weak positive correlation with attrition |
| Model Performance | Logistic Regression: 79.2% Recall, 57.1% F1 vs. Random Forest: 34.0% Recall, 46.2% F1 |

## 💡 Recommendations
- Review compensation structure for entry-level and lowest salary-band roles
- Monitor and reduce excessive overtime — the single strongest attrition driver identified
- Strengthen career development pathways for lower job levels
- Focus retention efforts on early-tenure employees, Sales, and Lab Technician roles
- Use the Logistic Regression model to flag at-risk employees for proactive retention outreach

## 🛠️ Tech Stack
- **Python:** Pandas, NumPy, Scikit-learn
- **Visualization:** Matplotlib, Seaborn, Power BI
- **Development:** Jupyter Notebook

## 📁 Project Files
- `HR_Analytics.ipynb` – Python data cleaning, EDA, and ML modeling (Logistic Regression vs Random Forest)
- `HR_Analytics.csv` – Employee dataset (1,480 raw records)
- `HR_Analytics_Dashboard.pbix` – Power BI dashboard

## 🎯 Skills Demonstrated
- Python & Data Analysis (Pandas, NumPy)
- Machine Learning, Classification & Model Comparison
- Handling Class Imbalance (class weighting, threshold tuning)
- Statistical Analysis & EDA
- Data Visualization (Power BI, Matplotlib, Seaborn)
- Business Intelligence & HR Analytics

---
## Dashboard Preview

![HR Analytics Dashboard](images/dashboard.jpeg)
---

**Author:** Tanuja  
