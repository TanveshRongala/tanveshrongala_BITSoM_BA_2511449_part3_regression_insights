# Model Comparison

| Model name | Variables used | R-squared | Significant variables | Business usefulness | Limitations |
|---|---|---:|---|---|---|
| Simple: marketing_spend | DV: monthly_sales; IV: marketing_spend | 0.1672 | marketing_spend | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Simple: footfall | DV: monthly_sales; IV: footfall | 0.7363 | footfall | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Simple: avg_discount_pct | DV: monthly_sales; IV: avg_discount_pct | 0.0083 | None at 5% | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Simple: inventory_availability_pct | DV: monthly_sales; IV: inventory_availability_pct | 0.0131 | inventory_availability_pct | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Simple: customer_rating | DV: monthly_sales; IV: customer_rating | 0.0007 | None at 5% | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Simple: staff_count | DV: monthly_sales; IV: staff_count | 0.6523 | staff_count | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Simple: competitor_distance_km | DV: monthly_sales; IV: competitor_distance_km | 0.0114 | Borderline: competitor_distance_km | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Simple: holiday_flag | DV: monthly_sales; IV: holiday_flag | 0.0381 | holiday_flag | Useful for directional insight; limited because it excludes other business drivers. | Single-variable model; may suffer omitted-variable bias. |
| Multiple: final selected model | DV: monthly_sales; IVs: marketing_spend, footfall, avg_discount_pct, staff_count, inventory_availability_pct, competitor_distance_km, holiday_flag, customer_rating, store_type dummies, region dummies | 0.8570 | marketing_spend, footfall, staff_count, inventory_availability_pct, competitor_distance_km, holiday_flag, customer_rating, store_type_High_Street, store_type_Residential, region_South, region_West | Best decision model because it explains the most variation and controls for store type and region. | Association only; may exclude local events, price mix, promotions, seasonality depth, and store-level fixed effects. |

## Summary
The simple regression models are useful for isolating one relationship at a time. `footfall` is the strongest single driver with R² = 0.7363. `staff_count` is also strong as a simple model with R² = 0.6523, but staff count may partly reflect store size and traffic rather than a pure staffing effect.

The final multiple regression model is more useful for leadership decisions because it controls for multiple drivers, store type, and region. Its R² is 0.8570 and adjusted R² is 0.8504. This means it explains a large share of monthly sales variation while still leaving room for factors not captured in the dataset.

## Key Takeaway
Use the multiple model for decision-making, but use the simple models to communicate intuitive relationships such as the importance of footfall.
