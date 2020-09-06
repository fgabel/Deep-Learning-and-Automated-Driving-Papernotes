# [The Fishyscapes Benchmark: Measuring Blind Spots in Semantic Segmentation](https://arxiv.org/pdf/1904.03215.pdf)

**Problem**: CNNs react unpredictably for inputs that deviate from their training distribution. 
In the presence of an outlier object, this is interpolated with available classes, a behaviour similar to what is known in human perception as ‘blind spot’.

![BILD](../images/fishyscapes.png?raw=true "Wireframe001")

**Solution**:  The authors introduce Fishyscapes, a benchmark that evaluates uncertainty estimates for semantic segmentation. The benchmark measures
how well methods detect potentially hazardous anomalies in driving scenes.

**Notes**:
* The Fishyscapes dataset is based on overlaying images from the Cityscapes dataset with random objects such as animals or inanimate objects such as toys. There are three different versions of the dataset: FS static (novelties sampled from Pascal VOC; their visual diversity is limited, which is important to make
sure that it contains none of the overlayed objects), FS Web (novelties sampled from the internet; otherwise similar to FS static) and FS Lost&Found (images from the Lost&Found dataset; generally from a different distribution than the ones from Cityscapes).
* Evaluating the performance of novelty detection algorithms rests upon the average precision (AP), but also the IoU of the original segmentation algorithm as novelty detection should not hurt performance.
* There are a number of existing methods on novelty detection, namely methods based on the Softmax score, training with novelties, Bayesian DeepLab, Dirichlet Prior Networks and kNN Embedding. The authors also propose a new method termed Learned Embedding Density. 
