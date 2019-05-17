# [Few-Shot Unsupervised Image-to-Image Translation](https://arxiv.org/pdf/1905.01723.pdf)

**Problem**: First off, the paper deals with unsupervised image-to-image translation. The authors observe that humans are much better at generalization than even the best DL algorithms and have the capability of picking up the essence of a novel object from a small number of examples. Today's algorithms typically need a large number of training examples to learn the joint distribution from marginal distributions.
This paper bridges this gap by using a few-shot (that is, a low number of training examples), unsupervised image-to-image translation algorithm that works on previously unseen target classes that are specified at test time, only by a few example images.
In other words, the target class is never seen and only given at test time which is quite unusual.

**Solution**: A network called FUNIT (Few-shot UNsupervised Image-to-image Translation), consisting of essentially two novelties: first, the generator gets a whole set of target images (of course, not too many) as input to learn the style properly.

**Notes**:
* The images are a combination of two things: a representation of the content image, and the mean of class representation from all the destination images.
* The content image is encoded using what's called the content encoder. It contains a more information dense representation of the image being transformed. All destination images are encoded using what's called a class encoder. The average of all encoded destination images is then used in the decoder.
* The decoder uses AdaIN, and reconstructs an image from the content representation, while normalizing using scale and bias values from the class encoding. This is what allows the content to remain integral in the image, but the features to resemble whatever the classes are.
* **Summary**: The interplay between content and class encoders ensures that contents are taken from source images while features (e.g. style) is taken from the target class images.

