# Heart Health Classification

Two self-contained academic Decision Tree case studies based on the public Heart Failure Prediction dataset:

1. four-class prediction of `ChestPainType`,
2. binary prediction of `HeartDisease`.

## Project Overview

The project investigates how the same cardiovascular dataset can support two related classification questions. The analysis combines exploratory data assessment, interpretable preprocessing, Decision Tree modelling and reproducible evaluation.

The dataset contains 918 observations and 12 demographic, symptomatic and clinical attributes.

## Research Questions

- Can patient attributes distinguish between four chest-pain categories?
- Can the selected attributes identify whether heart disease is present?
- Which features contribute most strongly to each Decision Tree?
- How do overall accuracy and class-balanced metrics differ when the target classes are imbalanced?

## Methodology

- data-quality and target-distribution assessment,
- treatment of zero cholesterol and blood-pressure values as unavailable measurements,
- median imputation learned only from training data,
- quantile-based discretisation inside the modelling pipeline,
- one-hot encoding of categorical attributes,
- stratified 80/20 holdout evaluation,
- stratified 10-fold cross-validation,
- accuracy, balanced accuracy, F1, kappa and ROC AUC,
- confusion matrices, classification reports and tree visualisations.

## Case A - Chest Pain Type

The first model predicts four chest-pain categories using Age, Cholesterol, Fasting Blood Sugar, Maximum Heart Rate, Resting Blood Pressure and Sex.

The analysis focuses on patients aged 35 or older. Because the target classes are imbalanced, balanced accuracy and macro F1 are reported alongside overall accuracy.

## Case B - Heart Disease

The second model predicts the binary `HeartDisease` target using Age, Chest Pain Type, Cholesterol, Exercise-Induced Angina, Fasting Blood Sugar, Resting Blood Pressure, Resting ECG and Sex.

It includes a confusion matrix, classification report, ROC AUC, feature importance and a readable visualisation of the first tree levels.

## Results

| Case | Evaluation | Accuracy | Balanced Accuracy | F1 | ROC AUC | Kappa |
|---|---|---:|---:|---:|---:|---:|
| Chest Pain Type | 10-fold CV mean | 0.484 | 0.317 | 0.320 macro | - | - |
| Chest Pain Type | Holdout | 0.494 | 0.314 | 0.320 macro | - | 0.115 |
| Heart Disease | 10-fold CV mean | 0.734 | 0.732 | 0.759 | 0.759 | - |
| Heart Disease | Holdout | 0.772 | 0.774 | 0.786 | 0.818 | 0.542 |

Case A illustrates the challenge of an imbalanced four-class problem. Case B produces the stronger predictive result and achieves useful discrimination on the unseen holdout sample.

## Repository Structure

```text
heart_health_classification/
├── .gitignore
├── heart_health_classification.ipynb
├── README.md
└── requirements.txt
```

## How to Run

1. Confirm that the dataset exists at:

```text
E:\data\heart.csv
```

2. Install the dependencies:

```bash
pip install -r requirements.txt
```

3. Open `heart_health_classification.ipynb` and run the cells from top to bottom.

If the dataset is stored elsewhere, update `DATA_PATH` in the first code cell.

## Technologies

Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn and Jupyter Notebook.

## Disclaimer

This project is intended for academic and portfolio purposes. It explores associations in a public dataset and must not be used as a medical diagnostic tool.
