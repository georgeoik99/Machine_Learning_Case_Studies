# Classification Projects

A collection of applied classification projects developed in Python.

This section focuses on supervised machine learning problems where the objective is to assign observations to predefined classes. Projects may include binary, multiclass and imbalanced classification problems across scientific, business and operational datasets.

## Scope

The projects in this folder may cover:

- binary classification,
- multiclass classification,
- imbalanced classification,
- probability estimation,
- risk scoring,
- model comparison,
- feature selection,
- hyperparameter tuning,
- model explainability,
- threshold optimisation.

## Classification Algorithms

### Linear Models

- Logistic Regression
- Multinomial Logistic Regression
- Regularised Logistic Regression
- Ridge Classification
- Linear Discriminant Analysis
- Quadratic Discriminant Analysis

### Tree-Based Models

- Decision Trees
- Random Forest
- Extra Trees
- AdaBoost
- Gradient Boosting
- Histogram-Based Gradient Boosting

### Advanced Boosting Models

- XGBoost
- LightGBM
- CatBoost

### Margin-Based Models

- Support Vector Machines
- Linear Support Vector Classification
- Kernel SVM

### Distance-Based Models

- K-Nearest Neighbours
- Radius Neighbours Classification

### Probabilistic Models

- Gaussian Naive Bayes
- Multinomial Naive Bayes
- Bernoulli Naive Bayes
- Bayesian Classifiers

### Ensemble Methods

- Voting Classifiers
- Stacking Classifiers
- Bagging
- Soft and Hard Voting
- Blended Model Predictions

### Neural Classification Models

- Multi-Layer Perceptrons
- Feed-Forward Neural Networks
- Deep Neural Networks
- Convolutional Neural Networks for image-based tasks

## Supporting Techniques

Projects may also include:

- missing-value treatment,
- categorical-variable encoding,
- feature scaling,
- feature engineering,
- feature selection,
- dimensionality reduction,
- cross-validation,
- hyperparameter optimisation,
- probability calibration,
- decision-threshold tuning,
- class-weight adjustment,
- oversampling and undersampling,
- SMOTE and related resampling methods,
- model explainability with feature importance or SHAP.

## Model Evaluation

Classification performance may be assessed using:

- Accuracy
- Precision
- Recall
- F1 Score
- Specificity
- Confusion Matrix
- ROC Curve and ROC-AUC
- Precision-Recall Curve
- Average Precision
- Log Loss
- Matthews Correlation Coefficient
- Balanced Accuracy
- Calibration Curves

Metric selection depends on the analytical or business objective. Accuracy alone is not sufficient when classes are imbalanced or when different errors have different costs.

## Recommended Workflow

Each classification case study aims to follow a clear workflow:

1. Define the prediction problem and target variable.
2. Inspect data quality and class distribution.
3. Prepare and transform the features.
4. Establish a simple baseline model.
5. Train and compare multiple algorithms.
6. Use cross-validation and appropriate evaluation metrics.
7. Tune the strongest candidate models.
8. Interpret the model and important features.
9. Translate results into practical conclusions.

## Folder Structure

```text
classification/
├── README.md
├── nasa_object_classification/
│   ├── README.md
│   ├── nasa_classification.ipynb
│   ├── requirements.txt
│   └── data/
└── future_classification_project/
```

Folders will be added progressively as new classification case studies are completed.

## Project Standards

Each project should include:

- a clearly defined problem,
- documented data preparation,
- justified model selection,
- baseline and advanced model comparison,
- appropriate evaluation metrics,
- interpretable results,
- practical conclusions,
- reproducible Python code,
- a project-specific README.

## Technologies

- Python
- pandas
- NumPy
- SciPy
- scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

Advanced projects may additionally use:

- XGBoost
- LightGBM
- CatBoost
- imbalanced-learn
- SHAP
- TensorFlow or PyTorch

## Purpose

The objective is not only to train classification models, but also to understand which algorithms are appropriate for different datasets, how model performance should be evaluated and how predictions can be translated into meaningful analytical or business decisions.
