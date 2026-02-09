🧹 SQL Data Cleaning Project — Layoffs Dataset This project focuses on cleaning and preparing a layoffs dataset using SQL. The workflow includes removing duplicates, standardizing inconsistent values, handling nulls, and dropping unnecessary rows or columns. The goal is to transform raw data into a clean, analysis‑ready dataset using industry‑standard SQL techniques.

📁 Project Overview This SQL project demonstrates a complete data‑cleaning pipeline using a real‑world dataset. Key tasks include:

Creating staging tables to protect raw data
Identifying and removing duplicate records
Standardizing text fields (company, industry, country)
Converting date formats
Handling null and blank values
Removing unnecessary rows and columns The final output is a fully cleaned and structured dataset ready for analysis or visualization.

🛠️ Skills & Concepts Demonstrated ✔ SQL Techniques Used

CREATE TABLE … LIKE
INSERT INTO … SELECT
ROW_NUMBER() OVER (PARTITION BY …)
Common Table Expressions (CTEs)
TRIM(), LIKE, string cleaning functions
STR_TO_DATE() for date conversion
ALTER TABLE … MODIFY COLUMN
Self‑joins for filling missing values
DELETE and DROP COLUMN ✔ What I Learnt
How to build safe, repeatable data‑cleaning workflows
Best practices for staging tables
Detecting and removing duplicates using window functions
Standardizing messy text data
Converting text dates into proper SQL DATE format
Using joins to intelligently fill missing values
Cleaning datasets to professional, analysis‑ready standards

📌 Data Cleaning Steps

1️⃣ Removing Duplicates Process:

Created a staging table (layoffs_staging) to preserve raw data
Used ROW_NUMBER() with PARTITION BY to identify duplicate rows
Created a second staging table (layoffs_staging2) including a row_num column
Removed duplicates where row_num > 1 Key SQL Concepts:
Window functions
CTEs
Safe deletion using staging tables

2️⃣ Standardizing Data Tasks Completed:

Removed leading/trailing spaces using TRIM()
Standardized inconsistent industry names (e.g., all “Crypto%” → “Crypto”)
Cleaned country names by removing trailing periods
Converted date strings (MM/DD/YYYY) into SQL DATE format Key SQL Concepts:
String cleaning
Pattern matching with LIKE
Date conversion with STR_TO_DATE()
Column type modification

3️⃣ Handling Null or Blank Values Steps:

Identified null or blank values in key fields
Used self‑joins to fill missing industry values based on matching company names
Replaced blank strings with NULL
Ensured consistent and complete data across the dataset Key SQL Concepts:
IS NULL
Self‑joins
Conditional updates

4️⃣ Removing Unnecessary Rows & Columns Actions:

Deleted rows where both total_laid_off and percentage_laid_off were null
Dropped the helper column row_num after cleaning Key SQL Concepts:
DELETE
ALTER TABLE … DROP COLUMN

📊 Final Outcome By the end of the project, the dataset was:

Fully deduplicated
Standardized and consistent
Free of blank or null inconsistencies
Cleanly formatted with correct data types
Ready for analysis, visualization, or dashboarding
