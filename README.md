# per-prediction-regression
This repository contains all the code, datasets, and visualizations used in the analysis for "Modeling PLayer Performance in Basketball Through Beta Regression." The scripts and notebooks implement a full end-to-end workflow for statistical modeling and prediction of NBA player efficiency ratings using pre-draft college and combine data. In this project we used:
- **Beta Regression Analysis:** Scripts for fitting beta regression models to predict normalized Player Efficiency Rating (PER), including data pre-processing, feature engineering, and custom metric calculations.
- **Longitudinal Modeling:** Implementation of random-intercept (mixed effects) beta regression to model trends in player efficiency acorss multiple NBA season, accounting for repeated measurements per athelte.
- **Backward Elimination:** Automated feature selection routines using backward elimination to idenity the most important predictors for NBA efficieny in the longituidnal dataset.
- **Visualization:** Generation of all analysis plots, including distribution histograms, coefficient plots, goodness-of-fit diagnostics, and predictive accuracy charts.

Player Efficiency Rating (PER) is a NBA league wide metric used to rate players on a scale based on their statistics for the season compared to the league statistics. This helps to seperate the role players, starters, superstars, and MVP-caliber players in the league. Being able to predict this value based on college and combine data will help teams and fans know if the player will be a boom or bust.


## Setup
### Clone the repository 
```
https://github.com/<yourname>/per-prediction-regression.git
cd per-prediction-regression
```

### Install Dependencies
Ensure you have R (≥4.0) installed, along with the following packages:
```r
install.packages(c("ggplot2","dplyr","gridExtra","glmmTMB","MuMIn","multcomp","emmeans","DHARMa","betareg","xtable",
"caret","lme4","lmerTest","parameters","tidyr","stringr"))
```

## Data Preprocessing
Go to the relevant analysis folder and run the preprocessing script. For instance:
```r
setwd("path/to/per-prediction-regression")
source("beta_regression/data_preprocessing")
```
or for longitudinal:
```r
setwd("path/to/per-prediction-regression")
source("longitudinal/data_preprocessing")
```
This will clean up the data to have it ready for running the model fits.

## Fit Models
### Beta Regression Modeling
```r
setwd("path/to/per-prediction-regression")
source("beta_regression/model")
source("beta_regression/train_test")
source("beta_regression/deviance_test")
```

### Longitudinal Modeling
```r
setwd("path/to/per-prediction-regression")
source("longitudinal/model_formula")
source("longitudinal/model")
```

## Feature Selection
### Backward Elimination
This script outputs model reduction steps and final significant predictors:

```r
setwd("path/to/per-prediction-regression")
source("backward_elimination/script")
```

## Visualizations
All plots should fall under the following sections or within their respective code files.
```r
setwd("path/to/per-prediction-regression")
source("longitudinal/plots")
source("plots/predictors")
```



## project Structure
```
per-prediction-regression/
├── beta_regression/
│   ├── data_preprocessing
│   ├── model
│   ├── train_test
│   ├── deviance_test
│   ├── utils
├── longitudinal/
│   ├── data_preprocessing
│   ├── model
│   ├── hypotheses_tests
│   └── plots/
├── backward_elimination/
│   └── script
├── plots/
│   └── predictors
├── .gitignore
└── README.md
```
