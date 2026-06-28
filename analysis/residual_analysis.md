# Residual Analysis

## Part 3 – Regression-Based Business Insights

**Student:** Satya Sampelli
**Student ID:** 211817

---

# What is a Residual?

A residual measures the difference between the actual monthly sales of a store and the sales predicted by the regression model.

**Residual = Actual Sales − Predicted Sales**

* A **positive residual** means the store performed better than predicted.
* A **negative residual** means the store performed worse than predicted.

Large residuals suggest that factors not included in the regression model may be influencing sales.

---

# Model Used

Residuals were calculated using the final **Multiple Regression Model** with the following variables:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* type_Mall

**Model Statistics**

* R-squared: **0.7903**
* Adjusted R-squared: **0.7869**
* Standard Error: **47,898**
* Observations: **320**

This model explains approximately **79%** of the variation in monthly sales and was selected as the final model because it had the highest explanatory power.

---

# Top 5 Largest Positive Residuals

These stores achieved much higher sales than the model predicted.

| Observation | Actual Sales | Predicted Sales |    Residual |
| ----------: | -----------: | --------------: | ----------: |
|         298 |   763,162.45 |      653,365.13 | +109,797.32 |
|         112 |   713,611.16 |      609,895.21 | +103,715.95 |
|         107 |   795,153.84 |      692,267.43 | +102,886.41 |
|         202 |   787,715.51 |      686,098.65 | +101,616.86 |
|         104 |   625,514.04 |      525,337.77 | +100,176.27 |

### Business Interpretation

These stores generated over **₹100,000 more in monthly sales** than predicted by the regression model. This suggests there are additional factors contributing to their performance that were not included in the analysis.

Possible explanations include:

* Better store management
* Strong customer loyalty
* More effective product assortment
* Better in-store experience
* Local market conditions that favour higher sales

Studying these stores could help identify successful practices that may be applied across other locations.

---

# Top 5 Largest Negative Residuals

These stores performed considerably below the model's predictions.

| Observation | Actual Sales | Predicted Sales |    Residual |
| ----------: | -----------: | --------------: | ----------: |
|          45 |   595,467.60 |      734,312.83 | -138,845.23 |
|          90 |   627,171.90 |      751,657.72 | -124,485.82 |
|          33 |   641,865.03 |      763,867.74 | -122,002.71 |
|          67 |   685,379.08 |      802,735.69 | -117,356.61 |
|           4 |   658,920.30 |      775,164.99 | -116,244.69 |

### Business Interpretation

These stores earned significantly less than expected despite having characteristics that the model associates with higher sales.

Possible reasons include:

* Operational inefficiencies
* Strong local competition
* Inventory or merchandising issues
* Lower customer conversion rates
* External economic conditions not captured in the dataset

These stores may benefit from further business investigation to understand why they are underperforming.

---

# Under-Prediction and Over-Prediction

The model both under-predicts and over-predicts sales for certain stores.

Stores with large positive residuals indicate that some business drivers affecting sales are not included in the model. Likewise, stores with large negative residuals suggest that favourable values for marketing spend, footfall or other predictors do not always guarantee higher sales.

The model's **standard error of approximately ₹47,898** shows that individual store predictions may differ from actual sales by a noticeable amount. Therefore, the model is more appropriate for identifying overall business trends than for making highly accurate predictions for individual stores.

---

# Limitations

Although the model explains nearly **79%** of the variation in monthly sales, several limitations remain.

* The regression identifies **associations**, not cause-and-effect relationships.
* Important business factors such as local competition, store management quality, product assortment and seasonal demand were not included in the dataset.
* Staff count was not statistically significant at the 5% significance level, so its impact should be interpreted cautiously.
* Some prediction errors are expected because every factor influencing sales cannot be measured in a single model.

---

# Conclusion

The residual analysis shows that while the multiple regression model performs well overall, it cannot fully explain the performance of every store. The largest positive residuals highlight stores that exceed expectations, whereas the largest negative residuals identify stores that may require additional business attention. These findings can help leadership identify both best-performing stores and locations that may benefit from operational improvements.
