# Task 1: Data Cleaning & Preparation

## Project Overview

This project focuses on cleaning and preparing the UCI Online Retail dataset using Python and Pandas.

The objective is to identify and handle missing values, duplicate records, inconsistent text, and data quality issues to make the dataset suitable for further analysis.

## Dataset Information

* **Dataset Name:** Online Retail
* **Source:** UCI Machine Learning Repository
* **Original Records:** 541,909
* **Columns:** 8
* **File Format:** Excel (.xlsx)

### Dataset Columns

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

### 1. Missing Values

* Replaced missing Description values with "Unknown Product".
* Retained missing CustomerID values because customer information was unavailable.

### 2. Duplicate Records

* Identified 5,268 duplicate rows.
* Removed all duplicate rows.

### 3. Data Type Correction

* Converted CustomerID from float to string.
* Kept InvoiceDate in datetime format.

### 4. Text Cleaning

* Removed unnecessary leading and trailing spaces from Description and Country.

### 5. Quantity and UnitPrice Analysis

* Identified negative Quantity values, which may represent returns or cancellations.
* Identified zero UnitPrice records and retained them for further analysis.
* Inspected two negative UnitPrice records. Both were related to "Adjust bad debt" accounting adjustments, so they were retained.

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

## Project Structure


Task-1-Data-Cleaning/
│
├── data/
│   └── Online retail.xlsx
│
├── notebooks/
│   └── data_cleaning.ipynb
│
├── output/
│   └── cleaned_online_retail.csv
│
└── README.md


## How to Run This Project

1. Clone or download this repository.
2. Open the project in VS Code.
3. Install the required libraries:

pip install pandas openpyxl notebook


4. Open the Jupyter Notebook:

notebooks/data_cleaning.ipynb


5. Run all notebook cells from top to bottom.

6. Find the cleaned dataset inside the `output` folder.

## Output

The cleaned dataset is saved as:

`output/cleaned_online_retail.csv`

It contains 536,641 rows and 8 columns.

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

**Project:** Task 1 – Data Cleaning & Preparation
