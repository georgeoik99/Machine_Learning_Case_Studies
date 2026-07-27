# NASA Hazardous Asteroid Classification

Academic Python reproduction of a RapidMiner classification workflow for
predicting whether a near-Earth object is potentially hazardous.

## Objective

The project studies whether physical and orbital asteroid characteristics can
be used to classify the binary target `hazardous` with a Decision Tree.

## RapidMiner-to-Python workflow

The notebook reproduces the steps defined in `Nasa_classification.rmp`:

1. Load the NASA asteroid dataset.
2. Retain the first 3,000 observations.
3. Remove duplicate records.
4. Select the five predictors used by the original process.
5. Discretise the numeric variables into five equal-frequency intervals.
6. Create the original 20%/80% data partition.
7. Apply 10-fold cross-validation to the first partition.
8. Train and evaluate a Decision Tree classifier.
9. Examine correlation-based feature relevance and descriptive statistics.

## Variables

| Variable | Description |
|---|---|
| `absolute_magnitude` | Intrinsic brightness of the object |
| `est_diameter_min` | Estimated minimum diameter |
| `est_diameter_max` | Estimated maximum diameter |
| `relative_velocity` | Relative velocity of the object |
| `miss_distance` | Estimated miss distance |
| `hazardous` | Binary classification target |

## Methodological note

RapidMiner uses the **gain ratio** criterion. Scikit-learn does not implement
gain ratio directly, so the notebook uses an entropy-based Decision Tree as the
closest standard Python equivalent.

The original process sends the 20% partition into 10-fold cross-validation.
This choice is retained so the notebook remains faithful to the submitted
RapidMiner workflow.

## Files

```text
nasa_hazardous_asteroid_classification/
├── .gitignore
├── nasa_hazardous_asteroid_classification.ipynb
├── README.md
└── requirements.txt
```

## Run

Install the dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook, update `DATA_PATH` if necessary, and run the cells from top
to bottom.

## Technologies

Python, pandas, NumPy, Matplotlib, Seaborn and scikit-learn.

## Disclaimer

This is an academic and portfolio project derived from an original RapidMiner
process. It is not intended for operational asteroid-risk assessment.
