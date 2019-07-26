# [VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection](https://arxiv.org/pdf/1711.06396.pdf)

Accurate detection of objects in 3D point clouds is central to many applications such as autonomous navigation, everyday robots (housekeeping, lawnmawers etc.), and augmented/virtual reality

**Problem**: In 2D, object detection often utilizes a two-stage procedure where a **region proposal network** is first used to propose possible bounding boxes and then an image classifier is run inside these bounding boxes. However, LiDAR point clouds are much more sparse, making this approach hardly achievable. Most existing efforts have focused on hand-crafted feature representations, for example, a bird's eye view projection.

**Solution**: VoxelNet divides a point cloud into equally spaced 3D [voxels](https://en.wikipedia.org/wiki/Voxel) and transforms a group of points within each voxel into a unified feature representation through the newly introduced voxel feature encoding (VFE) layer. In this way, the point cloud is encoded as a descriptive volumetric representation, which is then connected to a RPN to generate detections.

**Notes**:
* TBD
