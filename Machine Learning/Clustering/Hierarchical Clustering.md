- Clustering based on similarities or distances
- Produces nested clusters
- Agglomerative: Start with the points as individual clusters and, at each step, merge the closest pair of clusters.
- Divisive: Start with one, all-inclusive cluster and, at each step, split a cluster until only singleton clusters of individual points remain.
- A hierarchical clustering is displayed graphically using a tree-like diagram called a dendrogram

- Strengths:
	- Do not have to assume any particular number of clusters – Any desired number of clusters can be obtained by `cutting` dendrogram at proper level
	- Produces dendrograms: visually representation of structure of data
	- Works well with small datasets
	- Works well with small datasets

- Weaknesses:
	- Scalability Issues: 
		- Computationally expensive on large datasets
	- Memory Intensive: 
		- Needs to store all pairwise distances at each step
	- Sensitive to noise/outliers: 
		- Can form additional clusters

![[Pasted image 20240916111316.png]]
