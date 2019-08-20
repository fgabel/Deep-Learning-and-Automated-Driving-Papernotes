# [Hybrid Task Cascade for Instance Segmentation](https://arxiv.org/pdf/1901.07518.pdf)

**Problem**: 
* *Instance segmentation* is the problem of detecting and delineating each distinct object of interest appearing in an image (and labeling them in a pixel-wise manner, e.g. Person 1, Person 2 etc.). In a way, instance segmentation can be interpreted as the unification of (individual) object detection and semantic segmentation.
* Instance segmentation is hard for two reasons: firstly, visual objects are often subject to deformation, occlusion and scale changes.
secondly, background clutters make object instances hard to be isolated.

**Notes**:
* The current state-of-the-art architecture is based on *cascades* which means a sequence of detectors trained with increasing IoU thresholds (that learn from each others and eradicate each other's weaknesses), mitigating the problem of low-quality detections (which appear when e.g. a IoU threshold of 0.5 is used).
* Most really accurate object detection algorithms have been two-stage detectors (e.g. Fast(er) RCNN, as supposed to one-stage detectors like YOLO or SSD) in the past, but more recently, so-called multi-stage detectors have come up, incorporateing an iterative localization mechanism that alternates between box scoring and location refinement.
* The key to a successful instance segmentation cascade is to fully leverage the reciprocal relationship between detection and segmentation.

**Solution**:
![HTC](../images/htc.png?raw=true "Hybrid Task Cascade Architecture")
* Progressively refine mask predictions by using a cascade framework: **Hybrid Task Cascade**. The above Figure illustrates the components of this framework nicely:
* In (a), a cascaded Mask R-CNN is depicted - hereby, the different stages relate to models trained on different IoU thresholds. Region proposals are then only considered if their IoU with a ground truth BB is higher than this threshold. The idea here is to have subsequent stages make use of different trade-offs between false-positives (i.e. found masks that do not contain objects, happens with low IoU thresholds) and false-negatives (i.e. objects that are not found, happens with high IoU thresholds), making it easier for higher-level models (i.e. high IoU) to learn from mistakes of earlier models (i.e. lower IoU). In this way, cascaded networks are multi-stage detectors.
* In (b),  bounding box regression and mask prediction is *interleaved* instead of executing them in parallel, so M1 (mask predictions of stage 1) has access to B1 (bounding box predictions of stage 1), allowing it to leverage the information contained in the bounding boxes.
* In (c), only the masks of different stages have connections between them. In (d), a global semantic segmentation head is added to capture higher-level interactions, and further help distinguishing the foreground from the cluttered background.
