# [Disentangling Monocular 3D Object Detection](http://openaccess.thecvf.com/content_ICCV_2019/papers/Simonelli_Disentangling_Monocular_3D_Object_Detection_ICCV_2019_paper.pdf)

**TL;DR** Deriving 3D object detections from RGB images (no LiDARs, no sensor fusion). Also, fixing Average Precision as the metric.

**Problem**: Deriving 3D bounding boxes is a highly ill-posed problem
**Solution**: 

![General fusion idea. Temporal information is incorporated.](../images/2dlidarrgbfuse.png)

![Architecture of the proposed network. Each block of the illustration presents the size of the tensors.](../images/2dlidarrgbfuse_architecture.png)

**Notes**:
* Their approach tends to learn calibration between both sensors which is neat. Also, they improve on orientation and translation accuracies provided by pure RGB odometry by some 20-40%. This was not to be expected as LiDAR and RGB cameras do have similar strengths.

* However, the authors simply extract a random layer from the Velodyne 3D LiDAR scans. This seems not robust to actual 2D LiDAR scans as the range covered is quite different.
* Another good read for self-localization is [this paper](https://www.sciencedirect.com/science/article/pii/S0386111217301206).
