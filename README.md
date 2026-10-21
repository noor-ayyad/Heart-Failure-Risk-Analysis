# ❤️ Heart Failure Prediction & Risk Analysis

## 📌 Project Overview

This project explores heart disease data using Microsoft Power BI to analyze patient characteristics, identify potential risk factors, and develop an interactive, rule-based risk assessment dashboard.

The report combines patient demographics, clinical indicators, risk scoring, and data analysis to present findings through interactive visualizations and patient-level assessments.

## 🎯 Project Objectives

- Analyze patient demographics and heart disease distribution.
- Explore relationships between clinical characteristics and heart disease.
- Develop a rule-based patient risk scoring and categorization system.
- Identify influential factors using Power BI Key Influencers.
- Compare assigned risk categories with recorded heart disease status.

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop** — Data visualization and interactive reporting.
- **DAX (Data Analysis Expressions)** — Calculated columns, risk scoring, risk categorization, and classification agreement calculations.
- **Power BI Key Influencers** — Exploration of factors associated with heart disease.

## 📊 Dashboard Pages

### 1. Overview
<img width="589" height="335" alt="image" src="https://github.com/user-attachments/assets/15fa79b6-1aab-4e16-8860-c4d1398f9084" />

Presents a high-level summary of the dataset, including:
- Total patients
- Patients without heart disease
- Patients with heart disease
- Heart disease distribution by age group and gender
- Heart disease cases by ST slope and chest pain type

### 2. Risk Factors
<img width="563" height="312" alt="image" src="https://github.com/user-attachments/assets/2628f89f-b7d7-407a-bc5e-31a4deb6bbf7" />

Explores factors associated with heart disease using Power BI Key Influencers, helping users investigate patterns within the patient data.


### 3. Risk Assessment
<img width="568" height="320" alt="image" src="https://github.com/user-attachments/assets/7a048a12-7629-4ba8-b4cf-28551bc0c034" />

Provides an overview of patient risk classifications, including:
- Distribution across four risk categories
- Risk scoring based on selected patient characteristics
- Patient-level risk assessment details
- A classification agreement measure comparing risk categories with recorded heart disease status

## 🧮 Risk Scoring Methodology

A rule-based scoring system was developed using DAX calculated columns. Each patient's score combines five factors.

| Factor | Scoring criteria |
|---|---|
| Age | 50 or older: 2 points; 40–49: 1 point; below 40: 0 points |
| Cholesterol | 240 or higher: 2 points; 200–239: 1 point; below 200: 0 points |
| Resting blood pressure | 140 or higher: 2 points; 120–139: 1 point; below 120: 0 points |
| Exercise-induced angina | Yes: 2 points; No: 0 points |
| Chest pain type | ASY: 3 points; ATA: 2 points; NAP: 1 point; other: 0 points |

The individual points are added to calculate the total patient risk score.

### Risk Categories

| Total risk score | Category |
|---:|---|
| 8 or higher | High Risk |
| 5–7 | Medium Risk |
| 3–4 | Low Risk |
| 0–2 | Minimal Risk |

A separate DAX calculated column assigns a sort order to display the risk categories consistently in the dashboard.

## 📈 Classification Agreement

A DAX measure calculates the proportion of records where the assigned risk category aligns with the recorded heart disease status.

- **High Risk / Medium Risk:** Counted as matching when the recorded status is Heart disease.
- **Low Risk / Minimal Risk:** Counted as matching when the recorded status is No Heart disease.

The dashboard displays a result of **60.35%** for this measure.

This value represents agreement under the project's rule-based classification approach. It should not be interpreted as the validated accuracy of a trained machine learning model.

## 🔍 Key Analytical Areas

- Heart disease distribution across patient demographics.
- Differences in heart disease cases by clinical characteristics.
- Factors highlighted by Power BI Key Influencers.
- Patient risk distribution based on the defined scoring rules.
- Comparison between rule-based risk categories and recorded outcomes.

## ⚠️ Limitations

- Risk categories are based on predefined scoring rules rather than a clinically validated prediction model.
- The classification agreement measure depends on the scoring thresholds and the mapping between risk categories and recorded outcomes.
- The findings describe patterns in the dataset and should not be used as a substitute for professional medical assessment.

## 💡 Key Takeaways

This project demonstrates the use of Power BI and DAX to transform patient data into an interactive analytical report. It combines exploratory analysis, rule-based risk scoring, patient-level categorization, and visual reporting to support data-driven investigation of heart disease.

---

*Disclaimer: This project is for educational and analytical purposes only. It is not intended for clinical diagnosis or medical decision-making.*
