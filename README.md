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
```

8. Removed the duplicate join column after merging.
9. Exported the final cleaned dataset in Tableau for Visualization.


Analysing Data and Finding insights using Tableau


1. Here are the Top products generating highest Sales and The top stores which provides highest sales
<img width="761" height="839" alt="dash_sales" src="https://github.com/user-attachments/assets/221a056b-c52e-41d0-9860-7f46da155030" />




2. Top chips products which are sold the most and contribute to the sales in highest manner.
<img width="878" height="586" alt="Screenshot 2026-04-17 at 7 52 47 AM" src="https://github.com/user-attachments/assets/7b564abd-7c20-40b1-9f8e-293a4035efcc" />


3.In this chart ,The chart comparing total sales across customer life stages and customer categories shows that older families and retirees contribute the highest sales overall.
Key Insights
* Budget Older Families generate the highest total sales, contributing approximately 168K in revenue.
*  Among Mainstream customers, Young Singles/Couples and Retirees are the strongest-performing segments, both generating more than 155K in sales.
*  Premium customers contribute lower overall sales compared to Budget and Mainstream categories, although Premium Older Singles/Couples still generate more than 132K in revenue.
*   New Families are the lowest-spending customer group across all customer categories.
*  The results suggest that mature households and older customers are the most valuable segments, while younger families and new families contribute significantly less.

<img width="965" height="714" alt="Screenshot 2026-04-17 at 8 37 22 AM" src="https://github.com/user-attachments/assets/9a25b81e-b845-40e1-8c37-4182e70bf146" />







    

