# 💳 Credit Card Analytics Dashboard

A Power BI reporting solution that analyzes credit card transactions and customer demographics to support business decisions around revenue, risk, and customer segmentation. The report is refreshed on a weekly basis.

## 📑 Table of Contents
- [Overview]
- [Data Preparation & Transformations]
- [Dashboard 1: Credit Card Transaction Report]
- [Dashboard 2: Credit Card Customer Report]
- [Data Summary]
- [Tools Used]
- [How to Use]
- [Suggested Future Enhancements]

## 📌 Overview
This project consists of two interconnected report pages built in Power BI:

1. **Credit Card Transaction Report** – focuses on transaction-level metrics (revenue, interest, transaction volume) sliced by card category, spending category, and customer profile.
2. **Credit Card Customer Report** – focuses on customer-level metrics (income, demographics, acquisition) to understand who is generating revenue and how.

Both pages share a common set of interactive filters (slicers) so users can drill into the same time period, card type, gender, or income segment across either view.

## ⚙️ Data Preparation & Transformations
This report is built on a weekly-based dataset. The following transformations and custom columns were created during data preparation (Power Query / DAX) to support the analysis:

* **Age Group Column:** Created a new calculated column that groups the raw `Customer_Age` values into age bands (e.g., 20-30, 30-40, 40-50, 50-60, 60+) for easier segmentation and visualization.
* **Income Group Column:** Added a new column that categorizes customers into income bands (Low, Medium, High) based on their income values.
* **Revenue Column:** Added a calculated Revenue column (derived from transaction/interest data) to serve as the primary metric across both report pages.
* **Week Num 2 Column:** The original `Week Num 1` column was not sorting correctly (sorting alphabetically instead of chronologically), so a new `Week Num 2` column was created and used to properly sort week-wise data in visuals like "Revenue by Week."

## 📊 Dashboard 1: Credit Card Transaction Report

### Key Metrics (KPI Cards)
* **Revenue:** 55M
* **Transaction Amount:** 44.5M
* **Interest Earned:** 7.8M
* **Transaction Count:** 655.7K

### Visuals
| Visual | Description |
| :--- | :--- |
| **Card Category Table** | Breaks down Revenue, Total Transaction Amount, and Interest Earned by card tier (Blue, Silver, Gold, Platinum). |
| **QTR Revenue & Total Trans Count** | Combo chart comparing quarterly revenue (bars) against total transaction volume (line), Q1–Q4. |
| **Revenue by Use Chip** | Compares revenue generated via Swipe, Chip, and Online transaction methods. |
| **Revenue by Expenditure Type** | Revenue split across spending categories: Bills, Entertainment, Fuel, Grocery, Food, Travel. |
| **Revenue by Education** | Revenue contribution by customer education level (Graduate, High School, Post-Graduate, Doctorate, etc.). |
| **Revenue by Customer Job** | Revenue split by occupation type: Business Owner, White-collar, Self-employed, Government, Blue-collar, Retiree. |
| **Customer Acquisition Cost** | Acquisition cost comparison across card categories. |

### Filters/Slicers
* Quarter (Q1–Q4)
* Card Category (Silver, Blue, Gold, Platinum)
* Week Start Date
* Gender (F/M)
* Income Category (Low/Med/High)

## 📈 Dashboard 2: Credit Card Customer Report
### Key Metrics (KPI Cards)
* **Revenue:** 55M
* **Income:** 576M
* **Total Interest:** 8M
* **CSS (Customer Satisfaction Score):** 3.19

### Visuals
| Visual | Description |
| :--- | :--- |
| **Revenue by Week** | Weekly trend line comparing revenue across two segments (e.g., gender) from Jan 2023 to Oct 2023. |
| **Revenue by Age Group** | Revenue distribution across age bands (20-30, 30-40, 40-50, 50-60, 60+). |
| **Customer Job Table** | Revenue, Income, and Interest Earned by job type (Businessman, White-collar, Self-employed). |
| **Top 5 States** | Top 5 states by revenue and income contribution (TX, NY, CA, FL, NJ). |
| **Revenue by Marital Status** | Revenue/Income split by Married, Single, Unknown. |
| **Revenue by Income Group** | Revenue/Income split by High, Medium, Low income bands. |
| **Revenue by Dependent** | Revenue/Income split by number of dependents. |
| **Revenue by Education** | Revenue/Income split by education level. |

### Filters/Slicers
* Quarter (Q1–Q4)
* Week Start Date
* Gender (M/F)
* Card Category (Silver, Blue, Gold, Platinum)
* Transaction Method (Swipe, Online, Chip)

## 📋 Data Summary

| Metric | Value |
| :--- | :--- |
| **Total Revenue** | 55,315,410 |
| **Total Transaction Amount** | 44,522,013 |
| **Total Interest Earned** | 7,843,382.23 |
| **Total Income** | 575,914,439 |

## 🛠️ Tools Used
* **Power BI Desktop** – data modeling, DAX calculations, and report design
* **Power Query** – data cleaning and column transformations (Age Group, Income Group, Revenue, Week Num 2)
* **DAX** – calculated columns and measures
* **Slicers & Cross-filtering** – enables synchronized filtering across both report pages

## 🚀 How to Use
 Clone this repository to your local machine:
Open the Credit_Card_Analytics.pbix file in Power BI Desktop.
Use the slicers on the right/top of each page (Quarter, Card Category, Gender, Income Group) to filter the data.
Switch between the Transaction Report and Customer Report tabs to view different angles of the same dataset.
Hover over charts to see exact values via tooltips.

🔮 Suggested Future Enhancements
[ ] Add YoY / MoM growth indicators
[ ] Add a churn/attrition analysis page
[ ] Add drill-through from summary cards to customer-level detail
[ ] Add forecast for future quarter revenue.
