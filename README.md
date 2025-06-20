# Pizza_Sales_Project_sql_Powerbi

## **Objective**  
The goal of the project is to analyze pizza sales data using SQL and Power BI to generate valuable business insights for data-driven decision-making.We focus on evaluating key performance indicators (KPIs) that are crucial for understanding customer behaviour and sales trends.


### **Technology Stack**  
- **Data Sources:** MySQL, Excel, CSV . 
- **Tools:** Power BI, Power Query, DAX.  

### **Execution Steps**  

1. **Data Importation:** Connected to various sources (MySQL, Excel, CSV) for a comprehensive dataset.  
2. **Data Standardization:** Converted local currencies to USD using exchange rates for consistent reporting.  
3. **Run SQL Queries for KPIs:** Established relationships between tables, merged product data, and calculated profitability.  
4. **Data Analysis:** Developed interactive dashboards with multiple pages and visualizations like donut charts, bar charts, and maps.  
5. **Advanced measures on Power BI:** Created dynamic DAX measures for KPIs such as revenue, profit, and YoY growth.  
6. **Build Power BI Dashboard:** Implemented automated data refresh and configured RLS for secure data access.

---

## **Project Structure**  

### 1.Database Setup
- **Database Creation**: Created a database named `pizza_db`.
- **Table Creation**: Created tables for pizza sales.
```sql
CREATE TABLE pizza_db.pizza_sales(
        pizza_id INT,
		order_id INT,
		pizza_name_id VARCHAR(300),
		quantity INT,
		order_date DATE,
		order_time TIME,
		unit_price FLOAT,
		total_price FLOAT,
		pizza_size VARCHAR(100),
		pizza_category VARCHAR(100),
		pizza_ingredients VARCHAR(300),
		pizza_name VARCHAR(100)
);
```
### 2.KPIs Findings
**Task 1. Find the total revenue generated**
```sql
SELECT SUM(total_price) AS total_revenue
FROM pizza_sales ;
```

**Task 2. Average Order value**
```sql
SELECT SUM(total_price) / COUNT(DISTINCT order_id) AS average_order_value
FROM pizza_sales ;
```
**Task 3. Total Pizza sold**
```sql
SELECT SUM(quantity) AS total_pizza_sold
FROM pizza_sales;
```
**Task 4. Total Orders**
```sql
SELECT COUNT(DISTINCT order_id) AS total_orders
FROM pizza_sales ;
```
**Task 5. Average Pizza per Order**
```sql
SELECT SUM(quantity) / COUNT(DISTINCT order_id) AS average_pizza_per_order
FROM pizza_sales ;
```
### 3.Data Analysis

### 4.Dashbaord Creation





**Sales Overview Dashboard**  
![Sales Overview](https://github.com/najirh/XGRIP-Power-BI-Executive-Dashboard/blob/main/dark%20dashboard.png)  

**Product Analysis Dashboard**  
![Product Analysis](https://github.com/najirh/XGRIP-Power-BI-Executive-Dashboard/blob/main/product.png)  

**Map Analysis Dashboard**  
![Map Analysis](https://github.com/najirh/XGRIP-Power-BI-Executive-Dashboard/blob/main/dark%20map.png)  

**Light and Dark Mode Example**  
![Light and Dark Mode](https://github.com/najirh/XGRIP-Power-BI-Executive-Dashboard/blob/main/light%20dashboard.png)

---

## **Access the Dashboard**  
Explore the live dashboard here: **[Link to Online Reports Page](https://app.powerbi.com/view?r=eyJrIjoiMDE5N2U2ZTAtZDA2Zi00MDgyLWI0MjMtZTlkYjc1ODc0MWVkIiwidCI6ImY3NDM5NmYzLTgwMTUtNGI3NC1iNDY4LWNkYTA0NTEzZDg0YyJ9)**  

---

## **How to Use the Dashboard**  
1. Use slicers to filter data by region, product category, or time period.  
2. Navigate between pages using bookmarks and buttons.  
3. Drillthrough on products or returns charts for detailed insights.  
4. Toggle between light and dark modes for your viewing preference.

---

### **Copyright:**  
Project dataset created by ZeroAnalyst; it is a simulated company for learning purposes.
