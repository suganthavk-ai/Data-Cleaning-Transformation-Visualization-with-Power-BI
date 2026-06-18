# Data-Cleaning-Transformation-Visualization-with-Power-BI
This Sales Report dashboard provides an overview of business performance by analyzing sales, targets, quantity, profit, and customer contributions across product categories.

## 🎯Project Overview

### Business Problem
Businesses often struggle to monitor sales performance, profitability, and target achievement due to scattered and unstructured data. Without a centralized reporting system, it becomes difficult to identify trends, track business growth, evaluate product performance, and make informed decisions. This dashboard addresses these challenges by transforming raw business data into meaningful insights through interactive visual analytics.

### Objective
The objective of this dashboard is to provide a comprehensive view of business performance by integrating transformed data into a dynamic reporting solution. It enables stakeholders to:
Monitor overall sales, profit, and business growth. 
Track performance against sales targets. 
Identify top-performing and low-performing products/categories. 
Analyze customer purchasing behavior and regional performance. 
Support data-driven decision-making through interactive visualizations. 

### Target Audience
This dashboard is designed for the following users:
Executive Leadership – To monitor overall business performance and support strategic decision-making. 
Sales Operations Team – To track sales targets, revenue trends, and operational efficiency. 
Business Analysts / Data Analysts – To analyze KPIs and generate actionable insights. 
Department Managers – To evaluate category, product, and regional performance. 
Management Teams – To identify opportunities for business growth and improve profitability.

##  🗃️ Data Sources & Architecture

### Source Systems
Local Excel Files (.xlsx) were used as the primary data source for importing and transforming the dataset into Power BI. 
Data was loaded and prepared through Power Query Editor before creating relationships and measures. 

### Data Volume
Timeframe Covered: Based on the dataset available in the workbook (mention actual period if known, e.g., Jan 2024 – Dec 2025). 
Approximate Row Count: Add the total rows loaded into the model (example: ~10,000–50,000 rows depending on your dataset). 
Multiple tables were integrated for analysis and reporting. 

### Storage Mode
Import Mode 
oData is imported into the Power BI model and stored inside the .pbix file. 
oProvides faster report performance and supports full Power BI modeling features.

## ⚙️Data Transformation (ETL)

### Extract
Imported multiple source tables into Power BI. 

### Transform
Performed data cleaning and preparation:
Handled missing values 
Removed duplicates 
Corrected data types 
Created custom columns: 
oProfit Margin % 
oProfit Status 
Applied conditional columns 
Merged tables using Order ID 
Grouped and aggregated data 
Standardized values 

### Load
Loaded transformed tables into the Power BI data model. 

## 🧠 Data Model & DAX

### Data Modeling
Established relationships using Manage Relationships:
One-to-Many relationship using Order ID 
Category-based relationship with Sales Target

### DAX Calculations

### Profit Margin
```DAX
Profit Margin = DIVIDE([Profit],[Amount],0)
```
### Total Sale
```DAX
Total Sales = SUM('Order Details'[Amount])
```
### Total Profit
```DAX 
Total Profit = SUM('Order Details'[Profit])
```
### Target Achievement 
```DAX
Achievement =
DIVIDE([Total Sales],[Target],0)
```

## 🖥️ Dashboard Features

### Interactive dashboard components include:
 KPI Cards 
 Bar Chart 
 Line Chart 
 Pie/Donut Chart Scatter Chart 
 Gauge Chart 
 Table 

##  💡Key Insights

### Trend A: Category Sales Performance
Electronics generated the highest sales (165K), followed by Clothing (139K) and Furniture (127K). This indicates that Electronics is the strongest revenue-driving category and contributes significantly to total business growth.

### Trend B: Target vs Actual Performance Anomaly
Although Electronics achieved the highest sales amount (165K), it exceeded its target (129K), while Clothing and Furniture remained below or close to their assigned targets. This shows uneven category performance and opportunities to improve under performing categories.

### Recommendation:
Increase investment and promotional focus on Electronics to sustain growth while developing improvement strategies for Clothing and Furniture through pricing optimization, targeted campaigns, and inventory planning. Also review low-performing order clusters shown in the sales–quantity analysis to improve conversion and profitability.

### Conclusion:
The sales dashboard shows strong overall business performance with Total Sales of 435.90K and Electronics emerging as the top-performing category. However, performance gaps across categories suggest the need for category-specific strategies to maximize sales achievement and profitability.

## 🚀 How To Use

### Prerequisites:
Install the latest version of Power BI Desktop before opening the report.

### File Formats:
Clone or download the repository to access the .pbix or .pbit files.

### Data Refresh:
Open Transform Data → Data Source Settings and update the source file location to connect with your local dataset.

### Dashboard Navigation:
Review KPI cards for overall performance.
Analyze charts for sales, profit, and customer trends.
Compare category and product performance across visuals.

### Customization:
	Users can modify visuals, update measures, and extend the dashboard based on business 
  
## Tech Stack section
### Tech Stack
- Power BI Desktop
- Power Query
- DAX
- Excel
- Data Modeling
- ETL
  
## Add project outcomes
## Business Outcomes
✔ Improved reporting visibility  
✔ Reduced manual analysis effort  
✔ Enabled KPI monitoring  
✔ Supported data-driven decisions

