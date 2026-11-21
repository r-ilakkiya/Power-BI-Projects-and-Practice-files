# 📊 Power BI Assignment 1 – Data Transformation & Data Modeling

## 📌 Project Overview

This project focuses on data preparation, transformation, cleaning, aggregation, and data modeling using **Microsoft Power BI** and **Power Query Editor**.

The project uses an E-commerce sales dataset containing order-level, product-level, customer, and sales target information. The main objective is to transform raw datasets into a clean, structured, and business-ready data model for analysis.

This assignment demonstrates the practical application of data analytics concepts such as data cleaning, calculated columns, conditional logic, table merging, grouping, filtering, and relationship management.

## 🎯 Project Objectives

- Import multiple datasets into Power BI.
- Perform data cleaning and transformation using Power Query.
- Correct data types and formatting.
- Create custom and conditional columns.
- Calculate profit margin and profit status.
- Merge related tables using common keys.
- Identify and handle missing and duplicate values.
- Perform sorting and filtering operations.
- Group and aggregate sales data.
- Establish relationships between tables.
- Build a structured and reliable data model.

## 📂 Dataset Description

The assignment uses three datasets related to E-commerce sales.

### 1. List of Orders

Contains customer and order-level information.

| Column Name | Description |
|---|---|
| Order ID | Unique identifier for an order |
| Order Date | Date when the order was placed |
| Customer Name | Name of the customer |
| City | Customer's city |
| State | Customer's state |
| Category | Product category |
| Amount | Total order amount |
| Profit | Profit generated from the order |

### 2. Order Details

Contains product and sales-related information.

| Column Name | Description |
|---|---|
| Order ID | Identifier used to connect order records |
| Category | Product category |
| Sub-Category | Product sub-category |
| Quantity | Number of products ordered |
| Amount | Sales amount |
| Profit | Profit earned |

### 3. Sales Target

Contains monthly sales target information.

| Column Name | Description |
|---|---|
| Category | Product category |
| Month of Order Date | Month associated with the sales target |
| Target | Sales target amount |

## 🛠️ Tools & Technologies

- **Microsoft Power BI** – Data analysis and data modeling
- **Power Query Editor** – Data cleaning and transformation
- **Power BI Data Model** – Relationship management
- **Power Query M Language** – Custom column calculations and transformation logic

## 🔄 Data Transformation Workflow

### 1. Data Import

- Imported the List of Orders dataset into Power BI.
- Imported Order Details and Sales Target datasets.
- Opened the datasets in Power Query Editor using the Transform Data option.

### 2. Row Limiting and Data Types

- Restricted the List of Orders table to the first 500 rows.
- Changed the Order Date column to the Date data type.
- Converted Amount and Target columns to Fixed Decimal Number.
- Verified the data types of the remaining columns.

### 3. Text Formatting

- Applied Proper Case formatting to the Customer Name column.
- Standardized customer name capitalization.
- Improved consistency and readability of text data.

### 4. Column Creation

Created new columns to support business analysis.

#### 📍 Location Column

Combined City and State into a single column.

**Formula:**

```powerquery
[City] & ", " & [State]
```

**Example:**

`Chennai, Tamil Nadu`

#### 💰 Profit Margin Column

Calculated the profit margin based on profit and sales amount.

**Formula:**

```powerquery
[Profit] / [Amount]
```

**Calculation:**

Profit Margin = Profit ÷ Amount

The result is formatted as a percentage to make the profit performance easier to understand.

#### 📊 Profit Status Column

Created a conditional column to classify orders based on profit.

**Formula:**

```powerquery
if [Profit] < 0 then "Loss"
else if [Profit] = 0 then "Break-Even"
else "Profit"
```

**Business Logic:**

| Condition | Profit Status |
|---|---|
| Profit < 0 | Loss |
| Profit = 0 | Break-Even |
| Profit > 0 | Profit |

This classification helps identify profitable and non-profitable orders.

## 🔢 Calculated Column Summary

| Column Name | Formula | Purpose |
|---|---|---|
| Location | `[City] & ", " & [State]` | Combines city and state |
| Profit Margin | `[Profit] / [Amount]` | Calculates profit percentage |
| Profit Status | Conditional IF statement | Classifies profit performance |

*Note: These formulas use Power Query M language and are applied through the Custom Column option in Power Query Editor.*

## 🔗 Data Merging and Integration

### Merging Tables

Merged the List of Orders and Order Details tables using the common column **Order ID**.

The merged output table was named **Orders Data**.

This process combines customer, order, and product information into a single dataset for further analysis.

### Benefits of Data Merging

- Combines information from related datasets.
- Improves data accessibility.
- Supports detailed sales analysis.
- Helps prepare data for reporting and modeling.

## 🧹 Data Cleaning and Quality

Performed data quality checks to improve the accuracy and consistency of the datasets.

### Missing Value Handling

- Identified missing values across all tables.
- Reviewed missing records and values.
- Applied suitable strategies such as replacing missing values, removing records, or retaining null values where appropriate.

### Duplicate Data Handling

- Identified duplicate rows.
- Reviewed duplicate records based on business logic.
- Applied suitable handling methods to maintain data consistency.

## 🔍 Sorting and Filtering

### Sorting

- Sorted the Orders Data table by Order Date in descending order.
- Displayed the latest order records first.

### Filtering

- Applied filters to analyze orders from a specific state.
- Used Tamil Nadu as an example for state-level filtering.
- Supported focused analysis of regional sales data.

## 📈 Data Aggregation and Analysis

Performed grouping and aggregation operations to summarize sales information.

### Order Details Aggregation

Created a duplicate of the Order Details table and performed the following calculations:

- Count of Order ID
- Average Profit by Category
- Total Amount by Sub-Category

### Sales Target Aggregation

Created a duplicate of the Sales Target table and calculated:

- Total Target by Month of Order Date

These aggregations help summarize sales performance, profitability, and monthly target information.

## 🏗️ Data Modeling

Established relationships between the datasets to create a structured data model.

### Relationships

| Tables | Relationship Column |
|---|---|
| List of Orders ↔ Order Details | Order ID |
| Order Details ↔ Sales Target | Category |

Used the Manage Relationships option in Power BI to verify that the relationships were active and correctly defined.

### Benefits of Data Modeling

- Connects related datasets.
- Supports consistent data analysis.
- Improves the structure of the data model.
- Enables analysis across orders, categories, and sales targets.

## 📁 Project Files

| File Name | Description |
|---|---|
| `Data Transformation & Data Modeling.pbix` | Power BI project containing data transformations and modeling |
| `PowerBI Assignment1 – Querying Data.pdf` | Assignment instructions, tasks, and evaluation criteria |

## 📚 Key Learning Outcomes

Through this assignment, I gained practical experience in:

- Importing multiple datasets into Power BI.
- Using Power Query Editor for data preparation.
- Cleaning and formatting data.
- Creating custom and conditional columns.
- Applying Power Query M formulas.
- Merging datasets using common keys.
- Handling missing and duplicate values.
- Performing sorting and filtering.
- Grouping and aggregating sales data.
- Establishing relationships between tables.
- Understanding data transformation and data modeling concepts.

## 🚀 Project Workflow

**Raw Data → Data Import → Data Cleaning → Data Transformation → Data Merging → Data Aggregation → Data Modeling → Prepared Dataset**

## 👩‍💻 Project Information

- **Project:** Power BI Assignment 1
- **Domain:** Data Analytics
- **Tool:** Microsoft Power BI
- **Focus Areas:** Data Transformation, Data Cleaning, Data Aggregation, Data Modeling
- **Project Type:** Practical Data Analytics Assignment
