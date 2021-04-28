
# [Deep Unsupervised Anomaly Detection](https://openaccess.thecvf.com/content/WACV2021/papers/Li_Deep_Unsupervised_Anomaly_Detection_WACV_2021_paper.pdf)

**Problem**: Novelty detection refers to the identification of patterns that do not conform to expected normal behavior.  Fundamentally, an anomaly is something
with insufficient similarity to the rest of the data. This similarity can be computed on the basis of some feature difference. However, what makes an ideal feature representation
for the data depends on what constitutes an anomaly. This forces anomaly detection into a chicken-or-egg problem in which there are a pair of problems, neither of which can be
solved before the other.

**Solution**: The authors utilize an iterative clustering process, beginning with a process called [distribution-clustering](https://arxiv.org/abs/1804.02624), an algorithm for grouping high-dimensional data points such as images by their (unknown) underlying distribution. Using this clustering, they define a "normal" dataset and then iterating over clustering the latent space of a learned autoencoder based on normal data. The process is also shown in the below Figure.


![SiamMask](../images/deep_unsupervised_novelty_detection.png
?raw=true "Deep Unsupervised Novelty Detection")


**Notes**:
* SiamMask works by leveraging Siamese CNNs, which have equal branches with shared weights. By feeding two different inputs, the repective outputs can be compared to learn about similarity (or further processed). In SiamMask, the two inputs correspond to 1) a crop centered on the target object and 2) a larger crop centered on the last estimated position of the target. 
* The crucial idea is to try and maximize the similarity (over different randomized search areas) and thereby gain an understanding of the direction the target object moves to. By using Region proposal networks as CNNs, the outputs of the Siamese networks are region proposals whose similarity can be compared, yielding bounding box coordinates and similarity scores.
* The authors also introduce frame-wise binary segmentations within the predicted masks. This 
