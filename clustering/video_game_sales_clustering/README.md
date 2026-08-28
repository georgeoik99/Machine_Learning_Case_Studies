# Modern Video Game Sales and Market-Profile Clustering

An academic clustering study of video-game sales, genres, platforms, release periods and geographic markets from **1995 to 2024**.

## Project Story

This project revisits an academic study completed in 2020. It was my first practical exposure to machine learning and the project that motivated me to pursue Data Science.

The original intuition remains central:

> Video-game sales are connected to genre, platform, release period and geographic market.

The modern implementation describes **games, catalogue segments and market profiles**, rather than claiming to identify individual types of gamers.

## Research Questions

- Which market profiles emerge from reported regional video-game sales?
- How are genre, platform and release period connected?
- Do different clustering methods provide complementary perspectives?
- Which historical interpretations remain supported by the expanded analysis?

## Dataset and Study Period

The project uses the [Video Game Sales 2024 dataset](https://www.kaggle.com/datasets/asaniczka/video-game-sales-2024/data), stored locally at:

```text
E:\data\video_game_sales_2024.csv
```

The original file contains **64,016 records** covering releases from 1971 to 2024. This study focuses on releases from **1995 onward**, marking the transition into the modern 3D-console era.

After excluding releases before 1995 and rows without a valid release date, the working catalogue contains:

- **50,383 games**,
- **20 genres**,
- **66 platforms**,
- release years from **1995 to 2024**.

Available fields include title, platform, genre, publisher, developer, release date, critic score, total sales and reported sales for North America, PAL territories, Japan and other markets.

The dataset is not included in the repository. Update `DATA_PATH` in the notebook if it is stored elsewhere.

## Sales-Data Limitation

The catalogue is much larger than the older dataset, but sales coverage is incomplete:

- 18,487 games have at least one reported regional sales value,
- 12,608 games have reported PAL sales,
- missing sales are retained as unknown and are never automatically treated as zero.

For that reason, each clustering case reports the observations it actually uses.

## Clustering Cases

### Case 1 — K-Means

The first case preserves the central structure of the original study using:

- release year,
- reported PAL sales,
- one-hot encoded genre.

PAL sales are log-transformed, numeric variables are standardised and solutions from `k=2` to `k=10` are evaluated with Silhouette, Davies–Bouldin and Calinski–Harabasz metrics.

The final `k=5` solution is retained for richer interpretation and historical comparability. It is fitted to the **12,608 games with reported PAL sales**.

### Case 2 — X-Means

The second case uses the complete 1995–2024 catalogue and one-hot encoded:

- genre,
- platform.

X-Means starts from two clusters and uses the Bayesian Information Criterion to determine whether additional splits are justified, up to ten clusters.

No sales variable is required, so all **50,383 games** participate. The model reaches the configured upper boundary of ten clusters, indicating a granular genre-platform structure.

### Case 3 — Affinity Propagation

Affinity Propagation is applied to interpretable profiles created from the full catalogue:

```text
Genre × Platform × Release Era
```

Every retained game contributes to its profile's title count. Regional market shares and sales totals use only reported values, and profiles without any regional sales evidence are excluded from this sales-based model.

The features include:

- North American, PAL, Japanese and other-market sales shares,
- catalogue size and reported total sales,
- sales-data coverage,
- average release year,
- average critic score.

The final model identifies ten clusters from **683 sales-supported market profiles**. An Agglomerative Clustering reference model is fitted to the same profiles.

## Key Findings

- K-Means separates five broad release-period, genre and PAL-sales patterns, including a small high-sales segment and larger catalogue groups with lower reported sales.
- X-Means identifies ten genre-platform catalogue segments across all 50,383 dated releases and reaches its configured upper cluster boundary.
- Affinity Propagation identifies ten market-profile clusters, including North America-led, PAL-led and Japan-led structures.
- Affinity Propagation and Agglomerative Clustering show moderate structural agreement (`Adjusted Rand Index = 0.4935`), suggesting that part of the market structure is reproducible across methods.
- Genre, platform, release period and geographic sales composition are connected, but the dataset cannot identify individual gamer demographics or motivations.

## Evaluation and Visualisation

The notebook includes:

- Silhouette score,
- Davies–Bouldin index,
- Calinski–Harabasz score,
- PCA visualisations,
- cluster-size analysis,
- genre and platform profiles,
- regional market-share profiles,
- comparison with Agglomerative Clustering,
- a retrospective review of the original hypotheses.

Metrics from models trained on different feature spaces are presented as internal diagnostics and are not treated as directly comparable leaderboard scores.

## Repository Structure

```text
video_game_sales_clustering/
├── .gitignore
├── README.md
├── requirements.txt
└── video_game_sales_clustering.ipynb
```

## How to Run

Install the dependencies:

```bash
pip install -r requirements.txt
```

Download the dataset, confirm `DATA_PATH` inside the notebook and run all cells from top to bottom.

## Technologies

- Python
- pandas and NumPy
- scikit-learn
- pyclustering
- Matplotlib and Seaborn
- Jupyter Notebook

## Interpretation Boundary

The available data describe games, platforms and reported market sales. The clusters therefore represent **video-game and market profiles**, not observed demographic groups or individual customer personas.

Historical interpretations concerning audience age, violence preferences or purchase motivation are retained only as exploratory commercial hypotheses that would require demographic data to test.

## Disclaimer

This project is intended for academic and portfolio purposes.
