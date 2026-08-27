# Cohort Analysis

## Project Overview

This project analyzes customer purchasing behavior over time using cohort analysis.

Customers are grouped according to the period of their first successful purchase and then tracked across different months and weeks.

The analysis focuses on revenue, ARPU, cohort lifetime, retention, and churn in order to understand how customer behavior changes after the first purchase.

## Business Goal

The main goals of this project are to:

- identify the strongest customer cohorts,
- understand how customer activity changes over time,
- measure customer retention and churn,
- compare revenue and ARPU across cohorts,
- identify opportunities to improve repeat purchases and customer retention.

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset

The analysis is based on an e-commerce sales dataset named `sales.csv`.

The original dataset contains 286,392 rows and 33 columns. Each row represents an order line, meaning that the same `order_id` can appear in multiple rows when an order contains multiple items.

For the analysis, the most relevant columns were:

- `order_id` — unique order identifier
- `order_date` — date of the order
- `status` — order status
- `cust_id` — customer identifier
- `item_id` — product/item identifier
- `qty_ordered` — quantity ordered
- `price` — unit price
- `discount_amount` — discount applied
- `category` — product category
- `payment_method` — payment method

Only successful order statuses were kept for the cohort analysis.

> Note: The raw dataset is not included in this repository because it was provided for educational purposes.

## Analysis Workflow

The project was completed step by step through the following stages:

1. Data overview and initial inspection
2. Column name standardization
3. Missing value and duplicate checks
4. Order status filtering
5. Revenue calculation
6. First order date identification
7. Monthly cohort creation
8. Cohort summary analysis
9. Cohort visualization
10. Customer activity pivot table
11. Monthly revenue and customer metrics
12. ARPU calculation
13. Monthly cohort lifetime calculation
14. ARPU heatmap
15. Weekly cohort creation
16. Weekly cohort lifetime calculation
17. Weekly active customer analysis
18. Initial cohort size calculation
19. Retention and churn analysis
20. Final business interpretation and recommendations

## Key Findings

- The December 2020 cohort was the strongest cohort in terms of customer count, order volume, and total revenue.
- The December 2020 cohort generated approximately 73.36 million in total revenue from 14,020 unique customers and 35,055 unique orders.
- ARPU varied significantly across cohorts and lifetime periods, showing that customer value was not constant over time.
- Weekly retention dropped sharply after the initial purchase week.
- For the cohort starting on 2020-09-28, first-week retention was approximately 5.72%.
- As retention was low, weekly churn was correspondingly high. For the same cohort, first-week churn was approximately 94.28%.
- Some customers returned after inactive periods, which explains why retention can increase slightly in later weeks.
- Newer cohorts contain fewer observed lifetime periods because they have not yet had enough time to reach later weeks.

## Business Recommendations

Based on the cohort analysis, the following actions are recommended:

- Focus on improving the customer experience immediately after the first purchase, because retention drops sharply in the following weeks.
- Use follow-up campaigns, personalized offers, discount coupons, and loyalty programs to encourage repeat purchases.
- Investigate the December 2020 cohort to understand which campaigns, seasonal factors, or customer acquisition channels contributed to its strong performance.
- Analyze high-ARPU customer segments separately to understand which products, categories, and behaviors are associated with higher customer value.
- Monitor retention, churn, and ARPU together instead of evaluating revenue alone.
- Compare cohorts over similar lifetime periods to avoid unfair comparisons between older and newer cohorts.

## Project Conclusion

The analysis shows that although some cohorts generated strong revenue and ARPU, weekly customer retention was generally low and churn was high.

The main business opportunity is not only to acquire new customers, but also to improve repeat purchases and keep existing customers active for longer periods.

## Notebook

The complete analysis, code, visualizations, and detailed results are available in the Jupyter Notebook:

[View the full Cohort Analysis Notebook](cohort_analysis.ipynb)
