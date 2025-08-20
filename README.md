

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


FUTURE_DS_02
Task 2 — Social Media Campaign Performance Tracker (Power BI / Looker Studio)

A dashboard analyzing Facebook & Instagram ad campaign data to track engagement, CTR, and ROI, with funnel visualization for conversions.

📁 Files

Task2/Social_Media_Campaign.pbix — Power BI dashboard file


🎯 Objectives

Track Impressions, Clicks, CTR, Conversions, and ROI.

Create a Funnel Chart (Impressions → Clicks → Approved Conversions).

Compare performance by Campaign ID, Gender, Interests, and Placements.

Provide KPI Cards for quick insights.

Enable drill-down with filters for campaign analysis.

📊 Key Measures (DAX)
-- CTR
CTR = DIVIDE([Total Clicks], [Total Impressions], 0)

-- Conversion Rate
Conversion Rate = DIVIDE([Approved Conversions], [Total Clicks], 0)

-- ROI
ROI = DIVIDE([Revenue] - [Spend], [Spend])

-- Engagement Rate
Engagement Rate = DIVIDE([Clicks] + [Likes] + [Shares] + [Comments], [Impressions])

✅ Completed Tasks

Task 2 – Social Media Campaign Performance Tracker

Objective: Analyze Facebook/Instagram campaign data to evaluate CTR, ROI, and engagement.

Tools Used: Power BI, Google Looker Studio, Excel/Sheets, Canva (optional for design)

Skills Gained: Marketing analytics, campaign optimization, dashboard storytelling

Deliverable: Interactive dashboard with funnel visualization, KPIs, and campaign insights to support better ad spend strategy.

# 🎓 College Event Feedback Analysis – Internship Project (Task 3)

This project analyzes **student event feedback** to uncover satisfaction trends and provide actionable improvement recommendations.  
The project combines **Python NLP sentiment analysis** with a **Power BI dashboard** for visualization.

---

## 🚀 Objectives
- Analyze survey responses from students
- Perform **sentiment analysis** (positive/negative/neutral)
- Identify **average ratings & key improvement areas**
- Visualize trends using **interactive dashboard**

---

## 🛠️ Tools & Skills
- **Google Colab** → Data processing & NLP
- **pandas** → Data wrangling
- **TextBlob / VADER** → Sentiment analysis
- **seaborn / matplotlib** → Visualizations
- **Google Forms (CSV export)** → Raw data source
- **Power BI** → Final dashboard, charts & KPIs

---

## 📊 Insights
- **Average Rating:** 5.92 / 10  
- **Sentiment Distribution:** Mostly neutral with clear areas needing improvement  
- **Recommendations Table:** Question-wise average rating with suggested actions  

---

## 📂 Project Files
- `feedback_analysis.ipynb` → Jupyter/Colab notebook (Python NLP & charts)
- `College_Event_Feedback.pbix` → Power BI dashboard
- `data.csv` → Raw survey data
- `images/dashboard.png` → Dashboard screenshot

---

## 🎯 Skills Gained
- Data cleaning & preprocessing
- Text analytics & sentiment analysis
- Survey insights extraction
- Data visualization & storytelling
- Dashboard design (Power BI)

---

## 📌 How to Run
1. Open `feedback_analysis.ipynb` in Google Colab → run NLP & sentiment analysis
2. Open `.pbix` file in Power BI Desktop → view interactive dashboard
3. Explore slicers, KPIs, and question-wise recommendations



