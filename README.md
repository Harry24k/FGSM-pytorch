# FGSM-pytorch
**A pytorch implementation of "[Explaining and harnessing adversarial examples](https://arxiv.org/abs/1412.6572)"**

## Summary
1. The natural basis is not better than a random basis for inspecting the properties of latent vectors.
   - there are serveral directions which have the semantic meaning not only individual units.
2. We can generate images(_adversarial examples_) with small perturbations to fooling neural network models.
3. Weight Decay or Regularization couldn't help model to defend adversarial examples.
4. One adversarial example for a specific model is possible to deceive other models.
5. According to spectral analysis of unstability, the deeper models, the more stupid.

## Requirements
* python==3.6   
* numpy==1.14.2   
* pytorch==1.0.0   

## A limitation of this code
In the paper, L-BFGS is used to solve equation with constraints.   
However, in this code, backpropagation method is used instead of L-BFGS.   
Hence, it doesn't cover "4.2 Exprimental results" 
