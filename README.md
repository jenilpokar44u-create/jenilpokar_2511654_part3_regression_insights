# Part 3: Regression-Based Business Insights & Model Interpretation

## Business Problem Summary
I executed a multi-variable regression analysis across our retail network to identify the primary operational and environmental drivers of monthly store sales, giving leadership an empirical framework to optimize marketing spend, inventory levels, and real-estate investments.

## Dataset & Metric Definitions
* **Dependent Variable ($Y$):** `monthly_sales` (Continuous transactional volume).
* **Independent Predictors ($X$):** Continuous operational metrics (`marketing_spend`, `footfall`, `inventory_availability_pct`) and categorical qualifiers (`store_type`).

## Regression & Dummy Variable Approach
To evaluate categorical variables alongside continuous predictors, I transformed the `store_type` variable into dummy indicators. I explicitly selected `High Street` as the omitted reference category to evaluate how Mall, Residential, and Airport store formats perform relative to a standard brick-and-mortar baseline.

## Final Model Insights
Our Multiple Linear Regression framework achieved an $R^2$ value of 0.784, meaning it successfully accounts for 78.4% of all monthly store sales variations. Operational inventory availability and high-transit store formats (Airports and Malls) showed the most commanding influence on corporate revenue.

## Summary of Completed Deliverables
* Regression Workbook: `analysis/regression_workbook.xlsx`
* Residual Evaluation: `analysis/residual_analysis.md`
* Mathematical Formulations: `outputs/model_equations.md`
* Strategic Recommendations: `outputs/final_recommendation.md`
