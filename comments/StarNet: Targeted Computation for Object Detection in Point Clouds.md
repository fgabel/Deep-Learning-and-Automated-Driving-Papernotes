# [StarNet: Targeted Computation for Object Detection in Point Clouds](https://arxiv.org/pdf/1908.11069.pdf)

**Problem**: Generally, the aim is object detection on 3D point clouds. However, representations of 3D point clouds that are permutation invariant with respect to
i and agnostic to the number of points N are non-trivial to attain. 

Methods derived from image-based object detection literature (i.e. Birds-Eye-View or 3D Voxel Grid) suffer from
performance issues in large scenes. Also, LiDaR scenes are different from images as 3D objects have
real world scale with no perspective distortions, and rarely overlap.

**Solution**: Two main ideas to mitigate these issues:
* **Sample cheap proposals** on point clouds instead of trying to learn them.
* **Incorporate temporal context** (using only the outputs of previous frames) to improve region proposals specifically (hence "targeted computation").

More accurately: 
* The sampling works as follows: Select *n* points in a certain *z*-range (avoiding sampling points on the ground). As a selection method, the authors 
suggest either random uniform sampling (introducing a bias towards densely populated regions), [farthest point sampling](https://www.numerical-tours.com/matlab/fastmarching_5_sampling_2d/) (FPS - maximizing the spatial coverage across the point cloud), and
a hybrid approach of seeding FPS with preceding frame detections
* With these sampled "centers", randomly select *K* points in a radius around 
the centers. Features are then computed in a manner borrowed from graph-convolutional NN:
each point is fed through a fully connected network to achieve a 64-dimensional point-wise feature vector (see below image, left side).

![BILD](../images/starnet_net.png?raw=true "Wireframe001")
* These 64-dim feature vectors are fed through repeated *StarNet blocks*  (see below), which first concatenate a global feature 
(here: maximum) to each of the feature vectors and then feed this 128-dim vector through two
fully connected layers to achieve a final 64-dim point-wise feature vector.

![BILD](../images/starnet_block.png?raw=true "Wireframe001")

* Intuitively, high-confidence bounding box proposals output on previous time-steps in 3D are a good prior on the
location of objects in the current frame since objects have
limited ranges of motion. The authors combine FPS with the highest-confidence bounding boxes of previous frames.

**Notes**:
* The approach does not really use global information, but still achieves state-of-the-art
performance. The cheap region proposals speed up computations considerably.
* Also, the neural networks at hand are all non-convolutional as often is the case when no 
spatial regularity is assumed.
* Target computation is a cool feature that bases region proposals on previously found bounding
boxes, thereby cheaply utilizing temporal dependencies. A possible extension to their approach would be to 
utilize multiple previous proposals using some geometry which should also be cheap.