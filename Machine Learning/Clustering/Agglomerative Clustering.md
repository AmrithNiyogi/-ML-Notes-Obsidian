- Most popular hierarchical clustering technique
- Start with individual points as clusters, successively merge the two closest clusters until only one cluster remains.
- Algorithm - 
	1. Compute the proximity matrix, if necessary.
	2. repeat
		1. merge the closest two clusters
		2. Update the proximity matrix to reflect the proximity between the new cluster and the original clusters.
	3. until only one cluster remains
- Key operation is the computation of the proximity of two clusters
	- Different approaches defining the distance between clusters distinguish the different algorithms