# [Performance Evaluation of Object Tracking Algorithms ](https://pdfs.semanticscholar.org/ad76/bdc7d06a7ec496ac788d667c6ad5fcc0fe41.pdf)

**Problem**:  Very basic - this paper is about the evaluation of different performance metrics for video-based motion tracking algorithms regarding focus, strengths, weaknesses and failures.

**Prerequisite** 
* *"correct track"*: there is either sufficient overlap between ground truth bounding boxes and predicted bounding boxes, or some other threshold (e.g. Euclidean distance) is reached for a specific frame. 
* *"GT"*: ground truth
* *"BB"*: bounding box


**Metrics**:
* Correct detected track (CDT) or True Positive (TP): A GT track is said to be not detected when there is sufficient *temporal* **and** *spatial* overlap with a predicted track.
* False alarm track (FAT) of False Positive (FP): A track is a False Positive if there is no corresponding GT track with sufficient *temporal* **and** *spatial* overlap.
In the below figure, the left predicted track (red) has no temporal overlap and the right predicted track has nearly no spatial overlap.
![HTC](../images/false_positive_track.png?raw=true "False Positive Track")


* Track detection failure (TDF): A GT track is said to be not detected when there is either no *temporal* **or** *spatial* overlap with a predicted track.
* Track Fragmentation (TF): This occurs when the tracking system is not able
to produce continuous and stable tracking for the ground truth object such as below.

![HTC](../images/track_fragmentation.png?raw=true "Fragmented track")

* ID Change (IDC): When a predicted track is associated with different GT tracks, an ID change occurs. This is mostly not desirable.
* Latency of the predicted track (LT): Latency (time delay) of the predicted track is the time
gap between the time that an object starts to be tracked by the algorithm and the first appearance of the object. The optimal latency should be zero.
* Track Matching Error (TME): TME is the average distance error between a predicted
track and the GT track. 

![HTC](../images/mean_tracking_error.png?raw=true "Mean tracking error")

* Track Completeness (TC): This is defined as the time span that the system
track overlapped with GT track divided by the total
time span of GT track.

**Notes:**
* The authors use videos with a variety of challenges, such as illumination
changes, shadows, snow storm, quick moving objects,
blurring of FOV, slow moving objects, mirror image of
objects and multiple object intersections to compare two randomly chosen tracking algorithms.
* One of the algorithms outperformed the other in almost all metrics. The different metrics allow
concluding what is bad and good in particular.
* Most of these metrics (in particular CDT, FAT, TDF, TF, IDC) are very useful for multi-target tracking and less so for single-target tracking.