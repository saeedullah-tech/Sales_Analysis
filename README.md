# Diwali Sales Analysis 🪔

Exploratory data analysis of festive-season retail sales, identifying which customer segments drive revenue and what they buy — to support targeted marketing and inventory planning for the next sales cycle.

## Overview

This project analyzes 11,000+ retail transactions from India's Diwali shopping season to answer a core business question: **who is spending, and on what?** Using Python's data science stack, the raw transaction log is cleaned, explored, and segmented across gender, age, location, occupation, and product category to surface actionable purchasing patterns.

## Objective

- Clean and prepare raw transactional data for reliable analysis
- Identify which customer demographics generate the highest revenue
- Determine which states, occupations, and product categories perform best
- Translate the findings into a clear customer profile for targeted marketing

## Dataset

- **Source:** Diwali Sales Data (retail transaction log)
- **Raw size:** 11,251 records × 15 columns
- **Fields:** User ID, customer name, product ID, gender, age group, age, marital status, state, zone, occupation, product category, orders, and order amount

## Tools & Libraries

- **Python** – core analysis
- **Pandas / NumPy** – data cleaning, transformation, aggregation
- **Matplotlib / Seaborn** – data visualization
- **Jupyter Notebook** – development environment

## Data Cleaning

- Removed two irrelevant/empty columns (`Status`, `unnamed1`) that carried no analytical value
- Identified and dropped 12 records with missing `Amount` values, retaining **11,239 clean records (99.9% of the dataset)**
- Converted `Amount` from float to integer for consistent aggregation
- Verified column data types and checked descriptive statistics before analysis to catch outliers early

## Analysis & Key Insights

**1. Gender drives the majority of revenue**
Female customers generated **₹74.3M in sales versus ₹31.9M from male customers** — a **70/30 revenue split** despite a smaller gap in transaction counts, indicating women are placing higher-value orders on average.

![Sales by Gender](https://github.com/saeedullah-tech/Sales_Analysis/blob/b6ea8b3dd5d04486a5696f8b1e909e43cd7deb32/chart_2_1.png)

**2. The core buyer is 26–35 years old**
This age bracket recorded the highest transaction volume and total spend across both genders, making it the primary segment to target in campaign planning.

![Age Group by Gender](images/chart_3.png)
![Total Amount by Age Group](images/chart_4.png)

**3. Revenue is concentrated in a handful of states**
A small group of states — led by Uttar Pradesh, Maharashtra, and Karnataka — accounted for a disproportionate share of both order volume and total revenue, pointing to clear regional priorities for stock allocation.

![Top 10 States by Orders](images/chart_5.png)
![Top 10 States by Amount](images/chart_6.png)

**4. Married customers spend more consistently**
Married shoppers showed stronger purchasing activity than single customers, suggesting household and gifting-driven buying behavior during the festive period.

![Marital Status Distribution](images/chart_7.png)

**5. Occupation shapes purchasing power**
Customers working in IT, Healthcare, and Aviation sectors led in total spend, reflecting higher discretionary income among salaried professional segments.

![Amount by Occupation](images/chart_9.png)

**6. Food, Clothing, and Electronics dominate category sales**
These three categories consistently ranked highest in both order count and revenue, ahead of categories like Auto and Furniture.

![Amount by Product Category](images/chart_11.png)

## Business Recommendation

The data points to a clear primary customer profile: **married women, aged 26–35, based in Maharashtra and Uttar Pradesh, working in IT and healthcare fields, purchasing Food, Clothing, and Electronics products.** Marketing spend and inventory planning for the next Diwali cycle should prioritize this segment, while using the top-performing states and categories to guide regional stock distribution.

## Repository Structure

```
diwali-sales-analysis/
│
├── Diwali_Sales_Analysis.ipynb   # Full analysis notebook
├── Diwali Sales Data.csv         # Raw dataset
├── images/                       # Exported chart visuals
└── README.md
```

## How to Run

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Diwali_Sales_Analysis.ipynb
```

## Author

**Saeed Ullah**
GitHub: [@saeedullah-tech](https://github.com/saeedullah-tech)
