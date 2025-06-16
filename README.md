# Olist Store – Seller & Customer Behavior Analysis
Data Operations and Growth Area

Olist_Store_Final_Project_16.06.2025
## Goal

The goal of this project is to analyze sellers and customers on the Olist platform to support strategic decisions that can improve customer satisfaction, seller retention, and platform growth.

### Key Questions:
- Who are the existing sellers and customers?
- Which sellers are valuable and how can we improve retention?
- What product categories drive the most engagement?
- How does geography affect seller performance and customer behavior?
- What are the trends over time in activity, growth, and loss?

---
## Available Data

### Sellers
| Feature                  | Description                                      |
|--------------------------|--------------------------------------------------|
| `seller_id`              | Unique seller identifier                         |
| `seller_state`           | Seller's region/state                            |
| `main_product_category`  | Top-selling product category per seller          |
| `year_month`             | Monthly timestamp for trend analysis             |
| `new_sellers`            | Number of new sellers                            |
| `retained_sellers`       | Sellers active this and last month               |
| `lost_sellers`           | Sellers inactive this month                      |
| `reactivated_sellers`    | Sellers returning after inactivity               |
| `retention_rate`         | Seller retention rate (%)                        |

### Customers
| Feature                  | Description                                      |
|--------------------------|--------------------------------------------------|
| `customer_id`            | Unique customer ID                               |
| `customer_state`         | Region/state of customer                         |
| `review_score`           | Review rating for completed order (1–5)          |
| `order_id`               | Unique order ID                                  |
| `order_purchase_timestamp` | Timestamp of order                            |
| `avg_unique_customers_per_seller` | Buyer reach metric                     |

### Products
| Feature                  | Description                                      |
|--------------------------|--------------------------------------------------|
| `product_id`             | Unique product identifier                        |
| `product_category_name`  | Product category                                 |
| `price`                  | Product price                                    |
| `freight_value`          | Shipping cost                                    |

---

## Data Cleaning & Preparation

-  Removed nulls and outliers (e.g., missing product names, canceled orders)
-  Unified inconsistent category names (e.g., translated to English)
-  Converted `order_purchase_timestamp` into `year_month` format
-  Joined all necessary tables (orders, customers, sellers, products)
-  Removed irrelevant fields (e.g., constant columns)

---

## Exploratory Data Analysis (EDA)

### Business Metrics
- Total customers, sellers, orders, products
- Orders over time (`order_id` trend)
- Orders by product category and region

### Seller Retention
- Trends: new, retained, lost, and reactivated sellers
- Retention rate per month
- Breakdown by seller region and main product category

### Customer Behavior
- Order distribution by region
- Review scores by category
- Avg. customers per seller

### Product Category Performance
- Top categories by volume and rating
- Freight vs. price per category
- Seasonal patterns

### Correlation Analysis
- Seller retention vs. customer reach
- Order count vs. review score
- Product category vs. seller activity

---

## Dashboard (Looker Studio)

- **Overview Page**: KPIs, heatmaps, category shares
- **Seller Retention**: Monthly trends, state filters, status analysis
- **Product Insights**: Review breakdown, volumes, preferences
- **Customer Overview**: Locations, scores, frequency
- **Trends Over Time**: Time series for all key metrics

---

## Recommendations & Strategic Insights

-  Focus on high-retention categories and replicate top seller behaviors
-  Target underperforming regions with onboarding support
-  Promote popular categories with high review scores
-  Improve reactivation campaigns for lost sellers
-  Use customer segmentation to enhance product targeting

---

- Dataset: rdcc-sql-v2.olist_store
- Looker Studio Visualization: https://lookerstudio.google.com/s/nfPslEFx4vA
- BigQuery: https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1srdcc-sql-v2!2seurope-southwest1!3s43f221f1-d8c5-4d31-a8ef-55ff030f7573!2e1

