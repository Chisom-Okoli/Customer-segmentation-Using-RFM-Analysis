- # Customer-segmentation-Using-RFM-Analysis
RFM-based customer segmentation using excel to identify customer value tiers and drive business-focused insights.

## Overview
This project applies **RFM (Recency, Frequency, Monetary) analysis** to segment customers into **High**, **Medium**, and **Low value groups** using transactional retail data.  
The goal is to help the business understand **customer value distribution** and inform **retention, upsell, and engagement strategies**.

---

## Business Objective
Identify which customers drive the most value by answering:

- Who are the **most valuable customers**?
- How is revenue distributed across customer segments?
- Which customers should be prioritized for **retention** and **growth** initiatives?

---

## Dataset Description
- **Dataset:** Online Retail Transaction Data  
- **Total Records:** 541,909  
- **Unique Customers:** 4,000+  
- **Time Period:** 2010–2011  
- **Granularity:** Transaction-level data

---

### Key Columns Used
| Column | Description |
|------|-------------|
| InvoiceNo | Unique invoice identifier |
| InvoiceDate | Date of transaction |
| CustomerID | Unique customer identifier |
| Quantity | Number of units purchased |
| UnitPrice | Price per unit |
| Revenue | Quantity × UnitPrice (calculated) |

---

## Data Cleaning & Preparation
The following steps were performed before analysis:

- Removed rows with **missing CustomerID**
- Removed transactions with **negative Quantity or UnitPrice**
- Created a **Revenue** column
- Ensured correct data types:
  - InvoiceDate → Date
  - Revenue → Numeric

---

## Analytical Framework
The analysis uses the **RFM framework**, a standard customer segmentation methodology.

### Metrics Defined
- **Recency:** Days since last purchase  
- **Frequency:** Number of invoices per customer  
- **Monetary:** Total revenue generated per customer  

---

## Metric Calculation (Excel)
All metrics were calculated using **Excel Pivot Tables**.

### Recency
- Reference date: Latest transaction date in the dataset  
- Formula: Recency = Reference Date − Last Purchase Date

### Frequency
- Count of `InvoiceNo` per `CustomerID`

### Monetary
- Sum of `Revenue` per `CustomerID`

---

## RFM Scoring Methodology
Each metric was scored on a **1–5 scale using quintiles**:

- **Recency:**  
- Most recent customers → Score 5  
- Least recent → Score 1  

- **Frequency & Monetary:**  
- Highest values → Score 5  
- Lowest values → Score 1  

### Final RFM Score
RFM Score = RecencyScore + FrequencyScore + MonetaryScore


---

## Customer Segmentation Logic
Customers were segmented based on total RFM score:

| RFM Score Range | Segment |
|-----------------|---------|
| 12–15 | High Value |
| 8–11  | Medium Value |
| 3–7   | Low Value |

---

## Visualizations
The following visuals were created to support analysis:

1. **Bar Chart:** Number of customers per segment  
2. **Pie Chart:** Revenue contribution by segment

These visuals highlight **value concentration and engagement patterns**.

---

## Key Insights
- **High-value customers** represent 18% of total customers but generate 62% of total revenue
- **Medium-value customers** represent 35% of customers and contribute 28% of revenue, show strong potential for upselling and growth
- **Low-value customers** represent 47% of customers but only 10% of revenue,have low engagement and require cost-efficient engagement strategies

---

## Business Recommendations
| Segment | Recommendation |
|-------|----------------|
| High Value | Focus on retention, loyalty programs, and personalized offers |
| Medium Value | Targeted promotions and upsell strategies |
| Low Value | Automated engagement or reactivation campaigns |

---
## Business Impact

If implemented, this segmentation strategy could:

- Increase retention among high-value customers
- Improve marketing ROI through targeted campaigns
- Reduce acquisition costs by focusing on profitable segments

## Tools Used
- **Excel** (Pivot Tables, formulas, charts)

  
---
## Visualizations

### Customer Distribution by Segment
![Customers by Segment](![Revenue per Segment](https://raw.githubusercontent.com/Chisom-Okoli/Customer-segmentation-Using-RFM-Analysis/main/Customer%20per%20segment.png)
)

### Revenue Contribution by Segment
![Revenue by Segment](![Customer per Segment](![Customer per Segment](![Revenue per Segment](https://raw.githubusercontent.com/Chisom-Okoli/Customer-segmentation-Using-RFM-Analysis/main/Revenue%20per%20segment.png)


