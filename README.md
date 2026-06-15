# 🛍️ Customer Shopping Behavior Analysis

## 📌 Overview

This project analyzes customer shopping behavior to identify key purchasing patterns, customer segments, product performance, and business insights.
The workflow includes data loading with Python, exploratory data analysis, data cleaning, SQL analysis using relational databases, and dashboard creation in Power BI.

The goal is to transform raw customer shopping data into clear insights that can support business and marketing decisions.

## 📂 Dataset

The dataset contains customer shopping information such as:

* Customer demographics
* Product categories
* Purchase amount
* Review ratings
* Payment methods
* Shipping preferences
* Discounts and promo usage
* Subscription status
* Purchase frequency

The data is used to understand how customers buy, which products perform best, and which factors influence customer behavior.

## 🛠️ Tools Used

* **Python**: Data loading, cleaning, and exploratory data analysis
* **Pandas**: Data manipulation
* **SQL**: Data querying and business analysis
* **PostgreSQL / MySQL / SQL Server**: Database storage and SQL queries
* **Power BI**: Interactive dashboard and data storytelling
* **Jupyter Notebook**: Python analysis environment

## 🔄 Project Steps

### 1. Data Loading

The dataset was loaded into Python using Pandas.

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")
```

### 2. Exploratory Data Analysis

Initial analysis was performed to understand:

* Dataset size
* Column types
* Missing values
* Duplicate values
* Descriptive statistics
* Distribution of numerical and categorical variables

### 3. Data Cleaning

The cleaning process included:

* Handling missing values
* Removing unnecessary columns
* Checking duplicates
* Standardizing column names
* Creating new useful features
* Preparing the data for SQL and Power BI

### 4. SQL Analysis

The cleaned dataset was loaded into a relational database such as PostgreSQL, MySQL, or SQL Server.

SQL queries were used to answer business questions such as:

* Total revenue by product category
* Top customer segments
* Average purchase amount by gender or age group
* Revenue contribution by category
* Most used payment methods
* Customer behavior by subscription status
* Product performance by review rating

Example SQL query:

```sql
SELECT 
    category,
    SUM(purchase_amount) AS total_revenue
FROM customer
GROUP BY category
ORDER BY total_revenue DESC;
```

### 5. Power BI Dashboard

An interactive Power BI dashboard was created to visualize the main insights.

The dashboard includes:

* Total revenue
* Average purchase amount
* Number of customers
* Revenue by category
* Purchase behavior by age group
* Payment method analysis
* Customer segmentation
* Review rating analysis

## 📊 Dashboard

The Power BI dashboard provides a clear view of customer shopping behavior and helps users quickly identify trends and opportunities.

Main dashboard pages:

* Sales Overview
* Customer Segmentation
* Product Category Analysis
* Payment and Shipping Analysis
* Customer Behavior Insights

## ✅ Results

Key insights from the analysis include:

* Identification of the most profitable product categories
* Understanding of customer purchasing patterns
* Analysis of payment and shipping preferences
* Segmentation of customers by age group and behavior
* Detection of trends that can support marketing and sales decisions

These insights can help businesses improve targeting, optimize product strategy, and make better data-driven decisions.

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/customer-shopping-behavior-analysis.git
```

### 2. Install required Python libraries

```bash
pip install pandas matplotlib seaborn sqlalchemy psycopg2-binary
```

### 3. Run the Jupyter Notebook

Open the notebook and run all cells:

```bash
jupyter notebook
```

### 4. Load data into SQL database

Update your database connection details:

```python
from sqlalchemy import create_engine

engine = create_engine("postgresql+psycopg2://username:password@localhost:5432/database_name")

df.to_sql("customer", engine, if_exists="replace", index=False)
```

### 5. Run SQL queries

Use PostgreSQL, MySQL, or SQL Server to execute the SQL analysis queries.

### 6. Open the Power BI dashboard

Open the `.pbix` file in Power BI Desktop and refresh the data connection.

## 🎯 Business Value

This project demonstrates the ability to:

* Clean and analyze real-world customer data
* Write SQL queries for business insights
* Build an interactive Power BI dashboard
* Translate data into actionable recommendations
* Support marketing and sales decision-making

## 👤 Author

Created by Abderrahim EL FAZY
Data Analyst | Power BI | SQL | Python
