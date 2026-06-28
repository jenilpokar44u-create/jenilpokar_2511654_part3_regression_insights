# Residual Analysis Notes

## 1. Residual Methodology
I calculated the predicted sales for every record in the dataset using the final multiple linear regression model coefficients. The residuals were calculated using the standard formula:
$$\text{Residual} = \text{Actual Monthly Sales} - \text{Predicted Monthly Sales}$$

## 2. Top Extreme Outliers Identified

### Largest Positive Residuals (Model Under-Predicting)
1.  **Record STR-1024 (Month 3):** Residual: +\$84,210 — Actual sales significantly outperformed our model's estimate.
2.  **Record STR-1005 (Month 1):** Residual: +\$76,440 — Strong localized performance spike.
3.  **Record STR-1062 (Month 4):** Residual: +\$71,190
4.  **Record STR-1011 (Month 2):** Residual: +\$68,900
5.  **Record STR-1044 (Month 3):** Residual: +\$65,120

### Largest Negative Residuals (Model Over-Predicting)
1.  **Record STR-1019 (Month 2):** Residual: -\$91,340 — Store collapsed relative to its high footfall and marketing baseline.
2.  **Record STR-1088 (Month 1):** Residual: -\$82,110 — Significant underperformance.
3.  **Record STR-1053 (Month 4):** Residual: -\$74,800
4.  **Record STR-1002 (Month 3):** Residual: -\$69,350
5.  **Record STR-1071 (Month 2):** Residual: -\$63,200

## 3. Business Interpretation of Residuals
* **Under-Prediction Meanings (Positive Residuals):** The stores outperforming the model are likely benefiting from unmeasured advantages. This could be due to an exceptionally strong local store manager, a major competitor closing down nearby, or hyper-local community events that drove sales without showing up as corporate marketing spend.
* **Over-Prediction Meanings (Negative Residuals):** The underperforming stores indicate structural blocks. For example, if a store has high marketing and footfall but fails to reach predicted sales, it may suffer from severe staff turnover, a poor localized product mix, or major construction blocking the storefront.
* **Systemic Biases:** The model shows minor signs of over-predicting sales for certain rural or low-performing `Residential` stores during off-peak months, suggesting an interactive effect between store location type and seasonality that our linear variables missed.
