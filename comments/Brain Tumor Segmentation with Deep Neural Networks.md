# [Brain Tumor Segmentation with Deep Neural Networks](https://arxiv.org/pdf/1505.03540.pdf)

**Problem**: Brain tumors detection and segmentation using deep neural networks (ConvNets) is a hard task since they often are  diffused, poorly contrasted, and extend
tentacle-like structures that make them difficult to segment.

**Solution**: Try to improve the state of the art using various novel architectural choices for the ConvNets. Also, the proposed method is one order of magnitude faster than the current state-of-the-art.

**Notes**:
* Instead of using a fully connected (FC) layer at the end, the authors use another convoluational layer with 5 kernels, each corresponding to a segmentation label. In doing so, the prediction at test time for a whole brain will be 45 times faster.
