# CryptoClustering

# Cryptocurrency Market Data Clustering

## Overview

This project involves analyzing and clustering cryptocurrency market data using K-Means clustering and Principal Component Analysis (PCA). The goal is to identify distinct groups of cryptocurrencies based on their price change characteristics over various periods.

## Data

The dataset used for this analysis is a CSV file containing market data for various cryptocurrencies. The data includes the following features:

-   `price_change_percentage_24h`
-   `price_change_percentage_7d`
-   `price_change_percentage_14d`
-   `price_change_percentage_30d`
-   `price_change_percentage_60d`
-   `price_change_percentage_200d`
-   `price_change_percentage_1y`

The `coin_id` column serves as the unique identifier for each cryptocurrency.

## Analysis

### Data Scaling

The features of the dataset are scaled using `StandardScaler` to normalize the data. This ensures that each feature contributes equally to the clustering process.

### K-Means Clustering

K-Means clustering is applied to the scaled data to identify groups of similar cryptocurrencies. The optimal number of clusters is determined using the Elbow method, which helps in visualizing the inertia values for different numbers of clusters.

### Principal Component Analysis (PCA)

Using PCA, we managed to explain 89.5% of the data and effectively reduced the multi-dimensional data to 2D. This dimensionality reduction enhances the clarity of cluster relationships:

-   **Enhanced Clarity**: PCA provides a clearer image of the clusters, making it easier to differentiate between them.
-   **Correlation Insight**: The PCA plot reveals correlations between samples that are more apparent compared to the original high-dimensional data. For instance, clusters that seem to correlate without PCA are more distinguishable with PCA. Specifically, cluster 2, which seemed to correlate with cluster 1, shows clearer separation in the PCA plot.

### Visualization

Various visualizations, including scatter plots and PCA plots, are used to present the clustering results and analyze the relationships between different clusters.

## Skills Used

-   **Data Manipulation and Analysis**: `pandas`
-   **Data Visualization**: `hvplot.pandas`
-   **Data Scaling**: `StandardScaler` from `sklearn.preprocessing`
-   **Clustering**: `KMeans` from `sklearn.cluster`
-   **Dimensionality Reduction**: `PCA` from `sklearn.decomposition`
-   **Plotting and Interpretation**: Interactive plots using `hvplot`