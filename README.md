# Capstone-Project-2
## Project Title
Sales Performance Analysis

## Project Overview
This project is a comprehensive data analysis and visualization dashboard for sales performance. Using Power BI and SQL, it includes insights on top-performing products, customer purchasing behavior, and regional sales breakdowns. The goal is to enable easy, dynamic exploration of sales data to support strategic decision-making.

## Data Source
Incubator Hub, Capstone Project

## Tools Used
- **Excel**: For initial data processing and exploratory analysis[Download here](https://www.microsoft.com)
- **SQL Server**: For data storage, transformation, and management.[Download here](https://www.microsoft.com)
- **Power BI**: For creating interactive dashboards and visualizations.[Download here][Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/)
- **Github for Portfolio Building** (Github.com)

## Data Cleaning and Preparation
-**Data Type Validation**
- Converted `OrderDate` to `Date` format, `Quantity` and `UnitPrice` to numeric data types.
- Ensured `Product` and `Region` fields are consistent as text categories.
**Creating Additional Columns**
- **Total Sales**: Added a `Total Sales` column calculated as `Quantity * UnitPrice`.
- **Date Transformations**: Added `Year`, `Month`, and `Quarter` columns to support time-based analysis.
**Data Standardization**
- Standardized entries in `Region` to be consistent (e.g., “North” vs. “north” corrected).
- Removed leading/trailing spaces in all text fields.

## Data Analysis

The data consists of sales records with fields such as:
- `OrderID`
- `CustomerId`
- `Product`
- `Region`
- `OrderDate`
- `Quantity`
- `UnitPrice`
These were used to derive key metrics such as `Total Sales`, `Monthly Sales`, and `Top 5 Customers` based on purchase amount.

The dashboard provides the following visualizations and insights:

1. **Sales Overview**  
   - **Metric**: Total Sales (Revenue) for the dataset.
   - **Visualization**: Card Visual showing the total revenue.

2. **Monthly Sales Totals for Current Year**  
   - **Purpose**: Track sales trends and seasonality.
   - **Visualization**: Line or Column Chart with monthly breakdown.

3. **Top-Performing Products**  
   - **Purpose**: Identify the highest-grossing products.
   - **Visualization**: Bar Chart sorted by total sales for each product.

4. **Top 5 Customers by Purchase Amount**  
   - **Purpose**: Identify key customers by total sales value.
   - **Visualization**: Horizontal Bar Chart displaying the top customers.

5. **Regional Breakdown of Sales**  
   - **Purpose**: Show sales distribution by region.
   - **Visualization**: Donut Chart representing the percentage of total sales per region.

## SQL Queries Used

Below are some of the SQL queries used to generate key insights:

- **Number of Transactions per Region**:
    ```sql
    SELECT Region, COUNT(OrderID) AS No_of_Sales_Transaction
    FROM CapstoneProject
    GROUP BY Region;
    ```

- **Highest-Selling Product by Total Sales Value**:
    ```sql
    SELECT Top 1 Product, SUM(Quantity * UnitPrice) AS HighestSellingvalues
    FROM CapstoneProject
    GROUP BY Product
    ORDER BY TotalSales DESC
    ```

- **Total Revenue per Product**:
    ```sql
    SELECT Product, SUM(Quantity * UnitPrice) AS TotalRevenue
    FROM CapstoneProject
    GROUP BY Product;
    ```

## Power BI Visualization Details
Each visual in the Power BI dashboard was designed with interactivity in mind:
1. **Filter Panel**: Filters to allow viewers to narrow down data by date range, product, and region.
2. **Interactivity**: Clicking on regions, products, or customers updates all related charts.

## Data Visualizations

## Some Calculations carried out in Excel
![Average Sales data](https://github.com/user-attachments/assets/412ab1a7-36d2-4f3b-9518-73eec24818cf)

## Pivot Table
![Pivot table Sales data 1](https://github.com/user-attachments/assets/ce1a83d6-7e43-4947-b909-4fa1d5696f82)
![Pivot Table Sales data 2](https://github.com/user-attachments/assets/70de8dba-7ef9-4664-813b-b306a3b6fa89)

## Charts
![Charts sales data](https://github.com/user-attachments/assets/14a7ad54-c839-4027-a1cd-845616477443)

## SQL
![Capstone Project Sales data](https://github.com/user-attachments/assets/6cc85a36-4096-44a2-ae33-8d0be6a6f139)
![Capstone Project Sales data 1](https://github.com/user-attachments/assets/e17097bb-cc8d-4fbb-acde-66becdd92836)

## PowerBI
![Capstone Project PowerBI SalesData](https://github.com/user-attachments/assets/1c9e2f92-bfc5-497f-8e05-9afea2974b89)

## Conclusion
The analysis of the sales dataset provided valuable insights into product performance, regional sales distribution, and customer purchasing behavior. 







