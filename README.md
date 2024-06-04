# Power-BI-SQL-Project
Unveiling Pizza Sales Insights: A Data-Driven Approach

This Power BI report delivers a powerful combination of data visualization and SQL queries, empowering you to unlock valuable insights into your pizza sales.  It provides a comprehensive overview of sales performance through a variety of key performance indicators (KPIs) and showcases the SQL queries used to extract these metrics.

Demonstrating Your Data Analysis Expertise

This report not only presents the results but also unveils the thought process behind them. You'll find the corresponding SQL queries documented alongside each KPI and visualization, allowing you to understand the data manipulation and analysis that went into uncovering these insights.

Actionable Insights at Your Fingertips

Identify Sales Trends: Gain a clear understanding of sales patterns over time, including daily and monthly trends. (SQL Query: SELECT DATENAME(DW, order_date) AS order_day, COUNT(DISTINCT order_id) AS total_orders FROM pizza_sales GROUP BY DATENAME(DW, order_date))

Unlock Customer Preferences: Uncover which pizza categories and sizes are most popular with your customers. (SQL Query: SELECT pizza_category, CAST(SUM(total_price) AS DECIMAL(10,2)) as total_revenue, ... FROM pizza_sales GROUP BY pizza_category )
Make Data-Driven Decisions: Use the insights from this report to optimize your marketing strategies, identify sales opportunities, and maximize profitability.

Key Performance Indicators (KPIs) at a Glance

Total Revenue: Get a handle on the big picture and measure your overall sales performance. (SQL Query: SELECT SUM(total_price) AS Total_Revenue FROM pizza_sales).
Average Order Value: Understand the typical amount customers spend per order. (SQL Query: (SUM(total_price) / COUNT(DISTINCT order_id)) AS Avg_order_Value FROM pizza_sales).

Total Pizzas Sold & Total Orders: Track sales volume and identify periods of peak demand. (SQL Query: SUM(quantity) AS Total_pizza_sold & COUNT(DISTINCT order_id) AS Total_Orders FROM pizza_sales).

Average Pizzas per Order: Analyze customer purchase behavior and identify upselling or cross-selling opportunities. (SQL Query: CAST(CAST(SUM(quantity) AS DECIMAL(10,2)) / CAST(COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS DECIMAL(10,2)) AS Avg_Pizzas_per_order FROM pizza_sales).

Dive Deeper into Sales Trends

Daily & Monthly Trends: Visualize daily and monthly sales trends to spot seasonal patterns and optimize staffing and inventory accordingly. (Refer to the Daily Trend SQL Query above).

Pizza Category and Size: A Slice of the Pie

Percentage of Sales by Pizza Category & Size: See which pizza categories and sizes are driving the most sales and tailor your product offerings to meet customer preferences. (SQL Query: SELECT pizza_category, ... FROM pizza_sales GROUP BY pizza_category and SQL Query: SELECT pizza_size, ... FROM pizza_sales GROUP BY pizza_size).

Who's the Top Seller? Ranking the Stars

Top & Bottom Pizzas by Revenue, Quantity & Total Orders: Identify your best-selling pizzas and uncover any hidden gems that may be underperforming. Use these insights to inform marketing initiatives and promotions. (SQL Queries: Top 5 pizzas by Revenue & Quantity - SELECT Top 5 pizza_name, SUM(total_price) AS Total_Revenue/SUM(Quantity) AS Total_Pizza_Sold FROM pizza_sales GROUP BY pizza_name ORDER BY Total_Revenue/Total_Pizza_Sold DESC, Bottom 5 pizzas by Revenue & Quantity - Order By ASC, Top 5 Pizzas by Total Orders - SELECT Top 5 pizza_name, COUNT(DISTINCT order_id) AS Total_Orders FROM pizza_sales GROUP BY pizza_name ORDER BY Total_Orders DESC, Bottom 5 Pizzas by Total Orders - Order By ASC).

How to Use This Report
This report is designed to be a valuable tool for pizza business stakeholders, including managers, marketing teams, and sales teams. By leveraging the data and insights presented here, you can make informed decisions to:

Boost Sales and Revenue

Optimize Marketing Campaigns

Enhance Customer Satisfaction

Drive Profitability

Additional Notes

The data for this report is from a sample pizza sales dataset.
The report can be customized to include additional metrics and visualizations to meet your specific needs
