# Delhi Air Quality Forecasting
Predicting air pollution in Delhi using data and machine learning

# Why This Matters
Delhi winters often have dangerously high air pollution, affecting millions of people. I wanted to see if it was possible to predict these spikes so residents, authorities, and doctors could take action ahead of time.  

# What I Did
I analyzed four years of hourly air quality data (2021–2024) and built models that forecast Delhi's Air Quality Index (AQI). The model correctly predicted the severe pollution spike in Oct-Nov 2025. PM2.5 and PM10 were identified as the main drivers of poor air quality.

# Key Findings
- **Main culprits:** PM2.5 and PM10 (vehicles, construction dust, crop burning, Diwali fireworks)  
- **Seasonal patterns:** Winter = worst, Monsoon = cleanest, Transition months = moderate  
- **Human impact:** COVID lockdowns temporarily improved air quality; resuming normal activity caused pollution to rise again  

# How the Prediction Works
Three models were tested:
- **Linear Regression:** Simple predictions, 84% accuracy  
- **Random Forest:** Handles more complex patterns, 89% accuracy  
- **XGBoost:** Best overall, 89% accuracy  
I also used **Prophet** to forecast future AQI trends, which successfully predicted the Oct-Nov 2025 spike.

# Real-World Use
**Residents:** Check forecasts, plan outdoor activities, keep kids indoors on high-AQI days  
**Authorities:** Implement traffic restrictions, control construction, issue health alerts  
**Doctors:** Warn asthma/heart patients, prepare hospitals and medications  

# How It Was Built
- Collected and cleaned 35,000+ hourly measurements  
- Explored patterns and correlations between pollutants and AQI  
- Built, tuned, and tested machine learning and forecasting models  
- Validated predictions against real-world events  

# Tools Used
Python | Pandas | NumPy | Scikit-learn | XGBoost | Prophet | Matplotlib | Seaborn | Jupyter Notebook  

# Dataset
- Source: Kaggle – Delhi Air Quality Dataset  
- Time: Jan 2021 – Dec 2024, hourly measurements  
- Pollutants tracked: PM2.5, PM10, CO, NO₂, SO₂, O₃  

# Notes
This is a hands-on, practical project demonstrating how real data can inform decisions and reduce risk in highly polluted cities. The focus was on **predictive accuracy and actionable insights**, not just building models for their own sake.
