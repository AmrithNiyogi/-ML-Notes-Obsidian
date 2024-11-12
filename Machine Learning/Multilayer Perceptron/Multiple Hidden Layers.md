- MLP with one hidden layer is a universal approximator (Hornik et al., 1989), but using multiple layers may lead to simpler networks
- Each layer applies weights to its inputs; Sigmoid function is applied to the weighted sum at each hidden layer
- For regression,
$$z_{1h} = sigmoid(w^{T}_{1h}x)= sigmoid\left( \sum^{d}_{j=1} w_{1hj}x_{j} + w_{1h{0}} \right),h=1,\dots H_{1}$$
$$z_{2l} = sigmoid(w^{T}_{2l}z_{1})= sigmoid\left( \sum^{H_{1}}_{h=1} w_{2lh}x_{1h} + w_{2l{0}} \right),l=1,\dots H_{2}$$
$$y = v^{T}z_{2} = \sum^{H_{2}} v_{j}z_{2l} + v_{0}$$
- $w_{1h}$: First-layer weights and $w_{2l}$: Second-layer weights
- v: Third-layer weights
- $z_{1h}, z_{2h}$: Units in the first and second hidden layers
- This structure allows for learning more complex, hierarchical representations