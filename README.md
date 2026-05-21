# Delhi AQI Forecasting — Machine Learning & Time Series Analysis

This repository contains the full analysis pipeline for forecasting Delhi's Air Quality Index (AQI) using machine learning and time series models. The project uses four years of daily air quality data (2021–2024) from NSUT's campus monitoring station and validates a long-range Prophet forecast against actual CPCB AQI bulletin data from October–November 2025.

---

## Repository Structure

- `Delhi_AQI_EDA.ipynb` - Exploratory Data Analysis
- `Delhi_AQI_ML.ipynb` - Machine Learning Models & Prophet Forecasting

---

## EDA Notebook

Covers the full data exploration pipeline:

- **Dataset**: 1,461 daily observations of PM2.5, PM10, NO2, SO2, CO, and Ozone from NSUT's campus station (Kaggle)
- **Correlation analysis**: Pearson correlations between each pollutant and AQI, with scatter plots and a heatmap
- **Multicollinearity check**: VIF calculated for both raw pollutant features and 24 lagged features
- **Seasonal decomposition**: Additive decomposition separating AQI into trend, seasonal, and residual components
- **Lag feature construction**: Pollutant values at 1, 2, 3, and 7-day lags created to avoid same-time target leakage

---

## ML Notebook

Covers model training, evaluation, and forecasting:

- **Models**: Linear Regression (baseline), Random Forest, and XGBoost trained on 24 lagged pollutant features
- **Data split**: Chronological 80/20 split with five-fold TimeSeriesSplit for cross-validation and hyperparameter tuning
- **Tuning**: RandomizedSearchCV with TimeSeriesSplit used for both Random Forest and XGBoost
- **Evaluation metrics**: RMSE, MAE, R², and MAPE reported before and after tuning
- **CPCB benchmark**: Rule-based AQI calculation included to contextualize ML model performance
- **SHAP analysis**: TreeSHAP applied to the tuned XGBoost model with beeswarm and bar plots
- **Prophet forecasting**: Long-range forecast through 2026 with trend/seasonality decomposition
- **Baselines**: Seasonal naïve and SARIMA models included for honest Prophet comparison
- **2025 validation**: Prophet forecast validated against actual CPCB Daily AQI Bulletins (Oct–Nov 2025)

---

## Key Findings

- XGBoost achieved the best post-tuning performance (R² = 0.499, RMSE = 72.61)
- Short-term PM2.5 and PM10 lags dominated SHAP feature importance
- Prophet correctly classified 95.08% of days where AQI exceeded 400
- The CPCB rule-based benchmark outperformed all lagged ML models, confirming the lagged task is genuinely harder

---

## Requirements

```bash
pip install pandas numpy scikit-learn xgboost prophet shap pmdarima matplotlib seaborn statsmodels
```

---

## Data Source

[Delhi Air Quality Dataset - Kaggle](https://www.kaggle.com/datasets/kunshbhatia/delhi-air-quality-dataset)

2025 validation data sourced from [CPCB Daily AQI Bulletins](https://cpcb.nic.in/)
