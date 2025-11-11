Clustering Countries for Strategic Aid Allocation – HELP International
Project Overview

HELP International, a humanitarian NGO, has raised approximately $10 million to provide aid to countries in need. The CEO requires a data-driven method to identify countries most in urgent need of support based on socio-economic and health factors. The objective of this project is to categorize countries into clusters to guide strategic and effective allocation of aid.

Dataset

The dataset is sourced from Kaggle
 and contains socio-economic and health indicators for 167 countries, including:

child_mort – Child mortality rate

exports – Exports as % of GDP

health – Health expenditure

imports – Imports as % of GDP

income – GDP per capita

inflation – Inflation rate

life_expec – Life expectancy

total_fer – Total fertility rate

gdpp – GDP per capita

The country column identifies each country.

Note: Users should download the dataset from Kaggle and place it in the project directory as countries_data.csv (or the appropriate file name).

Problem Solving Approach
1. Data Inspection and Cleaning

Checked for missing values, data types, and summary statistics.

Ensured all numeric features were ready for clustering.

2. Feature Selection

Dropped non-numeric columns (country).

All 9 numeric features were retained for clustering since the dataset was small, and all features were relevant for socio-economic and health profiling.

3. Standardization

Applied StandardScaler to normalize features for clustering and PCA visualization.

4. Clustering

Used KMeans clustering to categorize countries.

Evaluated cluster quality using inertia (elbow method) and silhouette scores.

Found that 4 clusters provided the best balance between cohesion and separation.

5. Cluster Assignment

Added a cluster column to the DataFrame to indicate each country’s cluster.

Computed cluster-wise average values to understand each group’s characteristics.

6. Visualization

Plotted inertia vs number of clusters (elbow plot) and silhouette scores to determine optimal clusters.

Used PCA to reduce the data to 2 dimensions and visualize cluster separation in a scatter plot.

Created grouped bar charts of standardized feature means per cluster.

Key Findings

Cluster 2 & 3: Low-income countries with high child mortality and fertility; low life expectancy → highest priority for aid.

Cluster 0: Medium-income countries with moderate health outcomes → medium priority.

Cluster 1: High-income, well-developed countries → low priority for aid.

Conclusion

The clustering analysis provides a data-driven strategy for HELP International to allocate resources efficiently: focus on Clusters 2 and 3 for urgent aid, target Cluster 0 for preventive programs, and minimize resources in Cluster 1.
