# SWYNEX Internship – Task 1: Data Cleaning & Preparation

## Project Overview

This project focuses on cleaning and preparing the UCI Online Retail dataset using Python and Pandas.

The objective is to identify and handle missing values, duplicate records, incorrect data types, inconsistent text, and data quality issues.

## Dataset Information

* **Dataset Name:** Online Retail
* **Source:** UCI Machine Learning Repository
* **Original Records:** 541,909
* **Columns:** 8
* **Original Format:** Excel (.xlsx)

## Dataset Columns

1. InvoiceNo
2. StockCode
3. Description
4. Quantity
5. InvoiceDate
6. UnitPrice
7. CustomerID
8. Country

## Tools & Technologies

* Python
* Pandas
* Jupyter Notebook
* VS Code

## Data Quality Issues Identified

| Issue               | Records |
| ------------------- | ------: |
| Missing Description |   1,454 |
| Missing CustomerID  | 135,080 |
| Duplicate Records   |   5,268 |
| Zero UnitPrice      |   2,510 |
| Negative UnitPrice  |       2 |

## Data Cleaning Steps

1. Replaced missing Description values with `Unknown Product`.
2. Retained missing CustomerID values because customer information was unavailable.
3. Removed 5,268 duplicate records.
4. Converted CustomerID from float to string.
5. Kept InvoiceDate in datetime format.
6. Removed unnecessary leading and trailing spaces from Description and Country.
7. Identified negative Quantity values that may represent returns or cancellations.
8. Retained zero UnitPrice records for further analysis.
9. Inspected two negative UnitPrice records related to `Adjust bad debt` accounting adjustments and retained them.

## Final Dataset Validation

| Validation               | Final Result |
| ------------------------ | -----------: |
| Original Rows            |      541,909 |
| Duplicate Rows Removed   |        5,268 |
| Final Rows               |      536,641 |
| Final Columns            |            8 |
| Missing Description      |            0 |
| Unknown Product Records  |        1,455 |
| Missing CustomerID       |      135,037 |
| Remaining Duplicate Rows |            0 |

## Repository Files

* `README.md` – Project documentation
* `data_cleaning.ipynb` – Jupyter Notebook containing cleaning steps and analysis
* `cleaned_online_retail.zip` – Compressed cleaned dataset

## How to Run This Project

1. Download or clone this repository.
2. Extract `cleaned_online_retail.zip`.
3. Install the required libraries:

```bash
pip install pandas openpyxl notebook
```

4. Open `data_cleaning.ipynb` in VS Code or Jupyter Notebook.
5. Run the notebook cells from top to bottom.

## Output

The cleaned dataset is provided inside:

`cleaned_online_retail.zip`

Expected dataset dimensions:

* Rows: 536,641
* Columns: 8

## Learning Outcomes

* Understanding data quality issues.
* Handling missing values.
* Removing duplicate records.
* Correcting data types.
* Cleaning inconsistent text.
* Identifying unusual values.
* Validating and exporting cleaned datasets.

## Author

**Luvkush Saini**

Data Analytics Learner

**Internship:** SWYNEX Technologies

**Project:** Task 1 – Data Cleaning & Preparation
