# Generalization of Neural Networks

### Studying the L2-norm and the curvature in experiments with correct and random labeling of MNIST data.


Neural Networks generalize unreasonably well. They can have very high capacity, but some inner property greatly prevents it from overfitting. In other words, NN's have an intrinsic regularizing mechanism.

An experiment which highlights this property (see 1611.03530) compares the performance in classification of a NN trained with correctly versus randomized labels. When labels are randomized, training is successfull and the NN uses its capacity to memorize the data set. In fact, in this case, training is successful as long as there are as many parameters as data points and, naturally, performance on the test set is of about 50%. This shows that intrinsic regularization of NN's cannot be explained by uniform stability of Stochastic Gradient Descent, or some capacity measuer, as the Vapnik-Chervonenkis dimension. Here we look into to Neural Networks properties which differ with training with correct or random labels. In other words, we would like to investigate which are proper quantities to describe the NN's *effective* complexity.
We  start by taking a deeper look into the L2-norm and the curvatures of the Neural Network.
