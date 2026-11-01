# Data Quality Analysis & Validation (Python)

## Problem Statement
Real-world datasets often contain hidden quality issues. This project profiles a customer dataset, validates it against business rules, and documents the cleaning process.

## Dataset
Public Telco Customer Churn dataset (Kaggle), 7,043 rows and 21 columns.

## Tools
Python, pandas, NumPy, Matplotlib, Google Colab

## Process
1. Profiled the dataset (types, nulls, duplicates)
2. Detected hidden blank values in `TotalCharges`
3. Converted data types and handled missing values using business logic
4. Applied validation rules (value ranges, allowed values, consistency checks)
5. Detected outliers using the IQR method
6. Produced a before/after quality summary

## Key Findings
- Found 11 hidden blank values in `TotalCharges` that `isnull()` did not detect; all belonged to customers with `tenure = 0`.
- Imputed them with 0 based on business logic, so no rows were lost (7,043 before and after).
- All 5 validation rules passed with 0 violations; no outliers found using the IQR method.
- Converted `TotalCharges` from `object` to `float64`.

## Files
- `data_quality_validation.ipynb`: full analysis
- `Telco-Customer-Churn.csv`: raw dataset
- `telco_cleaned.csv`: cleaned dataset

## Author
Rushivardhan Mulkanooru | [LinkedIn](https://www.linkedin.com/in/rushivardhan-mulkanooru-95b045369)
