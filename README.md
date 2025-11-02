# Global-Superstore-Data-Analytics-Project
#🧩 Project Overview
This project analyzes the Global Superstore dataset to uncover business insights across sales, profit, customers, and product performance.
Using SQL, Excel, and Power BI, I designed a complete data analytics solution that converts raw data into meaningful visual insights and interactive dashboards.
The main goal was to help management identify profitable regions, customer behavior, seasonal patterns, and discount impacts — supporting smarter decision-making.
________________________________________
#🎯 Project Objective 
1.	Analyze sales and profit trends by region, category, and time.
2.	Identify top-performing products and customers.
3.	Understand how discounts affect profit margins.
4.	Build interactive dashboards for business users to explore insights dynamically.
________________________________________
#🧰 Tools & Technologies Used Tool	Purpose 
1. SQL (MySQL)	Data extraction, cleaning, and aggregation
2. Excel	Data cleaning, calculations, and preliminary visualization
3. Power BI	Final dashboard creation and data storytelling
4. DAX & Power Query	Used for advanced measures, relationships, and model building
________________________________________
#🧹 Step 1: Data Cleaning & Preparation  

#🔹 In SQL

  Imported raw CSV data into MySQL database.
  
#Used SQL queries to:

#Remove duplicates (DISTINCT)

#Fix missing values using COALESCE()

#Convert Order Date and Ship Date to date format (STR_TO_DATE())

#Create new fields for Year, Month, Quarter using date functions

# Example Query: 
•	 SELECT 
•	 Order_ID, 
•	Region, 
•	Category, 
•	YEAR(Order_Date) AS Year, 
•	MONTH(Order_Date) AS Month,
• Profit, Sales, Discount
•	FROM GlobalSuperstore;

#🔹 In Excel
1.	Imported SQL results into Excel.
2. 	Verified data consistency, formatted columns, and created dynamic named ranges.
3.	Added new calculated columns (Profit %, YoY Growth).
4.	Linked clean data into pivot tables for KPI validation.
________________________________________

#🏗️ Step 2: Data Modeling in Power BI 

1. Connected SQL database directly to Power BI for live data refresh.
2. Built data model with relationships:
3. Orders → Products → Customers → Regions
4. Created hierarchy: Year → Quarter → Month.
5. Built calculated columns and measures using DAX.
________________________________________

#⚙️ Important DAX Measures Used 
1. Total Sales = SUM(Sales[Sales])
2. Total Profit = SUM(Sales[Profit])
3. Profit Margin = DIVIDE([Total Profit], [Total Sales]) * 100
4. YoY Sales Growth = 
VAR CurrentYear = SELECTEDVALUE(Sales[Year])
VAR PrevYear = CurrentYear - 1
RETURN
DIVIDE(
    [Total Sales] - CALCULATE([Total Sales], Sales[Year] = PrevYear),
    CALCULATE([Total Sales], Sales[Year] = PrevYear)
)
Negative Profit Products = CALCULATE(COUNTROWS(Sales), Sales[Profit] < 0)
________________________________________
#🧾 Step 3: Dashboard Design & Structure
The report was divided into 5 interactive pages for storytelling clarity:
________________________________________
#📊 Page 1: Executive Summary 
Goal: Provide a high-level overview of performance.
Visuals Used:
1. KPI Cards → Total Sales, Profit, Quantity, Orders
2. 	Map → Sales by Region
3. 	Donut Chart → Segment-wise Distribution
4. 	Bar Chart → Top 5 Categories by Sales
Key Insights:
5. 	Technology category gives the highest profit margin.
6. 	West region leads in sales and revenue contribution.
________________________________________
#📈 Page 2: Regional Performance 
Goal: Compare revenue and profit across regions and countries.
Visuals Used:
1. 	Clustered Column → Sales by Region
2. 	Treemap → Sales by Country
3. 	Bar Chart → Profit by State
4. 	Line Chart → Sales Trend by Region
5. Slicers: Year, Region, Country, Category
Insight: The West region shows the best sales performance consistently.
________________________________________
#👥 Page 3: Customer Insights 
Goal: Understand customer contribution and loyalty patterns.
Visuals Used:
1. Table → Top Customers with Sales & Profit
2. Donut → New vs Repeat Customers
3. 	Line Chart → Customer Orders Over Time
4.  Column Chart → Profit Contribution by Segment
5. Slicers: Year, Segment, Region, Customer Name
Insight: Few top customers drive majority of profits.
________________________________________
#📦 Page 4: Product Analysis 
Goal: Evaluate product performance and discount impact.
Visuals Used:
1. 	Tree Map → Category/Sub-category Sales
2. 	Stacked Column → Profit by Product
3.  Bar Chart → Discount vs Profit Impact
4. 	KPI → Total Negative Profit Products
5. Slicers: Category, Sub-Category, Discount Range
Insight: Discounts above 20% reduce profit drastically.
________________________________________
#🕒 Page 5: Time Series Analysis 
Goal: Analyze seasonal and yearly trends.
Visuals Used:
1.	Line Chart → Monthly Sales Trend
2.	Area Chart → Quarterly Profit Trend
3.	Column Chart → YoY Comparison
4.	Scatter Chart → Seasonal Peaks
5.	Line Chart → MoM Profit Trend
6.	Stacked Column → Category-wise Trend
Slicers: Year, Month/Quarter, Region, Category, Sub-Category, Discount Range
Insight: Sales peak during November–December, reflecting holiday shopping patterns.
________________________________________
# Insights Summary
1.	Technology & Office Supplies are the most profitable categories.
2.	High discounts (>20%) cause profit decline.
3.	Consumer Segment dominates in both revenue and orders.
4.	Q4 sales peaks indicate strong seasonal opportunities.
5.	Top 10 customers account for a significant share of profit.
________________________________________
💼 Business Recommendations
1. 	Focus on retaining top customers with loyalty programs.
2. 	Optimize discount strategy for low-profit categories.
3.  Increase stock levels before holiday seasons (Q4).
4.	Improve performance in underperforming regions like South.
________________________________________
🚀 Project Outcome
This end-to-end project showcases how raw data can be cleaned with SQL, validated in Excel, and visualized interactively in Power BI.
It demonstrates full data analytics workflow skills — data preparation, modeling, visualization, and storytelling.
________________________________________
👨‍💻 About the Analyst
Name: Ramesh Dinne
Role: Data Analyst Trainee – INFOZ IT Solutions
Expertise: Excel, SQL, Power BI, Python (Pandas)
Focus: Turning data into stories that drive business decisions

