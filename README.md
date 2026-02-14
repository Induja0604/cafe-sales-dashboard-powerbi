# cafe-sales-dashboard-powerbi
## Project Overview
This project is an interactive Power BI dashboard built to analyze cafe sales performance.  
The dashboard provides insights into revenue trends, product performance, payment behavior, and location-wise sales using DAX and Power Query.

##  Dataset Information
The dataset contains transactional sales data with the following fields:
- transaction_id
- item
- quantity
- price_per_unit
- total_spent
- payment_method
- location
- transaction_date

##  Data Cleaning

The following transformations were performed using Power Query:

- Removed null and duplicate values
- Changed data types (total_spent → Decimal, transaction_date → Date)
- Trimmed and cleaned text columns
- Standardized payment_method values
- Verified date formatting

## DAX Measures

Total Revenue = SUM('dirty_cafe_sales'[total_spent])

Total Quantity = SUM('dirty_cafe_sales'[quantity])

Total Transactions = COUNT('dirty_cafe_sales'[transaction_id])

Average Order Value = 
DIVIDE([Total Revenue], [Total Transactions], 0)

## Dashboard Features

- KPI Cards (Revenue, Quantity, Transactions, AOV)
- Monthly Revenue Trend (Line Chart)
- Revenue by Item (Bar Chart)
- Revenue by Payment Method (Donut Chart)
- Revenue by Location (Bar Chart)
- Interactive Slicers (Date, Item, Payment Method)

## 📊 Dashboard Preview

![Cafe Sales Dashboard](screenshots/cafe-sales-dashboard.png)

## Key Insights

- Salad generated the highest revenue.
- Digital wallet was the most preferred payment method.
- In-store and takeaway sales were nearly equal.
- Monthly revenue remained stable with minor fluctuations.

  ## Tools Used

- Power BI
- Power Query
- DAX
- CSV Dataset


  ## Files Included

- cafe_sales_dashboard.pbix
- dirty_cafe_sales.csv
- Dashboard Screenshot
- README.md
