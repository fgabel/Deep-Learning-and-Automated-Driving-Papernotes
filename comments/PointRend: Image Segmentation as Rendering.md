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
propose PointRend, a plug-and-play module for CNNs. It takes typical feature maps of C channels and outputs
K class predictions for each pixel in the originating feature map. On a high level, a PointRend 
module consists of the following three ingredients:
  * point selection strategy (select points that exhibit large variations in segmentation wrt their neighbors)
  * point-wise feature representation
  * point head
  
**Notes**:
* TO BE CONTINUED
