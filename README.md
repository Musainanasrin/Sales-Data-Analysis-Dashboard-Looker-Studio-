#  **Sales Data Analysis Dashboard (Looker Studio)**

Live Dashboard
https://lookerstudio.google.com/reporting/9f4b5543-554e-48dd-8e63-0b8b3756071c

**Project Overview**

This project analyzes "e-commerce sales data" to uncover insights related to product performance, customer behavior, and sales trends.

An "interactive dashboard" was built using "Google Looker Studio", enabling stakeholders to explore data dynamically and make informed decisions.

---

**Objectives**

* Identify top-performing products
* Analyze sales trends over time
* Detect declining products
* Understand customer checkout behavior
* Compare weekend vs weekday performance
* Evaluate category-wise performance

---
 **Dataset Used**

* **Dataset Name:** `order_data.csv`
* **Key Fields:**

  * `order_date`
  * `sku_id`, `sku_name`
  * `category`
  * `qty_ordered`
  * `price`, `discount`
  * `customer_id`
  * `is_valid`, `is_gross`, `is_net`

---
 **Tools & Technologies**

*  Google Looker Studio
*  CSV Dataset
*  Data Blending
*  Calculated Fields

---
 **Key Features**

* Interactive filters (SKU, Date range)
* Cross-filtering between charts
* Time-series analysis
* Data blending across datasets
* Clean and user-friendly dashboard design

---

 **Tasks & Visualizations**

---

##  Task 1: Top 5 Products by Sales (2022)

**Objective:** Identify top products in *Mobiles & Tablets* category

**Approach:**

* Filter: category = Mobiles & Tablets, year = 2022, is_valid = 1
* Group by `sku_name`
* Rank by `qty_ordered`

**Insight:**

* Few products dominate sales
* Helps marketing team focus on high-performing products

---

##  Task 2: Sales Trend Analysis

**Objective:** Analyze sales over time

**Approach:**

* Time series using `order_date`
* Metric: `qty_ordered`

**Insight:**

* Sales show spikes → seasonal demand
* Helps in demand forecasting

---

##  Task 3: Customers Without Payment

**Objective:** Identify users who checked out but didn’t pay

**Approach:**

* Filters:

  * `is_gross = 1`
  * `is_valid = 0`
  * `is_net = 0`
* Remove duplicates

**Insight:**

* Potential customers for remarketing campaigns

---

##  Task 4: Weekend vs Weekday Sales

**Objective:** Compare performance in Q4 2022

**Approach:**

* Created `day_type` (Weekend/Weekday)
* Aggregated average `before_discount`

**Insight:**

* Weekend campaigns show different performance
* Useful for marketing optimization

---

##  Task 5: Sales Decrease Analysis (2021 vs 2022)

**Objective:** Find products with highest sales drop

**Approach:**

* Compare 2021 vs 2022
* Calculate:

  * `sales_diff`
  * Percentage change
* Rank lowest performers

**Insight:**

* Identifies declining products
* Helps in inventory and pricing decision

---

##  Task 6: Category/Product Trend Comparison

**Objective:** Compare trends across products/categories

**Approach:**

* Time series grouped by `category` / `sku_id`
* Monthly aggregation

**Insight:**

* Some products peak during specific months
* Helps identify seasonal best-sellers
---

# Key Insights

* Sales show **seasonal patterns**
* Few products dominate revenue
* Some products show **significant decline**
* Weekend campaigns impact performance
* Customer drop-offs identified for retargeting

---

#  Business Impact

* Better **inventory planning**
* Improved **marketing strategies**
* Data-driven **decision making**
* Identification of **growth opportunities**

---

# Conclusion

This project demonstrates how **data visualization and analytics** can transform raw data into actionable business insights.

The interactive dashboard enables stakeholders to explore trends, evaluate performance, and make informed strategic decisions.
---
