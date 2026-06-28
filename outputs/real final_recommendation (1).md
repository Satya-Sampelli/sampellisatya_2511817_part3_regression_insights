# Final Recommendation
## Part 3 — Regression-Based Business Insights
**Student:** Satya Sampelli | **ID:** 211817

---

## Business Objective

The objective of this analysis was to identify the factors that influence monthly sales across retail stores and determine which variables management should focus on to improve overall business performance.

Three regression models were developed and compared:

- Simple Regression using Footfall
- Simple Regression using Marketing Spend
- Multiple Regression using five independent variables

Among these, the multiple regression model provided the best overall performance.

---

## Key Findings

### 1. Footfall is the strongest driver of sales

Footfall has the greatest impact on monthly sales.

- **Coefficient:** 29.33
- **P-value:** 2.47E-23

This means that, on average, every additional customer visiting a store is associated with approximately **₹29.33** more in monthly sales, while keeping the other variables constant.

The simple regression model using only footfall achieved an **R-squared of 0.7363**, showing that customer traffic alone explains a large proportion of sales variation.

---

### 2. Marketing spend has a positive impact

Marketing spend also contributes positively to monthly sales.

- **Coefficient:** 1.11
- **P-value:** 2.55E-14

This suggests that every additional **₹1** spent on marketing is associated with approximately **₹1.11** in additional monthly sales after accounting for the other variables.

Although significant, its impact is smaller than that of footfall.

---

### 3. Higher discount percentages reduce revenue

Average discount percentage has a statistically significant negative relationship with monthly sales.

- **Coefficient:** -91,088.72
- **P-value:** 0.0218

The analysis indicates that higher discounts are associated with lower monthly revenue. This suggests that excessive discounting may reduce profitability and should be reviewed carefully.

---

### 4. Mall stores perform better

The variable **type_Mall** has a positive coefficient of **13,958.30** with a significant p-value of **0.0274**.

This indicates that Mall stores earn approximately **₹13,958** more per month than non-Mall stores after controlling for the other variables in the model.

---

### 5. Staff count is not statistically significant

Although staff count has a positive coefficient of **2,270.72**, its p-value is **0.0993**, which is above the 5% significance level.

Therefore, increasing staff numbers alone cannot be confidently linked to higher monthly sales based on this dataset.

---

## Recommended Business Actions

Based on the regression results, the following actions are recommended:

### Increase customer footfall

Since footfall is the strongest predictor of sales, management should invest in activities that attract more customers to stores, such as local marketing campaigns, loyalty programmes, promotional events and partnerships.

---

### Review discount policies

The analysis suggests that higher discounts are associated with lower revenue.

Management should review promotional strategies and ensure that discounts are used selectively rather than routinely.

---

### Continue investing in effective marketing

Marketing has a positive impact on sales and should continue to be used.

However, marketing investments should focus on campaigns that successfully increase store visits rather than simply increasing advertising expenditure.

---

### Prioritise Mall locations

Mall stores performed better than non-Mall stores in this analysis.

When selecting locations for future expansion, management should consider high-footfall Mall locations where possible.

---

### Investigate unusual store performance

The residual analysis identified several stores that performed significantly better or worse than predicted by the regression model.

Stores with large positive residuals may be following successful business practices that can be replicated elsewhere, while stores with large negative residuals should be investigated to identify operational or market-related issues.

---

## Limitations

This regression model explains approximately **79.03%** of the variation in monthly sales, leaving around **21%** unexplained.

Some important business factors were not included in the dataset, such as:

- Local competition
- Store layout
- Product assortment
- Customer satisfaction
- Seasonal effects
- Managerial performance

In addition, regression analysis identifies relationships between variables but does not prove cause-and-effect.

---

## Conclusion

Among the three models developed, the **Multiple Regression Model** provides the best explanation of monthly sales performance with an **R-squared of 0.7903** and an **Adjusted R-squared of 0.7869**.

The analysis shows that **footfall is the strongest driver of sales**, followed by **marketing spend**, while **higher discount percentages are associated with lower revenue**. Mall stores also demonstrate better performance than non-Mall stores, whereas staff count does not have a statistically significant impact.

Overall, these findings provide useful insights that can support business decisions related to marketing strategy, promotional planning and future store expansion.