
| Point | x   | y   |
| ----- | --- | --- |
| A     | 1   | 2   |
| B     | 2   | 3   |
| C     | 3   | 3   |
| D     | 5   | 4   |
| E     | 6   | 1   |


## Step 1: Compute the proximity matrix (euclidean distance)

The Euclidean distance dijd_{ij}dij​ between two points iii and jjj is calculated using the formula:

$$d_{ij} = \sqrt{(x_i - x_j)^2 + (y_i - y_j)^2}$$

| Points | Calculation                    | Distance (d) |
| :----: | ------------------------------ | ------------ |
|  A-B   | $\sqrt{(1 - 2)^2 + (2 - 3)^2}$ | 1.41         |
|  A-C   | $\sqrt{(1 - 3)^2 + (2 - 3)^2}$ | 2.24         |
|  A-D   | $\sqrt{(1 - 5)^2 + (2 - 4)^2}$ | 4.47         |
|  A-E   | $\sqrt{(1 - 6)^2 + (2 - 1)^2}$ | 5.10         |

| Points | Calculation                    | Distance (d) |
| :----: | ------------------------------ | ------------ |
|  B-C   | $\sqrt{(2 - 3)^2 + (3 - 3)^2}$ | 1.00         |
|  B-D   | $\sqrt{(2 - 5)^2 + (3 - 4)^2}$ | 3.16         |
|  B-E   | $\sqrt{(2 - 6)^2 + (3 - 1)^2}$ | 4.47         |

| Points | Calculation                    | Distance (d) |
| :----: | ------------------------------ | ------------ |
|  C-D   | $\sqrt{(3 - 5)^2 + (3 - 4)^2}$ | 2.24         |
|  C-E   | $\sqrt{(3 - 6)^2 + (3 - 1)^2}$ | 3.61         |

| Points | Calculation                    | Distance (d) |
| :----: | ------------------------------ | ------------ |
|  D-E   | $\sqrt{(5 - 6)^2 + (4 - 1)^2}$ | 3.16         |

### Proximity Matrix

|       | A    | B    | C    | D    | E    |
| ----- | ---- | ---- | ---- | ---- | ---- |
| **A** | 0    | 1.41 | 2.24 | 4.47 | 5.10 |
| **B** | 1.41 | 0    | 1.00 | 3.16 | 4.47 |
| **C** | 2.24 | 1.00 | 0    | 2.24 | 3.61 |
| **D** | 4.47 | 3.16 | 2.24 | 0    | 3.16 |
| **E** | 5.10 | 4.47 | 3.61 | 3.16 | 0    |

## Step 2: Hierarchical Clustering

| Cluster | Members |
| ------- | ------- |
| A       | A       |
| B       | B       |
| C       | C       |
| D       | D       |
| E       | E       |
### Iteration 1
From the Proximity Matrix, the smallest distance is between **B and C** with a distance of **1.00**.

| Cluster | Members |
| ------- | ------- |
| A       | A       |
| BC      | B, C    |
| D       | D       |
| E       | E       |
### Updated matrix

|        | A    | BC   | D    | E    |
| ------ | ---- | ---- | ---- | ---- |
| **A**  | 0    | 1.41 | 4.47 | 5.10 |
| **BC** | 1.41 | 0    | 2.24 | 3.61 |
| **D**  | 4.47 | 2.24 | 0    | 3.16 |
| **E**  | 5.10 | 3.61 | 3.16 | 0    |
#### How these values are calculated:

- **Distance between A and BC**: Minimum of $d(A,B)=1.41$ and $d(A,C)=2.24$, so $d(A,BC)=1.41$.
- **Distance between BC and D**: Minimum of $d(B,D)=3.16$ and $d(C, D) = 2.24$, so $d(BC,D)=2.24$.
- **Distance between BC and E**: Minimum of $d(B,E)=4.47$ and $d(C,E)=3.61$, so $d(BC,E)=3.61$.


### Iteration 2
From the Proximity Matrix, the smallest distance is between **A and BC** with a distance of **1.41**.

| Cluster | Members |
| ------- | ------- |
| ABC     | A, B, C |
| D       | D       |
| E       | E       |
### Updated matrix

|         | ABC  | D    | E    |
| ------- | ---- | ---- | ---- |
| **ABC** | 0    | 2.24 | 3.61 |
| **D**   | 2.24 | 0    | 3.16 |
| **E**   | 3.61 | 3.16 | 0    |
#### How these values are calculated:

- **Distance between ABC and D**: Minimum of $d(A,D)=4.47$ and $d(B,D)=3.16$, $d(C,D)=2.24$, so $d(ABC, D)=2.24$.
- **Distance between ABC and E**: Minimum of $d(A,E)=5.10$, $d(B,E)=4.47$ and $d(C,ED) = 3.61$, so $d(ABC,E)=3.61$.

### Iteration 3
From the Proximity Matrix, the smallest distance is between **ABC and D** with a distance of **2.24**.

| Cluster | Members    |
| ------- | ---------- |
| ABCD    | A, B, C, D |
| E       | E          |
### Updated matrix

|          | ABCD | E    |
| -------- | ---- | ---- |
| **ABCD** | 0    | 3.16 |
| **E**    | 3.16 | 0    |
#### How these values are calculated:

- **Distance between ABCD and E**: Minimum of $d(A,E)=5.10$ and $d(B,E)=4.47$, $d(C,E)=3.61$, $d(D,E)=3.16$, so $d(ABCD, E)=3.16$.

### Iteration 4
The smallest (and only) remaining distance in the matrix is between **ABCD** and **E**, with a distance of **3.16**. We now merge **ABCD** and **E** into the final cluster **ABCDE**.

| Cluster | Members       |
| ------- | ------------- |
| ABCDE   | A, B, C, D, E |

### Updated matrix

|           | ABCDE |
| --------- | ----- |
| **ABCDE** | 0     |

At this point, all points have been merged into a single cluster **ABCDE**.

## Final Dendrogram

The dendrogram at each step of the clustering process is as follows (with heights corresponding to the distances at which clusters were merged):

[[Dendrogram(transparent).png]]
![Dendrogram(transparent).png](Dendrogram(transparent).png)



