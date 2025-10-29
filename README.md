# 🛍️ Retail Sales Power BI Dashboard
## 📖 Project Overview

The Retail Sales Dashboard is an interactive Power BI project designed to analyze overall sales performance across different categories, demographics, and time periods.
It gives business users a single-page visual summary of key metrics like Total Sales, Quantity Sold, Average Order Value, and Category Contribution %, along with detailed insights such as monthly sales trends and customer demographics.

This project helps stakeholders identify top-performing categories, understand customer behavior, and track sales growth over time.

## 🎯 Project Objectives

Visualize total sales and order trends in one dashboard.

Analyze performance by product category, gender, and age group.

Identify top-performing months and customer segments.

Create an interactive and dynamic dashboard with filters and highlights.

Generate automated insights using Smart Narrative visual.

## 📂 Dataset Information

Dataset Name: Sales_Transactions.csv

Column Name	Description
Transaction ID	Unique ID for each transaction
Date	Date of transaction
Customer ID	Unique customer identifier
Gender	Male / Female
Age	Customer’s age
Product Category	Product type (Beauty, Clothing, Electronics)
Quantity	Number of items purchased
Price per Unit	Cost per unit item
Total Amount	Total purchase value (Quantity × Price per Unit)

## 🧮 Data Transformations

Data was cleaned and transformed in Power Query Editor:

Verified column data types (Date, Text, Whole Number, Decimal).

Added a calculated column for Age Group:

Age Group =
SWITCH(
    TRUE(),
    Sales_Transactions[Age] <= 25, "Youth (≤25)",
    Sales_Transactions[Age] <= 40, "Adult (26–40)",
    Sales_Transactions[Age] <= 60, "Middle Age (41–60)",
    "Senior (60+)"
)


Created DAX measures for KPIs and category contribution.

##💡 Key Performance Indicators (KPIs)
KPI Name	Formula / DAX	Description
Total Sales	SUM(Sales_Transactions[Total Amount])	Total revenue generated
Total Quantity Sold	SUM(Sales_Transactions[Quantity])	Total number of items sold
Average Order Value	DIVIDE([Total Sales], COUNT(Sales_Transactions[Transaction ID]))	Average value per order
Average Customer Age	AVERAGE(Sales_Transactions[Age])	Average customer age
Category Contribution %	DIVIDE(SUM(Sales_Transactions[Total Amount]), CALCULATE(SUM(Sales_Transactions[Total Amount]), ALL(Sales_Transactions)))	% contribution of each category
Sales Growth %	DIVIDE([Total Sales] - [Prev Month Sales], [Prev Month Sales])	Month-over-month growth rate

## 📈 Visuals Used
Visual	Type	Fields Used	Purpose
Sales by Gender	Donut Chart	Gender, Total Sales	Compare sales by gender
Monthly Sales Trend	Line Chart	Date (Month), Total Sales	View monthly performance trend
Avg Order Value by Category	Column Chart	Product Category, Avg Order Value	Compare AOV across categories
Sales by Product Category	Clustered Column Chart	Product Category, Total Sales	Identify top-selling categories
Sales by Age Group	Bar Chart	Age Group, Total Sales	Analyze sales distribution by age segment
Category Contribution %	Donut Chart	Product Category, Contribution %	Visualize share of each category
Sales Insights Summary	Smart Narrative	All KPIs	Automatically generated business insights

## 🎛️ Filters (Slicers) Used
Slicer	Field	Function
Date Range	Date	Filter dashboard by specific period
Product Category	Product Category	Focus on selected category
Gender	Gender	Filter visuals by male/female
(Optional)	Age Group, Customer ID	Drill down to segment level

## 🧠 Smart Narrative Insights

May recorded the highest Total Sales of ₹53,150, which was 125.02% higher than September, the month with the lowest sales of ₹23,620.

May contributed 11.66% of the overall yearly sales.

Across all 12 months, Total Sales ranged between ₹23,620 and ₹53,150, showing clear variation in monthly performance.

## 🎨 Dashboard Design

Theme: Yellow–Green (bright and professional).

Top section shows KPIs with icons for better readability.

Left panel includes Filter Section + Smart Insights Summary.

All visuals designed for clean alignment and color consistency.

Highlights, shadows, and rounded panels used for premium design feel.

## 🛠️ Tools Used

Microsoft Power BI Desktop

Power Query Editor

DAX (Data Analysis Expressions)

Excel / CSV Dataset

## 🏁 Final Outcome

✅ One-page interactive dashboard
✅ Real-time filtering with slicers
✅ Business insights auto-generated with Smart Narrative
✅ KPI summary for performance monitoring
✅ Professional layout ready for portfolio & interviews

## 📷 Dashboard Preview
<img width="1302" height="740" alt="Screenshot" src="https://github.com/user-attachments/assets/78757df9-0c48-4880-bc12-284d7deb31a8" />

## 👨‍💻 Created By

Prafull Wahatule
🎓 MCA (2023–25) | 💼 Aspiring Data Analyst
🧩 Tools: Power BI, SQL, Python, Excel
🔗 GitHub: prafull816
