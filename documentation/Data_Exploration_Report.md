# Data Exploration Report

## Project: E-Commerce Performance Analytics

### Objective

The purpose of this exploratory data analysis (EDA) is to understand the structure, quality, and business characteristics of the e-commerce dataset before performing data cleaning, advanced SQL analysis, and Power BI dashboard development.

---

# 1. Dataset Overview

The dataset consists of customer, order, product, inventory, delivery, marketing, and feedback information collected over an 18-month period.

## Table Summary

| Table Name            | Records |
| --------------------- | ------: |
| Customers             |   2,500 |
| Orders                |   5,000 |
| Order Items           |   5,000 |
| Products              |     268 |
| Inventory             |  75,172 |
| Customer Feedback     |   5,000 |
| Delivery Performance  |   5,000 |
| Marketing Performance |   5,400 |

---

# 2. Data Coverage Analysis

## Business Activity Period

| Metric                 | Date        |
| ---------------------- | ----------- |
| First Order            | 16-Mar-2023 |
| Last Order             | 04-Nov-2024 |
| First Feedback         | 16-Mar-2023 |
| Last Feedback          | 04-Nov-2024 |
| First Marketing Record | 17-Mar-2023 |
| Last Marketing Record  | 05-Nov-2024 |

### Key Finding

The dataset covers approximately **18 months of business activity**, providing sufficient historical data for trend analysis, customer behavior analysis, and operational performance evaluation.

---

# 3. Executive KPIs

| KPI                             |          Value |
| ------------------------------- | -------------: |
| Total Customers                 |          2,500 |
| Total Orders                    |          5,000 |
| Total Revenue                   | ₹11,009,308.50 |
| Average Order Value             |      ₹2,201.86 |
| Total Products                  |            268 |
| Total Customer Feedback Records |          5,000 |
| Conversion Rate                 |         10.02% |
| Return on Ad Spend (ROAS)       |           1.97 |

---

# 4. Customer Analysis

## Customer Segmentation

| Segment  | Customers |
| -------- | --------: |
| Regular  |       639 |
| Premium  |       633 |
| New      |       628 |
| Inactive |       600 |

### Key Findings

* Customer segments are evenly distributed.
* No single customer segment dominates the customer base.
* The business has opportunities for targeted retention and loyalty campaigns.

---

## Customer Registration Trend

Customer acquisition remained relatively consistent throughout the available period, indicating stable growth and acquisition efforts.

### Key Findings

* No major decline in customer registrations was observed.
* Customer acquisition appears sustainable across the reporting period.

---

# 5. Sales Analysis

## Revenue Metrics

| Metric              |          Value |
| ------------------- | -------------: |
| Total Revenue       | ₹11.01 Million |
| Total Orders        |          5,000 |
| Average Order Value |      ₹2,201.86 |
| Highest Order Value |      ₹6,721.46 |
| Lowest Order Value  |         ₹13.25 |

### Key Findings

* The business generated over ₹11 million in revenue.
* Customers spend an average of ₹2,201 per order.
* Significant variation exists between low-value and high-value transactions.

---

## Payment Method Distribution

| Payment Method | Orders |
| -------------- | -----: |
| Card           |  1,285 |
| Cash           |  1,257 |
| Wallet         |  1,244 |
| UPI            |  1,214 |

### Key Findings

* Payment methods are well distributed.
* No overdependence on a single payment channel exists.
* Multiple payment options appear to be widely accepted by customers.

---

# 6. Product Analysis

## Product Portfolio

| Category              | Products |
| --------------------- | -------: |
| Dairy & Breakfast     |       30 |
| Fruits & Vegetables   |       27 |
| Snacks & Munchies     |       27 |
| Household Care        |       27 |
| Personal Care         |       25 |
| Pet Care              |       25 |
| Pharmacy              |       25 |
| Grocery & Staples     |       24 |
| Cold Drinks & Juices  |       22 |
| Instant & Frozen Food |       20 |
| Baby Care             |       16 |

### Key Findings

* The business primarily operates within grocery and daily-consumption categories.
* Product assortment is balanced across major categories.

---

## Product Pricing

| Metric        |   Value |
| ------------- | ------: |
| Maximum Price | ₹995.98 |
| Minimum Price |  ₹12.32 |
| Average Price | ₹488.36 |

### Key Findings

