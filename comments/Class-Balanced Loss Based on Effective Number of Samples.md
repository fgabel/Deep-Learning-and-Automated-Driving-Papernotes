
# [Class-Balanced Loss Based on Effective Number of Samples](https://vision.cornell.edu/se3/wp-content/uploads/2019/05/class_balanced.pdf)

**Problem**: Today's large-scale, real world datasets contain edge cases and rare classes that deep learning algorithms don't learn about when not introducing a balancing scheme. Classicaly,
Existing solutions typically adopt class re-balancing strategies such as re-sampling and re-weighting based on the number of observations for each class. In this work, we argue that
as the number of samples increases, the additional benefit of a newly added data point will diminish.

**Solution**:  The authors introduce a more enhanced resampling scheme: by associating with each sample a small neighboring region rather than a single point, the effective number of samples
is defined as the volume of samples. This incorporates overlap efficiently and allows an effective balancing across classes.
The below Figure displays the general idea: No re-weighting causes a classifier to be biased towards the head of the distribution, inverse class frequency causes a bias towards the tail of the distribution.

![Class-balanced Reweighting](../images/reweighting.png?raw=true "Demonstration of Reweighting")


**Notes**: 
* Most of previous efforts on long-tailed imbalanced data can be divided into two regimes: **re-sampling**
(including over-sampling and under-sampling) and **cost-sensitive learning** (e.g. inverse frequency sampling).
* Mathematically, the authors borrow an idea called [random covering](https://projecteuclid.org/euclid.acta/1485890413) - i.e. associate each sample with a small neighboring region instead of a single point. This way, common data points which are close by each other don't skew the resampling towards this class: see the Figure below.
![Class-balanced Reweighting](../images/overlap.png?raw=true "Overlap")

* By weighing the losses of a data point with its associated class-balanced weights improves classification performance on CIFAR considerably (2% to 5%). Experiments on other vision tasks have not been conducted by the authors.

