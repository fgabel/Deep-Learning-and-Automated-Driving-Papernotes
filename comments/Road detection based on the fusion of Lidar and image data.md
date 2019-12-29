# [Road detection based on the fusion of Lidar and image data](https://journals.sagepub.com/doi/full/10.1177/1729881417738102)

**Problem**: Multimodality and redundancy of sensing need to be positively utilized for reliable
and consistent perception of the environment through sensor
data fusion. The goal of this paper is to fuse sensoric data from (2D) dense monocular images from electro-optical 
cameras and sparse (3D) point clouds from LiDaRs.

**Approach**:
* The main idea is to upsample sparse depth maps from LiDar using RGB images. However, RGB images 
suffer from variable lighting conditions and shadows. Therefore, the authors use
 ["shadow-free" conversion](https://ieeexplore.ieee.org/abstract/document/6957936) (middle image in the below Figure). 
 
![BILD](../images/shadow-free.png?raw=true "Wireframe001")
* The point clouds are projected into image space by matching coordinate frames (rotation and translation, known in advance), 
resulting in sparse depth maps within the RGB images.
* Interestingly, the authors use a good old ADABOOST for classification, which is amazingly fast 
with decent results.

![BILD](../images/segmentations.gif?raw=true "Wireframe001")

**Notes**:
* multimodality
* Monocular cameras are cheap and yield a dense depiction of a scene, but lack night-vision and depth
information. 3D perception systems (mostly LiDaR and stereo vision) often yield sparse data and lack resolution,especially for far-away objects, but are robust to changes in light
conditions.
* Shadow-freeing yields good shadow-free images, but we also get rid of several edges, e.g. the footwalk on the right. Better ideas
for this are needed.

