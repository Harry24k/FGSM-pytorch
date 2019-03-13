# FGSM-pytorch
**A pytorch implementation of "[Explaining and harnessing adversarial examples](https://arxiv.org/abs/1412.6572)"**

## Summary
This code is a pytorch implementation of FGSM(Fast Gradient Sign Method).   
In this code, I used FGSM to fool [Inception v3](https://arxiv.org/abs/1512.00567).   
The picture '[Giant Panda](http://www.image-net.org/)' is exactly the same as in the paper.   
You can add other pictures with a folder with the label name in the 'data'.   

## Requirements
* python==3.6   
* numpy==1.14.2   
* pytorch==1.0.0   

## Important results not in the code
- Mathmatical Results
   - There are some important difference between adversarial training and L1 weight decay. (p.4)
      - On logistic regression,
      - Adversarial training : the L1 penalty is subtracted off inside of the activation during training.
      - L1 weight decay : the L1 penalty is added to the training cost(=outside of the activation) during training.
- Experimental Results
   - We can use FGSM for a regularizer but it does not defend against all adversarial attack images. (p.5)
   - RBF networks are resistant to adversarial examples, but not for Linear. (p.7)
      - The author claims current methodologies all resemble the linear classifier, which is why do adversarial examples generalize
   - Alternative hypotheses(generative models with input distribution, ensembles) are not resistant to adversarial examples. (p.8)
