# [PointRend: Image Segmentation as Rendering](https://arxiv.org/pdf/1912.08193.pdf)

**Problem**: Image segmentation tasks involve mapping pixels sampled on a regular grid to a label map in a smooth manner, i.e. neighbouring pixels
should have the same label. 

However, a regular grid will unnecessarily oversample
the smooth areas while simultaneously undersampling object boundaries. The result is excess computation in smooth
regions and blurry contours (see the below Figure, left). It would be desirable to be able to focus on fine-grained 
structures in particular.
![BILD](../images/smooth.png?raw=true "Wireframe001")

**Approach**:  
* Analogous sampling issues have been studied for decades in computer graphics in rendering
(Rendering is the creation of a regular grid of pixels from a 3D scene).
* A common strategy is to compute pixel values at an irregular subset of adaptively selected points in the
image plane where variance of pixel values is highest. Known methods for this are
[subdivision](http://graphics.stanford.edu/courses/cs468-10-fall/LectureSlides/10_Subdivision.pdf) and 
[adaptive sampling](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.582.3808&rep=rep1&type=pdf).
* Rendering 2D segmentation maps from 3D scenes can be seen as a rendering problem. The authors 
propose PointRend, a plug-and-play module for CNNs. It takes typical feature maps f consisting of C channels and outputs
K class predictions for each pixel in the originating feature map. On a high level, a PointRend 
module consists of the following three ingredients:
  * point selection strategy (select points that exhibit large variations in segmentation wrt their neighbors)
  * point-wise feature representation (for each of these points, a feature representation is extracted
  from the 4 nearest neighbours on the grid of the feature maps f)
  * point head (using the features extracted above, a small neural network trained to predict a label from this point-wise
feature representation, independently for each point)
  
**Notes**:
* In short, the PointRend module concentrates on regions where fine-grained structures are to be expected.
This is done using knwon algorithms from rendering in computer vision (subdivision), thereby saving compute resources. During inference, the
authors use a subdivision algorithm. They also note that during training, this does not work
as well due to backpropagation (as the point head has to be trained, it needs to be done for sure), 
thus a random sampling is used (or a sampling based on the "confidence" of the segmentation).
* The **feature representation** is a crucial step of the approach (in the end, the point head neural network
uses these features to perform fine-grained segmentation). PointRend constructs point-wise features at selected
points by combining (e.g., concatenating) two feature types,
**fine-grained** and **coarse prediction features**. Fine-grained features are vectors containing 
*K* class predictions for a single point. Coarse prediction features are basically down-sampled feature maps (4 to 16 times smaller than the original image).
This way, the point head neural network can then utilize both global and local information.
* A PointRend module improves mIoU by more than 1% in most tasks which is especially nice as it is designed
for improvements on small-scale regions.
