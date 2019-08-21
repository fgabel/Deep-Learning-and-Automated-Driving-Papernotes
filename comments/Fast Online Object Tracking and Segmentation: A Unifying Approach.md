
# [Fast Online Object Tracking and Segmentation: A Unifying Approach](https://arxiv.org/pdf/1812.05050.pdf)

**Problem**: Tracking is an important applications in CV and particularly important is *online* tracking, where the tracker can not make use of future frames to reason about the current position of an object. The problem of video object segmentation (VOS) is very expensive compared to simple bounding-box based approaches, however, as pixel-level information is required. Thus, no approaches operating in real-time are available.

**Solution**: SiamMask, a conceptual combination of the fast [fully-convolutional Siamese networks](https://arxiv.org/abs/1606.09549) and [YouTube-VOS](https://youtube-vos.org/), a huge dataset of videos with pixel-level annotations, reaching 55 FPS and new state-of-the-art performances on the VOT2016 benchmark.
![SiamMask](../images/687474703a2f2f7777772e726f626f74732e6f782e61632e756b2f7e7177616e672f5369616d4d61736b2f696d672f5369616d4d61736b5f64656d6f2e676966.gif?raw=true "Demonstration of SiamMask")


**Notes**:
* TBD Network architecture, three branch - two branch stuff
