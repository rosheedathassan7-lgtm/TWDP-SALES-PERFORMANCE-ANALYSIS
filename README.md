# Sales Performance Dashboard

Using Microsoft Excel, I analysed commercial sales data to uncover insights on revenue, profitability, product lines, regional markets, sales rep performance, and settlement methods. I cleaned the raw dataset, structured PivotTables and PivotCharts, and designed an interactive dashboard with a synchronized City slicer to track overall business health and performance.

---

## Table of Contents
- [Dashboard Preview](#dashboard-preview)
- [Project Overview](#project-overview)
- [Dataset Structure](#dataset-structure)
- [Key Business Metrics](#key-business-metrics)
- [Dashboard Insights & Breakdown](#dashboard-insights--breakdown)
- [Strategic Recommendations](#strategic-recommendations)
- [How to Interact with the Dashboard](#how-to-interact-with-the-dashboard)
- [Repository Structure & Tools](#repository-structure--tools)
- [Author](#author)

---

## Dashboard Preview

![Sales Performance Dashboard](image/Sale%20Performance%20Dashboard.png)

---

## Project Overview

A company needs clarity on what fuels top-line revenue versus bottom-line profit. Without granular tracking, high-volume products can mask margin erosion, emerging regional markets can be overlooked, and sales resources are deployed without data-backed evidence.

This project delivers an interactive analytical dashboard in Excel to evaluate operational performance across multiple dimensions:
- Tracking headline financial metrics (Revenue, Profit, Orders, Volume).
- Measuring category and product-level contributions.
- Analysing regional sales distribution across 7 Nigerian commercial hubs.
- Evaluating monthly run-rates and volume seasonality.
- Assessing customer payment methods to understand liquidity and payment friction.

---

## Dataset Structure

The underlying data model captures single-line order transactions with the following fields:

| Field Name | Description |
| :--- | :--- |
| **Order ID** | Unique transaction identifier |
| **Order Date** | Date order was placed |
| **Ship Date** | Fulfilment/shipping dispatch date |
| **Salesperson** | Rep credited with the sale |
| **City** | Delivery destination / customer city |
| **Product** | Specific SKU sold |
| **Category** | Electronics, Furniture, Accessories, or Uncategorized |
| **Quantity Sold** | Number of units purchased |
| **Unit Price** | Selling price per unit before discounts |
| **Unit Cost** | Landed cost per unit |
| **Discount %** | Percentage concession applied to line items |
| **Gross Sales** | $\text{Quantity} \times \text{Unit Price}$ |
| **Discount Amount** | $\text{Gross Sales} \times \text{Discount \%}$ |
| **Revenue** | Gross Sales less Discount Amount |
| **Total Cost** | $\text{Quantity} \times \text{Unit Cost}$ |
| **Profit** | $\text{Revenue} - \text{Total Cost}$ |
| **Payment Method** | Card, Transfer, or Cash |

---

## Key Business Metrics

- **Overall Net Profit Margin**: $19.93\%$  
  $$\text{Margin} = \frac{₦8,325,900}{₦41,769,900} \approx 19.93\%$$
- **Average Order Value (AOV)**: $₦852,447$  
  $$\text{AOV} = \frac{₦41,769,900}{49\text{ orders}} \approx ₦852,447$$
- **Average Units Per Order**: $12.06\text{ units}$  
  $$\text{Basket Size} = \frac{591\text{ units}}{49\text{ orders}} \approx 12.06\text{ units}$$

---

## Dashboard Insights & Breakdown

### 1. Headline KPIs
- **Total Profit**: **₦8,325,900**
- **Total Revenue**: **₦41,769,900**
- **Total Orders**: **49**
- **Total Qty Sold**: **591 units**

The business closed 49 transactions generating over ₦41.7M in net revenue and ₦8.3M in product profit.

---

### 2. Revenue by Category
- **Electronics**: **₦22,986,550** (55.0% of revenue)
- **Furniture**: **₦9,515,300** (22.8% of revenue)
- **Accessories**: **₦8,603,050** (20.6% of revenue)
- **Unknown / Unassigned**: **₦665,000** (1.6% of revenue)

Electronics drives the majority of total sales receipts, surpassing Furniture and Accessories combined.

---

### 3. Top 5 Products by Revenue
1. **Laptop**: ₦11,722,500
2. **Monitor**: ₦7,314,300
3. **Office Chair**: ₦5,448,500
4. **Desk**: ₦4,066,800
5. **Printer**: ₦3,949,750

Laptops are the standout revenue anchor, generating ₦11.7M, followed by Monitors and Office Chairs.

---

### 4. Revenue by City
- **Lagos**: **₦13,871,450** (33.2%)
- **Abuja**: **₦8,841,150** (21.2%)
- **Ibadan**: **₦4,386,000** (10.5%)
- **Enugu**: **₦4,222,750** (10.1%)
- **Port Harcourt**: **₦3,991,050** (9.6%)
- **Kano**: **₦3,772,300** (9.0%)
- **Kaduna**: **₦2,685,200** (6.4%)

Lagos and Abuja account for **54.4%** of aggregate company revenue. Ibadan and Enugu serve as strong secondary regional centers, each exceeding ₦4.2M.

---

### 5. Monthly Revenue Trajectory
- **January**: ₦6,928,450
- **February**: ₦8,320,000
- **March**: ₦9,695,150
- **April**: ₦6,749,700 *(downturn)*
- **May**: ₦10,076,600 *(period peak)*

Revenue expanded steadily through Q1, experienced a sharp drop in April (₦6.75M), and rebounded to record the strongest period performance in May (₦10.08M).

---

### 6. Revenue by Payment Method
- **Card**: **45%** (Primary settlement channel)
- **Transfer**: **33%**
- **Cash**: **22%**

Electronic payment rails (Card + Direct Bank Transfer) represent **78%** of total transaction value, confirming minimal reliance on physical cash.

---

### 7. Salesperson Performance
1. **Tolu**: ₦5,142,400
2. **Chioma**: ₦4,658,400
3. **Kunle**: ₦4,455,000
4. **Seyi**: ₦4,386,000
5. **Ade**: ₦4,274,050

Sales representation is competitive and well-distributed across the top tier, led by Tolu with over ₦5.1M in revenue.

---

## Strategic Recommendations

1. **Incentivize Accessory Bundling**: Because Electronics accounts for 55% of revenue, attach high-margin Accessories (cables, adapters, peripherals) to every Laptop and Monitor sale to lift blended margins.
2. **Establish Tiered Discount Governance**: Set fixed concession guardrails on high-ticket items like Laptops to prevent discount leakage.
3. **Expand Secondary Territory Distribution**: Invest in dedicated distribution and logistics support for Ibadan and Enugu, reducing concentration vulnerability in Lagos.
4. **Investigate the April Slump**: Audit inventory levels, order lead times, and sales incentives from April to identify causes of the ₦6.75M dip and reinforce the retention drivers that led to May's ₦10.08M recovery.

---

## How to Interact with the Dashboard

1. Clone or download the repository to your local machine.
2. Navigate to the `excel/` folder and open `Sales-Performance_Dashboard.xlsx` in **Microsoft Excel**.
3. Use the interactive **City** slicer on the right pane to filter all KPI cards and charts simultaneously.

---

## Repository Structure & Tools

```text
.
├── README.md
├── Sales_Performance_Report.pdf    # Complete documentation and analytical report
├── excel/
│   └── Sales-Performance_Dashboard.xlsx   # Main Excel workbook with formulas & slicers
└── image/
    └── Sale Performance Dashboard.png     # Full-resolution dashboard capture
```

- **Tools Used**: Microsoft Excel (PivotTables, PivotCharts, Slicers, Data Validation, Dynamic Aggregation Functions).

---

## Author

**Data Analyst**  
- **GitHub**: [@YourUsername](https://github.com)  
- **LinkedIn**: [Profile Link](https://linkedin.com)  
- **Email**: [contact@example.com](mailto:contact@example.com)
