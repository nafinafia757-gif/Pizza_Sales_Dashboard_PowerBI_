# Pizza_Sales_Dashboard_PowerBI_

### Project Objective:

The goal of this project is to analyze pizza sales transaction data and convert it into meaningful business insights using interactive visuals.

This dashboard helps understand:

Which pizza categories and sizes generate the most revenue

Customer ordering patterns by time

Monthly sales trends

Overall business performance using KPIs

### Dataset Description:

The dataset contains :

order_id

order_date

order_time

pizza_category

pizza_size

quantity

total_price

Each row represents a pizza item within an order.

## Data Cleaning :

Data was preprocessed before visualization:

Removed unwanted/duplicate columns

Checked and handled null values

Renamed columns for clarity

Corrected data types:

Date column → Date format

Time column → Time format

Quantity & Price → Whole/Decimal numbers

Ensured consistency in category and size names

Loaded the cleaned data into the data model

 ## DAX Calculations:
 
 Calculated Columns
 
DAX


Hour = HOUR('pizza_sales'[order_time])

Month = FORMAT('pizza_sales'[order_date], "MMM")

These columns enable time-based analysis.

 Measures:
 
DAX

Total Revenue = SUM('pizza_sales'[total_price])

Total Pizzas Sold = SUM('pizza_sales'[quantity])

Average Order Value =
DIVIDE([Total Revenue], DISTINCTCOUNT('pizza_sales'[order_id]))

These measures power the KPI cards and charts.

 ## Dashboard Visuals:
 
### Cards (Top Section):

1. Total Orders
   
Shows the total number of unique orders placed.

3. Total Pizzas Sold
   
Displays how many pizzas were sold in total.

4. Total Revenue
   
Shows the overall revenue generated from all orders.

5. Average Order Value
   
Represents the average spending per order.

These KPIs give a quick overview of overall business performance.

 ### Revenue by Category (Bar Chart):
 
This chart shows how much revenue each pizza category generates.

Insight:

Classic and Supreme categories contribute the highest revenue.

Veggie category contributes the least.

Marketing strategies can focus on improving low-performing categories.

### Revenue by Size (Bar Chart):

Displays revenue distribution based on pizza size.

Insight:

Large (L) size pizzas generate the most revenue.

XL and XXL sizes contribute very little.

Customers clearly prefer Large size.

 ###Category vs Size (Stacked Bar Chart):
 
This visual shows which pizza sizes are most sold within each category.

Insight:

Large size dominates across all categories.

Helps understand size preference per category.

Useful for inventory planning.

### Revenue by Month (Line/Trend Chart):

Shows monthly revenue trend across the year.

Insight:

Some months show high sales, others low.

Indicates seasonality in sales.

Offers and promotions can be planned for low-performing months.

### Orders by Hour (Bar Chart):

Shows at what time customers place the most orders.

Insight:

Evening hours are peak ordering time.

Morning hours have very low orders.

Staffing and delivery preparation should be stronger during peak hours.

### Slicers Used:

Pizza Category

Pizza Size

Month

These slicers make the dashboard interactive and allow dynamic filtering.

## Business Insights Summary:

Large pizzas are the primary revenue driver.

Classic & Supreme categories are customer favorites.

Customers prefer ordering in the evening.

Sales show monthly variation (seasonal trend).

Customers often purchase multiple pizzas in a single order.

## Conclusion:

This dashboard converts raw pizza sales data into actionable insights.

It helps stakeholders make informed decisions related to:

Inventory management

Marketing campaigns

Staffing during peak hours

Product and size focus
