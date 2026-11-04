# M5 Food Demand Forecasting

A food demand forecasting project using the Walmart M5 dataset to support inventory replenishment and supply chain planning.

The project processes **27.5 million daily sales records** covering **1,437 food products across 10 stores**. It combines historical sales with calendar events, prices, and SNAP indicators to analyze demand and compare forecasting models.

## Project Highlights

- Used **RAPIDS cuDF and CuPy** for GPU-accelerated data preparation and feature engineering.
- Compared baseline methods, Linear Regression, Ridge Regression, Random Forest, and GPU XGBoost.
- Evaluated model performance alongside training time and GPU memory usage.
- Aggregated sales into **30 store-department time series** to address sparse product-level demand.
- Selected **Tuned Prophet** for the final **28-day demand forecast**, using chronological training, validation, and test periods.

## Final Test Results

Results for Tuned Prophet on the held-out 28-day test period:

| Metric | Result |
|---|---:|
| WMAPE | 10.30% |
| MAE | 96.99 units |
| RMSE | 146.79 units |
| R² | 0.9679 |

Tuned Prophet slightly outperformed the four-week weekday baseline, which achieved a WMAPE of **10.42%**.

## Technologies

Python · RAPIDS · cuDF · cuML · CuPy · XGBoost · Prophet · pandas · Matplotlib · Google Colab

## Repository Contents

- **Jupyter Notebook:** Data preparation, exploratory analysis, modeling, and evaluation.
- **Project Report:** Methodology, findings, and business interpretation.
