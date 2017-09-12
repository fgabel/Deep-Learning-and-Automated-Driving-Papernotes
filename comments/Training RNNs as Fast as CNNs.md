# [Training RNNs as Fast as CNNs](https://arxiv.org/pdf/1709.02755.pdf)

**Problem**: Recurrent neural nets (RNNs) are currently hard to parallelize due to temporal dependencies. This introduces computation bottlenecks in Deep Learning tasks.

**Solution**: Propose an alternative RNN implementation by deliberately simplifying the state computation and exposing more parallelism. This way, the proposed recurrent unit operates as fast as a convolutional layer and 5-10x faster than cuDNN-optimized LSTM in classification, question answering, language modeling, translation and speech recognition tasks.

**Notes**:
* *Simple Recurrent Unit (SRU)* drop connections between consecutive states h<sub>t</sub> and h<sub>t-1</sub>, which previously broke independence and parallelization. Instead, use highway connections and variational dropout.
* Representational capabilities are preserved - SRUs also allow for using much more layers.
