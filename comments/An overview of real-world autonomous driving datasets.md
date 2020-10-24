# An overview of real-world autonomous driving datasets

**TL;DR** In the last few years, several annotated real-world datasets of traffic scenes have been published - the most prominent ones will be shown here.

![Cityscapes semantic segmentation example](../images/cityscapes_segmentation.png)


* There are datasets that contain annotations in 2D (either semantic/instance segmentation or 2D object detection i.e. bounding boxes) or 3D (mostly 3D object detection with 9 degrees of freedom. This ![nice paper from Bosch](https://arxiv.org/pdf/1902.07830.pdf) subsumes these conclusively:

![2D-3D-semantic-segmentation-object-detection-datasets](../images/3D-2D-datasets_all.png)

* Even more sensoric information can be used if both 3D and 2D data are available. This ![recent paper](https://arxiv.org/pdf/2006.07864v1.pdf) lists all datasets that can be used as such:

![2D-3D-paired-datasets](../images/3D-2D-datasets.png)
