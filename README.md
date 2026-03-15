# E-commerce Funnel Drop-off Analysis

An end-to-end analytics project analyzing customer progression through an e-commerce purchase funnel using Python, SQL, SQLite, and Tableau to identify the highest drop-off stages and uncover conversion differences across device type, traffic source, and region.

## Overview

An e-commerce business wants to understand where customers abandon the purchase journey and which customer segments convert more effectively. This project evaluates user movement through a four-step funnel — Product View, Add to Cart, Checkout Start, and Purchase — and provides insight into where conversion breaks down.

Note: the dataset used in this project is synthetically generated to simulate a realistic e-commerce customer journey while avoiding privacy concerns.

## Business Question

At which step of the e-commerce funnel are users dropping off the most, and how does funnel conversion vary across device type, traffic source, and region?

## Funnel Stages

- **Product View**
- **Add to Cart**
- **Checkout Start**
- **Purchase**

## Tools Used

- **Python** for synthetic event-level data generation and analysis scripting
- **SQLite** for structured event storage
- **SQL** for funnel stage aggregation and segment-level conversion analysis
- **CSV** for dashboard-ready metric exports
- **Tableau** for funnel and segment performance visualization

## Skills Demonstrated

- Funnel conversion analysis
- Customer journey analytics
- Drop-off analysis
- Segment-level performance evaluation
- SQL-based event aggregation
- Python analytics scripting
- Tableau dashboard storytelling
- Business recommendation framing for conversion optimization

## Dataset

The event-level dataset includes the following fields:

- `user_id`
- `session_id`
- `event_time`
- `event_type`
- `device_type`
- `traffic_source`
- `region`
- `product_category`
- `order_value`

Event types used in the analysis:

- `product_view`
- `add_to_cart`
- `checkout_start`
- `purchase`

## Overall Funnel Results

| Funnel Stage | Users |
|-------------|------:|
| Product Views | 5000 |
| Add to Carts | 1773 |
| Checkout Starts | 1061 |
| Purchases | 500 |

### Step Conversion Rates

- **Product View → Add to Cart:** 35.46%
- **Add to Cart → Checkout Start:** 59.84%
- **Checkout Start → Purchase:** 47.13%
- **Overall Product View → Purchase:** 10.00%

## Segment Highlights

### Device Performance

- **Best:** Desktop — 10.97% overall purchase rate
- **Worst:** Mobile — 9.28% overall purchase rate

### Traffic Source Performance

- **Best:** Email — 12.17% overall purchase rate
- **Strong:** Direct — 12.04%
- **Weakest:** Social — 6.40%
- **Also weak:** Paid Search — 7.98%

### Regional Performance

- **Best:** South — 10.94% overall purchase rate
- **Worst:** Central — 8.36%

## Key Findings

- The funnel loses the largest share of users between **Product View and Add to Cart**, which is expected at the top of the journey.
- The most actionable downstream friction appears between **Checkout Start and Purchase**, where only 47.13% of checkout starters complete a purchase.
- **Desktop users** convert better than **Mobile users**, suggesting weaker downstream conversion on smaller devices.
- **Email**, **Direct**, and **Organic Search** produce stronger overall purchase conversion than **Social** and **Paid Search**, indicating meaningful differences in traffic quality or landing-page intent.
- **Central region** underperforms relative to the rest of the business and may require deeper investigation.

## Business Recommendation

Based on the funnel and segment analysis, the business should prioritize:

1. improving late-stage checkout completion, especially before purchase
2. investigating mobile checkout usability and friction points
3. reviewing lower-converting acquisition channels such as Social and Paid Search
4. monitoring weaker regional performance, especially in the Central region

## Project Files

- `data/ecommerce_user_events.csv` — event-level customer funnel dataset
- `data/funnel_summary_metrics.csv` — overall funnel summary metrics
- `data/segment_funnel_metrics.csv` — segment-level funnel performance metrics
- `sql/funnel_conversion_analysis.sql` — overall funnel stage conversion query
- `sql/segment_funnel_analysis.sql` — segment-level funnel conversion query
- `analysis/funnel_analysis.py` — Python summary script for overall funnel results
- `analysis/segment_analysis.py` — Python segment comparison script
- `analysis/export_metrics.py` — CSV export script for Tableau-ready metrics
- `generate_funnel_data.py` — synthetic event data generation script
- `load_to_sqlite.py` — SQLite loading script
- `dashboard/ecommerce_funnel_dashboard.twbx` — Tableau dashboard workbook
- `images/dashboard_preview.png` — dashboard preview image

## Dashboard Preview

![Dashboard Preview](images/dashboard_preview.png)

## How to Run This Project

1. Run `generate_funnel_data.py` to generate the synthetic event-level dataset.
2. Run `load_to_sqlite.py` to load the dataset into SQLite.
3. Run the SQL files in the `sql/` folder to calculate funnel conversion and segment performance metrics.
4. Run the analysis scripts in the `analysis/` folder to generate summary interpretations.
5. Open `dashboard/ecommerce_funnel_dashboard.twbx` in Tableau Desktop to explore the dashboard.

## Business Impact

This project demonstrates how event-level funnel analysis can identify where customers drop off in the purchase journey and how conversion varies across key customer segments. It shows how analytics can support conversion optimization, mobile experience improvements, and more effective acquisition channel decisions.
