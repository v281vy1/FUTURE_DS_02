# Social Media Campaign Performance Tracker

“Task 2 – Social Media Campaign Performance Tracker | Future Interns Data Science & Analytics Program”

---

## 📘 Project Overview
Modern digital marketing relies heavily on data-driven decisions.  
This project focuses on analyzing key performance metrics such as:

- Impressions  
- Clicks  
- Conversions  
- CTR (Click-Through Rate)  
- CPC (Cost Per Click)  
- CPA (Cost Per Acquisition)  
- CPM (Cost Per Mille)  

The final output is a **Power BI dashboard** that highlights campaign performance, efficiency, and optimization opportunities.

---

## 🎯 Objectives
- Evaluate overall campaign performance  
- Identify high-performing and low-performing campaigns  
- Compare platform performance (Facebook vs Instagram)  
- Analyze audience segments (age, gender)  
- Visualize key metrics through an interactive dashboard  
- Present insights that can help optimize future campaigns  

---

## 🧰 Tools Used
| Tool | Purpose |
|------|---------|
| **Power BI** | Dashboarding & Data Visualization |
| **Google Sheets / Excel** | Data Cleaning & Preparation |
| **Kaggle Dataset** | Facebook Ads Performance Data |
| **Markdown Files** | Documentation |
| **GitHub** | Version Control & Project Hosting |

---

## 📂 Repository Structure
```plaintext
FUTURE_DS_02/
│
├── README.md
│
├── dataset/
│   └── cleaned_facebook_ads.csv
│
├── dashboard/
│   └── Dashboard.png
│
└── analysis/
    ├── data_cleaning_steps.md
    ├── dax_measures.md
    └── insights_summary.md


```

## 🔍 Dataset Description
The dataset contains the following columns:

- `impressions`  
- `clicks`  
- `spent`  
- `approved_conversion`  
- `campaign_id`  
- `fb_campaign_id`  
- `age`  
- `gender`  
- `platform`  
- `reporting_start` / `reporting_end`  

There are **no engagement columns** (likes, comments, shares), so engagement rate was not used.

---

## 🧹 Data Cleaning Steps
Cleaning was done in **Google Sheets**, including:

- Removing duplicates  
- Standardizing column names  
- Converting data types (numbers, dates)  
- Fixing missing data  
- Creating calculated columns for analysis  
- Exporting the cleaned dataset as `cleaned_facebook_ads.csv`

Full steps are available in:  
📄 `analysis/data_cleaning_steps.md`

---

## 📊 DAX Measures Used
Key measures created inside Power BI:

Total Impressions = SUM('cleaned-data-facebook'[impressions])
Total Clicks = SUM('cleaned-data-facebook'[clicks])
Total Spend = SUM('cleaned-data-facebook'[spent])
Total Conversions = SUM('cleaned-data-facebook'[approved_conversion])

CTR (%) = DIVIDE([Total Clicks], [Total Impressions], 0)
CPC = DIVIDE([Total Spend], [Total Clicks], 0)
CPA = DIVIDE([Total Spend], [Total Conversions], 0)
CPM = DIVIDE([Total Spend], [Total Impressions], 0) * 1000


Complete list is available in:  
📄 `analysis/dax_measures.md`

---

## 📈 Dashboard Highlights
The Power BI dashboard includes:

- KPI Cards (Spend, CTR, CPC, CPA, Conversions, Impressions, Clicks)
- Top Campaigns by CTR  
- Spend vs Conversions by Platform  
- Clicks Trend Over Time  
- Impressions Share by Platform  
- Filters for Date, Platform, Campaign, Age, Gender  

A snapshot is included at:  
📸 `reports/Dashboard_Snapshot.png`

---

## 🧠 Key Insights
Some major findings from the analysis:

- CTR varies significantly by age and gender  
- CPC increases during high-competition periods  
- Facebook generally yields higher impressions  
- Some campaigns deliver conversions at a very low CPA  
- Spend and conversions do not always follow the same trend  
- Optimization is needed for campaigns with high spend but low clicks

Full insights in:  
📄 `analysis/insights_summary.md`

---

## 🚀 How to Run
1. Download the repository  
2. Open the PBIX file in **Power BI Desktop**  
3. Ensure the dataset path is correctly mapped  
4. Refresh data if needed  
5. Explore dashboard using filters  

---


Future Data Science Program – Task 2  
GitHub Repo: **FUTURE_DS_02**

