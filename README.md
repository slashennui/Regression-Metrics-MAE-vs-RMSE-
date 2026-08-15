# Regression Metrics: MAE vs RMSE

A reproducible notebook for understanding common regression metrics on held-out data, with emphasis on the difference between **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.

## What it demonstrates

- train/test evaluation with linear regression
- a mean-prediction baseline
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Median Absolute Error
- coefficient of determination (\(R^2\))
- how one extreme residual affects MAE and RMSE differently
- residual plots
- baseline-relative error ratios
- why \(R^2\) can be negative

## MAE versus RMSE

For the same set of residuals:

- MAE is the arithmetic mean of absolute residual magnitudes.
- RMSE is the square root of the arithmetic mean of squared residuals.
- RMSE is always greater than or equal to MAE.
- RMSE gives greater weight to large residuals because of the squaring step.

Neither metric is universally superior. Choose the metric according to the application's error costs and report the target units and a relevant baseline.

## Important interpretation points

- There is no universal "good" MAE or RMSE threshold.
- Raw MAE/RMSE values are scale-dependent.
- \(R^2\) can be negative on evaluation data.
- A scalar metric does not replace residual diagnostics or checks for distribution shift and data leakage.

## Reproducibility

The notebook:

- uses a fixed random seed
- evaluates on a held-out test split
- uses `sklearn.metrics.root_mean_squared_error` directly
- keeps outputs and execution counts cleared in Git

Binder/repo2docker uses `requirements.txt` for dependencies and `runtime.txt` for the Python version.

## Run locally

```bash
python -m pip install -r requirements.txt
jupyter lab
```

Then open:

`Regression Metrics (MAE vs RMSE).ipynb`
