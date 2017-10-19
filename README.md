# hierarchical-clustering
This is python implementation of hierarchical clustering

## what is hierarchical clustering?
It is a clustering algorithm, which clusters the datapoints in group.

## Hierarchical algorithm:
1. Start by assigning each item to its own cluster, so that if you have N items, you now have N clusters, each containing just one item. 
2. Find the closest pair of clusters and merge them into a single cluster, so that now you have one less cluster.
3. Compute distances between the new cluster and each of the old clusters.
4. Repeat steps 2 and 3 until all items are clustered into a single cluster of size N.


