# Delhi Air Quality Forecasting
Predicting air pollution in Delhi using artificial intelligence
## What This Does
I built a smart computer program that predicts Delhi's air pollution levels. Think of it like a weather forecast, but for air quality instead of rain or sunshine.
## Why Delhi?
Delhi is one of the most polluted cities in the world. Every winter, the air gets so bad that even healthy people struggle to breathe. If we can predict when pollution will spike, people can prepare and authorities can take action.
## The Problem
Every year, especially in October-November, Delhi's air becomes dangerously polluted. The Air Quality Index (AQI) shoots above 400 - that's the "Severe" category where just breathing outside is harmful.
## What causes this?

Cars and trucks everywhere
Construction dust
Farmers burning crop leftovers in nearby states
Diwali firecrackers
Winter weather that traps all the pollution near the ground

###The big question: Can we predict when this will happen?
###What I Discovered
## The Real Culprits
I analyzed 4 years of pollution data (2021-2024) and found the smoking guns:
PM2.5 and PM10 (tiny dust particles you can't even see)

### These are THE main villains
PM10 correlation: 0.90 (almost perfect relationship with bad air)
PM2.5 correlation: 0.82 (also super strong)

### Other pollutants like CO, NO₂, SO₂, Ozone?

Barely matter in comparison
Weak connection to overall air quality

Simple translation: If you want to fix Delhi's air, focus on reducing dust and smoke particles. Everything else is secondary.
Seasonal Patterns
#### The pollution follows a predictable cycle every year:
Winter (Nov-Jan): 🔴 Terrible

### AQI often crosses 400
### Smog everywhere
### Hardest to breathe

Monsoon (Jul-Sep): 🟢 Best air quality

Rain washes away pollution
Cleanest months

Spring/Fall: 🟡 Medium

Better than winter, worse than monsoon

## The COVID Effect
Something interesting happened during COVID lockdowns:

2021-2023: Air quality improved (less traffic, less industry)
Late 2023 onwards: Pollution started rising again
2024: Back to pre-COVID pollution levels

### What this proves: Human activity directly causes Delhi's bad air. When we reduced activity, air improved. When we went back to normal, pollution returned.
How the Prediction Works
### The Models I Built
I tested three different "prediction engines":

### Linear Regression - Basic, simple

#### Accuracy: 83.5%
Couldn't handle complex patterns


### Random Forest - Smarter, asks many questions

#### Accuracy: 88.7%
Much better!


### XGBoost - The smartest one

#### Accuracy: 88.9% 🏆
Winner!



### Making Future Predictions
I also used a special program called "Prophet" (made by Facebook) to predict future pollution:
### What it predicted for Oct-Nov 2025:
"AQI will cross 400 - severe pollution expected"
### What actually happened:
Delhi's AQI DID exceed 400 multiple times in Oct-Nov 2025! ✅
This proved the model works in real life!
Results in Simple Terms
### Model Performance Comparison
### Model How Good?
Best ForLinear Regression84% ⭐⭐⭐Simple predictionsRandom Forest89% ⭐⭐⭐⭐Complex patternsXGBoost89% ⭐⭐⭐⭐Overall winner
## All three are decent, but XGBoost is the champion.
###  What These Numbers Mean
#### 89% accuracy = Out of 100 predictions, 89 are correct
#### RMSE of 36.5 = On average, predictions are off by about 36 points (pretty good when AQI ranges from 0-500)
Real-World Impact
How This Helps People
For Regular People:

## Check 5-7 day pollution forecast
Plan outdoor activities on cleaner days
Keep kids indoors when severe pollution is predicted
Buy air purifiers before bad air arrives

## For Authorities:

Implement traffic restrictions before pollution peaks
Stop construction during predicted bad days
Send health alerts in advance
Plan emergency response

## For Doctors:

Warn asthma/heart patients ahead of time
Stock up on medications
Prepare hospitals for respiratory cases

## Why Prediction Matters
### Without prediction:
"Oh no, the air is terrible today! What do we do?"
### With prediction:
"Next week will have severe pollution. Let's take action NOW."
It's the difference between reacting and preparing.
## What I Used to Build This
Tools (in plain English):

### Python - The programming language
### Pandas - Organizing data (like super-powered Excel)
### XGBoost - The AI brain that makes predictions
### Prophet - Forecasts future trends
### Matplotlib - Creates charts and graphs

## Data Source:

35,000+ hourly measurements from 2021-2024
Downloaded from Kaggle (a website for datasets)
Tracked 6 pollutants: PM2.5, PM10, CO, NO₂, SO₂, O₃

## Key Insights
What Actually Drives Delhi's Pollution
## Top Contributors:

Vehicles 🚗 - Biggest problem
Construction dust 🏗️ - Everywhere
Crop burning 🔥 - In Punjab/Haryana
Diwali crackers 🎆 - Short but intense spike
Winter weather ❄️ - Traps everything

### What doesn't help much:

Individual lifestyle changes (too small)
Blaming one source (it's multiple things)

### What WOULD help:

Reduce vehicles (EVs, metro, car-pooling)
Control construction dust
Stop crop burning
Regulate firecrackers
Plant more trees

## The Process (Step by Step)

Collected data - 4 years of pollution measurements
Cleaned it - Removed errors, organized properly
Analyzed patterns - Found correlations, seasonal trends
Built models - Trained AI to recognize patterns
Fine-tuned - Optimized for better accuracy
Tested predictions - Checked if they work in real life
Validated - Compared with actual 2025 data ✅

### What I Learned
Technical stuff:

## XGBoost is really good for this kind of problem
Seasonal patterns are predictable
More data = better predictions

## About Delhi's air:

PM2.5 and PM10 are the real enemies
Winter + crop burning + Diwali = disaster combo
Human activity is the main driver

## Personal takeaway:
Even a high school student with a laptop can build tools that might help millions of people breathe easier. That's pretty cool.
Limitations (Being Honest)
What this model CAN'T do:

Predict sudden events (emergency lockdowns, unusual weather)
Account for new pollution sources
Work for other cities without retraining
Replace expert meteorologists

### What could make it better:

Add weather data (wind speed, temperature, rain)
Use data from multiple monitoring stations
Include real-time traffic information
Test with more years of data

## About Me
Shaurya Pandey
High school student who got tired of breathing bad air and decided to do something about it using code.
