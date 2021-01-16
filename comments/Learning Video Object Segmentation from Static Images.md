# [Learning Video Object Segmentation from Static Images](https://graphics.ethz.ch/~perazzif/masktrack/files/masktrack.pdf)

**Problem**: Training data for object segmentation within videos is expensive and demanding.

**Solution**: Use input annotations on static images (such as bounding boxes and segments) as ground truths for following images. The output of a previous frame is then used as input of the next frame. This is achieved using a novel ConvNet architecture ('MaskTrack').

**Notes**:
* The authors note that their approach also works with bounding boxes instead of segmentation masks. 
* More particularly, the authors describe their approach as "mask refinement" - the basic idea is to augment the input 3-channel RGB but a rough mask of the object (as segmented in the previous frame) and to then predict the precise mask of the object. 
![HTC](../images/refinement.png?raw=true "Refinement Network Architecture")
