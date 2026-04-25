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

4. This chart shows the montly sales trend , comparing the 2018 and 2019 each months sale.

<img width="1462" height="887" alt="Screenshot 2026-04-24 at 7 27 29 AM" src="https://github.com/user-attachments/assets/780d897d-8b8b-4a06-bef2-056614c3391d" />
Key Insights
* Starting from July,2018 , it maintains $162k sales till november.
* The chart  shows highest sales in December peaking upto $167k probably due to Holidays like Christmas and New Year which shows people generally order more .
* The dip starting in Jan,2019 to Feb,2019 shows post holidays sales decrease probably due to working season.
* Sales starts improving after Feb,2019 and continues to go back to around $160k .
* The results suggests that sales peaks in Holidays when all the families come together to celebrate and dips when holiday season gets over.

5. -Older Families are the highest spenders across all tiers

Budget: $36.01 | Mainstream: $36.54 | Premium: $36.04
Consistently the top dot in every panel — regardless of premium tier, this segment spends the most per customer

- Young Families are a strong second

Budget: $34.69 | Mainstream: $34.01 | Premium: $34.54
Close behind Older Families — family segments as a whole clearly outspend all other lifestages
<img width="1462" height="887" alt="Screenshot 2026-04-24 at 7 26 38 AM" src="https://github.com/user-attachments/assets/2f70ff6f-e007-45fa-a9e6-b980b3075960" />

Family lifestage, not premium tier, is the primary driver of individual customer spend. The gap between Older Families ($36) and Young Singles ($16) is more than 2x — making lifestage a far stronger predictor of value than whether a customer shops Budget or Premium.

Recommendation

Prioritise family segments in ranging, promotions, and shelf strategy
Don't over-invest in converting Budget families to Premium — the spend uplift is negligible (~$0.03)
Focus on frequency tactics for Young Singles — their per-visit spend won't grow much, but visit frequency can


<img width="604" height="651" alt="Screenshot 2026-04-24 at 7 53 25 AM" src="https://github.com/user-attachments/assets/88fe8bcd-c2c7-4f89-8967-ce7f63e6b9e4" />

6.What the chart shows
A ranked table of the top 20 products by pack size (grams), with a heat-map colour scale — darker blue = larger pack, lighter teal = smaller pack.

Key Observations
1. Two brands dominate the largest pack sizes (380g)

Smiths Crinkle Chip Original Big Bag and Dorito Corn Chip Supreme both sit at 380g
These are clearly the "bulk/sharing" format — positioned for group occasions or family consumption

2. Three pack size tiers are clearly visible

Large format (270g–380g): Smiths, Doritos, Cheezels, Old El Paso, Twisties
Mid format (175g): Kettle dominates entirely — 6 out of 7 products in this range are Kettle
Small format (150g): Exclusively Kettle Tortilla and Sensations lines

3. Kettle owns the mid-to-small pack space

9 of the top 20 products are Kettle
All Kettle products sit between 150g–175g — a very consistent, premium portion-controlled sizing strategy
No Kettle product appears in the large format tier

4. Old El Paso is the only non-chip brand in the list

Three salsa dip products at 300g each
Suggests cross-category complementary purchasing — customers buying chips likely also buying dips

5. Smiths and Doritos lead the large sharing format

Both appear multiple times at 330g–380g
Smiths has 3 products in the top 20 (380g, 330g x2) — strong large-format ranging
 
 <img width="405" height="473" alt="Screenshot 2026-04-24 at 7 59 49 AM" src="https://github.com/user-attachments/assets/d942eeb6-4b1f-4c03-9e1b-0410f06af0f9" />


Recommendations 

Range both large and mid formats — they serve different missions (sharing occasion vs. individual snacking) and different segments
Kettle's 175g sweet spot aligns with its premium positioning — avoid discounting into large-format as it may dilute brand perception
Old El Paso dips appearing in a chip pack size chart suggests a meal deal or cross-category promotion opportunity — bundle chips with dips for family segments
Cheezels and Twisties at 270–330g are mid-large players that could be repositioned as value sharing alternatives to Smiths/Doritos


The project successfully delivered a clean, merged retail dataset ready for analytical use. Raw transaction and customer behaviour data were processed through a two-stage pipeline: Excel for initial formatting, null checks, and duplicate validation, followed by SQL to join the two tables on LYLTY_CARD_NBR — a step necessary due to Excel's size limitations. The final dataset was exported and visualised in Tableau.
    

<img width="649" height="358" alt="Screenshot 2026-04-25 at 3 18 02 PM" src="https://github.com/user-attachments/assets/68b4ed06-896c-4ab7-bdd2-5ef41d6ee894" />

CONCLUSION
The most important finding is that lifestage — particularly family status — is a far stronger driver of spending than whether a customer shops in the Budget, Mainstream, or Premium tier. Older and Young Families outspend all other segments by a wide margin (up to 2x more than Young Singles), and that gap barely moves across tiers. This means budget spent trying to "upgrade" Budget Families to Premium is largely wasted.
Seasonality is clear and predictable: sales peak sharply in December (likely Christmas and New Year gatherings) and dip through January–February, before recovering. This pattern can directly inform promotional planning and stock decisions.
On the product side, pack format serves distinct missions: large formats (Smiths, Doritos at 330–380g) are sharing occasions, while Kettle's 150–175g range serves premium individual snacking. Mixing these strategies would dilute brand positioning. The appearance of Old El Paso dips in the chip pack-size ranking points to a natural cross-category bundle opportunity, especially for the family segments identified as highest-value.
