# [VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection](https://arxiv.org/pdf/1711.06396.pdf)

Accurate detection of objects in 3D point clouds is central to many applications such as autonomous navigation, everyday robots (housekeeping, lawnmawers etc.), and augmented/virtual reality

**Problem**: LiDAR point clouds are mostly very sparse and have highly variable point density, due to factors such as non-uniform sampling of the 3D space, effective range of the sensors, occlusion, and the relative pose. Most existing efforts have focused on hand-crafted feature representations, for example, a bird's eye view projection.

**Solution**: VoxelNet divides a point cloud into equally spaced 3D [voxels](https://en.wikipedia.org/wiki/Voxel) and transforms a group of points within each voxel into a unified feature representation through the newly introduced voxel feature encoding (VFE) layer (3D convolution). Then, principles from classic [two-stage object detectors](https://lilianweng.github.io/lil-log/2017/12/31/object-recognition-for-dummies-part-3.html) can be applied.

![HTC](../images/voxelnet_architecture.png?raw=true "General flow of data in the VoxelNet architecture.")


**Notes**:
* TBD
