# Improving-Deep-Neural-Networks-Hyperparameter-Tuning-Regularization-and-Optimization

This repository includes below topics:

**1) [Initialization](https://github.com/Zahra-Bakhtiari/Improving-Deep-Neural-Networks-Hyperparameter-Tuning-Regularization-and-Optimization/blob/main/Initialization.ipynb)**

Training your neural network requires specifying an initial value of the weights. A well-chosen initialization method helps the learning process.
In the [Initialization](https://github.com/Zahra-Bakhtiari/Improving-Deep-Neural-Networks-Hyperparameter-Tuning-Regularization-and-Optimization/blob/main/Initialization.ipynb) notebook, I tried out a few different initializations, including random, zeros, and He initialization, and see how each leads to different results.

A well-chosen initialization can:

    a) Speed up the convergence of gradient descent
    b) Increase the odds of gradient descent converging to a lower training (and generalization) error
    c) Avoid vanishing/exploding gradients, which also slows down the optimization algorithm. 


**2) [Regularization (L2 Regularization and Dropout)](https://github.com/Zahra-Bakhtiari/Improving-Deep-Neural-Networks-Hyperparameter-Tuning-Regularization-and-Optimization/blob/main/Regularization.ipynb)**

Deep Learning models have so much flexibility and capacity that overfitting can be a serious problem, if the training dataset is not big enough. Sure it does well on the training set, but the learned network doesn't generalize to new examples that it has never seen!
In the [Regularization](https://github.com/Zahra-Bakhtiari/Improving-Deep-Neural-Networks-Hyperparameter-Tuning-Regularization-and-Optimization/blob/main/Regularization.ipynb) notebook, L2 Regularization and Dropout are being implemented as methods to reduce chance of overfitting occurance. 

**L2 Regularization** relies on the assumption that a model with small weights is simpler than a model with large weights. Thus, by penalizing the square values of the weights in the cost function we drive all the weights to smaller values. It becomes too costly for the cost to have large weights! This leads to a smoother model in which the output changes more slowly as the input changes. 


**Dropout**
Finally, dropout is a widely used regularization technique that is specific to deep learning. It randomly shuts down some neurons in each iteration. When you shut some neurons down, you actually modify your model. The idea behind drop-out is that at each iteration, you train a different model that uses only a subset of your neurons. With dropout, your neurons thus become less sensitive to the activation of one other specific neuron, because that other neuron might be shut down at any time. A common mistake when using dropout is to use it both in training and testing. You should use dropout (randomly eliminate nodes) only in training. 

    
**3) [Gradient Checking](https://github.com/Zahra-Bakhtiari/Improving-Deep-Neural-Networks-Hyperparameter-Tuning-Regularization-and-Optimization/blob/main/Gradient_Checking.ipynb)

Gradient checking is a method to give us reassurance that backpropagation is actually working. Consider a 1D linear function 𝐽(𝜃)=𝜃𝑥. The model contains only a single real-valued parameter 𝜃, and takes 𝑥 as input. You will implement code to compute 𝐽(.) and its derivative ∂𝐽/∂𝜃. You will then use gradient checking to make sure your derivative computation for 𝐽 is correct. 

Note that gradient checking is slow! Approximating the gradient with ∂𝐽∂𝜃≈𝐽(𝜃+𝜀)−𝐽(𝜃−𝜀)/2𝜀 is computationally costly. For this reason, we don't run gradient checking at every iteration during training. Just a few times to check if the gradient is correct. Gradient Checking, at least as we've presented it, doesn't work with dropout. You would usually run the gradient check algorithm without dropout to make sure your backprop is correct, then add dropout.


