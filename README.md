# Business-Analysis-with-Power-BI

## Introduction
Following the completion of the "Mastering of DAX" course, I participated in an internship program organized by ForesightBI to apply my newly acquired DAX skills.

## Background:
Forggith Pharmaceuticals (Forggith) is a pharmaceutical manufacturing company based in Germany. They specialize in producing medical drugs distributed to consumers through their network of distributors. Forggith does not engage in direct sales to retailers or end-users but instead relies on a team of sales and marketing professionals to ensure the availability of their products to customers.

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

You can interact with the dashboard [here](https://app.powerbi.com/view?r=eyJrIjoiMzE3NWEyNTktNWI5Ny00ZmQ1LWIyOTItN2IyY2UwZjc4OTk1IiwidCI6ImExZGNjNGZiLTRlYzAtNGI1Ni04NDg1LTRmOTgzYzMyODY0MiJ9)

## Summary of Findings
-  Total Revenue exceeded the target set with a sum of $2.7 billion.
-  Team Delta emerged as the most successful team, generating 30.8% of the actual revenue, with Abigail being the top sales representative.
-  The top-selling product category was Analgesics, with Ionclotide leading as the top-performing product, generating a revenue of $165,614,153 and selling 262,463 units.
   Conversely, Amphesirox was the least performing product, yielding a revenue of $2,506,175.
-  Butzbach exhibited the highest revenue ($93,561,780) by location, surpassing Castrop-Rauxel by 122.41%.
-  Analgesics accounted for 20.21% of revenue, making it the top-performing product class, while Antimalarial products performed the least.
-  Actual Revenue Year-to-Date (YTD) and Total Target YTD showed the greatest disparity in 2022, with Actual Revenue YTD surpassing Total Target YTD by $881,113,714.
-  February saw the highest Actual Revenue Month-over-Month (MoM) increase at 43.86%.
-  Pharmacy contributed 52.90% ($5,881,894,078) of revenue by channel, with Retail having the highest Target Revenue percentage at 62.59%, followed by Government, Institution, and 
   Private channels.
-  Volume Achieved and Volume Target showed the greatest disparity in 2022, with Volume Achieved surpassing Volume Target by 2,140,110 units.

## Recommendations
-  Offer bonuses and incentives to Abigail Thompson and Team Delta to maintain motivation and morale.
-  Implement additional marketing strategies for underperforming products.
-  Consider rebranding underperforming products and expanding into new markets.
-  Optimize search engine visibility to enhance product exposure on websites and web pages.

## Thank you for reading.
