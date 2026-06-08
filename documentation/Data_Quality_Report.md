# Data Quality Report

## Project: E-Commerce Performance Analytics

### Objective

The purpose of this report is to assess the quality, consistency, completeness, and integrity of the dataset before performing advanced analytics and dashboard development.

---

# 1. Data Quality Assessment Summary

| Quality Check         | Status                 |
| --------------------- | ---------------------- |
| Missing Values        | Passed                 |
| Duplicate Records     | Passed                 |
| Referential Integrity | Passed                 |
| Invalid Values        | Passed                 |
| Revenue Validation    | Warning                |
| Inventory Validation  | Requires Investigation |

---

# 2. Missing Value Analysis

## Customers

| Check                  | Result |
| ---------------------- | -----: |
| Null Customer ID       |      0 |
| Null Customer Name     |      0 |
| Null Registration Date |      0 |

### Observation

No missing values were identified in critical customer fields.

---

## Orders

| Check            | Result |
| ---------------- | -----: |
| Null Order ID    |      0 |
| Null Customer ID |      0 |
| Null Order Total |      0 |
| Null Order Date  |      0 |

### Observation

All order records contain complete transactional information.

---

## Products

| Check           | Result |
| --------------- | -----: |
| Null Product ID |      0 |
| Null Category   |      0 |
| Null Price      |      0 |

### Observation

No missing values were identified within the product catalog.

---

# 3. Duplicate Record Analysis

## Orders

Result: No duplicate Order IDs found.

## Customers

Result: No duplicate Customer IDs found.

## Products

Result: No duplicate Product IDs found.

### Observation

Primary key uniqueness is maintained across all major entities.

---

# 4. Referential Integrity Validation

## Relationship Checks

| Validation Check             | Invalid Records |
| ---------------------------- | --------------: |
| Orders without Customers     |               0 |
| Order Items without Orders   |               0 |
| Order Items without Products |               0 |
| Feedback without Orders      |               0 |

### Observation

All foreign key relationships are valid and complete.

### Conclusion

The dataset maintains strong referential integrity across transactional tables.

---

# 5. Invalid Value Validation

## Validation Results

| Validation Check          | Invalid Records |
| ------------------------- | --------------: |
| Negative Revenue          |               0 |
| Negative Product Price    |               0 |
| Negative Quantity         |               0 |
| Invalid Ratings           |               0 |
| Invalid Marketing Metrics |               0 |

### Observation

No invalid numerical values were detected.

### Conclusion

All business-critical metrics contain valid values.

---

# 6. Business Rule Validation

## Revenue Reconciliation Test

### Validation Logic

Expected Formula:

Revenue = Quantity × Unit Price

### Findings

| Metric                            | Value |
| --------------------------------- | ----: |
| Orders Records                    | 5,000 |
| Order Items Records               | 5,000 |
| Orders with Reconciliation Issues | 4,993 |

### Observation

A reconciliation check was performed between the Orders and Order_Items tables.

Findings:

* Each order contains exactly one line item.
* Order Total does not match Quantity × Unit Price for 4,993 orders.
* Differences occur in both positive and negative directions.

### Conclusion

The dataset appears to be synthetically generated and Order_Total is not derived directly from line-item calculations.

For all subsequent analysis:

**Order_Total will be treated as the authoritative revenue metric.**

---

# 7. Inventory Validation

## Inventory Damage Assessment

| Metric                | Value |
| --------------------- | ----: |
| Average Damaged Stock |  1.07 |
| Maximum Damaged Stock |     2 |
| Minimum Damaged Stock |     0 |

---

## Inventory Summary

| Metric            |   Value |
| ----------------- | ------: |
| Stock Received    | 147,526 |
| Damaged Stock     |  80,268 |
| Damage Percentage |  54.41% |

### Observation

The calculated damage percentage appears significantly higher than expected for a real-world inventory management system.

However:

* Individual damaged stock values remain extremely low.
* Average damaged stock per record is approximately 1 unit.
* The high aggregate percentage may result from dataset generation logic.

### Recommendation

Inventory damage calculations should be interpreted cautiously and validated further before making operational recommendations.

---

# 8. Final Assessment

## Data Quality Score

| Category                 | Status    |
| ------------------------ | --------- |
| Completeness             | Excellent |
| Consistency              | Excellent |
| Integrity                | Excellent |
| Validity                 | Excellent |
| Business Rule Compliance | Moderate  |
| Analytical Readiness     | Excellent |

---

# Conclusion

The dataset demonstrates strong overall quality with no missing values, duplicate records, referential integrity issues, or invalid values.

Two notable observations were identified:

1. Revenue values do not reconcile with line-item calculations.
2. Inventory damage percentages appear unusually high.

These findings suggest that portions of the dataset were synthetically generated. Despite these observations, the dataset remains suitable for analytical reporting, KPI development, SQL analysis, and Power BI dashboard creation.