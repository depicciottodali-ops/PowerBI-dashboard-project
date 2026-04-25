# Power BI Dashboard Project

An interactive Power BI dashboard created to analyze key business data and turn it into clear, actionable insights.

---

## Project Objective

The goal of this project was to:

- Explore a business dataset to understand its structure and contents
- Identify important trends and performance patterns
- Present the results through a clear and user-friendly interactive dashboard

---

## Tools Used

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard design, data modeling, and interactive visualization |
| **Excel / CSV** | Raw data storage and initial inspection |
| **Data Cleaning** | Removing duplicates, handling nulls, standardizing formats |
| **Data Visualization** | Charts, KPI cards, slicers, and trend lines |
| **Dashboard Design** | Layout, color scheme, and user experience |

---

## Repository Structure

```
PowerBI-dashboard-project/
├── data/
│   ├── sales_data.csv          # Raw sales dataset
│   └── data_dictionary.md      # Field descriptions and data types
├── dashboard/
│   └── PowerBI_Dashboard.pbix  # Power BI Desktop file (add your .pbix here)
├── screenshots/
│   └── (add dashboard screenshots here)
└── README.md
```

---

## Dataset Overview

The sample dataset (`data/sales_data.csv`) contains transactional sales records with the following key fields:

- **Order ID** – Unique identifier for each order
- **Order Date** – Date the order was placed
- **Region** – Geographic sales region
- **Category** – Product category
- **Product Name** – Name of the product sold
- **Sales** – Revenue generated (USD)
- **Quantity** – Number of units sold
- **Profit** – Profit earned (USD)
- **Customer Segment** – Customer type (Consumer, Corporate, Home Office)

See [`data/data_dictionary.md`](data/data_dictionary.md) for full field definitions.

---

## Dashboard Features

The Power BI dashboard includes the following pages / visuals:

1. **Executive Summary** – High-level KPIs: Total Sales, Total Profit, Order Count, Profit Margin
2. **Sales by Region** – Map and bar chart showing regional performance
3. **Category Analysis** – Sales and profit breakdown by product category
4. **Trends Over Time** – Monthly and quarterly revenue trend lines
5. **Customer Segments** – Sales distribution across customer segments
6. **Top Products** – Ranked list of best-performing products

Interactive slicers allow filtering by **date range**, **region**, **category**, and **customer segment**.

---

## Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free download)

### Steps

1. Clone this repository:
   ```bash
   git clone https://github.com/depicciottodali-ops/PowerBI-dashboard-project.git
   ```
2. Open `dashboard/PowerBI_Dashboard.pbix` in Power BI Desktop.
3. If prompted, update the data source path to point to `data/sales_data.csv`.
4. Refresh the data and explore the dashboard.

---

## Data Cleaning Steps

The following transformations were applied in Power Query before building the dashboard:

- Removed duplicate rows based on **Order ID**
- Filled or removed rows with null values in critical columns (Sales, Profit, Order Date)
- Standardized date formats to `YYYY-MM-DD`
- Trimmed whitespace from text columns (Region, Category, Product Name)
- Created calculated columns: **Profit Margin %**, **Year**, **Month**, **Quarter**

---

## Key Insights

> *(Update this section with findings from your specific dataset)*

- The **West** region consistently generates the highest sales revenue.
- **Technology** is the most profitable product category.
- Sales peak in **Q4**, driven by seasonal demand.
- **Corporate** customers contribute the largest share of total revenue.

---

## License

This project is for educational and portfolio purposes.
