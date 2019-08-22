
# [Fast Online Object Tracking and Segmentation: A Unifying Approach](https://arxiv.org/pdf/1812.05050.pdf)

**Problem**: Tracking is an important applications in CV and particularly important is *online* tracking, where the tracker can not make use of future frames to reason about the current position of an object. The problem of video object segmentation (VOS) is very expensive compared to simple bounding-box based approaches, however, as pixel-level information is required. Thus, no approaches operating in real-time are available.

**Solution**: SiamMask, a conceptual combination of the fast [fully-convolutional Siamese networks](https://arxiv.org/abs/1606.09549) and [YouTube-VOS](https://youtube-vos.org/), a huge dataset of videos with pixel-level annotations, reaching 55 FPS and new state-of-the-art performances on the VOT2016 benchmark.


![SiamMask](../images/687474703a2f2f7777772e726f626f74732e6f782e61632e756b2f7e7177616e672f5369616d4d61736b2f696d672f5369616d4d61736b5f64656d6f2e676966.gif?raw=true "Demonstration of SiamMask")


**Notes**:
* SiamMask works by leveraging Siamese CNNs, which have equal branches with shared weights. By feeding two different inputs, the repective outputs can be compared to learn about similarity (or further processed). In SiamMask, the two inputs correspond to 1) a crop centered on the target object and 2) a larger crop centered on the last estimated position of the target. 
* The crucial idea is to try and maximize the similarity (over different randomized search areas) and thereby gain an understanding of the direction the target object moves to. By using Region proposal networks as CNNs, the outputs of the Siamese networks are region proposals whose similarity can be compared, yielding bounding box coordinates and similarity scores.
* The authors also introduce frame-wise binary segmentations within the predicted masks. This 
