# Delhi Air Quality Forecasting with Machine Learning
Predicting Delhi's air pollution using real data and machine learning models
# What This Project Does
I analyzed 4 years of Delhi's air quality data (2021-2024) to figure out which pollutants actually cause the terrible air we breathe, and built ML models to predict future AQI levels. Spoiler: PM2.5 and PM10 are the real culprits.
# Quick Results

PM10 and PM2.5 = main pollution drivers (correlations of 0.90 and 0.82)
XGBoost = best model with 89% accuracy
Prophet successfully predicted the severe pollution in Oct-Nov 2025 (which actually happened!)
Winter months are brutal, monsoon months bring relief

# The Code Breakdown
## 1. Data Loading & Cleaning

Got 35,000+ hourly observations from Kaggle
Checked for missing values (there were none, nice!)
Converted timestamps and extracted month/season info

## 2. Exploratory Data Analysis (EDA)

Calculated correlations between pollutants and AQI
Created scatter plots to visualize relationships
Built correlation heatmaps
Analyzed seasonal patterns with box plots

# Key Finding: PM10 and PM2.5 have super strong correlations with AQI, while gases like O₃, NO₂, SO₂ barely matter

## 3. Machine Learning Models
Trained three models to predict AQI:
ModelRMSER² ScoreLinear Regression44.510.835Random Forest36.850.887XGBoost36.510.889

## 4. Hyperparameter Tuning

Used RandomizedSearchCV with 3-fold cross-validation
Tested 20 different configurations for each model
XGBoost came out on top after tuning

## 5. Time Series Forecasting

Used Facebook's Prophet model
Forecasted AQI trends through 2025-2026
Model correctly predicted the severe pollution spike in Oct-Nov 2025!

# Cool Findings
### Seasonal Patterns:

Winter (Nov-Jan) = worst air quality, AQI often hits 400+
Monsoon (Jul-Sep) = best air quality, rain clears things up
Transition months = moderate pollution

# COVID Impact:

AQI dropped from 2021 to mid-2023 (reduced traffic/activity)
Started rising again in late 2023 as everything reopened
Shows how much human activity impacts air quality

# What's Actually Causing This:

Vehicle emissions (the biggest problem)
Construction dust
Stubble burning in neighboring states
Diwali firecrackers
Winter weather traps everything near the ground

# Tech Stack

Python - main language
Pandas & NumPy - data handling
Scikit-learn - ML models
XGBoost - gradient boosting
Prophet - time series forecasting
Matplotlib & Seaborn - visualizations
Jupyter Notebook - development

# Dataset
Source: Kaggle - Delhi Air Quality Dataset

# Time period: Jan 2021 - Dec 2024
Frequency: Hourly measurements
Pollutants tracked: PM2.5, PM10, NO₂, SO₂, CO, O₃

# Files in This Repo

Delhi Air Quality.ipynb - main Jupyter notebook with all the code
AQI_Paper_2025.pdf - full research paper
README.md - you're reading it!
