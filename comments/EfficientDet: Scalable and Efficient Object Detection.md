# [EfficientDet: Scalable and Efficient Object Detection](https://arxiv.org/pdf/1911.09070.pdf)

**Problem**: Object detection has achieved tremendous progress in recent years, but often still involves a trade-off between speed and accuracy. 

**Solution**: The EfficientDet model introduces architecture choices that improve model efficiency by bringing into question well-established ideas such as feature pyramids to both increase accuracy and decrease the number of "uninvolved" network weights.

**Notes**:
* Modern object detectors perform multi-scale feature fusion (which started with the classical feature pyramid networks - see (a)). These days, feature aggregation involves ordered (b) or complex (c) connections and skip connections. In EfficientDet, some of these connections were not deemed useful and thus removed. Also, information can flow across scales (as opposed to the one-way information flow in classical feature fusion) This idea was taken from an architecture called [PANet](https://arxiv.org/abs/1803.01534). The particular biFPN architectures used in EfficientDet is subsumed in (d).

![biFPN architecture](../images/biFPN.png?raw=true "Wireframe001")
* As the name would suggest, EfficientDet is very efficient: it achieves better efficiency than previous detectors, being 4x – 9x smaller and using 13x - 42x less FLOPs across a wide range of accuracy or resource constraints.
![efficiency of EfficientDet in terms of TeraFlops](../images/ED_flops.png?raw=true "Wireframe001")

* It's interesting that EfficientDet even overtakes DeepLabV3+, the state of the art architecture for semantic segmentation. 
