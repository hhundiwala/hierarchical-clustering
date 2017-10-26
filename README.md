# hierarchical-clustering
This is python implementation of hierarchical clustering. This implementation use dynamic programming approach(memorization).

### what is hierarchical clustering?
It is a clustering algorithm, which clusters the datapoints in group. This algorithm follows aglomerative approach i.e. it starts with each datapoint as cluster and goes on merging the clusters based on similarity.

### Hierarchical algorithm:
1. Start by assigning each item to its own cluster, so that if you have N items, you now have N clusters, each containing just one item. 
2. Find the closest pair of clusters and merge them into a single cluster, so that now you have one less cluster.
3. Compute distances between the new cluster and each of the old clusters.
4. Repeat steps 2 and 3 until all items are clustered into a single cluster of size N.

Complexity of algorithm: O(n^3)

### Linkages:
Linkages are the distances(distance is directly proportional to similarity) between clusters. As stated in above algorithm, we go on merging the 2 nearest clusters. But the problem here is how to find the distance between 2 clusters?

There are multiple ways to find the clusters:
#### Single Linkage:
The distance considered is minimum distance between 2 clusters. Minimum distance between 2 datapoints in 2 clusters.

#### Complete Linkage:
The distance considered is maximum distance between 2 clusters. Maximum distance between 2 datapoints in 2 clusters.

#### Average Linkage:
The distance considered is average of distances between 2 clusters. Average of distances between all the datapoints in 2 clusters.

#### Centroid Linkage:
The distance considered here is, the distance between centroids of two clusters.

### Implementation
We use the concept of dynamic programming (memorisation technique) to achieve better time complexity. We will be maintaining the distance matrix which will maintain the distances between all the datapoints present. Thus, if we have "n" number of datapoints our distance matrix will be of order nxn. This matrix will be symmetric matrix. Since we want to merge the two closest datapoints, we will find the minimum distance and we will merge the 2 clusters updating the clusters distance from all other datapoints. We will reapeat the above step untill all the datapoints are under one cluster.  

For more detailed description of algorithm and code visit: http://www.hhundiwala.com/hie_clust
