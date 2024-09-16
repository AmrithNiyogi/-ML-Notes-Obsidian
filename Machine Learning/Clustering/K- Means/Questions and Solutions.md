![[Pasted image 20240916123705.png]]

Perform k-means clustering on given data for k=3

---
Answer - 
## First Iteration
### **Step 1:** Initializing the centroids - 

- Centroid 1 $\to (2,10) \to point \ 1$ 
- Centroid 2 $\to (8,4) \to point \ 3$
- Centroid 3 $\to (1,2) \to point \ 7$

### **Step 2:** Calculating distance from centroids for each point

we use euclidean distance formula
$$d = \sqrt{ (x_{2} - x_{1})^{2}+ (y_{2}-y_{1}^{2}) }$$


#### point 1 - (2,10)

- Distance to centroid 1 - 
$$d = \sqrt{ (2-2)^{2}+(10-10)^{2} } = 0$$
- Distance to centroid 2 - 
$$d = \sqrt{ (8-2)^{2} + (4-10)^{2} } = \sqrt{ 36 + 36 } = 8.49$$
- Distance to centroid 3 -
$$d =  \sqrt{ (2−1)2+(10−2)2}=\sqrt{ 1+64}=8.06​$$

**point 1 is closest to centroid 1.**

---
#### point 2 - (2,5)
- Distance to Centroid 1: 
$$d =\sqrt{(2 - 2)^2 + (5 - 10)^2} = \sqrt{0 + 25} = 5.0$$
- Distance to Centroid 2: 
$$d = \sqrt{(2 - 8)^2 + (5 - 4)^2} = \sqrt{36 + 1} = 6.08$$
- Distance to Centroid 3: 
$$d=\sqrt{ (2−1)^2+(5−2)^2}=\sqrt{ 1+9}=3.16$$
**point 2 is closest to centroid 3.**

---
#### point 3 - (8,4)

- Distance to Centroid 1: 
$$d =\sqrt{(8 - 2)^2 + (4 - 10)^2} = \sqrt{36 + 36} = 8.49$$
- Distance to Centroid 2: 
$$d=\sqrt{(8 - 8)^2 + (4 - 4)^2} = 0$$
- Distance to Centroid 3: 
$$d=\sqrt{(8 - 1)^2 + (4 - 2)^2} = \sqrt{49 + 4} = 7.28$$


**Point 3 is closest to Centroid 2.**

---
#### point 4 - (5,8)

- Distance to Centroid 1: 
$$d=\sqrt{(5 - 2)^2 + (8 - 10)^2} = \sqrt{9 + 4} = 3.61$$
- Distance to Centroid 2: 
$$d=\sqrt{(5 - 8)^2 + (8 - 4)^2} = \sqrt{9 + 16} = 5.0$$
- Distance to Centroid 3: 
$$d=\sqrt{(5 - 1)^2 + (8 - 2)^2} = \sqrt{16 + 36} = 7.21$$


**Point 4 is closest to Centroid 1.**

---
#### point 5 - (7,5)

- Distance to Centroid 1:
$$d=\sqrt{(7 - 2)^2 + (5 - 10)^2} = \sqrt{25 + 25} = 7.07$$
- Distance to Centroid 2:
$$d=\sqrt{(7 - 8)^2 + (5 - 4)^2} = \sqrt{1 + 1} = 1.41$$
- Distance to Centroid 3: 
$$d=\sqrt{(7 - 1)^2 + (5 - 2)^2} = \sqrt{36 + 9} = 6.71$$

**Point 5 is closest to Centroid 2.**

---
#### point 6 - (6,4)

- Distance to Centroid 1: 
$$d=\sqrt{(6 - 2)^2 + (4 - 10)^2} = \sqrt{16 + 36} = 7.21$$
- Distance to Centroid 2: 
$$d=\sqrt{(6 - 8)^2 + (4 - 4)^2} = \sqrt{4 + 0} = 2.0$$
- Distance to Centroid 3: 
$$d=\sqrt{(6 - 1)^2 + (4 - 2)^2} = \sqrt{25 + 4} = 5.39$$

**Point 6 is closest to Centroid 2.**

---
#### point 7 - (1,2)

- Distance to Centroid 1: 
$$d=\sqrt{(1 - 2)^2 + (2 - 10)^2} = \sqrt{1 + 64} = 8.06$$
- Distance to Centroid 2: 
$$d=\sqrt{(1 - 8)^2 + (2 - 4)^2} = \sqrt{49 + 4} = 7.28$$
- Distance to Centroid 3: 
$$d=\sqrt{(1 - 1)^2 + (2 - 2)^2} = 0$$
**Point 7 is closest to Centroid 3.**

---
#### point 8 - (4,9)

