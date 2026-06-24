# Final Recommendation

## Executive Recommendation
Leadership should focus on improving qualified store traffic, inventory availability, marketing effectiveness, and staffing alignment. The final multiple regression model explains a strong share of monthly sales variation with R² = 0.8570 and adjusted R² = 0.8504.

## Factors Most Strongly Associated with Monthly Sales
The regression evidence suggests the strongest useful associations are:

- **Footfall:** positive and highly significant. In the multiple model, each additional visitor is associated with about 27.34 higher monthly sales, holding other factors constant.
- **Marketing spend:** positive and highly significant. Each additional unit of marketing spend is associated with about 1.21 higher monthly sales.
- **Inventory availability:** positive and highly significant. Each additional percentage point of availability is associated with about 3,062 higher monthly sales.
- **Staff count:** positive and significant, but should be interpreted carefully because it may also reflect larger or busier stores.
- **Customer rating:** positive and significant in the multiple model.
- **Competitor distance:** negative competition pressure is visible. Stores farther from competitors show higher sales, all else equal.
- **Store type and region:** some categories differ meaningfully from the reference categories after controls.

## Variables Leadership Should Focus On
1. **Footfall generation:** prioritize campaigns and local actions that increase qualified traffic.
2. **Inventory availability:** reduce stockout risk and prioritize availability in stores with strong traffic.
3. **Marketing spend efficiency:** increase spend where footfall response and conversion potential are strongest.
4. **Staffing allocation:** align staffing with stores where traffic and sales potential justify additional coverage.
5. **Customer experience:** improve service and ratings, especially where residuals show under-performance.

## Variables Not to Over-Interpret
- **Average discount percentage:** the coefficient is negative but statistically weak in the multiple model. This does not prove discounts reduce sales. It may reflect tactical discounting in weaker stores or end-of-period clearance.
- **Mall store dummy:** the coefficient is not statistically strong relative to Airport stores in the final model.
- **Staff count:** positive, but it may proxy for store size or expected traffic rather than pure incremental labor productivity.

## Recommended Business Action
Run targeted operational pilots:
- Increase inventory availability in high-footfall stores.
- Reallocate marketing spend toward stores or regions with strong traffic response.
- Review staffing in high-traffic stores with negative residuals.
- Investigate top positive residual stores to identify transferable best practices.
- Investigate top negative residual stores for execution gaps, stockouts, local competition, or conversion problems.

## Risks and Limitations
- The dataset covers a limited time window, so seasonality may not be fully captured.
- Regression does not include all possible drivers such as product mix, local events, campaign quality, pricing, weather, or competitor promotions.
- Missing values were imputed using medians.
- Relationships may differ across store types and regions.

## Why Regression Does Not Automatically Prove Causation
Regression estimates association while holding included variables constant. It does not prove that changing one variable will cause sales to change by the coefficient amount. Causation would require stronger evidence such as randomized experiments, controlled pilots, natural experiments, or before/after testing with comparable control stores.
