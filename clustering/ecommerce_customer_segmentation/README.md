# Clustering and Unsupervised Learning Projects

A collection of applied clustering projects developed in Python.

This section focuses on unsupervised learning methods used to identify hidden structure, behavioural groups, natural segments and unusual observations in data.

## Scope

The projects in this folder may cover:

- customer segmentation,
- behavioural profiling,
- market segmentation,
- anomaly and outlier detection,
- pattern discovery,
- dimensionality reduction,
- cluster validation,
- comparison of clustering algorithms.

## Clustering Algorithms

### Partition-Based Clustering

- K-Means
- K-Medoids
- Mini-Batch K-Means

### Hierarchical Clustering

- Agglomerative Clustering
- Divisive Clustering
- Ward Linkage
- Complete Linkage
- Average Linkage
- Single Linkage
- Dendrogram Analysis

### Density-Based Clustering

- DBSCAN
- HDBSCAN
- OPTICS

### Model-Based Clustering

- Gaussian Mixture Models
- Expectation-Maximisation
- Bayesian Gaussian Mixture Models

### Graph and Spectral Methods

- Spectral Clustering
- Community Detection
- Similarity-Graph Clustering

### Advanced and Specialised Methods

- BIRCH
- Mean Shift
- Affinity Propagation
- Fuzzy C-Means
- Self-Organising Maps
- Deep Embedded Clustering
- Autoencoder-Based Clustering

## Supporting Techniques

Projects may also include:

- feature scaling and transformation,
- outlier treatment,
- Principal Component Analysis,
- t-SNE and UMAP visualisation,
- distance and similarity measures,
- cluster profiling,
- business interpretation,
- comparison of multiple clustering solutions.

## Cluster Evaluation

Where appropriate, clustering solutions are evaluated using:

- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Score
- Inertia
- Elbow Method
- Dendrogram inspection
- Stability analysis
- Business interpretability

## Current Projects

### E-Commerce Customer Segmentation

**Location:** `ecommerce_customer_segmentation/`

Customer-level segmentation using two complementary K-Means approaches:

1. Quantity and Spending Segmentation
2. RFM Customer Segmentation

The project includes transaction cleaning, customer-level feature engineering, outlier treatment, scaling, clustering diagnostics, PCA visualisation, cluster profiling and business interpretation.

## Folder Structure

```text
clustering/
├── README.md
├── ecommerce_customer_segmentation/
│   ├── README.md
│   ├── ecommerce_customer_segmentation.ipynb
│   └── requirements.txt
└── future_clustering_project/
```

## Project Standards

Each clustering case study aims to include:

- a clearly defined analytical or business problem,
- justified feature selection,
- appropriate preprocessing,
- comparison of clustering methods where useful,
- cluster validation,
- visual interpretation,
- cluster profiling,
- practical conclusions.

## Technologies

- Python
- pandas
- NumPy
- SciPy
- scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

Additional libraries such as `hdbscan`, `umap-learn`, `scikit-fuzzy` or deep-learning frameworks may be used in more advanced projects.

## Purpose

The objective is not only to apply clustering algorithms, but also to understand when different methods are appropriate and how unsupervised-learning outputs can be translated into meaningful analytical or business insights.
