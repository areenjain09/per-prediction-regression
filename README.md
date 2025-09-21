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


3. **Run Beta Regression Models**
- Navigate to `beta_regression/`.
- Run `data_preprocessing` to prepare input data.
- Use `model` and `train_test` scripts to fit and validate the beta regression.
- Evaluate results with `deviance_test` and create necessary evaluation plots.

4. **Perform Longitudinal Analysis**
- Navigate to `longitudinal/`.
- Preprocess data with `data_preprocessing`.
- Fit the random-intercept mixed effects model using `model`.
- Test hypotheses using `hypotheses_tests` and visualize results with scripts in `plots`.

5. **Backward Elimination (Feature Selection)**
- Go to `backward_elimination/`.
- Run `script` to perform automated backward elimination on the full model, producing a reduced feature set.
- Results output model summaries, reduced formulas, and key metrics.

6. **Visualization**
- Explore the `plots/` directory for all the analytical and diagnostic figures generated in the workflow.
- Figures include predictor breakdowns, coefficient plots, and longitudinal model results.

---

## Notes

- All folders are inter-linked: output from preprocessing steps feeds directly into modeling and visualization scripts.
- Each folder/module has clear, commented code blocks so you can follow the logic used in the paper.
- Results and figures are fully reproducible with the provided scripts and dependencies.

For any questions or issues, please open an issue or submit a pull request!  

