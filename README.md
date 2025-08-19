

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
# Task 2: Social Media Campaign Performance Tracker

**Objective:**  
Analyze Facebook & Instagram ad campaign data to evaluate performance, engagement, CTR, and ROI.  

**Tools Used:**  
- Power BI  
- Google Looker Studio  
- Excel/Google Sheets  
- Canva (for visual enhancement, optional)  

**Process:**  
- Designed a **dashboard** to track key campaign metrics including Impressions, Clicks, CTR, Conversions, and Spend.  
- Built a **Funnel Chart** (Impressions → Clicks → Approved Conversions) to visualize the customer journey.  
- Used **Matrix and Category Filters** for deeper breakdowns (CampaignID, Gender, Interests, Placements).  
- Enhanced storytelling with clean visuals and tooltips for better interactivity.  

**Skills Gained:**  
- Marketing Analytics  
- Campaign Optimization  
- Dashboard Storytelling & Data Visualization  

**Key Insights:**  
- CTR varied significantly across interests and placements.  
- Despite high impressions, certain campaigns showed **drop-offs** before conversion.  
- Gender- and interest-based targeting provided actionable insights for optimization.  

**Outcome:**  
Delivered a **Social Media Campaign Performance Tracker** dashboard that highlights strengths, inefficiencies, and ROI-driven insights for better ad strategy.





