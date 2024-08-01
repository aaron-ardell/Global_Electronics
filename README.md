# Global_Electronics
Analyzing a set of sales data for a fictitious global electronics retailer, including tables containing transactions, products, customers, stores and currency exchange rates.

## Source of Data
Electronics Global Retailer - https://mavenanalytics.io/data-playground

## Objectives
1. First objective is to ingest the data from raw CSV files, conduct some basic data profiling, feature engineering and QA, and build a customer calendar table to track performance by the day, week, month, quarter or year.
2. Second objective is to build a data model by connecting the foreign keys in the Sales table to the primary keys in each dimension table via 1:many relationships.
3. Third objective is to enrich the data model by adding calculated measures to track key business metrics, including total orders, revenue, average order value and delivery time.
4. Fourth and final objective is to design an interactive report that leadership team can use to explore performance by store and over time.

## Contents of Data - Tables (Data_Dictionary)

| Table | Field | Description | Data Type |
| ----- | ----- | ----------- | -- |
| Sales | Order Number | Unique ID for each order | Integer |
| Sales | Line Item | Identifies individual products purchased as part of an order | Integer |
| Sales | Order Date | Date the order was placed | Datetime |
| Sales | Delivery Date | Date the order was delivered | Datetime |
| Sales | CustomerKey | Unique key identifying which customer placed the order | Integer |
| Sales | StoreKey | Unique key identifying which store processed the order | Integer |
| Sales | ProductKey | Unique key identifying which product was purchased | Integer |
| Sales | Quantity | Number of items purchased | Integer |
| Sales | Currency Code | Currency used to process the order | Category |
| Customers | CustomerKey | Primary key to identify customers | Integer |
| Customers | Gender | Customer gender | Category |
| Customers | Name | Customer full name | Object |
| Customers | City | Customer city | Object |
| Customers | State Code | Customer state (abbreviated) | Object |
| Customers | State | Customer state (full) | Object |
| Customers | Zip Code | Customer zip code | Object |
| Customers | Country | Customer country | Category |
| Customers | Continent | Customer continent | Category |
| Customers | Birthday | Customer date of birth | Datetime |
| Products | ProductKey | Primary key to identify products | Integer |
| Products | Product Name | Product name | Object |
| Products | Brand | Product brand | Object |
| Products | Color | Product color | Object |
| Products | Unit Cost USD | Cost to produce the product in USD | Float |
| Products | Unit Price USD | Product list price in USD | Float |
| Products | SubcategoryKey | Key to identify product subcategories | Object |
| Products | Subcategory | Product subcategory name | Object |
| Products | CategoryKey | Key to identify product categories | Object |
| Products | Category | Product category name | Object |
| Stores | StoreKey | Primary key to identify stores | Integer |
| Stores | Country | Store country | Object |
| Stores | State | Store state | Object |
| Stores | Square Meters | Store footprint in square meters | Float |
| Stores | Open Date | Store open date | Datetime |

#### Entity Relationship Diagram

![ERD diagram of six tables and their relationships in .png format. Diagram created using dbdiagram.io.](https://github.com/aaron-ardell/Global_Electronics/blob/main/global_electronics_erd.png)

## Initial Analysis

1. What types of products does the company sell, and where are customers located?
   - The company sells the following categories of product: Audio, TV and Video, Computers, Cameras and camcorders, Cell phones, Music, Movies, Audio Books, Games, Toys, and Home Appliances.
   - This company's customers are located in the following countries: Australia, Canada, Germany, France, Italy, Netherlands, United Kingdom, and United States.

3. Are there any seasonal patterns or trends for order volume or revenue?

4. How long is the average delivery time in days? Has that changed over time?

5. Is there a difference in average order value (AOV) for online vs. in-store sales?
