# Customer Churn Analysis — Credit Card Portfolio

**Exploratory analysis & customer segmentation to help a bank reduce credit-card attrition.**

> A data-cleaning and EDA project on a real bank credit-card dataset. It identifies *who* is
> churning, *why*, and *which* at-risk customers are worth re-engaging — with concrete
> recommendations for a business manager. The cleaned output feeds a Tableau dashboard.

---

## Business problem
A bank is losing credit-card customers and wants to understand the drivers behind it. Working
as the analyst, I was asked to surface the patterns behind attrition and prepare a clean,
well-structured dataset for downstream modelling.

## Dataset
**Bank Churners** — ~10,000 credit-card customers and 21 features spanning demographics,
tenure, credit utilisation, transaction behaviour, and customer-service contacts.
Source: Kaggle.

## What I did
- **Cleaning:** removed `Unknown` records, consolidated income brackets, standardised data
  types and column names, and verified there were no nulls
- **EDA:** compared attrited vs. active customers across age, income, credit limit,
  utilisation ratio, card tier, and customer-service contact frequency
- **Segmentation:** flagged high-risk customers using the 30% credit-utilisation rule and
  binned by age to separate the "exclude" group from the "worth re-engaging" group
- **Handoff:** exported a clean dataset and built a **Tableau** dashboard for the business manager

## Key findings
- Attrited customers contacted customer service **~3 times on average** before leaving —
  unresolved service issues are a major churn driver
- **Low-income customers show the highest credit utilisation** (over-reliance on credit) and
  the highest attrition rate
- A segment of *active* customers shows the same inactivity pattern as those who churned — an
  early-warning group to retain now, before they leave
- High-utilisation (>30%) customers are higher-risk and better excluded from re-engagement spend

## Recommendations to the business
- Improve customer-service resolution and reorient KPIs around retention, not just call volume
- Exclude chronic high-utilisation customers from reactivation campaigns; focus spend on
  responsible, lower-risk users
- Run demographic-tailored retention offers for the early-warning active segment

## Tools
Python (pandas, NumPy, seaborn, matplotlib) · Tableau

---

## Planned upgrade
This project currently ends at EDA and segmentation. The next iteration will:
1. Load the data into a **SQLite/Postgres schema** (customers, transactions, demographics) and
   join it via SQL back into Python — demonstrating a data-engineering workflow
2. Build a **churn-prediction model** (logistic regression / tree-based) with a proper
   train/test split, class-imbalance handling, and recall-focused evaluation

---

*Originally completed as part of CodeOp Data Science coursework.*
