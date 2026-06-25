# Drunk-Driving-Fatality-Analysis
End-to-end data analytics project using Python, Machine Learning, Google BigQuery, and Tableau to analyze alcohol-related traffic fatalities.
# 🚔 Alcohol-Related Fatal Crash Analytics
### End-to-End Data Analytics Project using Python, SQL, BigQuery, Machine Learning, and Tableau

Interactive analysis of **203,000+ U.S. traffic fatalities (2015–2016)** to identify the geographic, temporal, and behavioral factors associated with alcohol-related fatal crashes.

---

## 📊 Interactive Dashboard

### Tableau Public Dashboard
https://public.tableau.com/shared/GDNJS4JKS?:display_count=n&:origin=viz_share_link

### Tableau Public Profile
https://public.tableau.com/app/profile/jared.oberg/vizzes

---

# Dashboard Preview

>  s<img width="800" height="447" alt="Recording2026-06-25130231-ezgif com-video-to-gif-converter" src="https://github.com/user-attachments/assets/8bf8a555-f20f-43c6-83bb-33a96dfb1060" />


![Dashboard](images/dashboard_overview.png)

---

# Executive Summary

Alcohol-impaired driving remains one of the leading causes of fatal traffic deaths in the United States. This project analyzes more than **203,000 fatal crashes** from the National Highway Traffic Safety Administration's Fatality Analysis Reporting System (FARS) to identify the characteristics most strongly associated with alcohol-related fatalities.

Using SQL, Google BigQuery, Python, machine learning, and Tableau, I built an end-to-end analytics workflow that cleans and integrates multiple FARS datasets, engineers predictive features, evaluates classification models, and presents the findings through an interactive dashboard.

Rather than predicting future crashes, the machine learning models identify which variables within the FARS dataset are most influential in distinguishing alcohol-related fatalities from other fatal crashes. These insights can support traffic safety research, policy development, and targeted enforcement strategies.

---

# Business Problem

Alcohol-related crashes account for thousands of fatalities every year. Although extensive crash data exists, extracting actionable insights requires integrating multiple datasets, identifying meaningful predictors, and presenting the results in a way that supports decision-making.

This project demonstrates how machine learning and interactive visualization can transform large public datasets into practical analytical tools.

---

# Project Workflow

```
FARS Dataset (NHTSA)
        │
        ▼
Google BigQuery
        │
        ▼
Python Data Cleaning
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Machine Learning
(Logistic Regression & Random Forest)
        │
        ▼
Interactive Tableau Dashboard
```

---

# Dashboard Features

The Tableau dashboard allows users to explore alcohol-related fatal crashes through interactive visualizations.

### Features include

- Interactive U.S. heat map
- State → County → Crash drill-down
- Dynamic KPI cards
- Geographic hotspot analysis
- Risk factor comparisons
- Time-of-day analysis
- Roadway analysis
- Interactive filtering
- Dashboard information tooltips

---

# Key Findings

### 🕒 Crash Timing
Time of crash was the strongest predictor of alcohol-related fatalities, accounting for **43% of model importance**.

### 🌙 High-Risk Hours
Evening (6pm–11pm) and Late Night (12am–5am) account for **77% of alcohol-related fatalities**.

### 🚫 Seatbelt Usage
**43%** of victims involved in alcohol-related fatalities were not wearing a seatbelt.

### 🚔 Prior DWI History
Drivers involved in alcohol-related fatalities were **4.0× more likely** to have a prior DWI conviction.

### 🛣 Roadway Risk
Principal arterials and interstate highways account for the highest number of alcohol-related fatalities.

### 🎯 Operational Insight
Combining **time** and **location** provides the strongest guidance for targeted enforcement and traffic safety initiatives.

---

# Machine Learning

Two supervised learning models were evaluated.

| Model | Purpose |
|---------|---------|
| Logistic Regression | Baseline classification model |
| Random Forest | Non-linear ensemble classifier |

The models were designed to classify whether a fatal crash involved alcohol impairment based on crash characteristics.

Performance demonstrated that temporal variables, roadway characteristics, licensing history, and driver behavior provide meaningful predictive information while also illustrating the limitations of predicting complex human behavior using historical crash records alone.

---

# Technologies Used

### Languages

- Python
- SQL

### Libraries

- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

### Platforms

- Google BigQuery
- Google Colab
- Tableau Public
- GitHub

---

# Repository Structure

```
Drunk-Driving-Fatality-Analysis/

│
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_modeling.ipynb
│   └── 03_dashboard_metrics.ipynb
│
├── dashboard/
│   └── Tableau Workbook (.twb/.twbx)
│
├── images/
│   ├── dashboard_overview.png
│   ├── state_drilldown.png
│   └── county_drilldown.png
│
├── presentation/
│   └── Capstone Presentation.pdf
│
├── report/
│   └── Final Capstone Report.pdf
│
└── README.md
```

---

# Skills Demonstrated

- SQL Data Extraction
- Google BigQuery
- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis
- Machine Learning
- Logistic Regression
- Random Forest
- Model Evaluation
- Tableau Dashboard Development
- Interactive Visualization
- Business Intelligence
- Executive Reporting
- Data Storytelling

---

# Future Improvements

Potential enhancements include:

- Incorporate additional FARS years
- Add traffic volume data
- Integrate roadway geometry information
- Include weather severity indices
- Perform hotspot clustering
- Explore XGBoost and LightGBM models
- Build predictive risk scoring by geographic region

---

# Data Source

National Highway Traffic Safety Administration (NHTSA)

Fatality Analysis Reporting System (FARS)

https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars

---

# Author

## Jared Oberg

Bachelor of Science — Data Science

Passionate about transforming complex datasets into actionable business insights through analytics, machine learning, and interactive visualization.

### Portfolio

**Tableau Public**

https://public.tableau.com/app/profile/jared.oberg/vizzes

**GitHub**
https://github.com/obja1102
