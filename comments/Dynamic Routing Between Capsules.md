
# [Dynamic Routing Between Capsules](https://arxiv.org/pdf/1710.09829.pdf)

**Problem**: Neural networks don't resemble the human brain in that they can't focus on parts of the input space specifically. Developing methods for focussing on important features of some input vector space is worthwile.

**Solution**: Try to simulate how targeted human attention works; e.g. fixation point sequences in vision by building parse-trees of groups of neurons.

**Notes**:
* creating parse trees from a multilayer neural network works like carving a sculpture from a rock, whereby every layer is grouped into smallish groups of neurons called 'capsules'. Each node in a parase tree will correspond to an active capsule.
* dynamic routing: describes the capability of a system to automatically forward data streams via a different route based on the current communication circuits in a system - contrast to static routing
* performance on common classification tasks is similar to existing methods, but the introduction of capsules brings into play other desirable features
