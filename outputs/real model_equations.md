# Model Equations

## Part 3 – Regression-Based Business Insights

**Student:** Satya Sampelli
**Student ID:** 211817

---

# Simple Regression Equations

## Model 1 – Footfall

### Regression Equation

```
monthly_sales = 446,410.58 + (35.68 × footfall)
```

### Coefficient Interpretation

* **Intercept (446,410.58):** Estimated monthly sales when footfall is zero. While this situation is not realistic for a retail store, the intercept serves as the starting point for the regression equation.
* **Footfall (35.68):** Every additional customer visiting the store is associated with an increase of approximately **₹35.68** in monthly sales. This variable is highly statistically significant (p = 4.75E-94).

### Example

If a store receives **6,500 visitors** in a month:

Predicted Sales = 446,410.58 + (35.68 × 6,500)

Predicted Monthly Sales ≈ **₹678,331**

---

## Model 2 – Marketing Spend

### Regression Equation

```
monthly_sales = 560,777.35 + (2.13 × marketing_spend)
```

### Coefficient Interpretation

* **Intercept (560,777.35):** Estimated monthly sales when marketing spend is zero.
* **Marketing Spend (2.13):** Every additional **₹1** spent on marketing is associated with approximately **₹2.13** higher monthly sales. The relationship is statistically significant (p = 2.48E-14).

### Example

If marketing spend is **₹55,000**:

Predicted Sales = 560,777.35 + (2.13 × 55,000)

Predicted Monthly Sales ≈ **₹677,927**

---

# Multiple Regression Equation

```
monthly_sales =
396,155.77
+ (1.11 × marketing_spend)
+ (29.33 × footfall)
− (91,088.72 × avg_discount_pct)
+ (2,270.72 × staff_count)
+ (13,958.30 × type_Mall)
```

---

# Coefficient Interpretation

| Variable         | Coefficient |  P-value | Business Interpretation                                                                                                                             |
| ---------------- | ----------: | -------: | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Intercept        |  396,155.77 | 1.11E-99 | Estimated baseline monthly sales for the reference store type when all other variables are zero.                                                    |
| marketing_spend  |       +1.11 | 2.55E-14 | Each additional ₹1 spent on marketing is associated with approximately ₹1.11 higher monthly sales, after accounting for the other variables.        |
| footfall         |      +29.33 | 2.47E-23 | Each additional customer is associated with approximately ₹29.33 higher monthly sales, holding the other variables constant.                        |
| avg_discount_pct |  -91,088.72 |   0.0218 | Higher average discount percentages are associated with lower monthly sales after accounting for the other predictors.                              |
| staff_count      |   +2,270.72 |   0.0993 | Additional staff members are associated with slightly higher monthly sales, but this relationship is not statistically significant at the 5% level. |
| type_Mall        |  +13,958.30 |   0.0274 | Mall stores are associated with approximately ₹13,958 higher monthly sales than the reference category, after controlling for the other variables.  |

---

# Dummy Variable Approach

The variable **store_type** is categorical and therefore cannot be used directly in a regression model. It was converted into a dummy variable.

### Dummy Variable Used

* **type_Mall = 1** → Mall store
* **type_Mall = 0** → All other store types

### Reference Category

The reference category consists of **non-Mall stores**.

Using a reference category avoids the dummy variable trap (perfect multicollinearity), allowing the regression model to estimate the effect of Mall stores relative to other store types.

The positive coefficient of **13,958.30** indicates that Mall stores are associated with higher monthly sales than non-Mall stores, after controlling for the other variables in the model.

---

# Final Model Selected

**Selected Model:** Multiple Regression

### Variables Included

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* type_Mall

### Why This Model Was Selected

The multiple regression model was selected because it has the highest explanatory power among all models.

* **R-squared:** 0.7903
* **Adjusted R-squared:** 0.7869

This means the model explains approximately **79%** of the variation in monthly sales.

Compared with the simple regression models, it provides a more complete understanding of how several business factors are associated with sales at the same time.

The results indicate that **footfall** and **marketing spend** are positively associated with monthly sales, while **higher average discount percentages** are associated with lower monthly sales. **Mall stores** also tend to perform better than the reference category, whereas **staff count** was not statistically significant and should therefore be interpreted with caution.

Overall, the multiple regression model provides the strongest basis for business decision-making because it considers several important factors together rather than analysing each variable individually.
