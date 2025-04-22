This project explores the **impact of TV, Radio, and Newspaper advertising on product sales** using multiple linear regression and model diagnostics in R.

## Objective

Evaluate how advertising spending across different media channels influences sales and develop a predictive model that maximizes explanatory power while satisfying regression assumptions.

---

## 📊 Study Summary

- **Dataset**: `advertising.csv`
- **Predictors**: TV, Radio, Newspaper advertising budgets
- **Response Variable**: Product Sales (in thousands of units)
- **Sample Size**: 200 observations
- **Goal**: Identify which advertising channels drive sales most effectively

---

## 🔍 Methods

- Descriptive statistics & histograms
- Scatterplot matrix for correlation and linearity check
- Multiple Linear Regression:  
  `Sales ~ TV + Radio + Newspaper`
- Transformation via **Box-Cox** method
- Variable selection using **Forward AIC**
- Final reduced model:  
  `sqrt(Sales) ~ sqrt(TV) + Radio^0.72`
- Diagnostic plots: residuals, Q-Q, leverage
- Variance Inflation Factor (VIF) analysis

---

## 📈 Key Findings

- **TV** and **Radio** were statistically significant predictors  
  (p-value < 2e-16)
- **Newspaper** was **not significant**
- **Final model R²**: 0.9264 (Adjusted R²: 0.9257)
- Residual diagnostics validated model assumptions
- No multicollinearity detected (all VIFs ≈ 1)
- Forward selection confirmed that TV and Radio were optimal predictors

---

## 🧪 Tools Used

- **R**: `base`, `car`, `graphics`, `stats`
- Key functions: `lm()`, `powerTransform()`, `vif()`, `plot()`, `step()`

---

## 📄 Files Included

- `advertising.csv`: Dataset
- `AdSales_Model.pdf`: Full technical report and output
- `README.md`: Project summary

