# 📊 A/B Testing & Audience Segmentation Analytics

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Ezc1djYLyMyfTrDb_RF6X3xYwg_zXSsf?usp=drive_link)
[![Tableau Public](https://img.shields.io/badge/Tableau-Public_Dashboard-E97627?logo=tableau&logoColor=white)](https://public.tableau.com/views/ABTestAudienceSegmentationHubUpdated/ABTestAudienceSegmentationHub?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

An end-to-end data analytics project evaluating the statistical significance and business impact of an A/B experiment. The study covers data cleaning, anomaly detection, hypothesis testing in Python, and interactive audience segmentation analysis via a Tableau dashboard.

---

## 📌 Project Overview & Objectives

The goal of this project is to analyze experimental user data to determine whether the test variant generates a statistically significant conversion lift and to identify high-performing customer segments.

**Core Business Questions Addressed:**

1. **Overall Experiment Performance:** Does the test variant (`Group B`) generate a statistically significant lift in conversion rate or target metrics compared to the control group (`Group A`)?
2. **Data Integrity & Randomization:** Did the experiment suffer from Sample Ratio Mismatch (SRM), and are the baseline distributions balanced across cohorts?
3. **Audience Segmentation:** Which specific user segments (e.g., by device type, traffic source, or user tenure) respond best to the new variant?
4. **Strategic Rollout Recommendations:** Should the test variant be deployed globally, targeted to specific segments, or rejected?

---

## 🛠️ Data Pipeline & Project Workflow

The project follows a standard Data Analytics Lifecycle:

### 1. Data Ingestion & Schema Exploration
* **Source datasets merged:** User session logs, assignment groups (`control` vs. `test`), and demographic/device metadata.
* **Schema Validation:** Verified data types, column integrity, and unique identifiers (`user_id`).

### 2. Data Cleaning & Preprocessing
* **Missing Value Analysis:** Evaluated null proportions and handled incomplete records with appropriate business logic.
* **Sample Ratio Mismatch (SRM):** Conducted Chi-Square goodness-of-fit tests to ensure proper traffic split between control and test variants.
* **Duplicate & Outlier Detection:** Screened for multiple entries per user, bot traffic, and anomalous behavioral metrics.

### 3. Exploratory Data Analysis (EDA) & Feature Engineering
* **Derived Metrics:** Calculated conversion rates, average order values (AOV), and engagement ratios.
* **Cohort Categorization:** Segmented users based on behavioral and technical attributes to prepare for deep-dive slicing.

### 4. Statistical Hypothesis Testing & Segmentation
* **Hypothesis Testing:** Executed Z-tests for proportions and T-tests/Mann-Whitney U tests for continuous variables at $\alpha = 0.05$.
* **Segment-Level Breakdown:** Analyzed interaction effects between test variants and audience subgroups to uncover localized lifts or Simpson's Paradox.

---

## 💻 Tech Stack & Python Libraries

* **Environment:** Google Colab / Jupyter Notebook[cite: 160]
* **Data Wrangling:** `pandas`, `numpy`[cite: 160]
* **Statistical Analysis:** `scipy`, `statsmodels`
* **Data Visualization:** `matplotlib`, `seaborn`[cite: 160]
* **Business Intelligence:** Tableau Public

---

## 📊 Business Key Takeaways & Findings

* **Global Experiment Lift:** Evaluated overall conversion change between variants, establishing statistical significance ($p$-value evaluation).
* **Segment Insights:** Identified top-performing audience cohorts driving the positive variance, preventing premature blanket rollouts.
* **Risk Mitigation:** Confirmed data integrity through rigorous SRM checks, ensuring decisions are based on unbiased experimental data.

---

## 🔗 Notebook & Dashboard Access

You can view the full Google Colab report, code implementation, and interactive Tableau visualizations here:
* 👉 **[Open Google Colab Notebook](https://colab.research.google.com/drive/1Ezc1djYLyMyfTrDb_RF6X3xYwg_zXSsf?usp=drive_link)**
* 👉 **[Explore Tableau Public Dashboard](https://public.tableau.com/views/ABTestAudienceSegmentationHubUpdated/ABTestAudienceSegmentationHub?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**
