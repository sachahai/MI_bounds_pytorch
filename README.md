### Pytorch implementation of several variational lower bounds on mutual information, optimized with Neural Networks
---
All those bounds were derived from the work of Ben Poole and al., [*On Variational Bounds of Mutual Information*](https://arxiv.org/abs/1905.06922), 2019.

Their TensorFlow implementation, as well as useful insights, are available on their [GitHub](https://github.com/google-research/google-research/blob/master/vbmi/vbmi_demo.ipynb)

In the jupyter notebook  [```MI_bounds_pytorch.ipynb```](./MI_bounds_pytorch.ipynb) you'll find implementation and example with toy data of the following variational lower bounds on MI :
* NWJ / Mine-f lower bound. High variance, low bias. [ref](https://arxiv.org/abs/0809.0853)
* Noise Contrastive Estimation based (infoNCE bound). Low variance, high bias. [ref](https://arxiv.org/abs/1807.03748)
* Interpolated bound, control of bias-variance trade-off. [ref](https://arxiv.org/abs/1905.06922)

General guidelines from Ben Poole and al. :
* For representation learning purpose, use infoNCE lower bound
* For MI estimation purpose, use interpolated bound with a low alpha
