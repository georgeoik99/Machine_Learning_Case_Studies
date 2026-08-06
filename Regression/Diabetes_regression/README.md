# Skin Thickness Estimation with Linear Regression

An exploratory linear-regression project that studies the relationship between Body Mass Index (`BMI`) and `SkinThickness` in the diabetes dataset.

This project was originally developed independently before my MSc studies and was later revisited to improve the residual analysis and statistical interpretation.

## Objective

The main objective is to examine whether BMI can be used as a simple linear predictor of skin-thickness measurements. The model is intended as an educational statistical experiment, not as a clinical prediction tool.

## Workflow

- Dataset inspection and descriptive statistics
- Skewness, kurtosis and correlation analysis
- Identification of zero values and potential outliers
- Train/test split and simple linear-regression fitting
- Comparison of fitted and observed values
- Residual-versus-fitted plots, residual distributions and Q–Q plots

## Main finding

BMI and skin thickness show a positive relationship, but a single-predictor linear model explains only part of the observed variation. The residual diagnostics indicate that the assumptions and preprocessing choices require careful evaluation before drawing stronger conclusions.

## Current limitations

- Zero values in clinical measurements require a documented missing-data strategy.
- Outlier handling should be fitted on the training data and justified explicitly.
- Feature scaling must not include the target or use information from the test set.
- The AIC, BIC and R² calculations in the current notebook require correction.
- Metrics calculated on differently scaled targets should not be compared directly.

## Files

- `Diabetes_Regression.ipynb`: exploratory analysis, regression experiment and residual diagnostics.

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, SciPy and scikit-learn.

## Disclaimer

This repository is an educational data-analysis project and must not be used for medical diagnosis or clinical decision-making.
