# [Weight Agnostic Neural Networks](https://arxiv.org/abs/1906.04358)

**Problem**: That some neural network architectures work better than others is well known, but not well understood. Given that neural network outputs are a function of both its architecture and its weights, the relative importance of the architecture is deemed interesting (e.g. in the context of neural architecture search).
**Solution**:
* The authors  propose a search method for neural network architectures that can already perform a task without any explicit weight training.
* Instead of tuning the model by modifying learnable weights, the authors sample the weights from a uniform distribution and only modify the architecture.

**Notes**:
* Even though the problem of exaplainability in GANs relates to various tasks, the authors only come up with a solution for vision. The paper also lacks transfer to other domains.

