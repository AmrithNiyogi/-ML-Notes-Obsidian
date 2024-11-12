- The output units are
$$y^{t}_{i} = \sum^{H}_{h=1} v_{ih}z^{t}_{h}+v_{i{0}}$$
- The error is
$$E(W,V|X) = \frac{1}{2} \sum_{t}\sum_{i} (r^{t}_{i} - y^{t}_{i})^{2}$$
- The batch update rules are then
$$\Delta v_{ih} = \eta \sum_{t}(r^{t}_{i} - y^{t}_{i})z^{t}_{h}$$
$$\Delta w_{hj} = \eta \sum_{t}\left[ \sum_{i} (r^{t}_{i} - y^{t}_{i}) v_{ih} \right] z^{t}_{h} (1-z^{t}_{h})x^{t}_{j}$$

- The total error signal backpropagated to hidden unit h from all output units is
$$\sum_{i} (r^{t}_{i} - y^{t}_{i})v_{ih}$$


![[Pasted image 20241112113528.png]]
