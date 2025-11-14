# Data Cleaning Steps

This document describes all the data cleaning and preprocessing steps performed on the Facebook Ads dataset before analysis and visualization.

---

## 1. Imported Raw Dataset
- Dataset source: **Kaggle – Facebook Ads Performance Dataset**
- Format: CSV
- Loaded into **Google Sheets** for preprocessing.

---

## 2. Removed Duplicates
- Checked for duplicate rows based on:
  - `fb_campaign_id`
  - `campaign_id`
  - `reporting_start`
  - `reporting_end`
- Removed all exact duplicate rows using **Data → Remove Duplicates**.

---

## 3. Standardized Column Names
Renamed columns for consistency:
- `spent` → **spent**
- `approved_conversion` → **approved_conversion**
- Ensured all column names were lowercase and snake_case.

---

## 4. Checked and Converted Data Types
- `impressions`, `clicks`, `spent`, `approved_conversion` → **numeric**
- `reporting_start`, `reporting_end` → **date**
- `age`, `gender`, `platform` → **categorical (text)**

---

## 5. Handled Missing Values
- Verified no missing values in numerical fields.
- Missing conversions replaced with **0** (logical assumption).

---

## 6. Created Additional Calculated Columns (Optional)
Added fields for easier validation in Power BI:
- CTR Check = clicks / impressions
- CPC Check = spent / clicks

These were only used for verification and not included in the final dataset.

---

## 7. Exported Clean Dataset
- Final cleaned file saved as:
  - `cleaned_facebook_ads.csv`
- Used in Power BI for analysis and dashboard creation.

---

## 8. Verified Consistency
Performed final checks:
- No negative values
- Date ranges align correctly
- Platforms limited to valid values (Facebook, Instagram)

---

## 
Dataset is now fully clean, structured, and ready for analysis in Power BI.
