- Local Search Procedure: final k centroids depend on initial k centriods
- Various ways to select initial centroids
	- Take randomly selected k instances
	- take mean of all data points and add k small random vectors to get k initial centroids
	- Calculate PC, divide 
- Closeness between data points in one cluster can be measured by Euclidean distance, cosine similarity, etc.

- SSE(Sum of Squared Error): Calculate total error in a clustering solution
	- For each point, error is the distance between data point and the centroid of its cluster
	- $$SSE = \sum^{K}_{i=1} \sum_{x \epsilon C_{i}} ||x-m_{i}||^2$$
	- For given multiple sets of clusters, select the one with minimum SSE.