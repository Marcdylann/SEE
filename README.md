# Sessa Empirical Estimator (SEE) Clustering Analysis

This project implements the Sessa Empirical Estimator (SEE) to analyze prescription refill patterns using clustering techniques. The assignment compares the traditional K-Means clustering with an alternative approach, DBSCAN, to identify patterns and potential outliers.

---

## Project Overview

This project covers the following tasks:
1. **Data Preparation:** Simulated prescription data representing patient refill intervals.
2. **SEE with K-Means:** Original implementation of the Sessa Empirical Estimator using K-Means clustering.
3. **SEE with DBSCAN:** Alternative clustering approach using DBSCAN for flexible cluster detection and outlier identification.
4. **Comparison:** Evaluation of cluster quality, refill patterns, and outliers between K-Means and DBSCAN.
5. **Insights:** Key findings from the clustering results, highlighting adherence behaviors and potential irregularities.

---

## File Structure

- `SEE_Clustering_Analysis_KMeans_vs_DBSCAN.ipynb` — Jupyter Notebook with the full analysis and code.
- `synthetic_data.csv` (optional) — Simulated dataset used for clustering.
- `README.md` — Project documentation (this file).
- `outputs/` (optional) — Visualizations generated during the analysis.

---

## Methodology

1. **Data Simulation:**
   - Generated synthetic patient prescription data.
   - Calculated refill intervals between prescriptions.
   - Filtered extreme values using an empirical CDF cutoff.

2. **Clustering Approaches:**
   - **K-Means:** Fixed cluster count, grouping patients based on refill patterns.
   - **DBSCAN:** Density-based clustering, automatically detecting outliers and varying cluster shapes.

3. **Evaluation Metrics:**
   - Cluster counts, silhouette scores, median refill intervals, and visual inspection.

---

## Key Findings

1. **K-Means Results:**
   - Formed 2 main clusters (e.g., 14-day and 29-day refill intervals).
   - No outlier detection; all points assigned to clusters.

2. **DBSCAN Results:**
   - Identified 2 clusters and flagged several outliers (`cluster_id = -1`).
   - Outliers represented irregular refill behaviors that K-Means missed.
   - Silhouette score was higher for DBSCAN, indicating better-defined clusters.

---

## Visualizations

Key plots generated during the analysis include:
- **Histogram:** Refill interval distribution by cluster.
- **Boxplot:** Cluster-wise refill interval spread.
- **Time-Series Plot:** Refill patterns for selected patients.

---

## AI Assistance

AI assistance was used for code generation, troubleshooting, and refining the analysis approach. Prompts included:
- Implementing DBSCAN as an alternative to K-Means.
- Visualizing cluster results with histograms and boxplots.
- Comparing clustering outcomes and generating insights.

---

## How to Run

1. Ensure you have Python and Jupyter Notebook installed.
2. Install required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
