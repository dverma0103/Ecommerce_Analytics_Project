# E-Commerce Performance Analytics Dashboard

## Project Overview

This project analyzes e-commerce operations across customers, orders, products, inventory, delivery performance, marketing campaigns, and customer feedback.

The objective is to transform raw transactional data into actionable business insights using SQL and Power BI.

---

# Business Problem

E-commerce businesses generate large volumes of data from multiple operational systems. Decision-makers require consolidated reporting to understand:

* Revenue performance
* Customer behavior
* Product performance
* Delivery efficiency
* Inventory health
* Marketing effectiveness
* Customer satisfaction

This project addresses these challenges through end-to-end data analysis and dashboard development.

---

# Dataset Overview

The dataset contains 8 relational tables:

| Table                 | Records |
| --------------------- | ------: |
| Customers             |   2,500 |
| Orders                |   5,000 |
| Order Items           |   5,000 |
| Products              |     268 |
| Inventory             |  75,172 |
| Delivery Performance  |   5,000 |
| Customer Feedback     |   5,000 |
| Marketing Performance |   5,400 |

### Data Coverage

* Start Date: March 2023
* End Date: November 2024
* Total Coverage: 18 Months

---

# Project Architecture

```text
Customers
    |
Orders
    |
Order_Items
    |
Products

Orders
    |
Delivery_Performance

Products
    |
Inventory

Orders
    |
Customer_Feedback

Marketing_Performance
```

---

# Tools Used

* SQL
* MySQL
* Power BI
* DAX
* GitHub
* Excel

---

# Project Workflow

## Phase 1: Data Exploration

Performed exploratory analysis to understand:

* Dataset size
* Business coverage
* Customer distribution
* Revenue metrics
* Product portfolio
* Marketing performance

---

## Phase 2: Data Quality Assessment

Validated:

* Missing values
* Duplicate records
* Referential integrity
* Invalid values
* Business rules

---

## Phase 3: SQL Analysis

Conducted analysis across:

### Customer Analytics

* Customer Segmentation
* Customer Growth
* Repeat Customers
* Customer Lifetime Value

### Sales Analytics

* Revenue Trends
* Average Order Value
* Payment Method Analysis

### Product Analytics

* Top Products
* Category Performance
* Product Revenue Contribution

### Delivery Analytics

* On-Time Delivery Rate
* Delay Analysis
* Delivery Partner Performance

### Inventory Analytics

* Inventory Health
* Damaged Stock Analysis
* Low Stock Monitoring

### Marketing Analytics

* Campaign Performance
* Conversion Analysis
* Return on Ad Spend (ROAS)

### Customer Feedback Analytics

* Rating Analysis
* Sentiment Analysis
* Feedback Category Analysis

---

# Key Business KPIs

| KPI                   |     Value |
| --------------------- | --------: |
| Total Revenue         |   ₹11.01M |
| Total Orders          |     5,000 |
| Total Customers       |     2,500 |
| Average Order Value   | ₹2,201.86 |
| Conversion Rate       |    10.02% |
| ROAS                  |      1.97 |
| On-Time Delivery Rate |     69.4% |

---

# Key Insights

### Customer Insights

* Customer segments are evenly distributed.
* Customer acquisition remained stable throughout the reporting period.

### Sales Insights

* Revenue exceeded ₹11 million.
* Average order value exceeded ₹2,200.

### Delivery Insights

* 69.4% of deliveries were completed on time.
* Traffic was the primary cause of delays.

### Marketing Insights

* New User Discount campaigns generated the highest conversions.
* Marketing efforts produced a positive ROAS of 1.97.

### Customer Experience Insights

* Average customer satisfaction remained moderate.
* Delivery and customer service generated the largest volume of feedback.

---

# Power BI Dashboard

The dashboard will contain:

## Executive Summary

* Revenue KPIs
* Customer KPIs
* Sales Trends

## Customer Analytics

* Segmentation
* Lifetime Value
* Repeat Purchase Analysis

## Product Analytics

* Product Performance
* Category Analysis
* Inventory Monitoring

## Delivery Analytics

* Delivery Performance
* Delay Analysis

## Marketing Analytics

* Campaign Performance
* ROAS Analysis

## Customer Feedback Analytics

* Ratings
* Sentiment Analysis
* Feedback Categories

---

# Repository Structure

```text
Ecommerce-Analytics/
│
├── data/
├── sql/
│   ├── 01_data_exploration.sql
│   ├── 02_data_quality_assessment.sql
│   ├── 03_data_cleaning.sql
│
├── powerbi/
│
├── documentation/
│   ├── Data_Exploration_Report.md
│   ├── Data_Quality_Report.md
│
├── assets/
│
└── README.md
```

---

# Future Enhancements

* Customer churn prediction
* Demand forecasting
* Product recommendation system
* Delivery delay prediction
* Marketing campaign optimization

---

# Author

Deepak Verma

Data Analytics | SQL | Power BI | Business Intelligence