* Product pricing supports both budget-conscious and premium customers.
* The catalog provides a diverse pricing strategy.

---

# 7. Delivery Performance Analysis

## Delivery Status Distribution

| Status                | Orders |
| --------------------- | -----: |
| On Time               |  3,470 |
| Slightly Delayed      |  1,037 |
| Significantly Delayed |    493 |

### Delivery Performance Metrics

| Metric                |        Value |
| --------------------- | -----------: |
| On-Time Delivery Rate |        69.4% |
| Delayed Delivery Rate |        30.6% |
| Average Delivery Time | 4.44 Minutes |

### Key Findings

* Nearly 70% of deliveries were completed on time.
* Approximately one-third of deliveries experienced delays.
* Delivery efficiency represents an area for operational improvement.

---

## Delay Analysis

| Delay Reason | Occurrences |
| ------------ | ----------: |
| Traffic      |       3,098 |

### Key Findings

* Traffic congestion is the primary contributor to delivery delays.
* Route optimization and delivery scheduling improvements may reduce delays.

---

# 8. Inventory Analysis

## Inventory Metrics

| Metric                  |   Value |
| ----------------------- | ------: |
| Total Inventory Records |  75,172 |
| Total Stock Received    | 147,526 |
| Total Damaged Stock     |  80,268 |

### Key Findings

* Damaged stock represents a substantial portion of total inventory activity.
* The damaged stock ratio appears unusually high and requires further validation during the data quality assessment phase.

### Potential Concern

Damaged Stock Ratio:

80,268 / 147,526 = 54.4%

This value should be investigated to determine whether duplicate records or aggregation issues exist.

---

# 9. Customer Feedback Analysis

## Rating Distribution

| Rating | Reviews |
| ------ | ------: |
| 5      |     816 |
| 4      |   1,708 |
| 3      |   1,398 |
| 2      |     538 |
| 1      |     540 |

### Estimated Average Rating

3.34 / 5

### Key Findings

* Customer satisfaction is moderate.
* Most customers provide ratings between 3 and 4 stars.

---

## Sentiment Analysis

| Sentiment | Reviews |
| --------- | ------: |
| Neutral   |   1,738 |
| Negative  |   1,642 |
| Positive  |   1,620 |

### Key Findings

* Sentiment distribution is balanced.
* Positive sentiment does not significantly exceed negative sentiment.
* Service improvements may be required to increase customer satisfaction.

---

## Feedback Categories

| Category         | Reviews |
| ---------------- | ------: |
| Delivery         |   1,271 |
| Customer Service |   1,266 |
| Product Quality  |   1,250 |
| App Experience   |   1,213 |

### Key Findings

* Customer concerns are evenly distributed across operational areas.
* Delivery and customer service are the most frequently discussed topics.

---

# 10. Marketing Performance Analysis

## Campaign Performance

Top-performing campaigns by conversions:

1. New User Discount
2. Category Promotion
3. Referral Program

### Marketing KPIs

| Metric          |  Value |
| --------------- | -----: |
| Conversion Rate | 10.02% |
| ROAS            |   1.97 |

### Key Findings

* Marketing campaigns are generating profitable returns.
* Customer acquisition campaigns outperform most other campaign types.
* Additional optimization opportunities exist to improve ROAS beyond the current level.

---

# 11. Overall Business Insights

## Strengths

* Strong revenue generation across 5,000 orders.
* Balanced customer segmentation.
* Diverse payment method adoption.
* Profitable marketing performance.
* Broad product portfolio across essential categories.

## Areas for Improvement

* Delivery delays affect approximately 31% of orders.
* Customer sentiment is not strongly positive.
* Inventory damage levels require investigation.
* Marketing efficiency can be further optimized.

## Recommended Next Steps

1. Perform detailed data quality assessment.
2. Validate inventory damage records.
3. Analyze repeat customer behavior.
4. Identify top-performing products and categories.
5. Evaluate customer lifetime value.
6. Build KPI-focused Power BI dashboards for executive reporting.

---

# Conclusion

The exploratory analysis indicates that the business demonstrates stable customer acquisition, healthy revenue generation, and effective marketing performance. However, opportunities exist to improve delivery operations, customer satisfaction, and inventory management. These findings will guide the next phase of data cleaning, advanced SQL analysis, and dashboard development.