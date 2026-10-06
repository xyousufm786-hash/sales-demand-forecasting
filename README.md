# Daily Sales Forecasting

Forecasts 90 days of daily retail sales using calendar features (weekday, season), a promotion flag and lagged sales, and compares machine-learning models with a seasonal-naive baseline.

## Highlights
| Model | MAE (RM) | MAPE |
|---|---|---|
| **Ridge regression** | **87.6** | **6.0%** |
| Gradient boosting | 94.7 | 6.7% |
| Same day last year (baseline) | 210.5 | 14.5% |

- The ML models **more than halve** the baseline's error by learning the growth trend
- Lags are at least 90 days back, so the model never uses information it wouldn't have at forecast time
- Produces a Q1 forecast with monthly totals for stock and staff planning

## Data
Three years (2023–2025) of simulated daily sales with trend, weekly and yearly seasonality, and 11.11 / Black Friday / year-end promotions, generated in the notebook.

## Run it
```bash
pip install -r requirements.txt
jupyter notebook sales-demand-forecasting.ipynb
```
Then **Run → Run All Cells**. Results are reproducible (fixed random seeds).

**Stack:** Python · pandas · scikit-learn · matplotlib
