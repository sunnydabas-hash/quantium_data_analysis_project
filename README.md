Quantium Data Analysis Project


Overview
This project was completed as part of the Quantium Data Analytics virtual experience program. The objective was to clean, merge, and prepare retail transaction data for further analysis.
The dataset was cleaned using Microsoft Excel and SQL before being combined into a final dataset for analysis.

Tools Used:

Microsoft Excel
SQL
Tableau
Git
GitHub

Data Cleaning Process

The following cleaning steps were completed:

 1. Firstly, File was opened in Excel and the whole data is selected as a table . Date was in general format so , It was corrected as Short Date Format. Similarly Total_Sales was corrected in Currency format.
 2. Checking Null columns: by activating filter function in columns and checking for null values. There were no null cells .
 3. Checking for repeating rows/data: LYLTY_CARD_NBR is the unique value column in both tables so checked the repeating value but didnot find one. Conclusion, Data is cleaned and checked for nulls and duplicate rows.
 4. Verified that quantity values were greater than 0.
 5. Verified that sales values were valid.
 6. Joining the transaction table and customer behaviour table using SQL JOIN function using the LYLTY_CARD_NBR column since excel was unable to join due the data size.
 7. # Quantium Data Analysis Project

## Overview

This project was completed as part of the Quantium Data Analytics virtual experience program. The objective was to clean, merge, and prepare retail transaction data for further analysis.

The dataset was cleaned using Microsoft Excel and SQL before being combined into a final dataset for analysis.

---

## Tools Used

* Microsoft Excel
* SQL
* Git
* GitHub

---

## Data Cleaning Process

The following cleaning steps were completed:

1. Identified and removed missing values in Excel
2. Checked for duplicate records and removed them
3. Verified that quantity values were greater than 0
4. Verified that sales values were valid
5. Cleaned inconsistent or repeated values
6. Joined the transaction table and customer table using the common column `LYLTY_CARD_NBR`
7. Removed the duplicate join column after merging
8. Removed the duplicate join column after merging.
9. Exported the final cleaned dataset


## SQL Used for Joining Tables

```sql
SELECT
    t1.DATE_D,
    t1.STORE_NBR,
    t1.LYLTY_CARD_NBR,
    t1.TXN_ID,
    t1.PROD_NBR,
    t1.PROD_NAME,
    t1.PROD_QTY,
    t1.TOT_SALES,
    t2.LIFESTAGE,
    t2.PREMIUM_CUSTOMER
FROM transactions t1
JOIN customers_behaviour t2
ON t1.LYLTY_CARD_NBR = t2.LYLTY_CARD_NBR;


8. Removed the duplicate join column after merging.
9. Exported the final cleaned dataset in Tableau for Visualization.







    