- Distance to Centroid 1: 
$$d=\sqrt{(4 - 2)^2 + (9 - 10)^2} = \sqrt{4 + 1} = 2.24$$
- Distance to Centroid 2: 
$$d=\sqrt{(4 - 8)^2 + (9 - 4)^2} = \sqrt{16 + 25} = 6.4$$
- Distance to Centroid 3: 
$$d=\sqrt{(4 - 1)^2 + (9 - 2)^2} = \sqrt{9 + 49} = 8.06
$$

**Point 8 is closest to Centroid 1.**


### Cluster Assignment - 

| Point   | Coordinates | Distance to Centroid 1 | Distance to Centroid 2 | Distance to Centroid 3 | Assigned Centroid |
| ------- | ----------- | ---------------------- | ---------------------- | ---------------------- | ----------------- |
| Point 1 | (2, 10)     | 0.00                   | 8.49                   | 8.06                   | Centroid 1        |
| Point 2 | (2, 5)      | 5.00                   | 6.08                   | 3.16                   | Centroid 3        |
| Point 3 | (8, 4)      | 8.49                   | 0.00                   | 7.28                   | Centroid 2        |
| Point 4 | (5, 8)      | 3.61                   | 5.00                   | 7.21                   | Centroid 1        |
| Point 5 | (7, 5)      | 7.07                   | 1.41                   | 6.71                   | Centroid 2        |
| Point 6 | (6, 4)      | 7.21                   | 2.00                   | 5.39                   | Centroid 2        |
| Point 7 | (1, 2)      | 8.06                   | 7.28                   | 0.00                   | Centroid 3        |
| Point 8 | (4, 9)      | 2.24                   | 6.40                   | 8.06                   | Centroid 1        |


### Compute new Centroids 

- Centroid 1 - 
$$New \ Centroid \ 1 = \left( \frac{{2+5+4}}{3}, \frac{{10+8+9}}{3} \right)= (3.67, 9.0)$$
- Centroid 2 - 
$$New \ Centroid \ 2 = \left( \frac{{8+7+6}}{3}, \frac{{4+5+4}}{3} \right) = (7.0,4.33)$$
- Centroid 3 - 
$$New \ Centroid \ 3 = \left( \frac{{2+1}}{2}, \frac{{5+2}}{2} \right) = (1.5,3.5)$$
---
---

## 2nd iteration

### Updated Centroids (After 1st Iteration):
- Centroid 1: (3.25, 9.25)
- Centroid 2: (6.5, 4.25)
- Centroid 3: (1.5, 3.0)

---

#### point 1 - (2,10)

- Distance to Centroid 1:  
$$d = \sqrt{(2 - 3.25)^2 + (10 - 9.25)^2} = \sqrt{1.5625 + 0.5625} = 1.38$$
- Distance to Centroid 2:  
$$d = \sqrt{(2 - 6.5)^2 + (10 - 4.25)^2} = \sqrt{20.25 + 33.0625} = 7.23$$
- Distance to Centroid 3:  
$$d = \sqrt{(2 - 1.5)^2 + (10 - 3.0)^2} = \sqrt{0.25 + 49.0} = 7.0$$

**Point 1 is closest to Centroid 1.**

---

#### point 2 - (2,5)

- Distance to Centroid 1:  
$$d = \sqrt{(2 - 3.25)^2 + (5 - 9.25)^2} = \sqrt{1.5625 + 18.0625} = 4.43$$
- Distance to Centroid 2:  
$$d = \sqrt{(2 - 6.5)^2 + (5 - 4.25)^2} = \sqrt{20.25 + 0.5625} = 4.58$$
- Distance to Centroid 3:  
$$d = \sqrt{(2 - 1.5)^2 + (5 - 3.0)^2} = \sqrt{0.25 + 4.0} = 2.06$$

**Point 2 is closest to Centroid 3.**

---

#### point 3 - (8,4)

- Distance to Centroid 1:  
$$d = \sqrt{(8 - 3.25)^2 + (4 - 9.25)^2} = \sqrt{22.5625 + 27.5625} = 7.17$$
- Distance to Centroid 2:  
$$d = \sqrt{(8 - 6.5)^2 + (4 - 4.25)^2} = \sqrt{2.25 + 0.0625} = 1.51$$
- Distance to Centroid 3:  
$$d = \sqrt{(8 - 1.5)^2 + (4 - 3.0)^2} = \sqrt{42.25 + 1.0} = 6.52$$

**Point 3 is closest to Centroid 2.**

---

#### point 4 - (5,8)

- Distance to Centroid 1:  
$$d = \sqrt{(5 - 3.25)^2 + (8 - 9.25)^2} = \sqrt{3.0625 + 1.5625} = 2.0$$
- Distance to Centroid 2:  
$$d = \sqrt{(5 - 6.5)^2 + (8 - 4.25)^2} = \sqrt{2.25 + 14.0625} = 3.95$$
- Distance to Centroid 3:  
$$d = \sqrt{(5 - 1.5)^2 + (8 - 3.0)^2} = \sqrt{12.25 + 25.0} = 6.4$$

