### Wholesale Customer Clustering and PCA Analysis
## Overview
This project focuses on applying unsupervised learning techniques to a wholesale dataset. The dataset contains attributes such as Fresh, Milk, Grocery, Frozen, Detergents_Paper, and Delicassen to model and analyze customer purchasing behavior. The main objective is to identify distinct customer segments (clusters) and reduce the complexity of the data using Principal Component Analysis (PCA).

## Exploratory Data Analysis (EDA)
During the initial Exploratory Data Analysis (EDA), the following steps were performed:

* Data Cleaning: 
The dataset was checked for missing values, duplicates, and erroneous entries.
* Correlation Analysis:
 The correlation matrix was computed to find relationships between variables, highlighting features that are correlated with each other.
* Outlier Detection: 
Outliers were identified in the data using the Interquartile Range (IQR) method.

## Unsupervised Learning Techniques
# K-means Clustering
K-means clustering was applied to group customers into clusters based on their purchasing patterns. The optimal number of clusters was determined using the Elbow Method.SS

The dataset was scaled to ensure that features with different units (e.g., Fresh vs. Milk) do not disproportionately influence the clustering process.
The model was trained using the chosen number of clusters (3 clusters in this case).
# Hierarchical Clustering
Hierarchical Clustering was also applied to create a dendrogram to visualize the hierarchical relationships between customers. This method does not require specifying the number of clusters upfront, allowing us to explore different levels of clustering.

Ward's linkage method was used, which minimizes the variance within clusters at each step.
The optimal number of clusters was determined by cutting the dendrogram at a specific height.
# Principal Component Analysis (PCA)
PCA was used to reduce the dimensionality of the dataset. By transforming the data into a set of principal components, PCA helps capture the most important variance in the data while reducing its complexity.

The first three principal components captured the most variance in the dataset.
The resulting principal components were used for further analysis and visualization.

## Results and Findings
# Customer Segmentation:

The K-means clustering model grouped customers into 3 clusters, each representing a distinct purchasing behavior pattern.
Hierarchical clustering further supported this segmentation, showing the relationships between clusters at different levels.
Principal Component Analysis (PCA):

The first three principal components captured most of the variance in the data, enabling us to reduce the complexity of the dataset.
'Milk' and 'Grocery' contributed significantly to the first component, while 'Frozen' and 'Delicassen' were important in the second component. The third component showed interactions between 'Fresh' and 'Frozen' items.
Outliers:

Some outliers were detected in features like 'Milk' and 'Frozen' during the EDA, but further analysis would be required to decide if they should be removed or investigated further.
## Future Considerations
Outlier Investigation:

A deeper investigation into the identified outliers can help understand whether they represent genuine anomalies or if they can be removed for better model performance.
Data Enrichment:

Gathering more data from different customers and regions would help improve the accuracy of the clusters and make the model more robust.