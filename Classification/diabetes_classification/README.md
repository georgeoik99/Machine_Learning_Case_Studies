# Diabetes Classification

This case study compares six classification methods on a common stratified train/test split:

- logistic regression;
- K-nearest neighbours;
- a cross-validated pruned decision tree;
- a random forest tuned only within training resamples;
- linear discriminant analysis;
- quadratic discriminant analysis.

Zero-coded missing measurements are imputed using training medians. KNN scaling is also estimated from training data only. Evaluation includes sensitivity, specificity, balanced accuracy, ROC-AUC, PR-AUC, and a complete-case sensitivity analysis.

View the [rendered analysis](diabetes_classification.md) on GitHub. To edit or rerun it, open `diabetes_classification.qmd` in RStudio and use **Run All**. The dataset is stored locally at `data/pima_diabetes.csv`.

The analysis is written in R with Quarto. Its main packages are `dplyr`, `ggplot2`, `rsample`, `caret`, `tree`, `randomForest`, `pROC`, `corrplot`, `class`, and `MASS`.

This is an educational comparison, not a clinical prediction system.
