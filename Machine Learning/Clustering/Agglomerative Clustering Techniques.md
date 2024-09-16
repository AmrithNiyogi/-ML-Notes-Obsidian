- **MIN (single link clustering)**:
	- proximity between the closest points
	- $$d(G_{i}, G_{j}) = \buildrel min \over {x^{r}\epsilon G_{i}, x^{s}\epsilon G_{j}} \  d(x^{r}, x^{s})$$

- **MAX (complete link clustering: **
	- proximity between the farthest points
	- $$d(G_{i}, G_{j}) = \buildrel max \over {x^{r}\epsilon G_{i}, x^{s}\epsilon G_{j}} \  d(x^{r}, x^{s})$$
	
- **Group Average:**
	- Cluster proximity as the average pairwise proximities of all pair of points from different clusters
	- $$d(G_{i}, G_{j}) = \buildrel ave \over {x^{r}\epsilon G_{i}, x^{s}\epsilon G_{j}} \  d(x^{r}, x^{s})$$