# [What Do Compressed Deep Neural Networks Forget?](https://arxiv.org/pdf/1911.05248v2.pdf)

**Problem**: Deep neural network pruning and quantization require less memory, consume less energy, and have lower inference
latency. Also, they typically suffer from only very minor performance degradation. However, it is unclear to what extent and where that performance is lost and outputs are changed.

**Solution**: The authors note that typical measures of performance are not very useful for answering the above question. To measure and characterize the impact of compression on model generalization, more extensive techniques need to be developed. To that end, the authors introduce the concept of Pruning Identified Exemplars (PIEs) - images where there is a high level of disagreement between the predictions of pruned and non-pruned models.
[LINK](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf) 
![BILD](../images/adversarial_semseg.jpg?raw=true "Wireframe001")

**Notes**:
* 
