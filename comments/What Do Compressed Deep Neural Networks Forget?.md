# [What Do Compressed Deep Neural Networks Forget?](https://arxiv.org/pdf/1911.05248v2.pdf)

**Problem**: An understanding of the trade-offs incurred by model compression is critical when
quantized or compressed deep neural networks are used for sensitive tasks such as face recognition, health care diagnostics or self-driving cars. Deep neural network pruning and quantization require less memory, consume less energy, and have lower inference
latency. However, it is unclear where in the data distribution the performance is lost and outputs are changed.

**Solution**: The authors note that typical measures of performance are not very useful for answering the above question. To measure and characterize the impact of compression on model generalization, more extensive techniques need to be developed. To that end, the authors introduce the concept of Pruning Identified Exemplars (PIEs) - images where there is a high level of disagreement between the predictions of pruned and non-pruned models.

**Results**: * Certain parts of the data distribution are far more sensitive to varying the number of weights in a network, and bear the brunt cost of varying the weight representation.
* PIEs are often mislabelled and also hard to classify for humans - see below Figure, which is trained to discern between blondes and non-blondes.
* Compressed networks are far more brittle than non-compressed models to small changes in the distribution that humans are robust to. This sensitivity is amplified at higher levels of compression.

![BILD](../images/pruning_identified_examples.png?raw=true "Wireframe001")

**Notes**:
* The pruning technique used is *magnitude pruning* from [Zhu et al. (2017)](https://arxiv.org/abs/1710.01878) and the quantization methods used are [*float16* quantization](https://arxiv.org/pdf/1710.03740.pdf), [*hybrid dynamic range quantization with int8 weights*](https://www.isca-speech.org/archive/Interspeech_2016/abstracts/0128.html) and [*fixed-point only quantization with int8 weights*](https://research.google/pubs/pub37631/) - those are all post-training quantization methods, no quantization aware training was evaluated. 
* The extent to which these methods impact model performance by altering predictions is shown below - there is a steady relationship between amount of compression applied and model performance. 
![BILD](../images/pie_extent.png?raw=true "Wireframe001")
* Generally, I find the results of this paper quite intuitive. You could subsume them by stating that predictions with low confidence are at a high risk of being wrong when model compression is performed, while predictions with high confidence aren't affected very much at all. It would be interesting to see if this observations translates to more complex tasks such as semantic segmentation and object detection.
