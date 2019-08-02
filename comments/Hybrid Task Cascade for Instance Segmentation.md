# [Hybrid Task Cascade for Instance Segmentation](https://arxiv.org/pdf/1901.07518.pdf)

**Problem**: * *Instance segmentation* is the problem of detecting and delineating each distinct object of interest appearing in an image (and labeling them in a pixel-wise manner, e.g. Person 1, Person 2 etc.). 
* Instance segmentation is hard for two reasons: firstly, visual objects are often subject to deformation, occlusion and scale changes.
secondly, background clutters make object instances hard to be isolated.

**Notes**:
* The current state-of-the-art architecture is based on *cascades* which means a sequence of detectors trained with increasing IoU thresholds (that learn from each others and eradicate each other's weaknesses), mitigating the problem of low-quality detections (which appear when e.g. a IoU threshold of 0.5 is used).
* Most really accurate object detection algorithms have been two-stage detectors (e.g. Fast(er) RCNN, as supposed to one-stage detectors like YOLO or SSD) in the past, but more recently, so-called multi-stage detectors have come up, incorporateing an iterative localization mechanism that alternates between box scoring and location refinement.

**Solution**:
* The key to a successful instance segmentation cascade is to fully leverage the reciprocal relationship between detection and segmentation.
