# [Hybrid Task Cascade for Instance Segmentation](https://arxiv.org/pdf/1901.07518.pdf)

**Problem**: *Instance segmentation* is the problem of detecting and delineating each distinct object of interest appearing in an image (and labeling them in a pixel-wise manner, e.g. Person 1, Person 2 etc.). The current state-of-the-art architecture is composed of a 
*Cascade architecture* which are composed of a sequence of detectors trained with increasing IoU thresholds, mitigating the problem of low-quality detections (which appear when e.g. a IoU threshold of 0.5 is used).

**Notes**:
* 
