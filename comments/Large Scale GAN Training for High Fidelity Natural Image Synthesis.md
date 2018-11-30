
# [Large Scale GAN Training for High Fidelity Natural Image Synthesis](https://arxiv.org/pdf/1809.11096v1.pdf)

**Problem**: As of now, generating high-resolution images using GANs is difficult; successfully generating
high-resolution, diverse samples from complex datasets such as ImageNet remains an elusive goal

**Solution**: Study the instabilities specific to large-resolution image generation and employ techniques to deal with them - particularly the so called "truncation trick" (see below)

**Notes**:
* The inception score (a way of assessing the realism of created images, see [more information](https://sudomake.ai/inception-score-explained/)) of current generated state-of-the-art ImageNet images is 52.5, while real images reach 233.
* Scaling, i.e. increasing the number of parameters and the batch size, increases performance dramatically (up to 99.3 inception score)
* **truncation trick** Usually, GANs are trained using a random vector z from a normal distribution N(0, I) which is also used for sampling. Using a truncated normal distribution for sampling, where values falling outside a certain range are immediately resampled, improves the inception score.
* The authors conclude that pretty vanilla techniques are sufficient for training GANs on images of up to 512x512 without the need of multi-layer training approaches.


