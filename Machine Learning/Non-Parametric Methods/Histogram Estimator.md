- Oldest and most popular method
- Data is divided into bins
- Given origin $x_{0}$ and width of bins, $h$; bins are intervals 
	- $$[x_{0} +mh, x_{0}+(m+1)h]$$, m is an integer
- Estimator
	- $$\hat{p}(x) = \frac{{\#}\{x^{t} \ \mathrm{in \ the \ same \ bin \ as} \ x\}}{Nh}$$
## Example - 

- $$X={151,154,157,159,162,165,167,170,173,175,178,180}$$
	- $$X_{0} = 150,\  h= 5$$
	- estimate density at $x=160$

#### Bin Definition:

The bin width is $h=5$, so we create bins starting from $X_{0} = 150$

The bins will be:

- Bin 1: $[150,155)$
- Bin 2: $[155,160)$
- Bin 3: $[160,165)$
- Bin 4: $[165,170)$
- Bin 5: $[170,175)$
- Bin 6: $[175,180)$
- Bin 7: $[180,185)$
#### Counting the points in each bin

- Bin 1: $[150,155)$ contains 3 points: $151,1541$
- Bin 2: $[155,160)$ contains 3 points: $157,159$
- Bin 3: $[160,165)$ contains 2 points: $162,165$
- Bin 4:$[165,170)$ contains 3 points: $167,170$
- Bin 5: $[170,175)$ contains 2 points: $173,175$
- Bin 6: $[175,180)$ contains 2 points: $178,180$


#### Estimate density at $x = 160$
Since $x=160$ falls into **Bin 3**: $[160,165)$, which contains 2 data points, we calculate the density using the formula for histogram density estimation:

$$f(x) = \frac{\mathrm{Number \ of \ points \ in \ the \ bin}}{N * h}$$
where
- $N = 12$, the total number of points in the dataset
- $h = 5$

For **Bin 3**
$$f(160) = \frac{2}{12*5} = \frac{2}{60} = \frac{1}{30} = 0.0333$$


![[Pasted image 20240917190122.png]]
