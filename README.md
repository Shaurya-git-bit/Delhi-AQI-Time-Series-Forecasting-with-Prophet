# Delhi Air Quality Forecasting
Predicting dangerous air pollution in Delhi using data and machine learning

## Why This Matters
Delhi winters often have dangerously high air pollution, affecting millions of people. I wanted to see if I could predict when pollution would spike so residents, authorities, and doctors could take action ahead of time. Having seen Delhi's winters firsthand during visits, I've experienced those days when you can barely see across the street

## What I Did
I analyzed four years of hourly air quality data from 2021 to 2024 and built models to forecast the Air Quality Index (AQI). The models successfully predicted the severe pollution spike in October and November 2025, which was a huge validation that this approach actually works. My analysis showed that PM2.5 and PM10 are the main culprits behind poor air quality, while gases like CO, NO₂, SO₂, and O₃ have much weaker effects.

## Key Findings
The seasonal patterns were striking. Winter months consistently have the worst air quality, often exceeding an AQI of 400 (dangerous to breathe outside). Monsoon months are relatively clean since rainfall clears the air, while spring and fall sit somewhere in the middle. 

What really stood out was the impact of human activity. During COVID lockdowns, air quality temporarily improved dramatically, but as traffic and industry resumed, pollution levels climbed right back up. It showed me just how much our daily activities contribute to the problem.

## How the Prediction Works
I trained three models: Linear Regression, Random Forest, and XGBoost. Linear Regression gave basic predictions but couldn't handle the complex patterns in the data. Random Forest performed much better, and XGBoost came out on top with 89% accuracy.

<img width="1790" height="790" alt="BEF_HYP" src="https://github.com/user-attachments/assets/1d362271-4993-45c0-afd7-49be93975487" />
*Comparing predictions across all three models. The tighter clustering around the diagonal line for XGBoost showed it was capturing patterns the other models missed.*

I also used Facebook's Prophet to forecast future AQI trends. When it correctly predicted the October-November 2025 spike, I was genuinely surprised at how well it worked. That real-world validation made all the hours of tuning hyperparameters worth it.

<img width="989" height="612" alt="download (1)" src="https://github.com/user-attachments/assets/905ee221-a868-474a-b17e-9a6754b4625e" />

*Prophet forecast from 2021-2026. The blue line shows predictions with confidence intervals. You can see the model caught the 2025 winter spike before it happened—that's when I knew this could actually be useful.*

## Hyperparameter Tuning
Getting XGBoost to 89% accuracy wasn't straightforward. The untuned version was decent, but after spending time adjusting learning rates, tree depth, and regularization parameters, the predictions tightened up significantly.

<img width="1389" height="590" alt="download" src="https://github.com/user-attachments/assets/05f2775b-ca50-44ac-befb-e5b5fecd3bc2" />

*Before and after hyperparameter tuning. The tuned version (right) shows predictions clustering much closer to actual values, especially in the 200-400 AQI range where accurate forecasts matter most.*

## Real-World Applications
These predictions could help residents plan outdoor activities, keep children indoors on high-pollution days, and prepare with air purifiers. Authorities could implement traffic restrictions, limit construction, and issue health alerts in advance. Doctors could warn patients with respiratory or heart conditions and make sure hospitals are prepared with medications.

My goal was to build something that goes beyond just a school project—something that could actually be useful for people dealing with this crisis every winter.

## How It Was Built
I started by collecting and cleaning over 35,000 hourly measurements, which took way longer than I expected. Spent a lot of time exploring correlations and seasonal trends to understand what was actually driving the pollution. Then I built the machine learning models and fine-tuned them for better accuracy. The hardest part was validating predictions against actual 2025 AQI data, but that's what made me confident the model was reliable.

## Tools Used
Python, Pandas, NumPy, Scikit-learn, XGBoost, Prophet, Matplotlib, Seaborn, Jupyter Notebook

## Dataset
The dataset comes from Kaggle and contains hourly measurements from January 2021 to December 2024, tracking six pollutants: PM2.5, PM10, CO, NO₂, SO₂, and O₃.

## Research Paper
I've also written a research paper documenting this work in detail, covering the methodology, results, and implications. It's currently in the process of being reviewed for publication.
#### YOU WILL FIND THE RESEARCH PAPER IN THIS REPOSITORY. IT'S NAMED AS "AQI_Paperrr_2025.pdf"


## What I Learned
This project taught me that building accurate models is only half the battle—understanding what the data actually means and how it can help people is just as important. Working with time series data and handling real-world messiness (missing values, outliers, seasonal variations) was challenging but incredibly rewarding.
