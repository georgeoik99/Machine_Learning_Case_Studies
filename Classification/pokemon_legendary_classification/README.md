# Pokémon Legendary Classification

Academic Python reproduction and completion of a RapidMiner workflow for
predicting whether a Pokémon is Legendary.

## Objective

The project investigates whether a Pokémon's type and battle statistics can
distinguish Legendary from non-Legendary Pokémon using a Decision Tree.

## RapidMiner-to-Python workflow

The notebook follows the original `Pokemon prediction.rmp` process:

1. Load the Pokémon dataset.
2. Select the original seven predictors and target.
3. Replace missing secondary types.
4. Define `Legendary` as the classification target (`Rank` in RapidMiner).
5. Split the observations into 80% training and 20% testing data.
6. Apply 10-fold cross-validation to the training partition.
7. Train a Decision Tree using information gain.
8. Evaluate predictions with classification metrics.

The Python version also evaluates the final model on the 20% holdout partition.
The RapidMiner XML creates this partition but does not connect it to an
evaluation operator.

## Variables

| Python variable | RapidMiner name | Role |
|---|---|---|
| `Type 1` | First type | Predictor |
| `Type 2` | Secondary type | Predictor |
| `Total` | Total strenght | Predictor |
| `HP` | Health points | Predictor |
| `Sp. Atk` | Special Attack strenght | Predictor |
| `Sp. Def` | Special defence resistance | Predictor |
| `Speed` | Speed | Predictor |
| `Legendary` | Rank | Target |

## Files

```text
pokemon_legendary_classification/
├── .gitignore
├── pokemon_legendary_classification.ipynb
├── README.md
└── requirements.txt
```

## Run

Install the dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook, update `DATA_PATH` if required, and run all cells.

## Methodological notes

- Duplicate records are removed because the supplied CSV contains repeated
  copies of the same 800 Pokémon observations.
- Missing secondary types are handled inside the modelling pipeline.
- Categorical variables are one-hot encoded.
- Cross-validation is performed only on the training partition.
- The untouched 20% partition provides the final out-of-sample evaluation.
- The displayed tree is limited to its first three levels for readability.

## Technologies

Python, pandas, Matplotlib, Seaborn and scikit-learn.

## Disclaimer

This project is intended for academic and portfolio purposes.
