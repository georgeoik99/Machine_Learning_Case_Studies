# Regression Case Studies

A collection of applied machine learning projects focused on predicting continuous outcomes.

The projects cover complete regression workflows: data preparation, feature engineering, baseline development, model comparison, cross-validation, residual analysis, interpretation and practical conclusions.

## Scope

Regression case studies may include:

- numerical and continuous target prediction,
- linear and nonlinear relationships,
- regularisation and feature selection,
- robust modelling in the presence of outliers,
- tree-based and ensemble methods,
- uncertainty and prediction intervals,
- model interpretation and explainability.

## Methods Covered

### Linear Models and Regularisation

- Simple and Multiple Linear Regression
- Polynomial Regression
- Ridge Regression
- Lasso Regression
- Elastic Net
- Stepwise Feature Selection
- Generalised Additive Models

Linear, Ridge, Lasso and Elastic Net can be studied from both statistical-modelling and machine-learning perspectives. In this repository, emphasis is placed on out-of-sample prediction, cross-validation and model comparison.

### Robust and Distributional Regression

- Huber Regression
- RANSAC Regression
- Quantile Regression
- Theil–Sen Regression
- Tweedie Regression
- Poisson and Gamma Regression

### Tree-Based Models

- Decision Tree Regression
- Random Forest Regression
- Extra Trees Regression
- Gradient Boosting Regression
- Histogram-Based Gradient Boosting

### Modern Boosting Frameworks

- XGBoost
- LightGBM
- CatBoost

These methods are particularly important for modern tabular machine learning because they can model nonlinear relationships, feature interactions and complex decision boundaries with limited preprocessing.

### Kernel, Distance and Neural Models

- Support Vector Regression
- K-Nearest Neighbours Regression
- Multi-Layer Perceptron Regression

### Ensemble Strategies

- Voting Regression
- Stacking Regression
- Blending
- Bagging
- Model Benchmarking

## Evaluation

Projects may use:

- Mean Absolute Error
- Mean Squared Error
- Root Mean Squared Error
- R² and Adjusted R²
- Mean Absolute Percentage Error, where appropriate
- Cross-validation scores
- Residual diagnostics
- Learning curves
- Prediction intervals
- Baseline comparisons

Metrics are calculated on held-out data whenever the objective is predictive modelling. Preprocessing and feature transformations are fitted only on the training data to prevent data leakage.

## Model Interpretation

Depending on the model, interpretation may include:

- regression coefficients,
- feature importance,
- permutation importance,
- partial dependence plots,
- SHAP values,
- residual analysis,
- error analysis across data segments.

## Project Standards

- a clearly defined prediction problem,
- a documented target and feature set,
- reproducible preprocessing,
- a simple baseline model,
- cross-validation or train/test evaluation,
- comparison of appropriate regression methods,
- residual and error analysis,
- interpretation of results,
- practical limitations and conclusions.

## Technologies

- Python
- pandas
- NumPy
- SciPy
- scikit-learn
- statsmodels
- Matplotlib
- Seaborn
- XGBoost
- LightGBM
- CatBoost
- SHAP
- Jupyter Notebook

Technologies are listed according to the overall scope of the collection; individual projects use only the libraries required for their analysis.

## Disclaimer

These projects are intended for educational, academic and portfolio purposes. Projects involving health-related datasets must not be interpreted as medical diagnostic systems.