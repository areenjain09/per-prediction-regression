# per-prediction-regression
This repository contains all the code, datasets, and visualizations used in the analysis for "Modeling PLayer Performance in Basketball Through Beta Regression." The scripts and notebooks implement a full end-to-end workflow for statistical modeling and prediction of NBA player efficiency ratings using pre-draft college and combine data. In this project we used:
- **Beta Regression Analysis:** Scripts for fitting beta regression models to predict normalized Player Efficiency Rating (PER), including data pre-processing, feature engineering, and custom metric calculations.
- **Longitudinal Modeling:** Implementation of random-intercept (mixed effects) beta regression to model trends in player efficiency acorss multiple NBA season, accounting for repeated measurements per athelte.
- **Backward Elimination:** Automated feature selection routines using backward elimination to idenity the most important predictors for NBA efficieny in the longituidnal dataset.
- **Visualization:** Generation of all analysis plots, including distribution histograms, coefficient plots, goodness-of-fit diagnostics, and predictive accuracy charts.

Player Efficiency Rating (PER) is a NBA league wide metric used to rate players on a scale based on their statistics for the season compared to the league statistics. This helps to seperate the role players, starters, superstars, and MVP-caliber players in the league. Being able to predict this value based on college and combine data will help teams and fans know if the player will be a boom or bust.


## Setup
### Clone the repository 
'''
git clone https://github.com/<your-username>/early-sepsis-pred.git
cd early-sepsis-pred
'''
