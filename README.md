# Retail Customer Segmentation & Cancellation Behaviour Analysis

## Project Overview

An exploratory analysis of customer purchasing and cancellation behaviour for a UK-based online retailer using **Python, Pandas, and Matplotlib**.

The project applies **RFM (Recency, Frequency, Monetary) analysis** to segment customers and examines purchasing patterns, revenue contribution, and cancellation activity across customers, products, countries, and time periods.

## Project Objective

The analysis focuses on:

* Segmenting customers based on **Recency, Frequency, and Monetary (RFM)** characteristics.
* Comparing purchasing patterns and revenue contribution across customer segments.
* Comparing **one-time and repeat customers** based on purchase activity and revenue.
* Identifying products and countries with higher cancellation activity.
* Analyzing purchasing and cancellation trends across months and years.

## Dataset

The project uses the **Online Retail** dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail).

The dataset contains transaction records from **1 December 2010 to 9 December 2011** for a UK-based, registered non-store online retailer. The company mainly sells unique all-occasion gifts, and many of its customers are wholesalers.

Key fields used in the analysis include:

* `InvoiceNo`
* `InvoiceDate`
* `StockCode`
* `Description`
* `Quantity`
* `UnitPrice`
* `CustomerID`
* `Country`

For this analysis, records with missing `CustomerID` values were excluded from customer-level analysis. Transactions with negative quantities were treated as **cancellation records**.


## Tools & Libraries

* **Python**
* **Pandas** — data cleaning, transformation, grouping, and analysis
* **Matplotlib** — data visualization
* **Jupyter Notebook** — analysis and documentation

## Analysis Performed

### 1. Data Cleaning & Preparation

* Removed duplicate records.
* Handled missing customer identifiers.
* Converted date and customer ID fields to appropriate formats.
* Created calculated purchase value using `Quantity × UnitPrice`.
* Separated purchase and cancellation records for analysis.

### 2. Customer Segmentation

Customers were segmented using **RFM analysis**:

* **Recency** — how recently a customer made a purchase.
* **Frequency** — how often a customer purchased.
* **Monetary** — how much purchase revenue a customer generated.

The resulting segments include:

* Champions
* Loyal Customers
* New Customers
* At Risk Customers
* Lost Customers
* Others

### 3. One-Time vs Repeat Customers

The analysis compares one-time and repeat customers based on:

* Customer count
* Purchase revenue
* Cancellation value
* Average purchase revenue
* Monthly purchase activity

### 4. Cancellation Behaviour

Cancellation activity was analyzed across:

* Customers
* Products
* Countries
* Months and years

This helps identify periods and areas where cancellation activity was more concentrated.

## Final Insights

### Customer Segmentation

* **Champions generated £5.77M**, accounting for approximately **65.3% of total purchase revenue (£8.83M)**.
* Loyal Customers generated **£1.45M**, followed by At Risk Customers at **£790.34K** and Lost Customers at **£516.43K**.
* Purchase revenue was strongly concentrated among recently active, frequent, and high-value customers.

### One-Time vs Repeat Customers

* The analysis included **1,496 one-time customers** and **2,839 repeat customers**.
* Repeat customers generated **£8.21M** in purchase revenue compared with **£619.09K** from one-time customers.
* Repeat customers contributed approximately **93.0% of total purchase revenue**, compared with **7.0% from one-time customers**.
* Average purchase revenue was **£2,893.52 per repeat customer**, compared with **£413.83 per one-time customer**.
* One-time customer purchase activity was highest during **October–November 2011**, while repeat-customer purchase activity peaked in **November 2011**.

### Cancellation Behaviour

* Cancellation records had a total transaction value of approximately **-£490.83K**, compared with **£8.83M in purchase revenue**.
* Repeat customers accounted for approximately **-£396.52K** in cancellation value, while one-time customers accounted for approximately **-£91.20K**.
* Based on the customer-group comparison, repeat customers accounted for approximately **80.8%** of the absolute cancellation value, while one-time customers accounted for approximately **18.6%**. The small difference from 100% reflects records included in the overall cancellation total that were not assigned to either customer group.
* Cancellation activity increased toward the end of 2011, with **November 2011** showing the highest cancellation activity.
* Product- and country-level analysis identified areas where frequently occurring cancellation records could be investigated further.

## Overall Conclusion

The analysis shows that purchase revenue was highly concentrated among **high-value and repeat customers**. Champions generated **£5.77M (65.3%)** of the **£8.83M** total purchase revenue, while repeat customers generated **£8.21M (93.0%)**.

Cancellation activity represented approximately **-£490.83K** in transaction value. Repeat customers accounted for the majority of the cancellation value, and cancellation activity increased toward the end of 2011, reaching its highest level in **November 2011**.

The analysis provides areas for further investigation, including **high-value customer behaviour, customer retention, frequently cancelled products, and periods with elevated cancellation activity**.
