# E-Commerce Funnel Drop-off Analysis

An end-to-end product analytics project analyzing user behavior across an e-commerce purchase funnel to identify conversion bottlenecks and optimization opportunities.

This project demonstrates how analysts evaluate funnel performance, diagnose drop-off points, and generate data-driven product recommendations using Python, SQL, SQLite, and Tableau.

---

# Business Problem

E-commerce companies typically lose a significant percentage of users between product discovery and purchase completion.

Understanding **where users abandon the purchase journey** is critical for improving conversion rates, customer experience, and revenue.

This project analyzes a simulated e-commerce dataset to identify the largest funnel drop-off points and uncover performance differences across customer segments.

---

# Key Business Question

**Which stages of the e-commerce funnel experience the largest drop-offs, and which user segments contribute most to lost conversions?**

---

## Funnel Overview

| Funnel Stage | Description |
|--------------|-------------|
| Product View | User views a product page |
| Add to Cart | User adds the product to their cart |
| Checkout Start | User begins the checkout process |
| Purchase | User successfully completes the order |


---

# Dataset

The dataset simulates realistic e-commerce user sessions and contains behavioral events across the purchase funnel.

The dataset intentionally uses rounded sample sizes to make funnel behavior easier to interpret while demonstrating the analytical workflow.

Each record includes:

- User ID
- Device type
- Traffic source
- Geographic region
- Funnel stage events

---

## Methodology

This project simulates an e-commerce purchase funnel to demonstrate how product analytics teams analyze conversion performance.

User sessions are generated programmatically and move through the funnel stages:

Product View → Add to Cart → Checkout Start → Purchase.

Each stage has a probability that determines whether a user continues to the next stage. These probabilities allow the dataset to mimic realistic user drop-off patterns in an e-commerce funnel.

The analysis then calculates funnel conversion rates and evaluates performance across key segments such as device type, traffic source, and geographic region.

## Assumptions

The dataset used in this project is synthetically generated for demonstration purposes.

Because the data is simulated:

* The goal is to demonstrate an analytics workflow rather than analyze real production data.
* Behavioral probabilities are used to mimic realistic funnel drop-off patterns.
* The analytical methods shown here are the same methods analysts use on real event data.


# Tools & Technologies

- Python
- SQL (SQLite)
- Pandas
- Data Analysis
- Tableau
- Product Analytics
- Funnel Analysis
---

# Project Workflow

1. Generate synthetic user-session data representing funnel behavior
2. Load the dataset into a relational SQLite database
3. Aggregate funnel stage metrics using SQL queries
4. Calculate conversion rates between funnel stages
5. Analyze conversion performance across customer segments
6. Visualize results using an interactive Tableau dashboard

This workflow mirrors a typical product analytics pipeline used in real organizations.

---

# Funnel Performance Results

| Funnel Stage   | Users  | Conversion Rate |
| -------------- | ------ | --------------- |
| Product View   | 10,000 | —               |
| Add to Cart    | 3,546  | 35.46%          |
| Checkout Start | 1,782  | 50.25%          |
| Purchase       | 1,000  | 56.13%          |

Overall conversion from **Product View → Purchase: 10.0%**

The largest drop-off occurs between **Product View and Add to Cart**, indicating potential friction in product discovery or purchase intent.

---

## Key Insights

The funnel analysis reveals several important behavioral patterns that explain where users drop off in the purchase journey.


- The largest drop-off occurs between **Product View and Add to Cart**, indicating that many users browse products but do not show purchase intent.

- **Mobile users convert at a lower rate than desktop users**, suggesting potential usability or checkout friction on mobile devices.

- **Traffic sources such as Direct and Email demonstrate higher conversion rates**, while Social and Paid Search traffic show lower downstream conversion.

- Regional differences in conversion behavior suggest that **local factors such as shipping cost visibility or payment options may influence purchase completion**.

---

# Segment Performance Insights

### Device Analysis

Mobile users demonstrate lower purchase conversion compared to desktop users, suggesting potential checkout friction or usability challenges on smaller screens.

### Traffic Source Analysis

Users arriving via **Direct and Email channels convert at higher rates**, while **Paid Search and Social traffic show weaker downstream conversion**, indicating differences in purchase intent across acquisition channels.

### Regional Analysis

Conversion differences across geographic regions may indicate variations in shipping costs, localization, product demand, or payment preferences.

---

# Business Recommendations

Based on the funnel analysis:

### Improve Product Page Engagement

* Enhance product descriptions
* Improve product imagery
* Highlight customer reviews and trust signals

### Optimize Mobile Checkout Experience

* Reduce checkout form complexity
* Improve mobile usability
* Enable faster payment options

### Improve Traffic Quality

* Re-evaluate paid acquisition targeting
* Optimize campaigns for high-intent users
* Monitor acquisition channel ROI

### Investigate Regional Friction

* Improve shipping cost transparency
* Optimize localization and payment methods
* Analyze region-specific purchase behavior

---

# Tableau Dashboard

The Tableau dashboard visualizes:

* Funnel stage conversion performance
* Segment-level conversion comparisons
* Identification of major conversion bottlenecks

Dashboard preview:

![Dashboard](images/dashboard_preview.png)

---

# Project Structure

```
ecommerce-funnel-dropoff-analysis
│
├── data
│   └── ecommerce_funnel_data.csv
│
├── sql
│   └── funnel_analysis_queries.sql
│
├── analysis
│   └── funnel_analysis.py
│
├── dashboard
│   └── ecommerce_funnel_dashboard.twbx
│
├── images
│   └── dashboard_preview.png
│
├── generate_funnel_data.py
├── load_to_sqlite.py
└── README.md
```

---

# Skills Demonstrated

Product Analytics
Funnel Analysis
SQL Querying
Segment Analysis
Data Visualization
Business KPI Reporting
Analytics Storytelling

---

# How to Run This Project

Generate dataset

```
python generate_funnel_data.py
```

Load dataset into SQLite

```
python load_to_sqlite.py
```

Run analysis

```
python analysis/funnel_analysis.py
```

Open the Tableau dashboard

```
dashboard/ecommerce_funnel_dashboard.twbx
```

---

# Author

Sankeerthana Mulukutla
