# 🍕 Pizza Sales Report & Analytics Dashboard

[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)](https://www.tableau.com/)
[![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/excel)
[![Data Analytics](https://img.shields.io/badge/Data_Analytics-0078D4?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNk+M9QDwADhgGAWjR9awAAAABJRU5ErkJggg==&logoColor=white)](https://github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

---

## 📌 Executive Summary

The **Pizza Sales Report & Analytics Dashboard** provides a comprehensive end-to-end data analysis solution for tracking key business metrics, sales performance, customer ordering patterns, and product popularity for a pizza retail chain. 

Built using **Tableau** and **Microsoft Excel**, this interactive dashboard translates **48,620 transaction records** across **21,350 total orders** into actionable business insights to drive menu optimization, pricing strategies, inventory management, and operational efficiency.

---

## 📊 Key Performance Indicators (KPIs)

| Metric | Value | Description |
| :--- | :---: | :--- |
| 💰 **Total Revenue** | **$817,860.05** | Sum of total sales across all orders |
| 📦 **Total Orders** | **21,350** | Total count of distinct orders placed |
| 🍕 **Total Pizzas Sold** | **49,574** | Cumulative count of individual pizzas sold |
| 💵 **Average Order Value (AOV)** | **$38.31** | Average revenue generated per order |
| 📈 **Average Pizzas per Order** | **2.32** | Average number of pizzas per customer transaction |

---

## 🖼️ Dashboard Architecture & Features

The Tableau workbook (`pizza sales report.twb`) comprises **two primary interactive dashboards**:

### 1. 🏠 Executive Overview Dashboard (`Home`)
- **Hourly Sales Trend**: Visualizes peak sales hours to optimize kitchen staffing and delivery readiness.
- **Weekly Sales Trend**: Identifies highest-volume days (e.g., Fridays and Saturdays) for targeted marketing and inventory planning.
- **Sales Breakdown by Pizza Category**: Analyzes revenue share across `Classic`, `Supreme`, `Chicken`, and `Veggie`.
- **Sales Breakdown by Pizza Size**: Evaluates customer size preferences (`S`, `M`, `L`, `XL`, `XXL`).
- **Total Orders & Pizzas Sold by Category**: Cross-evaluates sales volume against order frequency per category.

### 2. 🏆 Best & Worst Sellers Dashboard (`Best / Worst Sellers`)
- **Top 5 Pizzas by Revenue**: Highlights revenue drivers (**The Thai Chicken Pizza**, **The Barbecue Chicken Pizza**).
- **Bottom 5 Pizzas by Revenue**: Pinpoints low-yield pizzas (**The Brie Carre Pizza**, **The Green Garden Pizza**).
- **Top 5 Pizzas by Quantity**: Tracks highest unit volume (**The Classic Deluxe Pizza**, **The Barbecue Chicken Pizza**).
- **Bottom 5 Pizzas by Quantity**: Identifies slow-moving products (**The Brie Carre Pizza**, **The Mediterranean Pizza**).
- **Top 5 & Bottom 5 Pizzas by Total Orders**: Measures customer frequency and repeat demand.

---

## 📈 Deep-Dive Analytics & Key Findings

### 🍕 Category Performance

| Category | Revenue | % Revenue | Units Sold | Revenue Rank |
| :--- | :---: | :---: | :---: | :---: |
| **Classic** | $220,088.10 | **26.91%** | 14,888 | 🥇 #1 |
| **Supreme** | $208,197.00 | **25.46%** | 11,987 | 🥈 #2 |
| **Chicken** | $195,919.50 | **23.96%** | 11,050 | 🥉 #3 |
| **Veggie** | $193,655.45 | **23.68%** | 11,649 | #4 |

* **Insight**: Sales are cleanly distributed across categories, with **Classic** leading both revenue and volume. **Chicken** pizzas generate higher average revenue per unit despite lower total volume.

---

### 📐 Size Performance

| Size | Code | Revenue | % Revenue | Units Sold |
| :--- | :---: | :---: | :---: | :---: |
| **Large** | `L` | $375,318.70 | **45.89%** | 18,956 |
| **Medium** | `M` | $249,382.25 | **30.49%** | 15,635 |
| **Small** | `S` | $178,076.50 | **21.77%** | 14,403 |
| **X-Large** | `XL` | $14,076.00 | **1.72%** | 552 |
| **XX-Large** | `XXL` | $1,006.60 | **0.12%** | 28 |

* **Insight**: **Large (L)** and **Medium (M)** sizes account for **76.38% of total revenue** and **69.77% of volume**, signaling strong customer preference for shared/family portions.

---

### 🥇 Top 5 vs. 🛑 Bottom 5 Performers

#### By Revenue 💰
* **Top 5**:
  1. 🥇 **The Thai Chicken Pizza** — `$43,434.25`
  2. 🥈 **The Barbecue Chicken Pizza** — `$42,768.00`
  3. 🥉 **The California Chicken Pizza** — `$41,409.50`
  4. 🏅 **The Classic Deluxe Pizza** — `$38,180.50`
  5. 🏅 **The Spicy Italian Pizza** — `$34,831.25`
* **Bottom 5**:
  1. 🔴 **The Brie Carre Pizza** — `$11,588.50`
  2. 🟠 **The Green Garden Pizza** — `$13,955.75`
  3. 🟡 **The Spinach Supreme Pizza** — `$15,277.75`
  4. 🟢 **The Mediterranean Pizza** — `$15,360.50`
  5. 🔵 **The Spinach Pesto Pizza** — `$15,596.00`

#### By Order Volume 📦
* **Top 5**:
  1. **The Classic Deluxe Pizza** — `2,329 orders` (`2,453 units`)
  2. **The Hawaiian Pizza** — `2,280 orders` (`2,422 units`)
  3. **The Pepperoni Pizza** — `2,278 orders` (`2,418 units`)
  4. **The Barbecue Chicken Pizza** — `2,273 orders` (`2,432 units`)
  5. **The Thai Chicken Pizza** — `2,225 orders` (`2,371 units`)

---

## 🗂️ Data Dictionary & Schema

The dataset (`pizza_sales_excel_file (1).xlsx`) contains transaction granular records:

| Field Name | Data Type | Description |
| :--- | :--- | :--- |
| `pizza_id` | Integer | Unique identifier for each line item record |
| `order_id` | Integer | Unique identifier for the customer order |
| `pizza_name_id` | String | Abbreviated SKU identifier (e.g., `hawaiian_m`) |
| `quantity` | Integer | Quantity of pizzas ordered in the line item |
| `order_date` | Date | Date when order was placed |
| `order_time` | Datetime | Time when order was placed |
| `unit_price` | Float | Price per individual pizza ($) |
| `total_price` | Float | Extended price (`quantity` × `unit_price`) ($) |
| `pizza_size` | String | Size designation (`S`, `M`, `L`, `XL`, `XXL`) |
| `pizza_category` | String | Classification (`Classic`, `Supreme`, `Veggie`, `Chicken`) |
| `pizza_ingredients` | String | Comma-separated list of ingredients |
| `pizza_name` | String | Full display name of the pizza |

---

## 💡 Strategic Recommendations

1. **Menu Optimization**:
   - Consider revising or removing underperforming offerings like **The Brie Carre Pizza** ($11.5k rev) or re-bundling its ingredients to reduce food waste.
2. **Promotions & Bundling**:
   - Pair top volume sellers (**Classic Deluxe**, **Hawaiian**) with high-margin items or beverages to increase Average Order Value (AOV) beyond **$38.31**.
3. **Inventory & Operational Planning**:
   - Focus ingredient stock heavily on **Large (L)** and **Medium (M)** crusts and boxes, as they represent over 76% of sales revenue.
4. **Staff Optimization**:
   - Align kitchen and delivery staff schedules with peak ordering hours and peak weekdays (Fridays/Saturdays) to lower delivery times and improve customer satisfaction.

---

## 📁 Repository Structure

```gfm
pizza_sales_report_dashboard/
│
├── assets/                                 # Dashboard icons & visual assets
│   ├── asset-management.png
│   ├── choice.png
│   ├── delivery-man.png
│   ├── home (1).png
│   ├── order (1).png
│   ├── order-delivery.png
│   ├── pizza-slice.png
│   ├── profit-growth.png
│   └── shipping-box.png
│
├── pizza sales report.twb                  # Tableau Workbook (Dashboards & Worksheets)
├── pizza_sales_excel_file (1).xlsx         # Primary Data Source (Excel Dataset)
├── Pizza Sales Images-20251018T104615Z...zip# Archive of Dashboard Assets
└── README.md                               # Project Documentation
```

---

## 🚀 Getting Started

### Prerequisites
- [Tableau Desktop](https://www.tableau.com/products/desktop) or [Tableau Public](https://public.tableau.com/) (Version 2020.2 or higher)
- Microsoft Excel or compatible spreadsheet reader

### How to Open & Explore
1. Clone the repository:
   ```bash
   git clone https://github.com/yugi252179/pizza_sales_report_dashboard.git
   ```
2. Open `pizza sales report.twb` in Tableau.
3. If prompted for data source path, locate and connect `pizza_sales_excel_file (1).xlsx`.
4. Navigate between the **`home`** and **`Best / worst sellers`** tabs to interact with dashboards and filters.

---


