# Prostate Cancer Clustering

This case study applies:

- hierarchical clustering with compatible distance/linkage combinations;
- reproducible K-means with multiple random starts;
- model-based clustering;
- principal component analysis;
- silhouette and gap-statistic evaluation;
- ARI and NMI comparisons between solutions and with the withheld diagnosis.

Continuous measurements are preserved. Potential outliers are not replaced with means; their influence is examined through a standard-versus-robust-scaling sensitivity analysis.

View the [rendered analysis](prostate_cancer_clustering.md) on GitHub. To edit or rerun it, open `prostate_cancer_clustering.qmd` in RStudio and use **Run All**. The dataset is stored locally at `data/prostate_cancer.csv`.

The analysis is written in R with Quarto. Its main packages are `dplyr`, `ggplot2`, `cluster`, `factoextra`, `mclust`, and `reshape2`.

The cluster summaries are descriptive and do not imply clinical aggressiveness or prognosis.
