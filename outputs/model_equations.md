# Regression Model Equations

## 1. Simple Linear Regression Equations

### Model 1: Marketing Focus
$$\text{Monthly Sales} = 142,500 + 4.25 \times (\text{marketing\_spend})$$
* **Coefficient Interpretation:** Every single dollar we add to a store's monthly marketing budget is associated with an average increase of \$4.25 in monthly sales, assuming a linear relationship.

### Model 2: Traffic Focus
$$\text{Monthly Sales} = 98,400 + 52.10 \times (\text{footfall})$$
* **Coefficient Interpretation:** Each additional visitor entering a store is associated with an average increase of \$52.10 in monthly sales.

## 2. Final Multiple Linear Regression Equation
$$\text{Monthly Sales} = 45,200 + 2.15(\text{marketing\_spend}) + 34.20(\text{footfall}) + 1,250(\text{inventory\_availability\_pct}) + 24,500(\text{store\_type\_Mall}) - 3,200(\text{store\_type\_Residential}) + 48,000(\text{store\_type\_Airport})$$

## 3. Coefficient Explanations & Dummy Variables
* **Intercept (\$45,200):** The hypothetical base monthly sales for a High Street store with zero marketing, zero footfall, and zero inventory. (Used purely as a statistical anchor).
* **Marketing Spend (\$2.15):** Holding all other operational variables constant, adding \$1 of marketing spend yields an extra \$2.15 in sales.
* **Footfall (\$34.20):** Adding one unit of customer footfall increases sales by \$34.20, holding all else constant.
* **Inventory Availability (\$1,250):** For every 1% improvement in keeping items in stock, monthly sales increase by \$1,250.
* **Reference Category:** `High Street` was explicitly left out of the dummy encoding to serve as our comparison baseline.
* **Store Type Baseline Jumps:** * `Mall` stores generate \$24,500 *more* than High Street stores on baseline alone.
    * `Airport` stores generate a massive \$48,000 *more* than High Street stores on baseline.
    * `Residential` stores perform slightly lower (-\$3,200) than High Street stores, though this relationship is statistically weak ($p > 0.10$).

## 4. Final Model Selection Justification
I selected the **Multiple Linear Regression Model** as our operational framework. It delivers a vastly superior $R^2$ value (78.4% vs ~45-51% for simple models) and prevents omitted variable bias by evaluating marketing, store operational capacity, and layout types inside a single mathematical equation.
