# Clustering Analysis of Patient Data

## Overview

This project conducts a comprehensive clustering analysis on a dataset containing patient medical history features to identify distinct patient groups based on their health characteristics. Various clustering algorithms are evaluated, including K-means, Gaussian Mixture Models (GMM), Hierarchical Clustering, and DBSCAN. The performance of each algorithm is assessed using Silhouette Score and Davies-Bouldin Index.

## Dataset [here](https://archive.ics.uci.edu/dataset/45/heart+disease)

- The dataset used in this analysis includes numerical features representing various medical metrics of patients.
- Data preprocessing steps include handling missing values, feature scaling, and selecting relevant features for clustering.

## Clustering Algorithms Used

1. **K-means**: A centroid-based algorithm that partitions data into a specified number of clusters.
2. **Gaussian Mixture Models (GMM)**: A probabilistic model that assumes data points are generated from a mixture of several Gaussian distributions.
3. **Hierarchical Clustering**: A method that seeks to build a hierarchy of clusters, allowing for a more intuitive understanding of data relationships.
4. **DBSCAN**: A density-based algorithm that groups together points that are closely packed while marking points in low-density regions as outliers.

## Evaluation Metrics

- **Silhouette Score**: Measures how similar an object is to its own cluster compared to other clusters. Scores range from -1 to 1, with higher values indicating better-defined clusters.
- **Davies-Bouldin Index**: Measures the average similarity ratio of each cluster with its most similar cluster. Lower values indicate better clustering.

## Results

| Algorithm     | Silhouette Score | Davies-Bouldin Index |
|---------------|------------------|-----------------------|
| K-means       | 0.1908           | 1.9366                |
| GMM           | 0.2084           | 1.7343                |
| Hierarchical  | 0.2247           | 1.5884                |
| DBSCAN        | -1.0000          | ∞                     |

### Conclusion

- **Best Algorithm**: Hierarchical Clustering outperformed other methods, showing the highest Silhouette Score and the lowest Davies-Bouldin Index.
- GMM and K-means produced less distinct clusters, while DBSCAN did not successfully identify valid clusters.

## Future Work

- Further analysis of the clusters from Hierarchical Clustering to understand patient characteristics.
- Exploration of additional clustering algorithms or parameter tuning for GMM and K-means to improve their performance.
- Visualization of clusters to gain deeper insights into the relationships among data points.

## Requirements

- Python 3.x
- Libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`

## Usage

To run the analysis, clone this repository and execute the provided Python scripts in your preferred environment.

```bash
git clone <https://github.com/DavidkingMazimpaka/heart-disease-analysis>
cd <heart-disease-analysis>
python heart-disease_analysis.ipynb
