# Data Cleaning: Messy Customer Dataset

**Track:** Data Analytics
**Level:** Level 1 — Task 3
**Internship:** Oasis Infobyte (OIBSIP)

## Objective
Demonstrate professional-level data cleaning skills by taking a deliberately messy dataset and systematically transforming it into a clean, analysis-ready dataset. Every decision is documented.

## Dataset
`messy_customer_data.csv` — a synthetic customer dataset (840 rows) deliberately containing:
- Missing values (Age, Salary, Email)
- Invalid ages (negative or unrealistically high)
- Inconsistent gender formatting ("Male", "male", "M", "m", etc.)
- Mixed date formats (YYYY-MM-DD, DD/MM/YYYY, MM-DD-YYYY, DD-Mon-YYYY)
- 40 duplicate rows
- Genuine salary outliers (a small number of executive-level salaries)

## Tech Stack
- Python
- pandas
- numpy
- Jupyter Notebook

## What This Project Covers
- Data quality report: nulls, duplicates, dtype issues, value range anomalies (before and after)
- Missing data handling with documented justification per column (median imputation for Age/Salary, no imputation for Email)
- Duplicate detection and removal
- Standardisation of inconsistent Gender values and mixed date formats
- Outlier detection using the IQR method, with a documented cap-vs-remove decision
- Data type correction (int, float, datetime)
- Before vs. after summary table
- Cleaned dataset saved as a new CSV file

## How to Run
1. Clone this repository
2. Navigate to this folder: `OIBSIP/DataAnalytics-L1-DataCleaning/`
3. Install requirements: `pip install pandas numpy jupyter`
4. Open the notebook: `jupyter notebook Data_Cleaning.ipynb`
5. Run all cells in order — the cleaned dataset will be saved as `cleaned_customer_data.csv`

## Key Findings
- The dataset contained 40 duplicate rows (4.8% of the original data), which were identified and removed based on all columns except the unique CustomerID.
- 131 Age values and 76 Salary values were missing or invalid; both were resolved using median imputation to avoid skew from outliers.
- Gender had 8 inconsistent variants representing only 2 true categories, requiring case-normalization and mapping to standardize.
- Salary contained 32 genuine outliers (likely executive-level earners), which were capped rather than removed to preserve valid information while limiting their statistical influence.

## Author
*Apoorva*
