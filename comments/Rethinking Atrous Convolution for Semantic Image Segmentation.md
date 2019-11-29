# [Rethinking Atrous Convolution for Semantic Image Segmentation](https://arxiv.org/abs/1706.05587)

**Problem**: Semantic segmentation of objects at multiple scales is not trivially possible. Solutions to this problem entail 1) the use of exhaustive training data (often prohibitive as multiple scales add an order of magnitude to dataset size) or 2) the use of special architectures such as 
- (a) hierarchical *feature pyramids* (where input images have varying sizes)
- (b) *Encoder-Decoder* (where parts of the features are encoded, but don't have to be due to skip connections, this approach is used by U-Net)
- (c) architectures that add extra modules designed to capture long-range dependencies by e.g. employing dilated convolutions
- (d) *spatial pyramid pooling* (probeing an incoming feature map with filters or pooling operations at multiple rates and multiple effective field-of-views in parallel).

![HTC](../images/multi-scale-architectures.png?raw=true "Alternative architectures to capture multi-scale context.")

* The repeated combination of max-pooling and striding at consecutive layers of these networks significantly reduces
the spatial resolution of the resulting feature maps. Deconvolution remedies this, but max-pooling still "throws away" information.

**Solution**:
* Atrous convolution (aka dilated convolution), fixes this by leaving "holes" in the filters, adding an additional hyperparameter (called the *rate*). This is equivalent to spatially expanding filters by adding zeros in between filter weights.

![HTC](../images/atrous_conv.png?raw=true "Atrous convolution with kernel size 3 × 3 and different
rates. Standard convolution corresponds to atrous convolution
with rate = 1. Employing large value of atrous rate enlarges the
model’s field-of-view, enabling object encoding at multiple scales.")

**Notes**:

* The authors emulate the above architectures with atrous convolutions: for one, they arrange atrous convolutional layers in cascade (similar to feature pyramids) and in parallel with different rates(similar to spatial pyramid pooling).
* Patches are cropped from the image during training. For atrous convolution with large rates to be effective, large
crop size is required; otherwise, the filter weights with large atrous rate are mostly applied to the padded zero region. 
