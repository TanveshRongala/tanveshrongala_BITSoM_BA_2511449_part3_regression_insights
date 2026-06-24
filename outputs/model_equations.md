# Model Equations

## Simple Regression Equations
- Simple: marketing_spend: monthly_sales = 560,777.35 + (2.1296 × marketing_spend); R² = 0.1672; p-value = 0.000000
- Simple: footfall: monthly_sales = 446,410.58 + (35.6780 × footfall); R² = 0.7363; p-value = 0.000000
- Simple: avg_discount_pct: monthly_sales = 697,835.63 + (-138,730.4547 × avg_discount_pct); R² = 0.0083; p-value = 0.103993
- Simple: inventory_availability_pct: monthly_sales = 484,814.26 + (2,217.8319 × inventory_availability_pct); R² = 0.0131; p-value = 0.040625
- Simple: customer_rating: monthly_sales = 701,366.86 + (-5,284.8663 × customer_rating); R² = 0.0007; p-value = 0.637644
- Simple: staff_count: monthly_sales = 400,551.47 + (16,984.0288 × staff_count); R² = 0.6523; p-value = 0.000000
- Simple: competitor_distance_km: monthly_sales = 692,482.82 + (-2,612.9596 × competitor_distance_km); R² = 0.0114; p-value = 0.055924
- Simple: holiday_flag: monthly_sales = 671,411.86 + (53,625.3354 × holiday_flag); R² = 0.0381; p-value = 0.000443

## Multiple Regression Equation
monthly_sales = 86,319.14 + 1.2099×marketing_spend + 27.3362×footfall - 41,243.1488×avg_discount_pct + 3,508.3992×staff_count + 3,062.2103×inventory_availability_pct - 3,438.1079×competitor_distance_km + 15,157.2873×holiday_flag + 12,509.4613×customer_rating - 24,475.8358×store_type_High_Street - 11,862.2414×store_type_Mall - 44,695.0949×store_type_Residential + 9,948.7136×region_North + 21,089.5657×region_South + 25,291.4189×region_West

## Coefficient Explanations
- **Intercept**: coefficient 86,319.1449, p-value 0.055583. Expected sales for Airport stores in East region when numeric predictors are zero; mainly a baseline.
- **marketing_spend**: coefficient 1.2099, p-value 0.000000. Higher marketing spend is associated with higher monthly sales, holding other variables constant.
- **footfall**: coefficient 27.3362, p-value 0.000000. Higher visitor count is strongly associated with higher monthly sales.
- **avg_discount_pct**: coefficient -41,243.1488, p-value 0.224365. Weak/uncertain discount relationship after controls; do not over-interpret.
- **staff_count**: coefficient 3,508.3992, p-value 0.002743. More staff is associated with higher sales, but may also proxy for larger/busier stores.
- **inventory_availability_pct**: coefficient 3,062.2103, p-value 0.000000. Better availability is associated with higher sales; stockouts likely constrain performance.
- **competitor_distance_km**: coefficient -3,438.1079, p-value 0.000000. Stores farther from competitors have higher sales, suggesting competition pressure.
- **holiday_flag**: coefficient 15,157.2873, p-value 0.013923. Holiday months are associated with higher sales.
- **customer_rating**: coefficient 12,509.4613, p-value 0.005245. Better customer rating is associated with higher sales after controls.
- **store_type_High_Street**: coefficient -24,475.8358, p-value 0.004798. Difference versus Airport stores, holding other variables constant.
- **store_type_Mall**: coefficient -11,862.2414, p-value 0.186917. Difference versus Airport stores, holding other variables constant.
- **store_type_Residential**: coefficient -44,695.0949, p-value 0.000001. Difference versus Airport stores, holding other variables constant.
- **region_North**: coefficient 9,948.7136, p-value 0.130835. Difference versus East region, holding other variables constant.
- **region_South**: coefficient 21,089.5657, p-value 0.001619. Difference versus East region, holding other variables constant.
- **region_West**: coefficient 25,291.4189, p-value 0.000024. Difference versus East region, holding other variables constant.

## Dummy Variables
Dummy variables were created for categorical variables.

### Store Type
Reference category: **Airport**

Included dummy variables:
- `store_type_High_Street`
- `store_type_Mall`
- `store_type_Residential`

Each coefficient compares that store type against Airport stores, holding other predictors constant.

### Region
Reference category: **East**

Included dummy variables:
- `region_North`
- `region_South`
- `region_West`

Each coefficient compares that region against East, holding other predictors constant.

The omitted reference categories prevent redundancy. Including every category plus an intercept would create perfect multicollinearity.

## Final Model Selected
The selected final model is the multiple regression model.

Reason for selection:
- It has the highest explanatory power among the tested models, with R² = 0.8570.
- It controls for several operational factors at once.
- It includes categorical business context through dummy variables.
- It supports practical leadership decisions around marketing, inventory, staffing, region, and store type.

## Business-Language Summary
The equation suggests that sales are most strongly associated with store traffic, marketing spend, inventory availability, staffing, customer rating, competitive environment, holidays, store type, and region. Discounting is included in the model but should not be treated as a strong lever because its p-value is weak after controls.
