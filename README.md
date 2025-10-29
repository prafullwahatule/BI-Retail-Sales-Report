# 🛍️ Retail Sales Power BI Dashboard

## 📖 Project Overview

The **Retail Sales Dashboard** is an interactive **Power BI** project designed to analyze overall sales performance across different categories, demographics, and time periods.  
It gives business users a **single-page visual summary** of key metrics like **Total Sales, Quantity Sold, Average Order Value**, and **Category Contribution %**, along with detailed insights such as **monthly sales trends** and **customer demographics**.

This project helps stakeholders identify **top-performing categories**, understand **customer behavior**, and track **sales growth over time**.

---

## 🎯 Project Objectives

- Visualize **total sales** and **order trends** in one dashboard.  
- Analyze performance by **product category, gender, and age group**.  
- Identify **top-performing months** and **customer segments**.  
- Create an **interactive and dynamic dashboard** with filters and highlights.  
- Generate **automated insights** using Smart Narrative visual.

---

## 📂 Dataset Information

**Dataset Name:** `Sales_Transactions.csv`

| Column Name       | Description |
|-------------------|-------------|
| Transaction ID    | Unique ID for each transaction |
| Date              | Date of transaction |
| Customer ID       | Unique customer identifier |
| Gender            | Male / Female |
| Age               | Customer’s age |
| Product Category  | Product type (Beauty, Clothing, Electronics) |
| Quantity          | Number of items purchased |
| Price per Unit    | Cost per unit item |
| Total Amount      | Total purchase value (Quantity × Price per Unit) |

---

## 🧮 Data Transformations

Data was cleaned and transformed in **Power Query Editor**:

- Verified column data types (Date, Text, Whole Number, Decimal).  
- Added a calculated column for **Age Group**:

  ```DAX
  Age Group =
  SWITCH(
      TRUE(),
      Sales_Transactions[Age] <= 25, "Youth (≤25)",
      Sales_Transactions[Age] <= 40, "Adult (26–40)",
      Sales_Transactions[Age] <= 60, "Middle Age (41–60)",
      "Senior (60+)"
  )
  ```
- Created DAX measures for KPIs and category contribution.

