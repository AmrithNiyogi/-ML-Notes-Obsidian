- Local Search procedure: 
	- final k centroid depend on initial k centroids
- Various ways to select initial centroids:
	- Take randomly selected k instances
	- Take mean of all data points and add k small random vectors to get k initial centroids
	- Calculate PC, divide its range into k equal intervals which divides data into k groups, take mean of each group to get k initial centroids
- Closeness between data points in one cluster can be measured by Euclidean distance, cosine similarity, etc.
- SSE(Sum of squared error): 
	- Calculates total error in a clustering solution
	- For each point, Error is the distance between data point and the centroid of its cluster
	- $$SSE = \sum_{i=1}^{K}\sum_{x \epsilon C_{i}} ||x-m_{i}||^{2}$$
	- For given multiple sets of clusters, select the one with minimum SSE.

- Pros:
	- Simple and Efficient: 
		- Easy and fast
	- Scalable: 
		- can handle large datasets
	- Works well with Spherical non-overlapping clusters
	- Guaranteed Convergence: 
		- converges to local minimum; finite number of iterations
	- Intuitive Results: 
		- Easy to interpret results

- Cons:
	- Sensitive to Initialization: 
		- Dependence on initial centroids; may converge to local minimum that is not globally optimal 
	- Fixed number of clusters: 
		- Need to specify k in advance which can be challenging if the true number of clusters is not known
	- Difficult to determine optimal k: 
		- Need additional techniques like elbow method 
	- Assumes spherical clusters: 
		- not suitable for clusters forming non-spherical shapes
	- Sensitive to outliers/noise, can lead to incorrect assignments and cluster centroids can be pulled towards outliers.