# telecom-customer-churn-analysis
# 📊 Telecom Customer Churn Analysis: End-to-End Analytics & Prescriptive Strategy

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-EDA-150458?style=for-the-badge&logo=pandas&logoColor=white)

## 📌 Project Overview
Customer churn is one of the most significant challenges faced by telecommunications companies, as retaining existing customers is substantially more cost-effective than acquiring new ones. This project presents an end-to-end analytics solution that identifies churn drivers, predicts customer attrition, and recommends actionable retention strategies.

By combining data cleaning, exploratory data analysis (EDA), statistical hypothesis testing, business intelligence reporting, machine learning, and prescriptive analytics, this workflow transforms raw telecom customer data into executive-ready business decisions.

---

## 🎯 Business Problem & Objectives
Telecom providers lose substantial recurring revenue when customers discontinue their services. The core objectives of this project are to:
* **Data Preparation:** Perform thorough data cleaning, validation, and preprocessing.
* **Exploratory Analysis:** Conduct EDA to uncover behavioral and usage patterns.
* **BI Reporting:** Build an interactive Power BI dashboard to monitor churn KPIs.
* **Statistical Validation:** Apply hypothesis testing and regression to isolate statistically significant churn drivers.
* **Predictive Modeling:** Develop a Random Forest classification model to score churn risk.
* **Prescriptive Strategy:** Recommend targeted, data-driven customer retention initiatives.

---

## 📈 Dataset Summary & Headline KPIs
Analysis was conducted on the `churn-bigml-80.csv` telecom customer dataset comprising **2,666 customer accounts**:

| Metric | Value | Business Context |
| :--- | :--- | :--- |
| **Total Customers** | **2,666** | Complete active & churned customer base analyzed |
| **Churned Customers** | **388** | Accounts that discontinued service |
| **Overall Churn Rate** | **14.55%** | Baseline attrition rate across the portfolio |
| **Revenue Lost to Churn** | **\$25,157.85** | Direct monthly revenue exposure from churned accounts |
| **Avg. Customer Service Calls** | **1.56** | Mean support interactions per customer |

---

## 🔄 End-to-End Project Workflow

### 1. Data Cleaning & Preparation
* Verified dataset integrity and schema consistency across 2,666 records.
* Audited for missing values and duplicate customer records.
* Standardized categorical and boolean variables (`Churn`, `International plan`, `Voice mail plan`) for statistical and machine learning compatibility.
* Engineered total usage and charge metrics for financial impact modeling.

### 2. Exploratory Data Analysis (EDA)
Key behavioral dimensions analyzed:
* Customer call usage patterns (Day, Evening, Night, and International minutes/charges)
* Revenue contribution across customer segments
* Customer service call frequency and support friction
* International plan and voice mail plan adoption rates

> **Key EDA Insight:** Customers making **four or more customer service calls** exhibited dramatically higher churn rates, pinpointing unresolved support issues as a critical retention risk.

### 3. Business Intelligence Dashboard (Power BI)
[Power BI Dashboard Preview](images/dashboard_preview.png)
An interactive Power BI executive dashboard was built to track:
!"C:\Users\Admin\OneDrive\Pictures\Screenshots\Screenshot 2026-11-24 102334.png"
* **Headline KPI Cards:** Total Customers (2,666), Churn Count (388), Churn Rate (14.55%), Revenue at Risk (\$25,157.85), and Avg. Service Calls (1.56).
* **Segment & Trend Breakdowns:** Churn distribution across customer service call tiers, geographic states, international plan adoption, and charge brackets.
* Business Intelligence & Statistical Validation
* **Task 1 — Power BI Executive Dashboard:** [`telecom_customer_churn.pbix`](bi_dashboard/telecom_customer_churn.pbix)
  * Built an interactive report tracking KPI cards, regional churn breakdowns, service call thresholds, and international plan exposure.
  
  ![Executive Dashboard](bi_dashboard/screenshots/01_executive_kpi_overview.png)

### 4. Statistical Analysis
To validate visual patterns from EDA, formal statistical tests were conducted:
* **Methods Applied:** Independent Two-Sample T-Test, Chi-Square Test of Independence, and Logistic Regression.
* **Statistically Significant Drivers:**
  1. Customer service call frequency
  2. Daytime charge and minute volume
  3. Active international plan subscription

### 5. Predictive Modeling
* **Algorithm:** Random Forest Classifier
* **Evaluation Framework:** Confusion Matrix, ROC-AUC Score, and Feature Importance ranking.
* **Outcome:** Successfully classified high-risk accounts and ranked the top predictive features driving customer attrition, enabling proactive retention scoring.

---

## 💡 Key Findings & Prescriptive Recommendations

### High-Risk Customer Profile
* Frequent customer support interactions (especially 3–4+ calls)
* High daytime call volume (exceeding 220 daytime minutes)
* Active international calling plans experiencing high per-minute charges

### Actionable Retention Strategy
1. **Early Service Escalation (Tier-2 Routing):** Automatically escalate customers to senior Tier-2 support after their **third customer service call** to resolve recurring issues before frustration leads to cancellation.
2. **International Plan Restructuring:** Redesign international calling packages and introduce tiered bundle discounts for high-usage international subscribers.
3. **High-Value Loyalty Incentives:** Deploy proactive retention credits, plan upgrades, and loyalty rewards for heavy daytime users—specifically targeting accounts exceeding **220 daytime minutes**.

---

## 🛠️ Technology Stack
* **Programming & Data Manipulation:** Python, Pandas, NumPy
* **Visualization & BI:** Power BI, Matplotlib, Seaborn
* **Statistical & Predictive Modeling:** Scikit-learn, SciPy / Statsmodels (T-Test, Chi-Square, Logistic Regression, Random Forest)

---

## 📂 Repository Structure
```text
├── data/          # Raw and processed telecom churn datasets
├── notebooks/     # Jupyter notebooks for EDA, statistical tests, and ML modeling
├── dashboard/     # Power BI (.pbix) interactive dashboard file
├── reports/       # Executive summary reports and statistical output tables
├── models/        # Saved Random Forest model artifacts
├── images/        # Dashboard screenshots and EDA/feature importance charts
└── README.md      # Project documentation

Author
Nnabuk Akpan
Data Analytics Internship Project | Telecom Customer Churn Analysis
