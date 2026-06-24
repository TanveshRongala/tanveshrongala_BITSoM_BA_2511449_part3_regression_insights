# Residual Analysis

## Final Model Used
The selected model is the multiple regression model with numerical drivers, store-type dummy variables, and region dummy variables. Predicted sales were calculated for every record in `analysis/regression_workbook.xlsx` on the `Prediction & Residuals` sheet.

Residual formula:

`residual = actual_monthly_sales - predicted_sales`

A positive residual means the store-month performed better than the model predicted. A negative residual means it performed worse than predicted.

## Largest Positive Residuals
| store_id | month | region | store_type | actual_sales | predicted_sales | residual |
|---|---|---|---|---:|---:|---:|
| STR-1058 | 2025-02-01 | East | High Street | 870,937.40 | 759,919.94 | 111,017.46 |
| STR-1028 | 2025-04-01 | East | Mall | 713,611.16 | 610,531.95 | 103,079.21 |
| STR-1073 | 2025-03-01 | East | Residential | 813,316.71 | 721,415.92 | 91,900.79 |
| STR-1051 | 2025-02-01 | East | Airport | 787,715.51 | 701,381.34 | 86,334.17 |
| STR-1026 | 2025-04-01 | East | Mall | 625,514.04 | 540,234.62 | 85,279.42 |

## Largest Negative Residuals
| store_id | month | region | store_type | actual_sales | predicted_sales | residual |
|---|---|---|---|---:|---:|---:|
| STR-1023 | 2025-02-01 | South | Mall | 627,171.90 | 764,038.71 | -136,866.81 |
| STR-1017 | 2025-03-01 | West | High Street | 685,379.08 | 805,279.85 | -119,900.77 |
| STR-1012 | 2025-01-01 | West | Residential | 595,467.60 | 709,913.78 | -114,446.18 |
| STR-1007 | 2025-02-01 | West | Mall | 800,451.94 | 912,344.87 | -111,892.93 |
| STR-1060 | 2025-01-01 | West | Mall | 721,079.35 | 808,021.71 | -86,942.36 |

## Business Interpretation
Large positive residuals may indicate stores that outperformed due to factors not captured in the model, such as local events, strong store management, product mix, local promotions, competitor disruption, or exceptional execution.

Large negative residuals may indicate stores that underperformed despite having sales drivers that should have supported stronger performance. These records may require investigation into stockouts at product level, store operations, service issues, pricing, local competition, or campaign execution.

## Under-Prediction and Over-Prediction Patterns
The model may under-predict stores that benefit from local demand spikes or exceptional execution that is not represented in the available variables. It may over-predict stores where footfall or staffing look strong but conversion, product availability at SKU level, or customer experience is weaker than expected.

## Limitation
Residual analysis identifies records worth investigating. It does not prove why those stores over- or under-performed.
