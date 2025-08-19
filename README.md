

🚀 Future Interns – Data Science & Analytics Internship

This repository contains all tasks completed as part of my internship with Future Interns. Each task demonstrates skills in data analysis, visualization, and business insights using tools like Power BI, Excel, and Python.


FUTURE_DS_01

# Task 1 — Business Sales Dashboard (Power BI)

A Power BI dashboard that analyzes retail sales to identify **sales trends over time** and **high-revenue categories**, with quick KPIs for decision-making.

---

## 📁 Files
- `Task1/Business_Sales.pbix` — main Power BI report


---

## 🎯 Objectives
1. Show overall performance (Total Sales, Total Orders, Total Quantity, Avg Order Value, Distinct Customers, Return %).
2. Visualize **Sales Trend Over Time** (Year-Month).
3. Identify **Top Products by Quantity**.
4. Identify **Top Categories by Revenue** (based on `StockCode`/Category or your categorical field).
5. Enable filtering by **Year** and **Month**.

---

## 📊 Key Measures (DAX)
> Replace `Table`/column names with yours.

```DAX
-- Core
Total Sales = SUMX(Table, Table[Quantity] * Table[Price])
Total Orders = DISTINCTCOUNT(Table[Invoice])
Total Quantity = SUM(Table[Quantity])
Distinct Customers = DISTINCTCOUNT(Table[CustomerID])
Average Order Value = DIVIDE([Total Sales], [Total Orders])

-- Returns (if you have a returns flag/quantity)
Return Orders = CALCULATE([Total Orders], Table[IsReturn] = TRUE())
Return % = DIVIDE([Return Orders], [Total Orders])

-- Time helpers
Year = YEAR(Table[InvoiceDate])
Month Name = FORMAT(Table[InvoiceDate], "MMMM")
Month Number = MONTH(Table[InvoiceDate])
Year-Month = FORMAT(Table[InvoiceDate], "YYYY-MMM")



✅ Completed Tasks

Task 1 – Business Sales Dashboard from E-Commerce Data

Objective: Analyze e-commerce data to identify best-selling products, sales trends, and high-revenue categories.

Tools Used: Power BI,Excel

Skills Gained: Data cleaning, DAX formulas, trend analysis, business storytelling

Deliverable: Interactive Power BI dashboard with visuals and insights

# FUTURE_DS_02 

Task 2 - Student Event Feedback Analysis

## 📌 Task Overview
This task focuses on analyzing student feedback collected from an event.  
The dataset includes responses to multiple questions with ratings, comments, and engagement metrics.  
The goal is to identify patterns, compute average ratings, and visualize insights using Power BI.

---

## 🔑 Objectives
- Clean and structure the feedback dataset.
- Calculate average ratings per question.
- Identify key trends in student satisfaction.
- Create visualizations for better understanding.

---

## 🛠️ Tools & Technologies
- **Power BI** (Data Visualization & Dashboarding)  
- **Excel / CSV** (Data Source)  
- **DAX** (Measures for calculations like average ratings)  

---

## 📊 Key Insights
- **Average Rating** per question was computed and visualized.  
- **Bar chart** representation showed variation in feedback across questions.  
- Identified questions with relatively lower satisfaction, which can be improved in future events.  

---


---

## 🚀 Learning Outcomes
- Learned to create **custom DAX measures** (e.g., Average Ratings).  
- Gained experience in designing **question-wise dashboards**.  
- Improved understanding of **feedback analytics and reporting**.  


