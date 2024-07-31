\# Day 2: Data Overview and Initial Integrity Checks

This document provides an overview of the tables available in our dataset and outlines the initial steps taken to ensure data integrity by verifying the number of rows in each table.

\#\# Dataset Overview

Our dataset comprises eight tables, each crucial for understanding various aspects of Target's operations in Brazil. Below is a glimpse of each table along with a brief description:

| SL. No | Table Name     | Description                                          |  
|--------|----------------|------------------------------------------------------|  
| 1      | \`Customers\`    | Contains information about the customers such as IDs, location, etc. |  
| 2      | \`Geolocation\`  | Details geographic coordinates of Brazilian zip codes. |  
| 3      | \`Order\_items\`  | Lists items purchased in each order including pricing and seller information. |  
| 4      | \`Order\_reviews\`| Customer reviews for orders including ratings and textual feedback. |  
| 5      | \`Orders\`       | Records of order transactions, status, and timestamps. |  
| 6      | \`Payments\`     | Payment details associated with each order including type and value. |  
| 7      | \`Products\`     | Information about product specifications like category, dimensions, and weight. |  
| 8      | \`Sellers\`      | Information about the sellers including their location and contact details. |

\#\# Initial Data Checks

To ensure the integrity and completeness of our imported data, we performed basic checks to count the rows in each table. This helps verify that the data loaded into our environment is as expected and complete.

\`\`\`sql  
\-- SQL Queries to check the number of rows in each table  
SELECT 'Customers' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Customers;  
SELECT 'Geolocation' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Geolocation;  
SELECT 'Order\_items' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Order\_items;  
SELECT 'Order\_reviews' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Order\_reviews;  
SELECT 'Orders' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Orders;  
SELECT 'Payments' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Payments;  
SELECT 'Products' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Products;  
SELECT 'Sellers' AS Table\_Name, COUNT(\*) AS Row\_Count FROM Sellers;

\-- SQL Queries to preview the first 10 rows from each table

\-- Customers table  
SELECT \* FROM Customers LIMIT 10;

\-- Geolocation table  
SELECT \* FROM Geolocation LIMIT 10;

\-- Order\_items table  
SELECT \* FROM Order\_items LIMIT 10;

\-- Order\_reviews table  
SELECT \* FROM Order\_reviews LIMIT 10;

\-- Orders table  
SELECT \* FROM Orders LIMIT 10;

\-- Payments table  
SELECT \* FROM Payments LIMIT 10;

\-- Products table  
SELECT \* FROM Products LIMIT 10;

\-- Sellers table  
SELECT \* FROM Sellers LIMIT 10;

