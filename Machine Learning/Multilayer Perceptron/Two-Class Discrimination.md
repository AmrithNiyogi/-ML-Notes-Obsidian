- Two classes, one sigmoid output unit suffices:
$$y^{t} = sigmoid\left( \sum_{h=1}^{H}v_{h}z_{h}^{t}+v_{0} \right)$$
- $y_{t} \ \mathrm{for} \ P(C_{1}|x_{t}) and P(C_{2}xy_{t}) \equiv 1-y_{t}$
- The error function in this case is:
$$E(W,v|X) = -\sum_{t}r^{t}\log y^{t}+ (1-r^{t})\log(1-y^{t})$$
- The update equations implementing gradient descent are
$$\Delta v_{h} = \eta \sum_{t}(r^t-y^t)z^{t}_{h}$$
$$\Delta w_{hj} = \eta \sum_{t}(r^t-y^t)j_{h}z^{t}_{h}(1-z^{t}_{h})x^{t}_{j}$$
- The update equations for regression and classification are identical, but values can be different.