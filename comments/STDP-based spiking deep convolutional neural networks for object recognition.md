# [STDP-based spiking deep convolutional neural networks for object recognition](https://arxiv.org/pdf/1611.01421.pdf)

**Problem**: It is still unclear how to best encode information and how to best train spiking neural networks (SNNs). In biological neural networks, a process called Spike-timing-dependent plasticity (STDP) governs this.

**Solution**: The authors propose a way to perform STDP in multiple-layer (deep) SNNs using a latency encoding scheme. For details, read on.

**Notes**:
* [Spike-timing-dependent plasticity (STDP)](https://en.wikipedia.org/wiki/Spike-timing-dependent_plasticity) is a biological process that adjusts the strength of connections between neurons in the brain. According to
STDP, synapses through which a presynaptic spike arrived before (respectively after) a postsynaptic one are reinforced (respectively depressed).

* The SNN architecture of the authors is as follows:
![Spiking neural network architecture](../images/snn_arch.png)
The first layer is a [DoG filter](https://en.wikipedia.org/wiki/Difference_of_Gaussians) which resembles the center-surround properties of the
ganglion cells of the retina. Following that, neurons in all convolutional layers are nonleaky integrate-and-fire neurons, which gather input spikes from presynaptic neurons and emit a spike when their internal potentials reach a prespecified threshold. Pooling layers help the network to gain invariance
by doing a nonlinear max pooling operation over a set of neighboring neurons with the same preferred feature.
