- There are K outputs with softmax activation to estimate mutually exclusive and exhaustive class probabilities
$$o^{t}_{i} = \sum^{H}_{h=1}v_{ih}z^{t}_{h} + v_{i{0}}$$
$$y_{i}^{t} = \frac{\exp o^{t}_{i}}{\sum_{k} \exp o^{t}_{k}} \equiv P(C_{i}|x^{t})$$
- The error function is
$$E{(W,V|X)}=-\sum_{t} \sum_{t} r^{t}_{i} \log y^{t}_{i}$$
- The update equations using gradient descent:
$$\Delta v_{ih} = \eta \sum_{t}(r^{t_{i}}- y^{t}_{i})z^{t}_{h}$$
$$\Delta w_{hj} = \eta \sum_{t}\left[ \sum_{i} (r^{t_{i}}- y^{t}_{i}) v_{ih} \right] z^{t}_{h} (1-z^t_{h})x^{t}_{j}$$
- MLPs with sufficient complexity and training data can estimate posterior probabilities (Richard & Lippmann, 1991)