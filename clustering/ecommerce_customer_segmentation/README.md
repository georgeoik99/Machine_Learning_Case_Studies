# E-Commerce Customer Segmentation

Customer-level segmentation of online retail customers using two complementary K-Means approaches:

1. **Quantity and Spending Segmentation**
2. **RFM Customer Segmentation**

## Project Overview

This project analyses transactional data from a UK-based online retailer and converts individual transactions into customer-level behavioural profiles.

The analysis begins with data-quality checks, transaction cleaning and exploratory analysis. It then applies two different K-Means clustering approaches to examine customers from both a commercial-value and customer-engagement perspective.

## Business Questions

The project addresses the following questions:

- How frequently do customers purchase?
- Which products are returned most often?
- Do order values differ between UK and international customers?
- Which customers purchase the highest quantities and generate the highest spending?
- Which customers are recent, frequent, valuable or potentially at risk?
- How do customer value segments compare with RFM behavioural segments?

## Segmentation Case A — Quantity and Spending

The first case improves the original project idea by creating customer profiles using:

- **Total Quantity Purchased**
- **Total Spending**

The variables are calculated at customer level:

```text
TotalQuantityPurchased = sum(Quantity)

TotalSpent = sum(Quantity × UnitPrice)
```

This approach identifies customers according to their purchasing volume and economic contribution.

## Segmentation Case B — RFM Analysis

The second case uses the established RFM framework:

- **Recency:** Days since the customer's latest purchase
- **Frequency:** Number of unique completed orders
- **Monetary:** Total customer spending

A four-cluster K-Means solution is used to support commercially interpretable customer groups such as:

- Champions
- Loyal Customers
- At Risk
- Low Engagement

Cluster names are assigned after examining the actual Recency, Frequency and Monetary profiles.

## Methodology

The project includes:

- data-quality assessment,
- duplicate and missing-value checks,
- separation of completed sales from returns and cancellations,
- customer purchase-frequency analysis,
- product-return analysis,
- UK versus international order-value comparison,
- Mann–Whitney U testing,
- customer-level feature engineering,
- log transformation and standardisation,
- 99th-percentile outlier capping for RFM variables,
- K-Means clustering,
- elbow and silhouette diagnostics,
- PCA visualisation,
- cluster profiling,
- comparison between value and RFM segments,
- business interpretation and recommended actions.

## Why Two Segmentation Approaches?

The two cases answer different business questions.

| Case | Variables | Main Purpose |
|---|---|---|
| Quantity and Spending | Total quantity, total spending | Identify customer value and purchase-volume tiers |
| RFM | Recency, frequency, monetary value | Identify engagement, loyalty and customer-lifecycle behaviour |

The approaches are complementary.

A customer may generate high historical spending but still be classified as **At Risk** if they have not purchased recently.

## Repository Structure

```text
Machine_Learning_Case_Studies/
└── clustering/
    └── ecommerce_customer_segmentation/
        ├── ecommerce_customer_segmentation.ipynb
        ├── README.md
        └── requirements.txt
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/georgeoik99/Machine_Learning_Case_Studies.git
cd Machine_Learning_Case_Studies/clustering/ecommerce_customer_segmentation
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Update `DATA_PATH` inside the notebook and run all cells from top to bottom.

The notebook uses the first `25,000` rows by default:

```python
NROWS = 25_000
```

To analyse the complete dataset:

```python
NROWS = None
```

## Technologies

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- scikit-learn
- Jupyter Notebook

## Key Takeaway

The project demonstrates how raw transactional data can be transformed into actionable customer segments.

The first model captures **commercial value**, while the second captures **customer engagement and lifecycle behaviour**.

## Disclaimer

This project is intended for educational and portfolio purposes.
