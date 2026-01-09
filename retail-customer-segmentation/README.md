# Customer Segmentation & RFM Analysis (UK Retail)

## 1. Executive Summary
**Translating Analytical Chemistry Rigor to Business Intelligence.**
This project analyzes ~540,000 transactions from a UK-based online retailer to improve marketing ROI. By moving from mass marketing to a targeted segmentation strategy, I identified that **20% of customers drive 80% of revenue** (Pareto Principle) and flagged a critical **"At Risk" segment (N=989)** that represents preventable churn.

## 2. Business Problem
The marketing team was using a "spray and pray" approach, leading to wasted budget and low engagement. The goal was to build a data-driven framework to:
* Identify VIP customers ("Champions") for loyalty programs.
* Detect "At Risk" customers before they churn.
* Personalize communication based on purchasing behavior.

## 3. Challenges & Methodology (Scientific Approach)
Unlike standard tutorials, this analysis tackles the messy reality of retail data with scientific rigor:

* **Sample Integrity:** 25% of the raw data lacked `CustomerID`. Instead of imputing values (which introduces bias), I treated this as sample contamination and removed these records to ensure the segmentation model was built only on verifiable user behavior.
* **Handling Skewed Data:** The monetary data followed a Power Law (long tail) rather than a Normal Distribution.
    * *Decision:* I rejected **K-Means Clustering** for the initial baseline because it assumes spherical clusters and is sensitive to extreme outliers (e.g., the "Whale" customer who spent £77k in one transaction).
    * *Solution:* I implemented **Percentile Ranking (Quintiles)** to score customers. This non-parametric approach is robust against outliers and easier for non-technical stakeholders to interpret (e.g., "Top 20%").

## 4. Key Findings
* **The "Whales" are real:** The top segment ("Champions") has an average Customer Lifetime Value (CLV) of **£6,732**, compared to just £222 for the bottom segment.
* **The Churn Risk:** The largest active segment is "At Risk" (N=989). These customers have average spend (€521) but high latency (114 days since last purchase).
* **Anomalies:** Detected operational anomalies (e.g., huge cancellations) that required filtering to prevent skewed financial reporting.

## 5. Tech Stack
* **Python:** Pandas (Data Engineering), NumPy (Math), Seaborn (Visualization).
* **Techniques:** RFM Analysis, Cohort Analysis logic, Statistical Distribution Checks.