# telecom-customer-churn-analysis
# Telecom Customer Churn: End-to-End Analytics & Prescriptive Strategy

A 6-stage data analytics and machine learning portfolio project completed during the **CodVeda Data Analytics Internship**, progressing from raw data ingestion to Power BI reporting, statistical hypothesis testing, Random Forest modeling, and prescriptive retention simulation.

## Executive KPI Snapshot (`churn-bigml-80.csv`)
* **Total Customers Analyzed:** 2,666
* **Overall Churn Rate:** 14.55% (388 churned accounts)
* **Direct Revenue Lost:** $25,157.85
* **Average Customer Service Calls:** 1.56 calls

---

## Project Roadmap & Deliverables

### Level 1 · Data Foundations & Exploration
* **Task 2 — Data Collection & Cleaning:** [`01_L1_T2_data_collection_and_cleaning.ipynb`](notebooks/01_L1_T2_data_collection_and_cleaning.ipynb)
  * Verified zero missing or duplicate records across 20 features, standardized categorical flags (`International plan`, `Voice mail plan`, `Churn`), and exported a clean modeling dataset.
* **Task 3 — Exploratory Data Analysis (EDA):** [`02_L1_T3_exploratory_data_analysis.ipynb`](notebooks/02_L1_T3_exploratory_data_analysis.ipynb)
  * Profiled central tendency and dispersion (Mean, Median, Mode, Std Dev) and identified a critical churn inflection point at **4+ customer service calls** where attrition exceeds 45%.

### Level 2 · Business Intelligence & Statistical Validation
* **Task 1 — Power BI Executive Dashboard:** [`telecom_customer_churn.pbix`](bi_dashboard/telecom_customer_churn.pbix)
  * Built an interactive report tracking KPI cards, regional churn breakdowns, service call thresholds, and international plan exposure.
  
  ![Executive Dashboard](bi_dashboard/screenshots/01_executive_kpi_overview.png)

* **Task 3 — Statistical Analysis for Business Decisions:** [`03_L2_T3_statistical_business_analysis.ipynb`](notebooks/03_L2_T3_statistical_business_analysis.ipynb)
  * Conducted T-Tests, Chi-Square tests of independence, and Logistic Regression ($p < 0.05$) confirming that daytime billing volume, international plan enrollment, and support call frequency are statistically significant churn drivers.

### Level 3 · Predictive Modeling & Prescriptive Strategy
* **Task 1 — Predictive Machine Learning:** [`04_L3_T1_predictive_churn_modeling.ipynb`](notebooks/04_L3_T1_predictive_churn_modeling.ipynb)
  * Trained a Random Forest Classifier on `churn-bigml-80.csv` and validated performance on unseen data (`churn-bigml-20.csv`) using Confusion Matrix, ROC-AUC, and Feature Importance plots.
* **Task 3 — Prescriptive Analytics & Strategic Recommendations:** [`05_L3_T3_prescriptive_retention_strategy.ipynb`](notebooks/05_L3_T3_prescriptive_retention_strategy.ipynb)
  * Scored active accounts by predicted churn probability and modeled net revenue recovery from three targeted interventions:
    1. **Automated Tier-2 Escalation** triggered on a customer's **3rd service call**.
    2. **International Bundle Restructuring** for high-usage international callers.
    3. **Daytime Usage Loyalty Credits** for accounts exceeding 220 daytime minutes.
