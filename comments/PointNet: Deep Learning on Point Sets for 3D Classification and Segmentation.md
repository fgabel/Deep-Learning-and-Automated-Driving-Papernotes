# [PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation](https://arxiv.org/abs/1612.00593)

**Problem**: Extrapolating methods and principles from 2D data (images) to 3D geometric data 
such as point clouds is not possible due to **sparsity** and **irregularity**. Most methods
"voxelize" point clouds to introduce regularity or calculate a collection of images (views)
from these point clouds. However, these representations entail a loss of information.

**Solution**: In PointNet, the complete spatial structure of all 3D points is preserved.
The below figure demonstrates the approach.

This works as the authors transform each of the *n* points into a 1024-dimensional space using 
a sequence of fully-connected networks. Hereby, it is crucial to note that each 3-D point
is processed individually - only the network weights are shared. This way, the ordering of 
points does not matter. The resulting (*nx1024*)-dimensional vector is then fed through a 
MaxPool layer (symmetric with respect to unordered input). The resulting 1024-dimensional **global feature** vector is then
fed through another MLP.

For 3D segmentation, an intermediate *(nx64)*-dimensional **local feature** vector is concatenated to the (*nx1024*)-dimensional **global feature** vector,
resulting in a *(nx1088)*-dimensional vector that is transformed to a vector of *(nxm)* output scores.
This procedure is called **Local and Global Information Aggregation**.

![PointNET Architecture](../images/pointnet.png?raw=true "Wireframe001")

**Notes**:
* It's interesting to note that no convolutional layers are used in PointNet. This is because
these assume structured inputs that irregular point clouds can't provide.
* Also, it's instructive that despite no early local coherence is introduced (as all the points are processed individually), really stable 
3D segmentations are achieved. In ConvNets, this would loosely correspond to each pixel being processed individually first.
* The authors note that MaxPooling is not the only symmetric function, but it tended to work best (summing or averaging would also be possible).
* The outputs are awesome:

![PointNET Architecture](../images/pointnet_res.png?raw=true "Wireframe001")
