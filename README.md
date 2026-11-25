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
[Power BI Dashboard Preview](images/dashboard_preview.png)!https://github.com/NnabukAkpan/telecom-customer-churn-analysis/blob/main/Telecom%20Dashboard.png
An interactive Power BI executive dashboard was built to track:
* **Headline KPI Cards:** Total Customers (2,666), Churn Count (388), Churn Rate (14.55%), Revenue at Risk (\$25,157.85), and Avg. Service Calls (1.56).
* **Segment & Trend Breakdowns:** Churn distribution across customer service call tiers, geographic states, international plan adoption, and charge brackets.
* Business Intelligence & Statistical Validation
* **Task 1 — Power BI Executive Dashboard:** [`telecom_customer_churn.pbix`](bi_dashboard/telecom_customer_churn.pbix)
  * Built an interactive report tracking KPI cards, regional churn breakdowns, service call thresholds, and international plan exposure.
  
  ![Executive Dashboard](bi_dashboard/"C:\Users\Admin\OneDrive\Pictures\Screenshots\Telecom Dashboard.png"/01_executive_kpi_overview.png)

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


# 📊 Telecom Customer Churn Analysis: End-to-End Analytics & Prescriptive Strategy

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-EDA-150458?style=for-the-badge&logo=pandas&logoColor=white)

## 📌 Project Overview
Customer churn is one of the most significant revenue risks in the telecommunications industry, where acquiring new customers costs up to five times more than retaining existing ones. This project presents an end-to-end data analytics and machine learning solution that identifies key churn drivers, quantifies financial exposure, predicts customer attrition, and formulates data-driven retention strategies.

By bridging data preprocessing, exploratory data analysis (EDA), statistical hypothesis testing, interactive business intelligence, and predictive modeling, this project turns raw telecom customer records into executive-level prescriptive insights.

---

## 🎯 Business Problem & Objectives
Unidentified customer churn directly erodes recurring monthly revenue. The primary goals of this project are to:
- **Data Preparation:** Clean, validate, and structure customer records for analysis.
- **Exploratory Data Analysis:** Uncover behavioral trends, service call dynamics, and usage patterns.
- **BI Reporting:** Build an executive Power BI dashboard to monitor churn metrics and segment breakdowns.
- **Statistical Validation:** Perform hypothesis testing and logistic regression to confirm statistically significant churn drivers.
- **Predictive Modeling:** Train a machine learning classifier to accurately score customer churn risk.
- **Prescriptive Strategy:** Deliver targeted, cost-effective retention recommendations for high-risk accounts.

---

## 📈 Dataset Summary & Headline KPIs
The analysis was performed on the `churn-bigml-80.csv` dataset, covering **2,666 customer accounts**:

| Metric | Value | Business Context |
| :--- | :--- | :--- |
| **Total Accounts Analyzed** | **2,666** | Complete active & churned customer base |
| **Total Churned Accounts** | **388** | Customer accounts that discontinued service |
| **Baseline Churn Rate** | **14.55%** | Portfolio-wide customer attrition rate |
| **Monthly Revenue at Risk** | **$25,157.85** | Direct financial exposure from churned accounts |
| **Avg. Service Call Frequency** | **1.56** | Average support interactions per customer |

---

## 🔄 End-to-End Project Workflow

### 1. Data Cleaning & Preprocessing
- Verified schema integrity and checked for missing or duplicated values across all 2,666 records.
- Formatted categorical features (`International plan`, `Voice mail plan`) and created a binary target variable (`Churn_binary`).
- Engineered aggregate usage and charge features to measure monetary impact across daytime, evening, night, and international calls.

### 2. Exploratory Data Analysis (EDA)
Explored key customer dimensions:
- Day, Evening, Night, and International usage minutes vs. billing charges.
- Service call volume as a measure of customer support friction.
- Churn rate variances between plan subscribers (International & Voice Mail plans).

> **Key EDA Finding:** Customer churn spikes sharply for users making **4 or more customer service calls**, pointing to unresolved technical or billing friction as a primary driver of attrition.

### 3. Business Intelligence Dashboard (Power BI)
![Power BI Executive Dashboard Preview]("C:\Users\Admin\OneDrive\Pictures\Screenshots\Screenshot 2026-11-24 102334.png"/dashboard_preview.png)

An interactive Power BI dashboard (`dashboard/telecom_customer_churn.pbix`) was developed to provide executive visibility:
- **KPI Summary Cards:** Total Customers (2,666), Churn Count (388), Churn Rate (14.55%), Revenue at Risk ($25,157.85), and Avg. Service Calls (1.56).
- **Interactive Visuals:** Geographic churn distribution across states, customer service call thresholds, and plan adoption rates.


### 4. Statistical Analysis & Hypothesis Testing
Validated visual EDA trends through rigorous statistical evaluation:
- **Methods:** Two-Sample T-Tests, Chi-Square Tests of Independence, and Logistic Regression.
- **Statistically Significant Drivers (p < 0.05):**
  1. Customer service call frequency
  2. Daytime minute volume & charge totals
  3. Active international plan subscription

### 5. Predictive Machine Learning Modeling
- **Model:** Random Forest Classifier
- **Evaluation Metrics:** Confusion Matrix, ROC-AUC Score, and Feature Importance ranking.
- **Result:** Successfully prioritized high-risk accounts, providing operational scores to target proactive retention interventions.

---

## 💡 Key Findings & Prescriptive Recommendations

### High-Risk Customer Profile
- **Support Friction:** Accounts with 3–4+ customer service interactions.
- **Heavy Usage:** High daytime usage exceeding **220 daytime minutes**.
- **International Subscribers:** Customers on international calling plans experiencing elevated per-minute billing rates.

### Actionable Retention Playbook
1. **Automated Tier-2 Support Escalation:** Automatically flag and route accounts to senior Tier-2 customer service reps upon reaching their **third support call** to address issues before cancellation.
2. **International Rate Package Overhaul:** Restructure international plans to offer tiered rates and usage bundles for frequent international callers.
3. **Proactive Daytime Loyalty Incentives:** Deploy targeted retention credits, loyalty rewards, or plan upgrades to heavy daytime users reaching usage thresholds.

---

## 🛠️ Technology Stack
- **Language & Data Processing:** Python 3.10+, Pandas, NumPy
- **Exploratory Visualization:** Matplotlib, Seaborn
- **Business Intelligence:** Power BI Desktop (`.pbix`)
- **Machine Learning & Statistics:** Scikit-Learn, SciPy, Statsmodels

---

## 📂 Repository Structure
```text
├── data/          # Raw and cleaned datasets (churn_cleaned.csv)
├── notebooks/     # Jupyter notebooks (EDA, Statistical Testing, ML Pipeline)
├── dashboard/     # Power BI file (telecom_customer_churn.pbix)
├── reports/       # Executive summaries and exported KPI reports
├── models/        # Trained Random Forest model artifacts
├── images/        # Dashboard screenshots (dashboard_preview.png) & charts
└── README.md      # Comprehensive project documentation
