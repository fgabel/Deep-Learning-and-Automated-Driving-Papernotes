# [Squeeze-and-Excitation Networks](https://arxiv.org/pdf/1911.09070.pdf)

**Problem**: CNNs use their convolutional filters to extract hierarchal information from images. Lower layers find trivial pieces of context like edges or high frequencies, while upper layers can detect faces, text or other complex geometrical shapes. They extract whatever is necessary to solve a task efficiently.
All of this works by fusing the spatial and channel information of an image. The different filters will first find spatial features in each input channel before adding the information across all available output channels. Networks weigh each of its channels equally when creating the output feature maps (by summing them up) - an asssumption that is at least questionable.

**Solution**: **Squeeze-and-Excitation Networks** are all about changing this by adding a content aware mechanism to weight each channel adaptively. In its most basic form this could mean adding a single parameter to each channel and giving it a linear scalar how relevant each one is.
However, the authors push it a little further. First, they get a global understanding of each channel by squeezing the feature maps to a single numeric value. This results in a vector of size *n*, where *n* is equal to the number of convolutional channels. Afterwards, it is fed through a two-layer neural network, which outputs a vector of the same size. These *n* values can now be used as weights on the original features maps, scaling each channel based on its importance.
![SENet architecture](../images/Squeeze-and-excite.png?raw=true "Wireframe001")
**Notes**:
* The authors show that by adding SE-blocks to ResNet-50 you can expect almost the same accuracy as ResNet-101 delivers. This is impressive for a model requiring only half of the computational costs. 


* There are several variants or scenarios in which SEBlocks (i.e. blocks featuring the above mechanism) are useful. The authors argue that object dete
![SENet variants](../images/variants_of_se_blocks.png?raw=true "Wireframe001")

* An interesting finding is that the SE activations (i.e. weighting factors of different activation maps) tend to become close to 1 (equalling the identity operation) for later layers (see SE_5_2 below) or at least quite constant (equalling a global scaling operation, see SE_5_3 below). Arguably, only activation maps of early layer benefit gravely from SE blocks.
![SENet activations](../images/activations_se_layers.png?raw=true "Wireframe001")
