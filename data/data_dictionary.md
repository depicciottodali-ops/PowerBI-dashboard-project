# Data Dictionary – Sales Dataset

This document describes all fields in `sales_data.csv`.

---

## File Information

| Property | Value |
|----------|-------|
| File name | `sales_data.csv` |
| Encoding | UTF-8 |
| Delimiter | Comma (`,`) |
| Date format | `YYYY-MM-DD` |
| Currency | USD |

---

## Field Definitions

| Column Name | Data Type | Description | Example |
|-------------|-----------|-------------|---------|
| `Order ID` | Text | Unique identifier for each sales order. Format: `CA-YYYY-NNN` | `CA-2023-001` |
| `Order Date` | Date | Date the order was placed. Format: `YYYY-MM-DD` | `2023-01-05` |
| `Region` | Text | Geographic sales region. Values: `West`, `East`, `South`, `Central` | `West` |
| `Category` | Text | High-level product category. Values: `Technology`, `Furniture`, `Office Supplies` | `Technology` |
| `Product Name` | Text | Name of the individual product sold | `Laptop Pro 15` |
| `Sales` | Decimal | Total revenue generated for the order line (USD) | `1299.99` |
| `Quantity` | Integer | Number of units sold in the order line | `1` |
| `Profit` | Decimal | Net profit earned on the order line (USD). Can be negative for discounted/returned items | `389.99` |
| `Customer Segment` | Text | Type of customer. Values: `Consumer`, `Corporate`, `Home Office` | `Corporate` |

---

## Derived / Calculated Columns (created in Power Query)

| Column Name | Formula | Description |
|-------------|---------|-------------|
| `Profit Margin %` | `Profit / Sales * 100` | Percentage profit margin per order line |
| `Year` | `Year([Order Date])` | Calendar year extracted from Order Date |
| `Month` | `Month([Order Date])` | Month number (1–12) extracted from Order Date |
| `Month Name` | `Format([Order Date], "MMMM")` | Full month name |
| `Quarter` | `"Q" & RoundUp(Month/3, 0)` | Calendar quarter (Q1–Q4) |

---

## Notes

- All monetary values are in **US Dollars (USD)**.
- The dataset covers the full calendar year **2023** (January–December).
- There are **4 regions**, **3 product categories**, and **3 customer segments**.
- Order IDs are unique per row; no aggregation is required at the raw level.
