### Abalone Age Prediction Using PyCaret

## Project Overview
Determining the age of abalone is traditionally a destructive and laborious process requiring microscopic ring counting. This project explores a machine learning approach to estimate age using non-invasive physical measurements (length, diameter, weight, etc.).

## Methodology
1) AutoML: Utilized PyCaret for rapid model comparison and tuning.

2) Feature Engineering: Created custom features to capture unexplained variance, including:

3) Volume (Diameter × Length × Height).

4) Weight_diff (Whole weight minus the sum of shucked, viscera, and shell weights).

5) Modeling: Evaluated various regression models, identifying Gradient Boosting as the top individual performer.

## Final Model & Results
To maximize predictive performance, a Voting Regressor was constructed using an ensemble of the top three tuned models: Gradient Boosting, Extra Trees, and Random Forest.

Metric	Score
R^2   	0.5878
RMSE	  2.0688
MAE	    1.4780


## Key Findings
Feature Importance: Shell_weight proved to be the most critical predictor of age.

Limitations: The model's performance plateaus around an R^2 of 0.58. 
This suggests inherent limitations in the dataset, specifically a skewed distribution favoring younger specimens and significant noise in the physical traits of older abalone.

Youtube - https://youtu.be/R_iV61XkiSc
