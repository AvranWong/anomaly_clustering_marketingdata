# Anomaly detection and clustering patterns with marketing data
Unsupervised learning is a essential component in machine learning. In this notebook, we will be implementing various Anomaly detection and clustering knowledge to find the relationship between income level and total spending. 

The original dataset can be found on kaggle here: https://www.kaggle.com/jackdaoud/marketing-data
## Supervised vs Unsupervised learning
The main difference between supervised and unsupervised learning is that supervised learning uses labeled datasets to "train" or supervised algorithms to predict outcomes accurately. The main two types of problems supervised learning tackles is classification and regression

Unsupervised learning on the other hand uses machine learning algorithms to label and cluster unlabelled datasets. We will be using unsupervised learning to tackle clustering.

# Anomaly detection algorithms
We will be using Nearest Neighbors and isolation forest from scikit.learn to identify anomalies in this notebook

#### Nearest Neighbors
The concept behind nearest neighbours is to find a predetermined number of samples closest to a point, and label them.

In this case we will be using nearest neighbours to identify outliers in order to remove them from the data set. The predetermined number of neighbors will be estimated at 10, and the fraction of Anomalies with respect to the total data will be 2%

#### Isolation forest
Isolation forest, similar to nearest neighbors, can be used to detect anomalies in a dataset. It identifies anomalies by isolating outliers in the data.

Isolation forest repeatedly generates partitions and then randomly selecting split values for the feature, creating a tree. The anomalies will be the points that have a shorter path to the tree

# Clustering algorithms
These are the algorithms we will be implementing in this notebook
#### K means clustering
K means clustering goes through these following steps
1. Choose the number of clusters K
2. Select K number of points randomly as centroids
3. Assign all points to the cluster centroid by comparing distances away from the centroid
4. Calculate the "total distance" away from the centroid
5. Repeat steps 3 and 4 until the total distance from the centroid is minimized.

We will be using the "elbow plot" method to determine K

#### Hierachical Clustering
Hierachical clustering goes through these following steps
1. Identify each point as an individual cluster
2. Identify two closest clusters 
3. Merge them together
4. Repeat steps 2-3 until only one big cluster is left
5. The main difference between hierachical clustering and K means clustering is that hierachical clustering starts with individual points and clusters them into one, while K means starts with the whole dataset and splits them off.

We will be using the dendogram to determine a good number of clusters.
