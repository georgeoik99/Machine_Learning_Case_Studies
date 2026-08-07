# Machine Learning Case Studies

A growing collection of applied machine learning projects developed in Python.

The repository is organised by modelling task and focuses on complete analytical workflows: data preparation, feature engineering, model development, evaluation, interpretation and business conclusions.

## Repository Scope

The collection will include case studies across:

- **Classification**
- **Regression**
- **Clustering and Unsupervised Learning**
- **Ensemble Methods**
- **Anomaly Detection**
- **Dimensionality Reduction**
- **Feature Selection and Regularisation**
- **Model Evaluation and Comparison**

## Methods Covered

### Classification

- Logistic Regression
- Decision Trees
- Random Forest
- Gradient Boosting
- Support Vector Machines
- K-Nearest Neighbours
- Naive Bayes

### Regression

- Linear Regression
- Polynomial and Nonlinear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net
- Decision Tree Regression
- Random Forest Regression
- Gradient Boosting Regression

### Clustering and Unsupervised Learning

- K-Means
- Hierarchical Clustering
- DBSCAN
- Gaussian Mixture Models
- Customer Segmentation
- Cluster Profiling and Business Interpretation

### Additional Machine Learning Topics

- Principal Component Analysis
- Outlier and Anomaly Detection
- Cross-Validation
- Hyperparameter Tuning
- Feature Scaling and Transformation
- Class Imbalance Handling
- Model Explainability
- Performance Metrics and Benchmarking

## Repository Structure

```text
Machine_Learning_Case_Studies/
│
├── README.md
├── classification/
├── regression/
├── clustering/
│   └── ecommerce_customer_segmentation/
│       ├── ecommerce_customer_segmentation.ipynb
│       ├── README.md
│       └── requirements.txt
├── ensemble_methods/
├── anomaly_detection/
└── dimensionality_reduction/
```

Folders will be added progressively as new case studies are completed.

## Current Case Studies

### E-Commerce Customer Segmentation

**Location:** `clustering/ecommerce_customer_segmentation/`

Customer-level segmentation using two complementary K-Means approaches:

1. Quantity and Spending Segmentation
2. RFM Customer Segmentation

The project includes transaction cleaning, feature engineering, outlier treatment, clustering diagnostics, PCA visualisation, cluster profiling and business recommendations.

## Project Standards

Each case study aims to include:

- a clearly defined problem,
- documented data preparation,
- appropriate feature engineering,
- model selection and evaluation,
- visual interpretation,
- practical conclusions,
- reproducible Python code,
- a project-specific README where appropriate.

## Technologies

- Python
- pandas
- NumPy
- SciPy
- scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Purpose

The repository documents practical progression across supervised and unsupervised machine learning.

Projects may originate from academic coursework, independent analysis or workflows initially developed in tools such as RapidMiner and later reimplemented in Python. Each project will be clearly described according to its origin and scope.

## Disclaimer

The projects are intended for educational, academic and portfolio purposes.
