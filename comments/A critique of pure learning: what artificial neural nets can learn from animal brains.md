# [A critique of pure learning: what artificial neural nets can learn from animal brains](https://www.biorxiv.org/content/biorxiv/early/2019/03/20/582643.full.pdf)

**Problem**: While artificial neural networks have undergone a revolution, mainly catalyzed by better tools for supervised learning, this kind of learning is quite different from biological learning: vast amounts of training data are required while biological learning merely consists of behaviour changes due to (very) limited experience.

**Notes**:
* The author notes that much of our sensory representations and behavior are innate (for example, blood is appetitive to a shark from birth or fox urine is aversive for a rat). This goes as far as rodents having actual "place cells" in their neocortex dedicated to learning a map of places that they have visited over their lifespans.
* Humans are no different and react to faces really well soon after birth. Also, humans are an exception as we're immature for a long time, allowing to learn a lot longer and more.
* Rules for this innate wiring of the brain of mammals are given by the genome - however, the genome can only encode about 1GB of data, so not the actual "weights", but rather very broad rules are encoded. There even has long been speculation that the neocortex consists of many
copies of a basic "canonical" microcircuit.

**Implications for deep learning**
* What happens in real brains seems to resemble some kind of *meta-learning*, where learning consists of an outer loop (evolution)  which optimizes learning mechanisms to have inductive biases that allow us to learn very specific things very quickly.
* *Transfer learning* resembles the general idea of innate abilities, but in reality, no specific weights are pre-disposed as the genome of mammals can't carry that amount of information. Instead, passing the information through the genomic bottleneck may select for wiring rules that are more generic.
* Classical ANNs largely ignored the details of network architecture. However, in reality, the genome encodes wiring rules and patterns, which then must instantiate behaviors and representations. It is these wiring rules that are the target of evolution. 
* Therefore, the search for AGI might equal the search for better, highly constrained network architectures (much like CNNs, that were in part motivated by the structure of visual receptive fields).
