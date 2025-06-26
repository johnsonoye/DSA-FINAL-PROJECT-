# PROJECT TITLE: LITA_CAPSTONE_PROJECT SALES DATA

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


