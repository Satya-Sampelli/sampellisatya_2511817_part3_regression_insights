# Model Comparison

## Part 3 – Regression-Based Business Insights

**Student:** Satya  Sampelli
**Student ID:** 211817

---

# Overview

Three regression models were developed to understand which business factors are most strongly associated with monthly sales across retail stores. Two simple regression models were built using individual predictors, followed by one multiple regression model that combined several business variables.

---

# Model 1 – Simple Regression (Footfall)

| Item | Value |
|------|------|
| Dependent Variable | monthly_sales |
| Independent Variable | footfall |
| R-squared | 0.7363 |
| Adjusted R-squared | 0.7355 |
| Coefficient | 35.68 |
| Intercept | 446,410.58 |
| P-value | 4.75E-94 |

### Regression Equation

monthly_sales = 446,410.58 + (35.68 × footfall)

### Business Interpretation

Footfall is the strongest individual predictor of monthly sales. On average, each additional customer visiting a store is associated with an increase of approximately **₹35.68** in monthly sales. This model explains **73.6%** of the variation in monthly sales.

### Business Usefulness

This model is useful for understanding how customer traffic relates to sales performance. Increasing footfall could have a meaningful impact on revenue.

### Limitation

Only one predictor is considered, so other important business factors are not included.

---

# Model 2 – Simple Regression (Marketing Spend)

| Item | Value |
|------|------|
| Dependent Variable | monthly_sales |
| Independent Variable | marketing_spend |
| R-squared | 0.1672 |
| Adjusted R-squared | 0.1646 |
| Coefficient | 2.13 |
| Intercept | 560,777.35 |
| P-value | 2.48E-14 |

### Regression Equation

monthly_sales = 560,777.35 + (2.13 × marketing_spend)

### Business Interpretation

Marketing spend has a positive relationship with monthly sales. On average, every additional ₹1 spent on marketing is associated with approximately **₹2.13** higher monthly sales. However, marketing spend alone explains only **16.7%** of the variation in sales.

### Business Usefulness

Marketing is statistically significant but is a relatively weak predictor when analysed on its own.

### Limitation

Most of the variation in sales is explained by factors other than marketing spend.

---

# Model 3 – Multiple Regression

| Item | Value |
|------|------|
| Dependent Variable | monthly_sales |
| Independent Variables | marketing_spend, footfall, avg_discount_pct, staff_count, type_Mall |
| Multiple R | 0.8890 |
| R-squared | 0.7903 |
| Adjusted R-squared | 0.7869 |
| Standard Error | 47,898 |
| Observations | 320 |

## Coefficient Summary

| Variable | Coefficient | P-value | Significant at 5%? | Business Interpretation |
|-----------|------------:|---------:|:------------------:|-------------------------|
| Intercept | 396,155.77 | 1.11E-99 | Yes | Baseline predicted monthly sales for the reference store type |
| marketing_spend | 1.11 | 2.55E-14 | Yes | Higher marketing spend is associated with higher monthly sales |
| footfall | 29.33 | 2.47E-23 | Yes | Higher customer footfall is associated with higher monthly sales |
| avg_discount_pct | -91,088.72 | 0.0218 | Yes | Higher discount percentages are associated with lower monthly sales |
| staff_count | 2,270.72 | 0.0993 | No | Positive relationship, but not statistically significant |
| type_Mall | 13,958.30 | 0.0274 | Yes | Mall stores are associated with higher monthly sales than the reference category |

### Business Usefulness

This is the strongest model because it explains approximately **79%** of the variation in monthly sales while considering multiple business drivers simultaneously.

### Limitation

The model shows statistical associations rather than cause-and-effect relationships. Staff count was not statistically significant at the 5% significance level.

---

# Model Comparison Summary

| Model | Independent Variables | R-squared | Adjusted R-squared | Business Value |
|------|------------------------|----------:|-------------------:|----------------|
| Simple Regression – Footfall | footfall | 0.7363 | 0.7355 | High |
| Simple Regression – Marketing Spend | marketing_spend | 0.1672 | 0.1646 | Moderate |
| Multiple Regression | marketing_spend, footfall, avg_discount_pct, staff_count, type_Mall | 0.7903 | 0.7869 | Highest |

**Selected Model:** Multiple Regression

The multiple regression model was selected because it has the highest R-squared value and provides the most comprehensive understanding of the factors associated with monthly sales.

---

# Residual Analysis

## Largest Positive Residuals

| Observation | Actual Sales | Predicted Sales | Residual |
|------------:|-------------:|----------------:|----------:|
| 298 | 763,162.45 | 653,365.13 | +109,797.32 |
| 112 | 713,611.16 | 609,895.21 | +103,715.95 |
| 107 | 795,153.84 | 692,267.43 | +102,886.41 |
| 202 | 787,715.51 | 686,098.65 | +101,616.86 |
| 104 | 625,514.04 | 525,337.77 | +100,176.27 |

These stores performed substantially better than predicted by the model, suggesting that additional factors such as local demand, promotions, customer preferences, or seasonal effects may have contributed to higher sales.

## Largest Negative Residuals

| Observation | Actual Sales | Predicted Sales | Residual |
|------------:|-------------:|----------------:|----------:|
| 45 | 595,467.60 | 734,312.83 | -138,845.23 |
| 90 | 627,171.90 | 751,657.72 | -124,485.82 |
| 33 | 641,865.03 | 763,867.74 | -122,002.71 |
| 67 | 685,379.08 | 802,735.69 | -117,356.61 |
| 4 | 658,920.30 | 775,164.99 | -116,244.69 |

These stores performed below the model's predictions. Possible explanations include operational challenges, local competition, inventory shortages, or other external factors not captured by the regression model.

---

# Conclusion

Among the three models, the multiple regression model provides the most useful business insights. Footfall and marketing spend were positively associated with monthly sales, while higher average discount percentages were associated with lower monthly sales after controlling for the other variables. Mall stores also showed higher expected sales than the reference store type. Although the model explains about **79%** of the variation in monthly sales, the results should be interpreted as statistical associations and not as proof of causation.