# PROJECT TITLE: LITA CAPSTONE PROJECT SALES DATA

[Project Overview](#project-overview)  
[Analysis Tools](#analysis-tools)  
[OUTCOME OF SALES DATA PROJECT USING MICROSOFT EXCEL](#outcome-of-sales-data-project-using-microsoft-excel)  
[Structured Query Language (SQL)](#structured-query-language-sql)  
[Microsoft Power BI](#microsoft-power-bi)  
[FINDINGS AND RECOMMENDATIONS](#findings-and-recommendations)

## Project Overview
This is a Sales Performance Analysis for a Retail Store, I am tasked with analyzing the sales performance of a retail store. You will need to explore sales data to uncover key insights such as top-selling products, regional performance, and monthly sales trends. The goal is to produce an interactive Power BI dashboard that highlights these findings

## Analysis Tools
i. Microsoft Excel <a href="https://www.microsoft.com/en-ng/">Download Here</a> ii. Structured Query Language iii. Microsoft PowerBI

I am to explore the Sales Data to uncover key insights such as top-selling products, regional performance, and monthly sales trends. With my Excel tool i will

- Perform an initial exploration of the sales data.
- Use pivot tables to summarize; Total sales by product, region, and month.
- Use Excel formulas to calculate metrics such as average sales per product and total revenue by region.
- Create any other interesting report.

# OUTCOME OF SALES DATA PROJECT USING MICROSOFT EXCEL
The first thing I did was to calculate the revenue for each of the row on the Sale Dataset by multiplying the Quantity row by the UnitPrice row

                    =F2*G2

For the result i got from the dataset worked on 

[githubsales.xlsx](https://github.com/user-attachments/files/20933803/githubsales.xlsx)


For easier visualization I added a screenshoot of my outcome

![Capture](https://github.com/user-attachments/assets/d39e7160-77cf-4329-b3c9-0fa86ce66903)

I thereaffter went on to use Pivot Table to create beautiful and interesting reports showcasing

a. Total Sales by Product b. Total Sales by Region c. Total Sales by Month d. Top-Selling Product e. Average Sales by Product

![Total Sales by Products](https://github.com/user-attachments/assets/3aa6e7b3-fa46-41c9-9517-fe4bfa38792f)


![Total sales by region](https://github.com/user-attachments/assets/9dacaf4a-9bd3-4d00-a517-50c773895005)


![Total Sales by month](https://github.com/user-attachments/assets/008e8bfd-77a4-4f53-af12-785b4e30c8d1)

![Top selling product by revenue](https://github.com/user-attachments/assets/310a5f2f-3a85-4aac-b3a3-b23260c724d3)

![Top selling Products](https://github.com/user-attachments/assets/0d8d4ddd-11d7-45fc-af6f-4275bcae6262)


![Average sales per product](https://github.com/user-attachments/assets/ef6966c5-bc20-4658-afd4-d89a78a2b3ee)


Pivort Charts were also added in order for the Sales Overview to be visualized


![11](https://github.com/user-attachments/assets/404db023-63ff-4ccb-b042-1bf36341432b)

![12](https://github.com/user-attachments/assets/0d6f925e-326b-47ae-80d0-1aabd9a580c9)

![13](https://github.com/user-attachments/assets/3831dcaa-00a0-43ff-8412-b2a665e645ff)


## Structured Query Language (SQL)

This is the second Analysis tool I used in exploring the Sales Dataset in this project. SQL means standard language for accessing, managing and modifying data in a relational dtatabase.

I used the SQL Tool to answer the following questions after I had successfully imported my data into a database i created which I named LITA_DB.

- retrieve the total sales for each product category.
- find the number of sales transactions in each region.
- find the highest-selling product by total sales value.
- calculate total revenue per product.
- calculate monthly sales totals for the current year.
- find the top 5 customers by total purchase amount.
- calculate the percentage of total sales contributed by each region.
- identify products with no sales in the last quarter.


## Microsoft Power BI

This is the third Analysis Tool I used in exploration of the Sales Data. PowerBI is a business analytics service by Microsoft that enables users to visualize and Analyze data from various sources. It provides interactive dashboards, reports and data visualization tools to help organizations make data-driven decisions.

I am tasked to use PowerBI to:
- Create a dashboard that visualizes the insights found in Excel and SQL. The dashboard should include a sales overview, top-performing products, and regional breakdowns.

The first step I took was to get my data from Excel Workbook, transform my data and check the data quality, profile and distribution. After transfroming my data into a clean state I proceeded to create the following Visuals from my dataset.

![14](https://github.com/user-attachments/assets/05413691-70ed-4d6a-8fb4-1655591a0b5f)

- Regional Performance
- Monthly Overview of Sales for Year 2023 and 2024
- Sum of Quantity by Product
- Sum of Revenue by Product

![15](https://github.com/user-attachments/assets/d1ca1ae6-2d92-4e0f-b9f7-51ced5315c02)

Slicers for Product and Region was added to create and interesting report and dashboard

## FINDINGS AND RECOMMENDATIONS
### Prouct Performance
- My analysis reveals that 'Hat' has the highest sales with a total of 15,929 showing a strong and steady market demand.
- Shoes generated the most revenue with a total of 613,380.
- There is room for sales improvement by conducting regular customer feedbacks in order to know why some products are raking in low sales.

![16](https://github.com/user-attachments/assets/bd590c79-251a-426f-b020-e6e8d2958ecc)

![17](https://github.com/user-attachments/assets/9b353eb1-3a06-403b-9783-8a37f279b6e1)

### Regional Performance
- Amongst the four (4) regions in the dataset, South had the most sales with a total 927,820 while West generated the lowest sales with a total of 300,345.
- This shows that there need for sales awareness e.g advertising, marketing to be created in the West region in order to boost their sales. Offer Sales plan and also Easy buy plan in the West.

![18](https://github.com/user-attachments/assets/7b27ef4d-6504-4700-b4bc-00fba6fbd66f)

### Monthly Sales Trend

- Sales were higher in the month of February of both year 2023 and 2024 while in year 2023 April sales was the lowest with a total sales of 7,425 and in year 2024 July had the lowest sales with a total of 37,200.
- There is need for the organization to coduct a sales poll in order to know why sales are particularly low in April of 2023 and 2024 this will give an insight into how sales can be boosted in those months in the coming year.

![19](https://github.com/user-attachments/assets/32bf7848-6838-429a-8887-404e17daca73)



I ran various codes in order to be able to extract the neccesary information i needed which are embedded in the Salesdata Table on my LITA_DB


select *from[dbo].[SalesData]

- TOTAL REVENUE PER PRODUCT

```sql

SELECT sum (revenue)as totalsale4hat FROM SalesData WHERE PRODUCT = 'HAT'

SELECT sum(revenue) as totalsale4shoes FROM SalesData WHERE PRODUCT = 'SHOES'

SELECT sum(revenue) as totalsales4shirt FROM SalesData WHERE PRODUCT = 'SHIRT'

SELECT sum(revenue) as totalsales4gloves FROM SalesData WHERE PRODUCT = 'GLOVES'

SELECT sum(revenue)as totalsales4socks FROM SalesData WHERE PRODUCT = 'SOCKS'

SELECT sum(revenue) as totalsale4jacket  FROM SalesData WHERE PRODUCT = 'JACKET'


- Find The Number Of Sales Transactions In Each Region.

SELECT REGION,
count(orderid)as regionalsales from [dbo].[SalesData] 
GROUP BY REGION
ORDER BY regionalsales DESC


- HIGHEST SELLING PRODUCT BY TOTAL SALES VALUE

select top 1 (product),
sum (revenue) as totalsales from [dbo].[SalesData]
group by product


- TOTAL REVENUE PER PRODUCT

SELECT PRODUCT,
SUM(REVENUE) AS TOTALREV FROM[dbo].[SalesData]
GROUP BY PRODUCT
ORDER BY TOTALREV DESC


- MONTHLY SALES TOTAL FOR THE CURRENT YEAR

SELECT MONTH (ORDERDATE)AS MONTHS,
SUM (REVENUE) AS MONTHLYSALES
FROM[dbo].[SalesData]
WHERE
YEAR(ORDERDATE)= YEAR (GETDATE())
GROUP BY MONTH (ORDERDATE) 
ORDER BY MONTHS


- TOP 5 CUSTOMERS BY TOTAL PURCHASE AMOUNT


SELECT TOP 5 (CUSTOMER_ID) AS TOPCUSTOMER, SUM (REVENUE) AS TOTAL_PURCHASEPRICE FROM [dbo].[SalesData] GROUP BY Customer_Id ORDER BY TOPCUSTOMER DESC

- PERCENTAGE OF TOTAL SALES CONTRIBUTED BY EACH REGION

```sql
SELECT REGION,
SUM(REVENUE) AS TOTAL_SALES,
(SUM(REVENUE)*100.0/(SELECT SUM(REVENUE) FROM[dbo].[SalesData]))
AS PERCENTAGE_TOTAL_SALES
FROM [dbo].[SalesData] 
GROUP BY REGION
ORDER BY PERCENTAGE_TOTAL_SALES DESC


- PRODUCTS WITH NO SALES IN THE LAST QUARTER

SELECT OrderID,
Product 
FROM [dbo].[SalesData] WHERE OrderID  NOT IN (SELECT OrderID 
FROM [dbo].[SalesData]
WHERE OrderDate >=
DATEADD (QUARTER, -1,GETDATE ()))


SELECT OrderID  
 FROM SalesData 
 WHERE Product NOT IN (
 SELECT DISTINCT Product  
 FROM SalesData  WHERE OrderDate between
 dateadd (quarter, -1, getdate())
 and getdate())

