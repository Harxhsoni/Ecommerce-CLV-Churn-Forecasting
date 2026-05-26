# E-Commerce Customer Lifetime Value (CLV) & Churn Forecasting

## 🎯 Business Problem
Customer Acquisition Costs (CAC) are skyrocketing. Modern B2C and e-commerce businesses bleed marketing budget on one-time buyers. The goal of this project is to build a predictive analytics pipeline that identifies high-risk churn customers and forecasts the future financial value of every customer cohort, allowing marketing teams to optimize retention spend.

## 📊 Business Impact & Key Insights
Using a transactional dataset of **1M+ rows**, the probabilistic models successfully segmented **5,881 active customers** and unlocked actionable revenue metrics:
* **Total Expected Revenue (Next 3 Months):** ₹2,255,307
* **Value at Risk:** Identified a critical "At Risk" customer segment that has historically high frequency but a <50% probability of being active.
* **Core Driving Segment:** Proved that the "Champions" segment generates over 75% of the total predicted quarterly revenue (₹1,736,236), justifying exclusive loyalty campaigns.

## 🛠️ Tech Stack & Methodology
* **Data Engineering & Cleaning:** Python (Pandas) - Handled missing values, treated order cancellations/returns, formatted temporal logs.
* **Predictive Modeling:** Lifetimes Library (Python)
  * **BG/NBD Model:** Processed purchase frequency and recency via a Poisson process to calculate individual `probability_alive` and future transaction counts.
  * **Gamma-Gamma Model:** Estimated conditional expected average order value (monetary value), satisfying the independence assumption (Frequency & Monetary Correlation: 0.023).
* **Executive BI Dashboard:** Tableau Public - Built a high-end minimalist interface utilizing data-driven 75th percentile thresholds for sharp user segmentation.

## 🖥️ Live Dashboard
<img width="1645" height="851" alt="Screenshot_20260525_201112" src="https://github.com/user-attachments/assets/fe80b8a6-1614-4c71-86c3-73480130af65" />

## 📁 Repository Structure
* `Online_Retail_CLV.ipynb`: End-to-end Python script containing data pipeline, model training, and probability matrices.
* `final_clv_predictions.csv`: Model outputs including churn risk probabilities and 3-month CLV predictions for every unique Customer ID.

## 📈 Key Visualizations Preview
* **Probability of Being Alive Matrix:** Heatmap mapping customer frequency against recency to isolate exact drop-off points.
* **Risk vs Reward Cloud:** Interactive scatter plot correlating 3-Month CLV against active probability to trigger automated retention marketing actions.

---
*Dataset Source: UCI Machine Learning Repository (Online Retail II)*
