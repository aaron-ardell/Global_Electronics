# Global_Electronics
Analyzing a set of sales data for a fictitious global electronics retailer, including tables containing transactions, products, customers, stores and currency exchange rates.

## Source of Data
Electronics Global Retailer - https://mavenanalytics.io/data-playground

## Objectives
1. First objective is to ingest the data from raw CSV files, conduct some basic data profiling, feature engineering and QA, and build a customer calendar table to track performance by the day, week, month, quarter or year.
2. Second objective is to build a data model by connecting the foreign keys in the Sales table to the primary keys in each dimension table via 1:many relationships.
3. Third objective is to enrich the data model by adding calculated measures to track key business metrics, including total orders, revenue, average order value and delivery time.
4. Fourth and final objective is to design an interactive report that leadership team can use to explore performance by store and over time.

## Contents of Data - Tables

- Customers
  - Keys: CustomerKey, Gender, Name, City, State Code, State, Zip Code, Country, Continent and Birthday.

- Data_Dictionary
  - Keys: Table, Field and Description. 

- Exchange_Rates
  - Keys: Date, Currency and Exchange. 

- Products
  - Keys: ProductKey, Product Name, Brand, Color, Unit Cost USD, Unit Price USD, Subcategory, CategoryKey and Category. 

- Sales
  - Keys: Order Number, Line Item, Order Date, Delivery Date, CustomerKey, StoreKey, ProductKey, Quantity and Currency Code. 

- Stores
  - Keys: StoreKey, Country, State, Square Meters and Open Date.

#### Entity Relationship Diagram

![ERD diagram of six tables and their relationships in .png format. Diagram created using dbdiagram.io.](https://github.com/aaron-ardell/Global_Electronics/blob/main/global_electronics_erd.png)

## Initial Analysis

1. What types of products does the company sell, and where are customers located?

2. Are there any seasonal patterns or trends for order volume or revenue?

3. How long is the average delivery time in days? Has that changed over time?

4. Is there a difference in average order value (AOV) for online vs. in-store sales?
