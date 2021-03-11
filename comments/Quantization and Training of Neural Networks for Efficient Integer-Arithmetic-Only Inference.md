# [Quantization and Training of Neural Networks for Efficient Integer-Arithmetic-Only Inference](https://arxiv.org/pdf/1712.05877.pdf)

**Problem**: * Deployment of neural networks is hard on memory and computational resources, which is especially relevant for embedded devices which are highly constrained environments. 
* State-of-the-art neural networks are often slow due to a heavy overparametrization by design in order to extract
marginal accuracy improvements. This, however, hurts inference performance - there are many ways to speed this up, but one very elegant one is to use a reduced-bitwidth representation of weights, biases and activations.
Integer-only arithmetic can be implemented very efficiently on commonly available integer-only hardware. 

* However, many quantization approaches do not deliver verifiable efficiency improvements on real hardware. Approaches that quantize only the weights are
primarily concerned with **on-device storage** and less with
**computational efficiency**. Notable exceptions are binary, ternary and bit-shift networks. These latter
approaches employ weights that are either 0 or powers of
2, which allow multiplication to be implemented by bit
shifts. However, while bit-shifts can be efficient in custom hardware, they provide little benefit on existing hardware with multiply-add instructions that, when properly
used (i.e. pipelined), are not more expensive than additions alone. Moreover, multiplications are only expensive
if the operands are wide, and the need to avoid multiplications diminishes with bit depth once both weights and activations are quantized. Notably, these approaches rarely provide on-device measurements to verify the promised timing
improvements. More runtime-friendly approaches quantize
both the weights and the activations into 1 bit representations. With these approaches, both multiplications and additions can be implemented by efficient bit-shift operations. However, 1 bit quantization often leads to substantial performance degradation, and may
be overly stringent on model representation. 

**Solution**:

**Notes**

![Attribution preservation](../images/weight_sharing.png)

* In the end, the authors leave a great section on *SPEEDUP AND ENERGY EFFICIENCY*, which I recommend readers to read themselves, it's enlightening.

