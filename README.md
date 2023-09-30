# Business-Analysis-with-Power-BI


## Introduction 
Upon concluding the "Mastering of DAX" course, I partook in an internship program organised by ForesightBI to put into practice my newly  acquired DAX skills. 
## Background:
Forggith Pharmaceuticals (Forggith) is a Pharmaceuticals Manufacturing Company based in Germany. They produce medical drugs which get to the consumers through their distributors. Forggith does not sell directly to retailers or end-users, but rather rely on their team of Sales and Marketing pros to ensure that customers get their products.

## Objectives
The task is to produce 2 reports whereby the Sales and marketing teams can track their performances and also for the Executive team to monitor and track revenue and align with the set targets, and also provide insights to the following questions:
1.	What is the total revenue and total target.
2.	What is the Year-To-Date for the Total Revenue and Total Target
3.	Compare the revenue achieved with target revenue
4.	What is the distribution of volume achieved to target volume
5.	What is the month-on-month percentage change based on the revenue
6.	What is the revenue distribution by location, channel and product class
7.	What is the revenue distribution by sales representatives and sales teams
8.	Target volume and revenue achievement by sales representatives.

## Skills Demonstrated
- DAX
- Data Modelling
- Quick Measures
- Storytelling with data

## The Dataset 
The data came in an excel files named pharma dataset and pharma target. Pharma dataset has 7 worksheet containing Dim Location, Dim Channel, Dim Sub-channel, Dim Employees, Dim Products, Sales 2022 and Sales 2023-2025 while Pharma target has just 1 worksheet. 

## Data Transformation
The data was cleaned using Power Query Editor of PowerBI. The data was load in Power Query and the following transformations were done.
-	Sales 2023 – 2025 was appended to Sales 2022 and renamed Sales
-	Sub-Channel was merged to Channel
-	In the Target workbook, the following were carried out:
      1.  Selected the following columns Productid, Sales Rep id, and month; and unpivoted the other columns
      2.  Merged month and year as Date and change the data type from text to date.
-	In the data view:

      i. Add a new column to both Sales and Target “Total Sales and Total Target”

 	            Total Sales = Sales[quantity] * Related (Dim Product[productprice])
 	
                Total Target = Sales[quantity] * Related (Dim Product[productprice]
 	
      ii. Created a Calendar Table using CALENDARAUTO ()
- Created a table for all my DAX Measures. Here are the measures created ![Here](https://github.com/Mayreeobi/Business-Analysis-with-Power-BI/blob/main/Measures.png)

## Data Modelling
Relationship was created using the Star Schema. There was two facts tables and 5 dimension tables including the calendar
![](https://github.com/Mayreeobi/Business-Analysis-with-Power-BI/blob/main/schema.png)

## Analysis and Visualization
Here a sneak peek of the report  ![here](https://github.com/Mayreeobi/Business-Analysis-with-Power-BI/blob/main/sales.png)

You can interact with the dashboard [here] (https://app.powerbi.com/view?r=eyJrIjoiMzE3NWEyNTktNWI5Ny00ZmQ1LWIyOTItN2IyY2UwZjc4OTk1IiwidCI6ImExZGNjNGZiLTRlYzAtNGI1Ni04NDg1LTRmOTgzYzMyODY0MiJ9)

## Summary of Findings
-	Total Revenue exceeded the target set with a sum of $2.7bn
-	Team Delta is the most successful team generating 30.8% of the actual revenue, while Abigail is the top sales rep.
-	Top selling product category was Top Performing product is Ionclotide, it generated a revenue of $165,614,153 and sold 262,463 quantities. While the least performing product is Amphesirox with a revenue of $2,506,175. 
-	Butzbach had the highest Revenue ($93,561,780) by Location and was 122.41% higher than Castrop-Rauxel, which had the lowest Revenue.
-	Analgesics accounted for 20.21% of Revenue thus making it the top performing product by class while Antimalarial is the least.
-	Actual Revenue YTD and Total Target YTD diverged the most in 
-	the Year was 2022, when Actual Revenue YTD were $881,113,714 higher than Total Target YTD. 
-	February had the highest Actual Revenue MoM% at 43.86%.
-	Pharmacy accounts for 52.90% ($5,881,894,078) of the Revenue by Channel. 
-	Retail had the highest Target Revenue % at 62.59%, followed by Government, Institution, and Private.  
-	Volume Achieved and Volume Target diverged the most when the Year was 2022, when Volume Achieved were 2,140,110 higher than Volume Target.

## Recommendations
-	Abigail Thompson and Team Delta should be given bonuses and incentives to keep them motivated and inspired.
-	More marketing strategies should be put in place for the least performing products
-	Rebranding the least performing product and launch to existing and new markets.
-	Optimize search engines to increase products visibility on the website and web pages.

## Thank you for reading.
