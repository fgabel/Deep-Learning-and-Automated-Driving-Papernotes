# [Rethinking Atrous Convolution for Semantic Image Segmentation](https://arxiv.org/abs/1706.05587)

**Problem**: Semantic segmentation of objects at multiple scales is not trivially possible. Solutions to this problem entail 1) the use of exhaustive training data (often prohibitive as multiple scales add an order of magnitude to dataset size) or 2) the use of special architectures such as hierarchical *feature pyramids* (where input images have varying sizes), *Encoder-Decoder* (where parts of the features are encoded, but don't have to be due to skip connections, this approach is used by U-Net), very tailored architectures that are designed to capture long-range dependencies by employing dilated convolutions and finally *spatial pyramid pooling* (probeing an incoming feature map with filters or pooling operations at multiple rates and multiple effective field-of-views in parallel).

![HTC](../images/multi-scale-architectures.png?raw=true "Alternative architectures to capture multi-scale context.")

**Solution**

**Notes**:
* 
