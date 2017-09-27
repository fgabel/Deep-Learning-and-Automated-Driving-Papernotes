# [Brain Tumor Segmentation with Deep Neural Networks](https://arxiv.org/pdf/1505.03540.pdf)

**Problem**: Brain tumors detection and segmentation using deep neural networks (ConvNets) is a hard task since they often are  diffused, poorly contrasted, and extend
tentacle-like structures that make them difficult to segment.
Also, CT images lack a 3rd spatial dimension; processing of slices of 2D images is required.

**Solution**: Try to improve the state of the art using various novel architectural choices for the ConvNets. The proposed method is one order of magnitude faster than the current state-of-the-art.

**Notes**:
* Instead of using a fully connected (FC) layer at the end, the authors use another convolutional layer with 5 kernels, each corresponding to a segmentation label. In doing so, the prediction at test time for a whole brain is 45 times faster.
Architecturally, this last convolutional layer uses as many kernels as there are different segmentation labels (in our case five). Each kernel thus acts as the ultimate detector of tissue from one of the segmentation labels.
* A single layer in the authors CNN corresponds to a convolutional layer, maxout and maxpool layers in succession.
* The authors try different network architectures. Conceptually, they can be separated into two classes: **Two-pathway architecture** and  **Cascaded architectures**
* **Two-pathway architecture**
* **Cascaded architectures**

