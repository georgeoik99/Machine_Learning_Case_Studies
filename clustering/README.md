# E-Commerce Customer Segmentation

Customer behaviour analysis and RFM-based segmentation using Python and K-Means.

## Project Overview

This project analyses transactional data from a UK-based online retailer. It combines exploratory analysis with customer-level segmentation to identify behavioural differences across the customer base.

## Business Questions

- How frequently do customers purchase?
- Which products are returned most often?
- Do order values differ between UK and international customers?
- Which customer segments emerge from recency, frequency and monetary behaviour?

## Methodology

The project includes:

- data-quality assessment and transaction cleaning,
- customer purchase and returns analysis,
- invoice-level UK versus international order comparison,
- Mann–Whitney U testing,
- RFM feature engineering,
- log transformation and standardisation,
- K-Means clustering,
- elbow and silhouette diagnostics,
- PCA visualisation,
- cluster profiling and business recommendations.

## Repository Contents

```text
Python_customer_segmentation/
├── ecommerce_customer_segmentation.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

1. Clone or download the repository.
2. Update `DATA_PATH` in the notebook.
3. Install the dependencies:

```bash
pip install -r requirements.txt
```

4. Run the notebook from top to bottom.

The notebook uses the first `25,000` rows by default. Set `NROWS = None` to analyse the full dataset.

## Technologies

Python, pandas, NumPy, Matplotlib, Seaborn, SciPy and scikit-learn.

## Disclaimer

This project is intended for educational and portfolio purposes.
