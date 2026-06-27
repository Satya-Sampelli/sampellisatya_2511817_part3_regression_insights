# Part 3 — Regression-Based Business Insights & Model Interpretation

**Student:** Satya Sampelli| **ID:** 211817
**Course:** Business Analytics — Bitsom
**Repo:** satya_211817_part3_regression_insights

---

## Business Problem Summary

A retail chain's leadership team wants to understand what factors drive monthly sales performance across their stores. They are considering actions such as increasing marketing spend, improving inventory availability, changing discounting strategy, reallocating staff, and prioritising certain store types or regions.

The task was to use regression analysis to identify which factors are most strongly associated with monthly sales and provide data-backed business recommendations.

---

## Dataset Description

| Detail | Value |
|---|---|
| File | business_regression_data.xlsx |
| Rows | 320 (80 stores × 4 months) |
| Columns | 14 |
| Time Period | January 2025 — April 2025 |
| Missing Values | competitor_distance_km (6), customer_rating (8) — filled with column averages |

---

## Dependent and Independent Variables

**Dependent Variable (Y):** monthly_sales

**Numerical Independent Variables:**
- marketing_spend — monthly marketing budget per store
- footfall — number of customer visits per month
- avg_discount_pct — average discount percentage applied
- staff_count — number of staff members
- inventory_availability_pct — percentage of products in stock
- competitor_distance_km — distance to nearest competitor
- customer_rating — average customer satisfaction rating
- holiday_flag — whether the month included a public holiday

**Categorical Variables (converted to dummies):**
- region — East, North, South, West
- store_type — Residential, High Street, Airport, Mall

**Variables NOT used in regression:**
- store_id — just an identifier
- month — time variable, not a business driver
- monthly_profit — outcome variable, not a predictor of sales

---

## Regression Approach

Three regression models were built:

1. **Simple Regression 1** — monthly_sales predicted by footfall only
2. **Simple Regression 2** — monthly_sales predicted by marketing_spend only
3. **Multiple Regression** — monthly_sales predicted by all numerical variables and dummy variables

All regressions were run using the Data Analysis ToolPak in Microsoft Excel.

---

## Dummy Variable Approach

Two categorical variables were converted to dummy variables:

**Region** (reference category = East):
- region_North, region_South, region_West
- East is the reference — when all three dummies are 0, the store is in East

**Store Type** (reference category = Residential):
- type_HighStreet, type_Airport, type_Mall
- Residential is the reference — when all three dummies are 0, the store is Residential

One category from each variable was left out as the reference to avoid multicollinearity.

---

## Model Comparison Summary

| Model | R-squared | Adj R-squared | Key Finding |
|---|---|---|---|
| Simple — Footfall | 0.7363 | 0.7355 | Footfall alone explains 73.6% of sales |
| Simple — Marketing | 0.1672 | 0.1646 | Marketing alone explains only 16.7% of sales |
| Multiple — All Variables | 0.8352 | 0.8288 | All variables together explain 83.5% of sales |

---

## Final Model Selected

**Multiple Regression** — selected because it has the highest explanatory power (83.5%) and identifies multiple actionable business levers simultaneously, giving leadership the most comprehensive and useful view of what drives sales.

---

## Business Recommendation

The strongest drivers of monthly sales are:

1. **Footfall** — the single most powerful predictor. Every additional monthly visitor adds ₹28.53 in sales. Driving traffic into stores should be the top priority.
2. **Store Type** — Airport stores earn ₹42,281 more per month than Residential stores. Future store expansion should prioritise Airport and Mall locations.
3. **Customer Rating** — each 1-point rating improvement adds ₹14,141 in monthly sales. Invest in service quality and staff training.
4. **Inventory Availability** — each 1% improvement adds ₹3,048 in monthly sales. Improve supply chain reliability.
5. **Discounting** — higher discount rates are associated with lower revenue. Review and reduce excessive promotional discounting.

---

## Assumptions and Limitations

- Regression shows association, not causation — findings should be validated with controlled experiments before major investment decisions
- The model covers only 4 months of data — seasonal variation may not be fully captured
- 16.5% of sales variation remains unexplained — factors like store manager quality, local competition, and product range are not in the dataset
- Missing values for competitor_distance_km and customer_rating were filled with column averages, which may slightly affect model accuracy

---

## Screenshots

| File | What It Shows |
|---|---|
| simple_regression_output.png | Simple regression output — footfall vs monthly_sales |
| multiple_regression_output.png | Multiple regression output with all variables |
| residuals_preview.png | Predicted values and residuals from multiple regression |
| model_comparison_preview.png | Model comparison table in regression_summary.xlsx |
