- Instead of fixing bin width, h, and counting number of instances; fix k and find k nearest instances
- For each x, $d_{1}(x) \le d_{2}(x) \le \dots \le d_{N}(x)$
- k-NN Density estimate:
$$\hat{p}(x) = \frac{k}{2Nd_{k}(x)}$$,$d_{k}(x) \to$ distance to the k<sup>th</sup> closest instance to x


![[Pasted image 20240917225846.png]]


## Example - 

- $$X={151,154,157,159,162,165,167,170,173,175,178,180}$$
	- $$X_{0} = 150,\  k= 5$$
	- estimate density at $x=160$

### Step 1: Define the Formula

The formula for the k-NN density estimator is:
$$\hat{p}(x) = \frac{k}{N*V_{k}(x)}$$
- $N$ is the total number of data points,
- $k$ is the number of nearest neighbors to consider,
- $V_k(x)$is the volume of the smallest region (or ball) that contains the $k$-nearest neighbors of the point $x$.


### Step 2: Define the Data

We are given the data points:

$$X=\{151,154,157,159,162,165,167,170,173,175,178,180\}$$

- $N=12$ (the number of data points),
- We are estimating the density at $x=160$,
- We will use $k=3$ (considering 3 nearest neighbors).

### Step 3: Compute the Distances to $x=160$

We will calculate the absolute distances between $x=160$ and each point in the dataset $X$.

$$|160-151| = 9$$
$$|160-154| = 6$$
$$|160-157| = 3$$
$$|160-159| = 1$$
$$|160-162| = 2$$
$$|160-165| = 5$$
$$|160-167| = 7$$
$$|160-170| = 10$$
$$|160-173| = 13$$
$$|160-175| = 15$$
$$|160-178| = 18$$
$$|160-180| = 20$$
### Step 4: Sort the Distances

We now sort the distances in ascending order:

$$1, 2, 3, 5, 6, 7, 9, 10, 13, 15, 18, 20$$

The $k=3$-th nearest neighbor distance is 3.

### Step 5: Calculate the Volume $V_k(x)$

In 1D, the volume is simply the distance to the $k$-th nearest neighbor. Therefore, the volume $V_k(x)$ is:

$$V_{k}(x) = 2 * d_{k}(x) = 2*3 = 6$$
The factor of 2 is because the distance encompasses both sides of $x=160$ (left and right).


### Step 6: Apply the k-NN Density Estimator Formula

Now, we can plug in the values into the k-NN formula:
$$\hat{p}(160) = \frac{k}{N*V_{k}(x)} = \frac{3}{12*6} = \frac{3}{72} = \frac{1}{24} = 0.04167$$


---
## Example - 

- Classify a new point $x=(4,4)$ for $k=3$

| Point | X   | Y   | Class |
| ----- | --- | --- | ----- |
| P1    | 1   | 1   | A     |
| P2    | 2   | 2   | A     |
| P3    | 3   | 3   | A     |
| P4    | 6   | 6   | B     |
| P5    | 7   | 7   | B     |
| P6    | 8   | 8   | B     |

The **k-Nearest Neighbour Estimator (k-NN)** is a non-parametric method used for both classification and regression. The formula for estimating the density at a point xxx using k-NN is:

$$\hat{p}(x) = \frac{k}{N*V_{k}(x)}$$
- $N$ is the total number of data points,
- $k$ is the number of nearest neighbors to consider,
- $V_k(x)$is the volume of the smallest region (or ball) that contains the $k$-nearest neighbors of the point $x$.

#### Data Given:

The new point to classify is x=(4,4)x = (4, 4)x=(4,4), and the value of k=3k = 3k=3. The table shows the coordinates of points with their classes


| Point | X   | Y   | Class |
| ----- | --- | --- | ----- |
| P1    | 1   | 1   | A     |
| P2    | 2   | 2   | A     |
| P3    | 3   | 3   | A     |
| P4    | 6   | 6   | B     |
| P5    | 7   | 7   | B     |
| P6    | 8   | 8   | B     |
We will use the **Euclidean distance** to find the distances between the point $(4,4)$ and each of the points $P1$ to $P6$, and then classify $(4,4)$ based on the closest 3 points.

#### Step 1: Calculate the Distances

Using the Euclidean distance formula:
$$d = \sqrt{ (x_{2} - x_{1})^{2}+ (y_{2} - y_{1})^2 }$$

**Distance from $(4,4)$ to $P_{1}(1,1)$**:
$$d = \sqrt{ (4-1)^{2 }+ (4-1)^{2}}= \sqrt{ 9+9 } = \sqrt{ 18 } \approx 4.24$$

**Distance from $(4,4)$ to $P_{2}(2,2)$**:
$$d = \sqrt{ (4-2)^{2 }+ (4-2)^{2}}= \sqrt{ 4+4 } = \sqrt{ 8 } \approx 2.83$$

**Distance from $(4,4)$ to $P_{3}(3,3)$**:
$$d = \sqrt{ (4-3)^{2 }+ (4-3)^{2}}= \sqrt{ 1+1 } = \sqrt{ 2 } \approx 1.41$$

**Distance from $(4,4)$ to $P_{4}(6,6)$**:
$$d = \sqrt{ (4-6)^{2 }+ (4-6)^{2}}= \sqrt{ 4+4 } = \sqrt{ 8 } \approx 2.83$$

**Distance from $(4,4)$ to $P_{5}(7,7)$**:
$$d = \sqrt{ (4-3)^{2 }+ (4-3)^{2}}= \sqrt{ 9+9 } = \sqrt{ 18 } \approx 4.24$$

**Distance from $(4,4)$ to $P_{6}(8,8)$**:
$$d = \sqrt{ (4-8)^{2 }+ (4-8)^{2}}= \sqrt{ 16+16 } = \sqrt{ 32 } \approx 5.66$$

#### Step 2: Find the 3 Nearest Neighbors

Now, we select the three closest points to $(4,4)$:


| Point | Distance | Class |
| ----- | -------- | ----- |
| P3    | 1.41     | A     |
| P2    | 2.83     | A     |
| P4    | 2.83     | B     |

#### Step 3: Classify the Point

Among the 3 nearest neighbors, we have:

- 2 points from class **A**,
- 1 point from class **B**.

Since class **A** is in the majority, the new point $(4,4)$ is classified as **A**.