
# [Class-Balanced Loss Based on Effective Number of Samples](https://vision.cornell.edu/se3/wp-content/uploads/2019/05/class_balanced.pdf)

**Problem**: Today's large-scale, real world datasets contain edge cases and rare classes that deep learning algorithms don't learn about when not introducing a balancing scheme. Classicaly,
Existing solutions typically adopt class re-balancing strategies such as re-sampling and re-weighting based on the number of observations for each class. In this work, we argue that
as the number of samples increases, the additional benefit of a newly added data point will diminish.

**Solution**:  The authors introduce a more enhanced resampling scheme: by associating with each sample a small neighboring region rather than a single point, the effective number of samples
is defined as the volume of samples. This incorporates overlap efficiently and allows an effective balancing across classes.


![SiamMask](../images/687474703a2f2f7777772e726f626f74732e6f782e61632e756b2f7e7177616e672f5369616d4d61736b2f696d672f5369616d4d61736b5f64656d6f2e676966.gif?raw=true "Demonstration of SiamMask")


**Notes**:
* SiamMask works by leveraging Siamese CNNs, which have equal branches with shared weights. By feeding two different inputs, the repective outputs can be compared to learn about similarity (or further processed). In SiamMask, the two inputs correspond to 1) a crop centered on the target object and 2) a larger crop centered on the last estimated position of the target. 
* The crucial idea is to try and maximize the similarity (over different randomized search areas) and thereby gain an understanding of the direction the target object moves to. By using Region proposal networks as CNNs, the outputs of the Siamese networks are region proposals whose similarity can be compared, yielding bounding box coordinates and similarity scores.
* The authors also introduce frame-wise binary segmentations within the predicted masks. This 
