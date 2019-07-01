# [Visualizing the Loss Landscape of Neural Nets](https://arxiv.org/abs/1712.09913)

**Problem**: Typically, loss functions of neural networks are highly non-convex and therefore possess many different local minima an optimizer can get stuck in - in fact, what one finds in general is a particular local minimum that generalizes well (see, e.g. (here)[https://stats.stackexchange.com/questions/106334/cost-function-of-neural-network-is-non-convex].
Visualizing these loss functions is highly prohibitive as they have as many dimensions as there are weights in a network (the loss is a function of feature/label pairs X/y and weights W).

**Solution**: 
* The authors propose a visualization method called "filter normalization"

**Notes**:
* Preface: For large-size networks, most local minima are equivalent and yield similar performance on a test set (see (this paper)[https://arxiv.org/pdf/1412.0233v3.pdf]
* filter normalization



