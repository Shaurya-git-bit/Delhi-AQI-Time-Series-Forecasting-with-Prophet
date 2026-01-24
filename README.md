# Delhi Air Quality Forecasting
Predicting dangerous air pollution in Delhi using data and machine learning

# Why This Matters
Delhi winters often have dangerously high air pollution, affecting millions of people. I wanted to see if it was possible to predict when pollution would spike so residents, authorities, and doctors could take action ahead of time.

# What I Did
I analyzed four years of hourly air quality data from 2021 to 2024 and built models to forecast the Air Quality Index (AQI). The models successfully predicted the severe pollution spike in October and November 2025. Analysis showed that PM2.5 and PM10 are the main pollutants driving poor air quality, while gases like CO, NO₂, SO₂, and O₃ have much weaker effects.

# Key Findings
The data revealed clear seasonal patterns. Winter months consistently have the worst air quality, often exceeding an AQI of 400, making it dangerous to breathe. Monsoon months are relatively clean, as rainfall clears the air, while spring and fall have moderate pollution. Human activity also plays a significant role. During the COVID lockdowns, air quality temporarily improved, but as traffic and industry resumed, pollution levels rose again.

# How the Prediction Works
I trained three models: Linear Regression, Random Forest, and XGBoost. Linear Regression provided basic predictions but struggled with complex patterns. Random Forest performed better, and XGBoost achieved the highest accuracy at 89 percent. I also used Facebook’s Prophet to forecast future AQI trends, and it correctly predicted the October-November 2025 spike, demonstrating the model’s reliability.

# Real-World Use
These predictions can help residents plan outdoor activities, keep children indoors on high-pollution days, and prepare with air purifiers. Authorities can implement traffic restrictions, limit construction, and issue health alerts. Doctors can warn patients with respiratory or heart conditions and prepare hospitals and medications in advance.

# How It Was Built
I collected and cleaned 35,000+ hourly measurements, explored correlations and seasonal trends, built machine learning models, and fine-tuned them for better accuracy. Predictions were validated against actual AQI data from 2025 to ensure reliability.

# Tools Used
Python, Pandas, NumPy, Scikit-learn, XGBoost, Prophet, Matplotlib, Seaborn, Jupyter Notebook

# Dataset
The dataset comes from Kaggle and contains hourly measurements from January 2021 to December 2024, tracking six pollutants: PM2.5, PM10, CO, NO₂, SO₂, and O₃.

# Notes
This project focuses on creating actionable predictions that can inform real-world decisions. It highlights how data-driven models can help communities, authorities, and medical professionals respond proactively to dangerous air pollution.
