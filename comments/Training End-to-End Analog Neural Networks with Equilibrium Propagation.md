# [Training End-to-End Analog Neural Networks with Equilibrium Propagation](https://arxiv.org/pdf/2006.01981.pdf)

**TL;DR** Train analog neural networks using diodes as activations and memristors as weights, enabling new generations of AI chips.

![3D bounding box detection](../images/d3d_overview.png)

**Problem**: The **von Neumann bottleneck** describes the problem arising from the separation of memory and processing in today's deep learning: moving the data back and forth between memory
and compute units leads to grave performance degradation. Building fast and energy-efficient neural networks requires a non-von Neumann computing paradigm which unifies memory and processing,
by performing neural computations at the physical location of the synapses, where the strength of the
connections (the weights of the neural network) are stored and adjusted.

**Solution**: 

* Standard approach for 3D object detection: extract features from images using some backbone. Then, use a 2D detection head to derive 2D bounding boxes (4D: center, width and height). Finally, perform 3D object detection using the 2D bounding boxes and the features from the backbone (10D). The below Figures display the backbone, 2D detection head and 3D detection head.

![Architectures for 3D bounding box detection](../images/d3d_backbone.png)
![Architectures for 3D bounding box detection](../images/d3d_2d_det_module.png)
![Architectures for 3D bounding box detection](../images/d3d_3d_det_module.png)

* The authors follow the same approach, their backbone is a ResNet34 with a Feature Pyramid Network (FPN) built on top of it, resulting in features of different scale. The 2D detection head uses a standard [Focal Loss](https://arxiv.org/abs/1708.02002), the 3D detection head a [Huber loss](https://en.wikipedia.org/wiki/Huber_loss).

* A major contribution of this paper is the use of a disentangled loss. Hereby, each semantic contribution to the loss (in the 2D detection head, this would be the center of a bounding box or the dimensions of a bounding box) gets an isolated loss term, while fixing all other contributors to the ground truth (so that they have 0 contribution to the loss at hand).

