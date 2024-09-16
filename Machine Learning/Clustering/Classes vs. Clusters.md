## Classes

- Supervised Learning
	- $$X = \{x^{t}, r^{t}\}_{t}$$
- Classes $C_{i} = 1, \dots, K$
	- $$p(x) = \sum_{i=1}^{K}p(x|C_{i})P(C_{i})$$
	- where, $p(x|C_{i}) \sim N\left( \mu_{i}, \sum_{i} \right)$
- $\phi = \left\{ P(C_{i}), \mu_{i}, \sum_{i} \right\}_{i=1}^{K}$
	- $$\hat{P}(C_{i}) = \frac{{\sum_{t}r^{t}_{i}}}{N}m_{i} = \frac{{\sum_{t}r^{t}_{i}x^{t}}}{\sum_{t}r^{t}_{i}}$$
	- $$S_{i} = \frac{{\sum_{t}r^{t}_{i}}(x^{t}-m_{i})(x^{t}-m_{i})^{r}}{\sum_{t}{r^t_{i}}}$$

---

### Clusters

- Unsupervised Learning
	- $$X = \{x^{t}\}_{t}$$
- Clusters $G_{i} = 1,\dots,k$
	- $$p(x) = \sum_{i=1}^{k}p(x|G_{i})P(G_{i})$$
	- where $p(x|G_{i}) \sim N\left( \mu_{i}, \sum_{i} \right)$
- $\phi = \left\{ P(G_{i}), \mu_{i}, \sum_{i} \right\}_{i=1}^k$
	- No labels $r^{t}_{i}$

