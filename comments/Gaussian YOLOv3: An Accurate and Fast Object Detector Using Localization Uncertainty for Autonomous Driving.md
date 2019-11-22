
# [Gaussian YOLOv3: An Accurate and Fast Object Detector Using Localization Uncertainty for Autonomous Driving](https://arxiv.org/pdf/1904.04620.pdf)

**Problem**: YOLOv3 is the fastest object detection network with (kind of) state-of-the-art performance. This goes even for small objects (a weakness of previous YOLO networks) due to the newly introduced [multi-scale object detection](https://d2l.ai/chapter_computer-vision/multiscale-object-detection.html). However, there is no intrinsic mechanism to quantify the uncertainty in bounding boxes and thus to indicate the reliability of a found bounding box.

**Solution**: Model the bounding box with Gaussian variables (consisting of a mean and variance component).

**Notes**:
- The central contribution is to add a notion of confidence/uncertainty to the bounding box **coordinates** -  not only for objectness scores and class probabilities within each candidate box.
- YOLOv3 uses the sum of the squared error loss for bbox, and the binary cross-entropy loss for the
objectness and class. Because the bbox coordinates are output as Gaussian parameters (mean mu and variance sigma), the
loss function of bbox is redesigned as a negative log likelihood (NLL) loss - pretty straightforward.
- By adding this localization uncertainty, the authors state that the proposed algorithm improves the accuracy, increases the TP, and significantly reduces the FP while maintaining the real-time capability. 
- It's not entirely clear how adding this uncertainty metric relates to improved measures of detection performance and by which mechanism results improve causally.
