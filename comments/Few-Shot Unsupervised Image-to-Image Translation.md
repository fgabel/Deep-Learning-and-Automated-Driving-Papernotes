# [Few-Shot Unsupervised Image-to-Image Translation](https://arxiv.org/pdf/1905.01723.pdf)

**Problem**: Humans are much better at generalization than even the best DL algorithms and have the capability of picking up the essence of a novel object from a small number of examples. Today's algorithms typically need a large number of training examples to learn the joint distribution from marginal distributions.
This paper bridges this gap by using a few-shot (that is, a low number of training examples), unsupervised image-to-image translation algorithm that works on previously unseen target classes that are specified at test time, only by a few example images.

**Solution**: A network called FUNIT (Few-shot UNsupervised Image-to-image Translation)

**Notes**:
* Instead of using a fully connected (FC) layer at the end, the authors use another convolutional layer with 5 kernels, each corresponding to a segmentation label. In doing so, the prediction at test time for a whole brain is 45 times faster.
Architecturally, this last convolutional layer uses as many kernels as there are different segmentation labels (in our case five). Each kernel thus acts as the ultimate detector of tissue from one of the segmentation labels.
* A single layer in the authors CNN corresponds to a convolutional layer, maxout and maxpool layers in succession.
* The authors try different network architectures. Conceptually, they can be separated into two classes: **Two-pathway architecture** and  **Cascaded architectures**
* **Two-pathway architecture ('TwoPathCNN'):** This architecture is made of two streams: a pathway with smaller 7 × 7 receptive fields and another with larger 13 × 13 receptive fields. The motivation for this architectural choice is that the authors would like the prediction of the label of a pixel to be influenced by two aspects: the visual details of the region around that pixel and its larger “context”, i.e. roughly where the patch is in the brain. Finally, the concatenation of the feature maps of both pathways is then fed to the output layer
(for example, a 11x11x50 feature map and a 11x11x20 feature map would result in a 11x11x70 feature map).
* **Cascaded architectures:** In the cascaded architecture, the authors chain two CNNs, feeding the outputs of a first CNN as additional inputs of a second CNN. The second CNN is an example of the above two-pathway architecture.
The authors try different architectural choices for both the first CNN itself and the way the outputs of the first CNN are fed to the second CNN.
* Results: The cascaded architecture 'InputCascadeCNN' with a single connection between the two cascaded CNNs outperformed all other models. The average loss was 0.88 as measured by dice, beating all other current state-of-the-art methods.




