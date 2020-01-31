# [FuseSeg: LiDAR Point Cloud Segmentation Fusing Multi-Modal Data](https://arxiv.org/pdf/1912.08487.pdf)

**Problem**: 
* Semantic segmentation of point clouds mostly uses single-modal input 
or multi-modal sensor fusion on a high level, i.e. after inputs have been processed individually.
* Thus, not all available information is
leveraged jointly. Objects poorly visible in one single sensor are prone to be missed. 
* Warping RGB images into LiDAR range space introduces visual distortion and limiting CNNs transfer learning capabilities

**Solution**: The idea is simple yet appealing: First establish point correspondences using RGB+LiDAR calibration as shown below, second 
use a plain pre-trained MobileNetV2 to calculate feature vectors at these corresponding points.
Thereby, a rather low-level fusion can be achieved. 
![BILD](../images/fuseseg_correspondence.png?raw=true "Wireframe001")



**Notes**:
* 
[LINK](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf) 
