<style TYPE="text/css">
code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;}
</style>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
    tex2jax: {
        inlineMath: [['$','$'], ['\\(','\\)']],
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry
    }
});
MathJax.Hub.Queue(function() {
    var all = MathJax.Hub.getAllJax(), i;
    for(i = 0; i < all.length; i += 1) {
        all[i].SourceElement().parentNode.className += ' has-jax';
    }
});
</script>
<script
# [Visualizing the Loss Landscape of Neural Nets](https://arxiv.org/abs/1712.09913)

**Problem**: Typically, loss functions of neural networks are highly non-convex and therefore possess many different local minima an optimizer can get stuck in - in fact, what one finds in general is a particular local minimum that generalizes well (see, e.g. (here)[https://stats.stackexchange.com/questions/106334/cost-function-of-neural-network-is-non-convex].

**Solution**: 
* The authors propose a visualization method called "filter normalization"
**Notes**:
* Preface: For large-size networks, most local minima are equivalent and yield similar performance on a test set (see (this paper)[https://arxiv.org/pdf/1412.0233v3.pdf]
* filter normalization



