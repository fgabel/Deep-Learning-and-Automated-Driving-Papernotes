
# [Gaussian YOLOv3: An Accurate and Fast Object Detector Using Localization Uncertainty for Autonomous Driving](https://arxiv.org/pdf/1904.04620.pdf)

**Problem**: YOLOv3 is the fastest object detection network with (kind of) state-of-the-art performance. This goes even for small objects (a weakness of previous YOLO networks) due to the newly introduced [multi-scale object detection](https://d2l.ai/chapter_computer-vision/multiscale-object-detection.html). However, there is no intrinsic mechanism to quantify the uncertainty in bounding boxes and thus to indicate the reliability of a found bounding box.

**Solution**: Model the bounding box with Gaussian variables (consisting of a mean and variance component).

**Notes**:
