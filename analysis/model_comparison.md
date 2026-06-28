# Model Comparison Analysis

## 1. Summary of Evaluated Models
I built and evaluated three separate linear regression models to determine what factors are driving monthly sales across our retail stores.

* **Model 1 (Simple Linear Regression):** Uses `marketing_spend` as the single independent variable to predict `monthly_sales`.
* **Model 2 (Simple Linear Regression):** Uses `footfall` as the single independent variable to predict `monthly_sales`.
* **Model 3 (Multiple Linear Regression):** Uses `marketing_spend`, `footfall`, `inventory_availability_pct`, and dummy variables for `store_type` (with `High Street` as the reference baseline) to predict `monthly_sales`.

## 2. Statistical Comparison Matrix

| Model Evaluation Criteria | Model 1: Marketing Spend | Model 2: Store Footfall | Model 3: Multiple Regression |
| :--- | :--- | :--- | :--- |
| **Dependent Variable** | `monthly_sales` | `monthly_sales` | `monthly_sales` |
| **Independent Variables** | `marketing_spend` | `footfall` | `marketing_spend`, `footfall`, `inventory_availability_pct`, `store_type_Mall`, `store_type_Residential`, `store_type_Airport` |
| **R-squared ($R^2$)** | 0.425 (42.5%) | 0.512 (51.2%) | 0.784 (78.4%) |
| **Statistically Significant Variables** | `marketing_spend` ($p < 0.001$) | `footfall` ($p < 0.001$) | All predictors ($p < 0.05$) except `store_type_Residential` |
| **Model Intercept** | \$142,500 | \$98,400 | \$45,200 |

## 3. Explanatory Power & Business Usefulness
* **R-squared Comparison:** Model 1 and Model 2 explain roughly 42% and 51% of the variation in store sales individually. However, Model 3 drastically outperforms them, explaining 78.4% of the variation. This means that retail sales are driven by a combination of marketing, customer traffic, operational availability, and store formats working together.
* **Business Application:** Model 3 is far more useful for leadership decisions. It allows us to simulate the financial return of scaling up marketing budgets while keeping operational factors like inventory steady, or accounting for the unique baseline shifts of opening a Mall store versus a standalone High Street location.

## 4. Limitations of the Analysis
While Model 3 captures the major operational levers, it doesn't account for macroeconomic shifts, local pricing changes, or seasonal shifts beyond what is embedded in the baseline numbers. Furthermore, some variables like `store_type_Residential` show high p-values, indicating their sales performance isn't distinct enough from the High Street baseline to be reliable on its own.
