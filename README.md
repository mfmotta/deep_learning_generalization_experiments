    in progress

# Generalization of Neural Networks

### Studying the L2-norm and the curvature in experiments with correct and random labeling of MNIST data.


Neural Networks generalize unreasonably well. They can have very high capacity, but some inner mechanism greatly prevents it from overfitting. In other words, NN's exhibit intrinsic regularization. While this phenomeon is not well understood, there have been attempts in identifying Neural Networks' properties which, at least, trace its *effective* capacity. 

An experiment which highlights key features of NN's generalization (see 1611.03530) compares the performance in classification of a NN trained with correct labels versus a NN trained with randomized labels. When labels are randomized, training can be successfull as long as there are as many parameters as data points, and the NN uses its capacity to memorize the data set. Naturally, performance on the test set is as good as random guess. This shows that intrinsic regularization of NN's cannot be explained by uniform stability of Stochastic Gradient Descent, or some capacity measure, as the Vapnik-Chervonenkis dimension. Here we look into to Neural Networks properties which differ with training with correct or random labels. In other words, we investigate which are proper quantities to describe the NN's *effective* complexity.

We  start by taking a deeper look into the L2-norm and the curvature of the Neural Network.