**Point 4 is closest to Centroid 1.**

---

#### point 5 - (7,5)

- Distance to Centroid 1:  
$$d = \sqrt{(7 - 3.25)^2 + (5 - 9.25)^2} = \sqrt{14.0625 + 18.0625} = 5.62$$
- Distance to Centroid 2:  
$$d = \sqrt{(7 - 6.5)^2 + (5 - 4.25)^2} = \sqrt{0.25 + 0.5625} = 0.79$$
- Distance to Centroid 3:  
$$d = \sqrt{(7 - 1.5)^2 + (5 - 3.0)^2} = \sqrt{30.25 + 4.0} = 5.74$$

**Point 5 is closest to Centroid 2.**

---

#### point 6 - (6,4)

- Distance to Centroid 1:  
$$d = \sqrt{(6 - 3.25)^2 + (4 - 9.25)^2} = \sqrt{7.5625 + 27.5625} = 6.03$$
- Distance to Centroid 2:  
$$d = \sqrt{(6 - 6.5)^2 + (4 - 4.25)^2} = \sqrt{0.25 + 0.0625} = 0.51$$
- Distance to Centroid 3:  
$$d = \sqrt{(6 - 1.5)^2 + (4 - 3.0)^2} = \sqrt{20.25 + 1.0} = 4.58$$

**Point 6 is closest to Centroid 2.**

---

#### point 7 - (1,2)

- Distance to Centroid 1:  
$$d = \sqrt{(1 - 3.25)^2 + (2 - 9.25)^2} = \sqrt{5.0625 + 52.5625} = 7.68$$
- Distance to Centroid 2:  
$$d = \sqrt{(1 - 6.5)^2 + (2 - 4.25)^2} = \sqrt{30.25 + 5.0625} = 5.86$$
- Distance to Centroid 3:  
$$d = \sqrt{(1 - 1.5)^2 + (2 - 3.0)^2} = \sqrt{0.25 + 1.0} = 1.12$$

**Point 7 is closest to Centroid 3.**

---

#### point 8 - (4,9)

- Distance to Centroid 1:  
$$d = \sqrt{(4 - 3.25)^2 + (9 - 9.25)^2} = \sqrt{0.5625 + 0.0625} = 0.79$$
- Distance to Centroid 2:  
$$d = \sqrt{(4 - 6.5)^2 + (9 - 4.25)^2} = \sqrt{6.25 + 22.5625} = 5.16$$
- Distance to Centroid 3:  
$$d = \sqrt{(4 - 1.5)^2 + (9 - 3.0)^2} = \sqrt{6.25 + 36.0} = 6.77$$

**Point 8 is closest to Centroid 1.**


---

| Point   | Coordinates | Distance to Centroid 1 | Distance to Centroid 2 | Distance to Centroid 3 | Assigned Centroid |
| ------- | ----------- | ---------------------- | ---------------------- | ---------------------- | ----------------- |
| Point 1 | (2, 10)     | 1.81                   | 8.43                   | 6.72                   | Centroid 1        |
| Point 2 | (2, 5)      | 4.27                   | 5.83                   | 1.80                   | Centroid 3        |
| Point 3 | (8, 4)      | 5.75                   | 0.33                   | 7.12                   | Centroid 2        |
| Point 4 | (5, 8)      | 1.77                   | 4.05                   | 6.52                   | Centroid 1        |
| Point 5 | (7, 5)      | 5.11                   | 0.94                   | 5.98                   | Centroid 2        |
| Point 6 | (6, 4)      | 5.19                   | 1.05                   | 4.52                   | Centroid 2        |
| Point 7 | (1, 2)      | 7.47                   | 6.86                   | 1.58                   | Centroid 3        |
| Point 8 | (4, 9)      | 0.47                   | 5.74                   | 7.21                   | Centroid 1        |

### Cluster Assignment After Second Step: 
- **Centroid 1**: Points 1, 4, 8 
- **Centroid 2**: Points 3, 5, 6 
- **Centroid 3**: Points 2, 7 
### Compute New Centroids (No Change) 

Centroid 1 - 
$$New \ Centroid \ 1 = \left( \frac{{2+5+4}}{3}, \frac{{10+8+9}}{3} \right)= (3.67, 9.0)$$
- Centroid 2 - 
$$New \ Centroid \ 2 = \left( \frac{{8+7+6}}{3}, \frac{{4+5+4}}{3} \right) = (7.0,4.33)$$
- Centroid 3 - 
$$New \ Centroid \ 3 = \left( \frac{{2+1}}{2}, \frac{{5+2}}{2} \right) = (1.5,3.5)$$

## Conclusion 

The algorithm converges after the second iteration with the final cluster assignments 

- **Cluster 1**: Points 1, 4, 8 
- **Cluster 2**: Points 3, 5, 6 
- **Cluster 3**: Points 2, 7