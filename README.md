# Retail Monthly Sales Regression Analysis

## Business Problem Summary
Leadership needs to decide which business levers are most associated with monthly sales performance across stores. The decision affects marketing budget allocation, inventory availability priorities, discount strategy, staffing plans, and store/region prioritization.

The dependent variable is `monthly_sales`. The analysis tests whether variables such as footfall, marketing spend, average discount, staff count, inventory availability, competitor distance, holiday periods, customer rating, region, and store type explain sales variation.

## Dataset Description
The source workbook is `data/business_regression_data.xlsx`. It contains:
- `store_performance`: 320 store-month observations and 14 columns.
- `data_dictionary`: business descriptions of each field.

Data quality notes:
- `customer_rating` had 8 missing values and was imputed with median 3.90.
- `competitor_distance_km` had 6 missing values and was imputed with median 3.365.
- Text categories were standardized for spacing.
- `month` was prepared as a monthly date field.
- `monthly_profit` was not used as a predictor because it is a related outcome metric, not a driver to explain sales.

## Dependent and Independent Variables
**Dependent variable:** `monthly_sales`

**Potential independent variables:**
- Numerical: `marketing_spend`, `footfall`, `avg_discount_pct`, `staff_count`, `inventory_availability_pct`, `competitor_distance_km`, `holiday_flag`, `customer_rating`
- Categorical: `region`, `store_type`

**Variables not selected for regression as predictors:**
- `store_id`: identifier, not a direct explanatory variable.
- `month`: useful for time/seasonality analysis, but the dataset contains only a short four-month window.
- `monthly_profit`: related business outcome and may create leakage if used to explain sales.

## Regression Approach
I created simple linear regression models using one independent variable at a time and a multiple regression model using numerical predictors plus dummy variables for store type and region.

## Dummy Variable Approach
Dummy variables were created for:
- `store_type`: High Street, Mall, Residential; reference category = Airport.
- `region`: North, South, West; reference category = East.

The reference category is omitted to avoid dummy-variable redundancy.

## Model Comparison Summary
The strongest simple model was `footfall` with R² = 0.7363. The final multiple regression model had R² = 0.8570 and adjusted R² = 0.8504, making it the best model for decision support.

## Final Model Selected
The final selected model is the multiple regression model with numerical business drivers, store-type dummies, and region dummies.

## Business Recommendation
Leadership should prioritize actions that increase qualified footfall, improve inventory availability, use marketing spend efficiently, and review staffing levels in high-potential stores. Discounting should not be over-interpreted because its coefficient is weak after controls.

## Assumptions and Limitations
- Regression shows association, not automatic causation.
- Missing values were median-imputed.
- The model does not fully capture local events, merchandising mix, product pricing, competitor promotions, campaign quality, or long-term seasonality.
- Footfall and staff count may be related because larger stores tend to have both higher traffic and more staff.

## Screenshots Included
- `screenshots/simple_regression_output.png`
- `screenshots/multiple_regression_output.png`
- `screenshots/residuals_preview.png`
- `screenshots/model_comparison_preview.png`

## Repository Contents
- `data/business_regression_data.xlsx`
- `analysis/regression_workbook.xlsx`
- `analysis/model_comparison.md`
- `analysis/residual_analysis.md`
- `outputs/regression_summary.xlsx`
- `outputs/model_equations.md`
- `outputs/final_recommendation.md`
- `screenshots/*.png`
